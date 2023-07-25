---
title: Lägg till eller verifiera Amazon API-nyckeln
description: I din Commerce-konfiguration gör den validerade Amazon API-nyckeln att du kan integrera dina butiker med ditt Amazon Seller-konto.
role: Admin, Developer
feature: Sales Channels, Integration, Tools and External Services
exl-id: 2257b64d-309d-4efd-ba79-6e0cdeed63cb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Lägg till eller verifiera Amazon API-nyckeln

Vid åtkomst till Amazon försäljningskanal [!DNL Commerce] kontrollerar och validerar automatiskt Amazon API-nyckeln som du har lagt till i din butikskonfiguration. Om den valideras kan du gå vidare till nästa steg, [Butiksintegrering](./store-integration.md).

Om Amazon API-nyckeln saknas, är ogiltig eller har gått ut måste du uppdatera nyckeln. Ett meddelande visas med en uppmaning om att skaffa en API-nyckel och lägga till nyckeln i din konfiguration för Amazon-försäljningskanal.

## Hämta och lägg till Amazon API-nyckeln enligt uppmaningen

API-nyckeln valideras varje gång du öppnar din Amazon-försäljningskanal.

1. Logga in på [!DNL Commerce] Admin.

1. På _[!UICONTROL Admin]_sidebar, gå till **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Om det är första gången du använder Amazon försäljningskanal eller om API-nyckeln måste uppdateras, får du en fråga från systemet.

   ![Hämta och lägg till nyckelfråga för Amazon API](assets/amazon-api-verification-prompt.png){width="500"}

1. Klicka **[!UICONTROL Sign in]** för att få tillgång till [!DNL Commerce] webbkonto.

   Sidan Commerce-konton öppnas på en ny webbläsarflik.

   - Om du är inloggad på [!DNL Commerce] konto, _[!UICONTROL API Portal]_i_[!UICONTROL My Account]_ visas automatiskt.

   - Om du inte är inloggad uppmanas du att ange [!DNL Commerce] användarnamn och lösenord för kontot före _[!UICONTROL API Portal]_visas.

   - Om du inte har något konto går du till [den [!DNL Commerce] kontosida](https://account.magento.com/customer/account/login/){target="_blank"} och registrera. Det här kontot ska ingå i ditt företag eller din verksamhet.

1. Om det behövs kan du visa och generera API-nycklar på _[!UICONTROL API Portal]_i [!DNL Commerce] konto.

   Om du vill skapa en API-nyckel anger du en beskrivning som `Amazon Sales Channel` och klicka **[!UICONTROL Add New]**. Den nya nyckeln genereras och visas med det namn du angav. Klicka **[!UICONTROL Copy]** för att kopiera den nya nyckeln.

   ![Generera eller kopiera en API-nyckel](assets/amazon-add-api-key.png){width="500" zoomable="yes"}

1. När den nya nyckeln har genererats och kopierats går du tillbaka till _[!UICONTROL Amazon Sales Channel]_i webbläsaren.

1. På _[!UICONTROL Welcome to Amazon Sales Channel]_sida, klicka **[!UICONTROL Add the key]**.

   Webbläsaren avslutar Amazon försäljningskanal och en butikskonfigurationssida öppnar _[!UICONTROL Api Keys]_sidan i [!DNL Commerce] Admin. Du kan öppna den här sidan manuellt när du går till **[!UICONTROL Stores]**>_[!UICONTROL Settings]_ > **[!UICONTROL Configuration]**, expandera **[!UICONTROL Services]** i den vänstra panelen och väljer **[!UICONTROL Magento Services]**.

1. Klistra in den kopierade nyckeln för **[!UICONTROL Production Api key]**.

1. Klicka **[!UICONTROL Save Config]**. Nu kan du gå tillbaka till Amazon försäljningskanal.

   ![Lägga till API-nyckeln i butikskonfigurationen](assets/config-magento-services-api-screen.png){width="600" zoomable="yes"}

1. På _[!UICONTROL Admin]_sidebar, gå till **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

   Reaccessing Amazon sales channel triggers [!DNL Commerce] verifiera och validera API-nyckeln så att du kan fortsätta.

   Om du uppmanas att verifiera nyckeln igen upprepar du detta _Lägg till och verifiera_ -processen.

![Nästa ikon](assets/btn-next.png) [**Fortsätt till butiksintegrering**](./store-integration.md)
