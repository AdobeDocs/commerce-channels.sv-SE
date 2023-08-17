---
title: Installera [!DNL Channel Manager]'
description: Installera[!DNL Channel Manager] tillägg.'
role: Admin, Developer
feature: Sales Channels, Install
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---


# Installera [!DNL Channel Manager]

Granska [krav](onboard.md#requirements) och samla in nödvändig information innan du installerar Channel Manager.

## Installera tillägget

Instruktionerna för Channel Manager-installationen beror på om Adobe Commerce eller Magento Open Source används lokalt eller på molninfrastrukturen.

- Installera på en [Lokal instans](#install-on-an-on-premises-instance).

- Installera på en [[!DNL Adobe Commerce] på molninfrastrukturinstans](#install-adobe-commerce-on-cloud-infrastructure)

Båda metoderna kräver att du använder kommandoradsgränssnittet (CLI).

>[!NOTE]
>
>Hjälp med installation [!DNL Commerce] med CLI, se [Installera ett tillägg](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

### Installera på lokal instans

Följ dessa anvisningar för att installera [!DNL Channel Manager] på Adobe Commerce och Magento Open Source till en lokal instans.

1. Logga in på [!DNL Commerce] server som [användare med behörigheter](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/file-system/configure-permissions.html) för att skriva till [!DNL Commerce] filsystem.

1. Lägg in webbsidor i [underhållsläge](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/maintenance-mode.html).

   ```bash
   $ bin/magento maintenance:enable
   ```

1. Från [!DNL Commerce] projektrotkatalog, lägg till kanalhanterare i `composer.json`.

   ```bash
    composer require magento/channel-manager --no-update
   ```

1. Ange nycklarna från din [!DNL Commerce] konto.

   Din offentliga nyckel är ditt användarnamn. Din privata nyckel är ditt lösenord.

1. Uppdatera beroendena och installera tillägget.

   ```bash
   composer update magento/channel-manager
   ```

   The `composer update` bara de beroenden som krävs för [!DNL Channel Manager]. Om du vill uppdatera alla beroenden använder du det här kommandot i stället: `composer update`.

1. Vänta tills Composer har uppdaterat projektberoenden och åtgärdat eventuella fel.

1. Verifiera modulinstallationen:

   - Kontrollera modulens status.

     ```bash
     bin/magento module:status Magento_SalesChannels
     ```

     Exempelsvar:

     ```terminal
     Module is enabled
     ```

   - Aktivera modulen om den inte är aktiverad.

   ```bash
   bin/magento module:enable Magento_SalesChannels
   ```

1. Registrera tillägget.

   ```bash
   bin/magento setup:upgrade
   ```

1. Kompilera om [!DNL Commerce] projekt.

   ```bash
   bin/magento setup:di:compile
   ```

1. Rensa cachen.

   ```bash
   bin/magento cache:clean
   ```

1. Inaktivera underhållsläge.

   ```bash
   bin/magento maintenance:disable
   ```

### Installera på en Adobe Commerce-instans i molninfrastrukturen

Arbeta i en utvecklingsgren när du lägger till ett tillägg i din molninstans.

Hjälp om hur du använder grenar finns i [Kom igång med att skapa grenar](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html) i _Handbok för Commerce on Cloud Infrastructure_.

Under installationen visas tilläggets namn (`magento\channel-manager`) infogas automatiskt i [app/etc/config.php](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/store-settings.html) -fil. Du behöver inte redigera filen direkt.

1. Byt till rotkatalogen för projektet i molnet på din lokala arbetsstation.

1. Skapa eller checka ut en utveckling [bankkontor](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/cli-branches.html).

1. Använd Composer-namnet för att lägga till tillägget i `require` i `composer.json` -fil.

   ```bash
   composer require magento/module-sales-channels-extension --no-update
   ```

1. Uppdatera beroendena och installera tillägget.

   ```bash
   composer update magento/module-sales-channels-extension
   ```

   The `composer update` bara de beroenden som krävs för [!DNL Channel Manager]. Om du vill uppdatera alla beroenden använder du det här kommandot i stället: `composer update`.

1. Lägg till, implementera och push-kodsändringar - inkludera ändringar i båda `composer.lock` och `composer.json` -fil.

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m "Install channel manager extension" 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. När bygg- och distributionsprocessen har slutförts använder du SSH för att logga in på fjärrmiljön och verifiera att tillägget har installerats korrekt.

```bash
   bin/magento module:status Magento_SalesChannels
```

Exempelsvar:

```terminal
Module is enabled
```

Om modulen är inaktiverad [aktivera i din lokala miljö](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/extensions.html) och driftsätta ändringarna.


1. När du har installerat tillägget loggar du in på [!UICONTROL Admin] till [konfigurera Commerce Services Connector](connect.md).

   >[!NOTE]
   >
   >Instruktioner om hur du uppdaterar Channel Manager till en ny release finns i [Uppgraderingsmoduler och tillägg](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html).


## Felsökning

Använd följande information för att åtgärda fel som inträffar under installationen av Channel Manager.

### Felaktiga dispositionsnycklar

Om [åtkomstnycklar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) som används för att autentisera till Composer-databasen är ogiltiga eller inte länkade till [!DNL MAGE ID] som har registrerat sig för [!DNL Channel Manager] visas följande fel.

```terminal
Could not find a matching version of package magento/channel-manager. Check the package spelling, your version constraint and that the package is available in a stability which matches your minimum-stability (stable).
```

Kontrollera nyckelkonfigurationen:

1. Hitta platsen för `auth.json` fil:

   ```bash
   $ composer config –global home
   ```

1. Visa `auth.json` -fil.

   ```bash
   $ cat /path/to/auth.json
   ```

1. Verifiera att autentiseringsuppgifterna i auth.json matchar [nycklarna som är kopplade till MAGE-ID](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) används för att registrera för Channel Manager-tjänsten.

### Otillräckligt minne för PHP

Följande fel visas om systemet inte har tillräckligt med minne för PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Använd någon av följande metoder för att lösa minnesproblemet:

- [Öka minnesgränsen för PHP](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/php-settings.html) i miljön `php.ini` -fil. Kontrollera även att Commerce-instansen har [rekommenderade värden](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) för andra PHP-inställningar.

- Ange minnesgränsen från kommandoraden.

  ```bash
  $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
  ```

  Exempel:

  ```bash
  $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
  ```

### Vyn saknas

Om du får ett felmeddelande om att en fil saknas `process_catalog_exporter_view` under installationen av Channel Manager kan du [uppdatera indexerare](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html).

```bash
php bin/magento indexer:refresh
```

### Distributionsfel i molnet

Information om problem med att distribuera tillägget till molnet finns i [distributionsfel för tillägg](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment.html).
