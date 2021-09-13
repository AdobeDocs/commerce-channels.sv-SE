---
title: Installera tillägget
description: Om du vill integrera ditt  [!DNL Commerce] catalog with [!DNL Amazon Seller Accounts] och sälja via [!DNL Amazon Marketplace] hämtar och installerar du tillägget Amazon Sales Channel.
exl-id: ebf22e28-b6a2-420b-80ca-2d750839286c
source-git-commit: 8d12a839bbdf77f27c732507b5b776729e252a9f
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Installera tillägget

>[!IMPORTANT]
>
>Endast [!DNL Amazon Sales Channel] version av tillägg 4.0+ stöds för Adobe Commerce och Magento Open Source 2.4.x. Om du kör en version 2.3.x ska du läsa dokumentationen för den [kompatibla versionen av Amazon-försäljningskanal](https://docs.magento.com/user-guide/v2.3/sales-channels/amazon/amazon-sales-channel.html){target=&quot;_blank&quot;}. Mer information om versionskompatibilitet finns på sidan [Tillgänglighet](https://devdocs.magento.com/release/availability.html){target=&quot;_blank&quot;} i utvecklardokumentationen.

Tillägget [!UICONTROL Amazon Sales Channel] installerar och lägger till funktioner för att integrera din Commerce-katalog med [!DNL Amazon Seller Accounts] som kan säljas via [!DNL Amazon Marketplace]. Mer information finns på sidan [Amazon Sales Channel](https://marketplace.magento.com/magento-module-amazon.html) i [!DNL Commerce Marketplace] och i [versionsinformationen](https://devdocs.magento.com/extensions/amazon-sales/release-notes/) i utvecklardokumentationen.

## Krav

- **Handelsinstans**: Tillägget  [!DNL Amazon Sales Channel] kan installeras på instanser med Magento Open Source, Adobe Commerce och Adobe Commerce i molninfrastrukturversion 2.3.x eller senare. Det stöds inte längre i version 2.1, 2.2 eller 1.x.
- **Commerce-webbkonto**: Du bör ha ett Commerce-webbkonto som används för att skapa och spåra en API-nyckel.
- **API-nyckel**: Skapa en API-nyckel för Amazon-försäljningskanal via ditt Commerce-webbkonto. Följande instruktioner innehåller dessa steg.

## Installera

Mer information om hur du använder Composer för den här processen finns i [installationsanvisningarna för tillägg](https://devdocs.magento.com/extensions/install/){target=&quot;_blank&quot;} i utvecklardokumentationen.

1. Logga in på [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Klicka på fliken **[!UICONTROL Marketplace]** och sedan på **[!UICONTROL My Purchases]**.

1. Leta reda på och välj **[!UICONTROL Amazon Sales Channel]**.

1. Välj version på tilläggssidan.

1. Klicka på **[!UICONTROL Technical Details]** som komponentnamn och version.

1. Använd namn- och versionsinformationen för att uppdatera tjänstkopplingsposten i din `composer.json`-fil.

   - Lägg till tilläggets namn och version i din `composer.json`-fil.

   - Navigera till din [!DNL Commerce]-projektkatalog och uppdatera din `composer.json`-fil.

   ```bash
   composer require magento/services-connector:~1.0.3
   ```

   - Ange dina [autentiseringsnycklar](https://devdocs.magento.com/guides/v2.4/install-gde/prereq/connect-auth.html){target=&quot;_blank&quot;}. Din offentliga nyckel är ditt användarnamn; din privata nyckel är ditt lösenord.

   - Vänta tills Composer har uppdaterat dina projektberoenden och kontrollera att inga fel uppstår.


1. [Verifiera tillägget](https://devdocs.magento.com/extensions/install/#verify-the-extension){target=&quot;_blank&quot;}.

## Lägg till API-nyckeln för Amazon-försäljningskanal

Efter installationen anger du en [API-nyckel](./amazon-verify-api-key.md) för att slutföra konfigurationen.

## Ange konfigurationsalternativ för Amazon-kanaler

Du har följande alternativ för att konfigurera Amazon försäljningskanal. Du behöver inte ändra de här inställningarna för att börja prenumerera och sälja på Amazon. Vi rekommenderar att avancerade administratörer tar hänsyn till dessa alternativ.

1. Logga in i Admin.

1. På sidofältet _Admin_ går du till **Store** > _Inställningar_ > **Konfiguration**.

1. Klicka på **Sales Channel** och sedan på **Globala inställningar**.

1. För **Rensa logghistorik** anger du intervallet för rensning av de insamlade loggarna.

   Alternativen är `Once Daily`, `Once Weekly` och `Once Monthly` (standard).

1. (Valfritt) Ändra inställningen till `Command Line (CLI) CRON` för källan **Bakgrundsuppgifter (CRON)**.

   Den här inställningen rekommenderas för **_avancerade användare/administratörer_**.

1. Klicka på **[!UICONTROL Save Config]**.

## Uppdatera tillägget

1. Logga in på [Commerce Marketplace](https://marketplace.magento.com/customer/account/){target=&quot;_blank&quot;}.

1. Klicka på fliken **[!UICONTROL Marketplace]** och sedan på **[!UICONTROL My Purchases]**.

1. Leta reda på och välj **[!UICONTROL Amazon Sales Channel]**.

1. Välj version på tilläggssidan.

1. Klicka på **[!UICONTROL Technical Details]** som komponentnamn och version.

1. Fyll i [instruktionerna för att uppgradera tillägg](https://devdocs.magento.com/extensions/install/#upgrade-an-extension){target=&quot;_blank&quot;} i utvecklardokumentationen.
