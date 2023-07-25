---
title: "Installera [!DNL Amazon Sales Channel] extension"
description: Integrera [!DNL Commerce] katalog med [!DNL Amazon Seller Accounts] och sälja genom [!DNL Amazon Marketplace]hämtar och installerar tillägget Amazon Sales Channel.
role: Admin, Developer
feature: Sales Channels, Install, Integration, Tools and External Services
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# Installera [!DNL Amazon Sales Channel] extension

>[!IMPORTANT]
>
>Endast [!DNL Amazon Sales Channel] version 4.0+ stöds för Adobe Commerce och Magento Open Source 2.4.x. Om du kör en 2.3.x-version, se dokumentationen för [kompatibel version av Amazon-försäljningskanal](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html). Mer information om versionskompatibilitet finns i [Tillgänglighet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) i utvecklardokumentationen.

The [!UICONTROL Amazon Sales Channel] tillägg installerar och lägger till funktioner för att integrera din Commerce-katalog med [!DNL Amazon Seller Accounts] att sälja genom [!DNL Amazon Marketplace]. Mer information finns i [Amazon Sales Channel](https://marketplace.magento.com/magento-module-amazon.html) sida in [!DNL Commerce Marketplace] och [versionsinformation](release-notes.md).

## Krav

- **Commerce-instans**: The [!DNL Amazon Sales Channel] tillägg kan installeras på instanser med Magento Open Source, Adobe Commerce och Adobe Commerce i molninfrastrukturversionerna 2.3.x eller senare. Det stöds inte längre i version 2.1, 2.2 eller 1.x.
- **Commerce-webbkonto**: Du bör ha ett Commerce-webbkonto som används för att skapa och spåra en API-nyckel.
- **API-nyckel**: Skapa en API-nyckel för Amazon-försäljningskanal via ditt Commerce-webbkonto. Följande instruktioner innehåller dessa steg.

## Installera

Mer information om hur du använder Composer för den här processen finns i [installation av tillägg](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) instruktioner i utvecklardokumentationen.

1. Logga in på [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Klicka på **[!UICONTROL Marketplace]** och sedan klicka på **[!UICONTROL My Purchases]**.

1. Leta rätt på och markera **[!UICONTROL Amazon Sales Channel]**.

1. Välj version på tilläggssidan.

1. För komponentnamnet och versionen klickar du på **[!UICONTROL Technical Details]**.

1. Använd namn- och versionsinformation för att uppdatera tjänstanslutningsinformationen i din `composer.json` -fil.

   - Lägg till tilläggets namn och version i `composer.json` -fil.

   - Navigera till [!DNL Commerce] projektkatalog och uppdatera `composer.json` -fil.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Ange [autentiseringsnycklar](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html). Din offentliga nyckel är ditt användarnamn; din privata nyckel är ditt lösenord.

   - Vänta tills Composer har uppdaterat dina projektberoenden och kontrollera att inga fel uppstår.

1. [Verifiera tillägget](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

## Lägg till API-nyckeln för Amazon-försäljningskanal

Efter installationen anger du [API-nyckel](./amazon-verify-api-key.md) för att slutföra konfigurationen.

## Ange konfigurationsalternativ för Amazon-kanaler

Du har följande alternativ för att konfigurera Amazon försäljningskanal. Du behöver inte ändra de här inställningarna för att börja prenumerera och sälja på Amazon. Vi rekommenderar att avancerade administratörer tar hänsyn till dessa alternativ.

1. Logga in i Admin.

1. På _Administratör_ sidebar, gå till **Lager** > _Inställningar_ > **Konfiguration**.

1. Klicka **Sales Channel** sedan **Globala inställningar**.

1. För **Rensa logghistorik** anger du intervallet för rensning av de insamlade loggarna.

   Alternativen inkluderar `Once Daily`, `Once Weekly`och `Once Monthly` (standard).

1. (valfritt) för **Källa för bakgrundsuppgifter (CRON)**, ändra inställningen till `Command Line (CLI) CRON`.

   Den här inställningen rekommenderas för **_avancerade användare/administratörer_**.

1. Klicka **[!UICONTROL Save Config]**.

## Uppdatera tillägget

1. Logga in på [Commerce Marketplace](https://marketplace.magento.com/customer/account/).

1. Klicka på **[!UICONTROL Marketplace]** och sedan klicka på **[!UICONTROL My Purchases]**.

1. Leta rätt på och markera **[!UICONTROL Amazon Sales Channel]**.

1. Välj version på tilläggssidan.

1. För komponentnamnet och versionen klickar du på **[!UICONTROL Technical Details]**.

1. Slutför [instruktioner för uppgradering av tillägg](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) i _Installationshandbok_.
