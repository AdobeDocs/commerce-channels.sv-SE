---
title: Store-integrering med en  [!DNL Amazon Seller Account]
description: Innan du kan påbörja introduktionsprocessen måste du skapa (lägga till) en Amazon Sales Channel store och ansluta den till ditt Amazon Seller-konto.
role: Admin, Developer
feature: Sales Channels, Configuration, Integration, Tools and External Services
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Store-integrering med en [!DNL Amazon Seller Account]

Om du vill komma igång med Amazon försäljningskanal måste du skapa (lägga till) en Amazon försäljningskanalbutik och ansluta den till din [!DNL Amazon Seller Account]. Dessa två steg integrerar dina [!DNL Commerce]- och Amazon-konton för att dela data, synkronisera produkter och mycket mer.

_Du behöver de primära inloggningsuppgifterna för ditt [!DNL Amazon Seller Central]-konto (e-postadressen eller telefonen som används för att skapa säljarkontot) för att kunna ansluta till din butik._

>[!NOTE]
>
>När du har integrerat din första butik uppmanas du att förnya din Amazon-anslutning till Amazon varje år genom att bevilja åtkomst igen. Du kan förnya eller återkalla auktoriseringen i tabellen _Aktuella auktoriseringar_ i avsnittet _Amazon MWS Developer Permissions_ på sidan **Settings** > **User Permissions** på ditt Seller Central-konto.

## Lägg till en Amazon-butik

1. Gå till **Markering** > _Kanaler_ > **Amazon-Sales Channel** på sidofältet _Admin_.

   När du lägger till din första Amazon-försäljningskanalbutik visas spärrfunktionen _Förinställningsuppgifter_. När din första butik har lagts till kan du få åtkomst till förinställningsuppgifter på startsidan för [Amazon-försäljningskanalen](./amazon-sales-channel-home.md) under _Utbildning och förberedelse_ på den vänstra menyn.

1. Klicka på **[!UICONTROL Add Amazon Store]**.

   Sidan _[!UICONTROL Add Amazon sales channel]_öppnas.

   ![Lägg till Amazon försäljningskanalbutik](assets/amazon-store-integration.png){width="500" zoomable="yes"}

1. För **[!UICONTROL Magento Website to use for Amazon Listing]** väljer du vilken av dina [!DNL Commerce]-webbplatser som ska anslutas till den här Amazon-säljkanalsbutiken.

   Den här inställningen definierar även standardbutiken [!DNL Commerce] för [import av Amazon-order](./order-settings.md).

1. Ange din e-postadress som du föredrar för **[!UICONTROL Email Address]**.

1. För **[!UICONTROL New Store Name]** anger du ett beskrivande namn för din nya Amazon-butik.

   >[!NOTE]
   >
   >Det här namnet används bara som en [!DNL Commerce]-referens och identifierar butiken på startsidan för [Amazon-försäljningskanalen](./amazon-sales-channel-home.md). Ni vill göra det till något som teamet lätt kan identifiera. Din Amazon-butik som säljer i USA kan till exempel heta `Amazon Store USA`.

1. För **[!UICONTROL Amazon Marketplace Country]** väljer du den region/det land där den här Amazon-säljkanalsbutiken säljer produkter. Alternativ:

   - Amerikas förenta stater
   - Kanada
   - Mexico
   - Förenade kungariket

1. Gör följande i avsnittet _[!UICONTROL Map your Magento attributes to Amazon]_:

   - För **[!UICONTROL Product ID on the Amazon market]** väljer du det Amazon-attribut som ska mappas till det [!DNL Commerce]-attribut som är markerat nedan.

     Detta ID hjälper till att matcha motsvarande produkter i din [!DNL Commerce]-katalog korrekt.

   - För **[!UICONTROL Map a Magento attribute]** väljer du produktattributet [!DNL Commerce] som ska mappas till det Amazon-attribut som valts ovan.

     [Mappningsattribut](./ob-creating-magento-attributes.md) säkerställer att din Amazon-lista matchar motsvarande produkt i din [!DNL Commerce]-katalog.

1. Klicka på **[!UICONTROL Connect]**.

   Dialogrutan stängs och den nya butiken visas på startsidan för [Amazon-försäljningskanalen](./amazon-sales-channel-home.md) med ett bekräftelsemeddelande.

## Anslut en butik till [!DNL Amazon Seller Central]

1. Klicka på **[!UICONTROL Connect store]** på butikskortet på kontrollpanelen för att starta [!DNL Amazon Seller Central] på en ny flik.

1. Ange autentiseringsuppgifterna för ditt [!DNL Amazon Seller Central]-konto och klicka på **[!UICONTROL Sign in]**.

   Om du vill slutföra den här anslutningen måste du logga in på ditt [!DNL Amazon Seller Central]-konto med inloggningsuppgifterna för den primära användaren (den e-postadress eller telefon som användes för att skapa säljarkontot).

1. Fyll i Amazon Two-Factor Authorization (2FA) genom att ange den kod du får från Amazon och klicka på **[!UICONTROL Sign in]** om du uppmanas till detta.

1. Markera kryssrutan [!UICONTROL I understand...] på bekräftelsesidan för _[!UICONTROL Amazon Marketplace Web Service]_och klicka på&#x200B;**[!UICONTROL Next]**.

1. Klicka på **[!UICONTROL Continue]** i meddelandet _[!UICONTROL You are almost done]_.

   Du har gett Amazon säljkanal behörighet att komma åt och dela data med ditt [!DNL Amazon Seller Central]-konto. Amazon-sidan stängs och ett bekräftelsemeddelande visas.

   Sidan [Startsida för Amazon-försäljningskanal](./amazon-sales-channel-home.md) öppnas med dina Amazon-butikskort.

   Klicka **[!UICONTROL View Store]** på butikskortet om du vill visa butikspanelen.

![Amazon-försäljningskanal hem med nytt butikskort](assets/asc-dashboard-after-2fa.png){width="600" zoomable="yes"}

Din nya Amazon säljkanalsbutik är nu ansluten till ditt [!DNL Amazon Seller Central]-konto.

![Nästa ikon](assets/btn-next.png) [**Fortsätt skapa en listregel**](./ob-create-listing-rule.md)
