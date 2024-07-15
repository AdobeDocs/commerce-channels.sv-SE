---
title: Installera tillägget  [!DNL Amazon Sales Channel]
description: Om du vill integrera din [!DNL Commerce] katalog med [!DNL Amazon Seller Accounts] och sälja via  [!DNL Amazon Marketplace] hämtar och installerar du tillägget för Amazon-Sales Channel.
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 010a95d7be29354515cf4dcbf5d557eebaa40ed6
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Installera tillägget [!DNL Amazon Sales Channel]

>[!IMPORTANT]
>
>Endast [!DNL Amazon Sales Channel] version av tillägg 4.0+ stöds för Adobe Commerce och Magento Open Source 2.4.x. Om du kör en version som är 2.3.x kan du läsa dokumentationen för den [kompatibla versionen av Amazon-försäljningskanalen](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). Mer information om versionskompatibilitet finns på sidan [Tillgänglighet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) i utvecklardokumentationen.

Tillägget [!UICONTROL Amazon Sales Channel] installerar och lägger till funktioner för att integrera din Commerce-katalog med [!DNL Amazon Seller Accounts] och sälja via [!DNL Amazon Marketplace]. Mer information finns på sidan [Amazon-Sales Channel](https://marketplace.magento.com/magento-module-amazon.html) i [!DNL Commerce Marketplace] och i [versionsinformationen](release-notes.md).

## Krav

- **Commerce-instans**: Tillägget [!DNL Amazon Sales Channel] kan installeras på instanser med Magento Open Source, Adobe Commerce och Adobe Commerce i molninfrastrukturversionerna 2.3.x eller senare. Det stöds inte längre i version 2.1, 2.2 eller 1.x.
- **Commerce webbkonto**: Du bör ha ett Commerce-webbkonto som används för att skapa och spåra en API-nyckel.
- **API-nyckel**: Skapa en API-nyckel för Amazon-försäljningskanal via ditt Commerce-webbkonto. Följande instruktioner innehåller dessa steg.

## Installera

Mer detaljerad information om hur du använder Composer för den här processen finns i [installationsanvisningarna för tillägget](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) i utvecklardokumentationen.

1. Logga in på [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Klicka på fliken **[!UICONTROL Marketplace]** och sedan på **[!UICONTROL My Purchases]**.

1. Leta reda på och välj **[!UICONTROL Amazon Sales Channel]**.

1. Välj version på tilläggssidan.

1. Klicka på **[!UICONTROL Technical Details]** för komponentnamnet och versionen.

1. Använd namn- och versionsinformationen för att uppdatera tjänstkopplingsposten i din `composer.json`-fil.

   - Lägg till tilläggets namn och version i din `composer.json`-fil.

   - Navigera till din [!DNL Commerce]-projektkatalog och uppdatera `composer.json`-filen.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Ange dina [autentiseringsnycklar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). Din offentliga nyckel är ditt användarnamn. Din privata nyckel är ditt lösenord.

   - Vänta tills Composer har uppdaterat dina projektberoenden och kontrollera att inga fel uppstår.

1. [Verifiera tillägget](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Lägg till API-nyckeln för Amazon-försäljningskanal

När du har installerat anger du en [API-nyckel](./amazon-verify-api-key.md) för att slutföra konfigurationen.

## Ange alternativ för kanalkonfiguration för Amazon

Du har följande alternativ för att konfigurera Amazon försäljningskanal. Du behöver inte ändra de här inställningarna för att börja prenumerera och sälja på Amazon. Vi rekommenderar att avancerade administratörer överväger dessa alternativ.

1. Logga in i Admin.

1. Gå till **Store** > _Settings_ > **Configuration** på sidofältet _Admin_.

1. Klicka på **Sales Channeler** och sedan på **Globala inställningar**.

1. För **Rensa logghistorik** definierar du intervallet för rensning av de insamlade loggarna.

   Alternativen är `Once Daily`, `Once Weekly` och `Once Monthly` (standard).

1. (Valfritt) Ändra inställningen till `Command Line (CLI) CRON` för **Bakgrundsuppgifter (CRON) Source**.

   Den här inställningen rekommenderas för **_avancerade användare/administratörer_**.

1. Klicka på **[!UICONTROL Save Config]**.

## Uppdatera tillägget

1. Logga in på [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Klicka på fliken **[!UICONTROL Marketplace]** och sedan på **[!UICONTROL My Purchases]**.

1. Leta reda på och välj **[!UICONTROL Amazon Sales Channel]**.

1. Välj version på tilläggssidan.

1. Klicka på **[!UICONTROL Technical Details]** för komponentnamnet och versionen.

1. Fyll i uppgraderingsinstruktionerna för [tillägget](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) i _installationshandboken_.
