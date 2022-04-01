---
title: Installera [!DNL Channel Manager]
description: Installera Channel Manager-tillägget.
exl-id: cb593ebd-f077-4a79-a661-bedf4cc70f97
source-git-commit: 4509528d1b084c9a91fd6be0d0a863782edb3bdd
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# Installera Channel Manager

Granska [krav](onboard.md#prerequisites) och samla in nödvändig information innan du installerar Channel Manager.

## Uppdatera inställningen för minsta stabilitet

Innan du installerar tillägget ska du uppdatera `minimum-stability` dina behov `composer.json` så att du kan installera tidigare versioner av Channel Manager med Composer.

Om du vill uppdatera konfigurationen lägger du till följande rader i `composer.json` -fil.

```json
{
   "minimum-stability": "alpha",
   "prefer-stable": true
}
```

## Installera tillägget

Instruktionerna för Channel Manager-installationen beror på om Adobe Commerce eller Magento Open Source används lokalt eller på molninfrastrukturen.

- Installera på en [Lokal instans](#install-on-an-on-premises-instance).

- Installera på en [[!DNL Adobe Commerce] på molninfrastrukturinstans](#install-adobe-commerce-on-cloud-infrastructure)

Båda metoderna kräver att du använder kommandoradsgränssnittet (CLI).

>[!NOTE]
>
>För hjälp med installation [!DNL Commerce] med CLI, se [Allmän CLI-installation](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;}.

### Installera på en lokal instans

Följ de här instruktionerna för att installera på Adobe Commerce- och Magento Open Source-plattformar.

1. Logga in på [!DNL Commerce] server som [användare med behörigheter](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/file-system-perms.html){target=&quot;_blank&quot;} för att skriva till [!DNL Commerce] filsystem.

1. Lägg in webbsajten i [underhållsläge](https://devdocs.magento.com/guides/v2.4/install-gde/install/cli/install-cli-subcommands-maint.html){target=&quot;_blank&quot;}.

   ```bash
   $ bin/magento maintenance:enable
   ```

1. Från [!DNL Commerce] projektrotkatalog, lägg till kanalhanterare i `composer.json`.

   ```bash
    $ composer require magento/channel-manager --no-update
   ```

1. Ange nycklarna från din [!DNL Commerce] konto.

   Din offentliga nyckel är ditt användarnamn; din privata nyckel är ditt lösenord.

1. Uppdatera beroendena och installera tillägget.

   ```bash
   $ composer update
   ```

   The `composer update` kommandot uppdaterar alla beroenden. Om du bara vill uppdatera beroenden som är relaterade till kanalhanteraren använder du det här kommandot i stället: `composer update magento/channel-manager`.

1. Vänta tills Composer har uppdaterat projektberoenden och åtgärdat eventuella fel.

1. Verifiera installationen

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Exempelsvar:

   ```terminal
   Module is disabled
   ```

1. Registrera tillägget.

   ```bash
   $ bin/magento setup:upgrade
   ```

1. Kompilera om [!DNL Commerce] projekt.

   ```bash
   $ bin/magento setup:di:compile
   ```

1. Kontrollera att tillägget är aktiverat:

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Exempelsvar:

   ```bash
   Module is enabled
   ```

1. Rensa cachen.

   ```bash
   $ bin/magento cache:clean
   ```

1. Inaktivera underhållsläge.

   ```bash
    $ bin/magento maintenance:disable
   ```

### Installera på en Adobe Commerce-instans i molninfrastrukturen

Arbeta i en utvecklingsgren när du lägger till ett tillägg i din molninstans.

Hjälp om hur du använder grenar finns i [Kom igång med att skapa grenar](https://devdocs.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;} i dokumentationen för Adobe Commerce-utvecklare.

Under installationen visas tilläggets namn (`&lt;VendorName>\_&lt;ComponentName>`) infogas automatiskt i [app/etc/config.php](https://devdocs-beta.magento.com/guides/v2.3/config-guide/config/config-php.html){target=&quot;_blank&quot;}. Du behöver inte redigera filen direkt.

1. Byt till rotkatalogen för projektet i molnet på din lokala arbetsstation.

1. Skapa eller checka ut en utveckling [bankkontor](https://devdocs-beta.magento.com/cloud/env/environments-start.html#getstarted){target=&quot;_blank&quot;}.

1. Använd Composer-namnet för att lägga till tillägget i `require` i `composer.json` -fil.

   ```bash
   $ composer require magento/channel-manager --no-update
   ```

1. Lägg till, implementera och push-kodsändringar - inkludera ändringar i båda `composer.lock` och `composer.json` -fil.

   ```bash
   $ git add -A
   ```

   ```bash
   $ git commit -m “Install channel manager extension” 
   ```

   ```bash
   $ git push origin <branch-name>
   ```

1. När bygget och distributionen är klar använder du SSH för att logga in på fjärrmiljön och verifiera att tillägget har installerats korrekt.

   ```bash
   $ bin/magento module:status channel-manager
   ```

   Exempelsvar:

   ```terminal
   Module is enabled
   ```

1. När installationen har slutförts loggar du in på [!UICONTROL Admin] till [konfigurera Commerce Services Connector](connect.md).

   >[!NOTE]
   >
   >Instruktioner om hur du uppdaterar Channel Manager till en ny release finns i [Uppgraderingsmoduler och tillägg](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html){target=&quot;_blank&quot;}.


## Felsökning

Använd följande information för att åtgärda fel som inträffar under installationen av Channel Manager.

### Felaktiga dispositionsnycklar

Om [åtkomstnycklar](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;} som används för att autentisera till Composer-databasen är ogiltiga eller inte länkade till [!DNL MAGE ID] har använt [!DNL Channel Manager] visas följande fel.

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

1. Kontrollera att autentiseringsuppgifterna i auth.json matchar [nycklarna som är kopplade till MAGE-ID](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;} som används för att registrera för Channel Manager-tjänsten.

### Otillräckligt minne för PHP

Följande fel visas om systemet inte har tillräckligt med minne för PHP.

```terminal
Fatal error: Allowed memory size of 2146435072 bytes exhausted (tried to allocate 4096 bytes) in phar:///usr/local/bin/composer/src/Composer/DependencyResolver/RuleWatchGraph.php on line 52
```

Använd någon av följande metoder för att lösa minnesproblemet:

- [Öka minnesgränsen för PHP](https://devdocs.magento.com/cloud/project/magento-app-php-ini.html#increase-php-memory-limit){target=&quot;_blank&quot;} i miljön `php.ini` -fil. Kontrollera även att Commerce-instansen har [rekommenderade värden](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/php-settings.html){target=&quot;_blank&quot;} för andra PHP-inställningar.

- Ange minnesgränsen från kommandoraden.

   ```bash
   $ php -d memory_limit=-1 \[path to composer]/composer require magento/payment-services.
   ```

   Exempel:

   ```bash
   $ php-d memory_limit=-1 vendor/bin/composer require magento/channel-manager
   ```

### Vyn saknas

Om du får ett felmeddelande om att en fil saknas `process_catalog_exporter_view` under installationen av Channel Manager kan du [uppdatera indexerare](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-index.html#config-cli-subcommands-index-reindex){target=&quot;_blank&quot;}.

```bash
php bin/magento indexer:refresh
```

### Distributionsfel i molnet

Information om problem med att distribuera tillägget till molnet finns i [distributionsfel för tillägg](https://devdocs.magento.com/cloud/trouble/trouble_comp-deploy-fail.html){target=&quot;_blank&quot;}.
