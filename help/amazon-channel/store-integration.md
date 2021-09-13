---
title: Butiksintegrering
description: Innan du börjar med introduktionsprocessen måste du skapa (lägga till) en Amazon Sales Channel store och ansluta den till ditt Amazon-återförsäljarkonto.
exl-id: ea79e91d-7d92-4992-a921-7ac7632a0519
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Integrering med Store

För att komma igång med Amazon säljkanal måste du skapa (lägga till) en Amazon-återförsäljarbutik och ansluta den till ditt Amazon-återförsäljarkonto. Dessa två steg integrerar dina [!DNL Commerce]- och Amazon-konton för att dela data, synkronisera produkter med mera.

_Du behöver de primära inloggningsuppgifterna för ditt  [!DNL Amazon Seller Central] konto (e-postadressen eller telefonen som används för att skapa säljarkontot) för att kunna ansluta till din butik._

>[!NOTE]
>
>När du har integrerat din första butik uppmanas du att förnya din Amazon-anslutning till Amazon varje år genom att bevilja åtkomst igen. Du kan förnya eller återkalla auktoriseringen i tabellen _Aktuella auktoriseringar_ i _Amazon MWS Developer Permissions_ under **Settings** > **User Permissions** på sidan Seller Central account.

## Lägg till en Amazon-butik

1. Gå till **Marknadsföring** > _Kanaler_ > **Amazon Sales Channel** på sidofältet _Admin_.

   När du lägger till din första Amazon-försäljningskanalbutik visas modala _uppgifter före installation_. När du har lagt till din första butik kan du komma åt förinställningsuppgifter på sidan [Amazon säljkanalhem](./amazon-sales-channel-home.md) under _Utbildning och förberedelse_ på den vänstra menyn.

1. Klicka på **[!UICONTROL Add Amazon Store]**.

   Sidan _[!UICONTROL Add Amazon sales channel]_öppnas.

   ![Lägg till Amazon säljkanalsbutik](assets/amazon-store-integration.png)

1. För **[!UICONTROL Magento Website to use for Amazon Listing]** väljer du vilken av dina [!DNL Commerce]-webbplatser du vill ansluta till för den här Amazon-säljkanalsbutiken.

   Den här inställningen definierar också standardarkivet [!DNL Commerce] för [import av Amazon-order](./order-settings.md).

1. För **[!UICONTROL Email Address]** anger du din e-postadress till kontaktperson.

1. I **[!UICONTROL New Store Name]** anger du ett beskrivande namn för din nya Amazon-butik.

   >[!NOTE]
   >
   >Det här namnet används endast som en [!DNL Commerce]-referens och identifierar butiken på [startsidan för Amazon-försäljningskanalen](./amazon-sales-channel-home.md). Ni vill göra det till något som teamet lätt kan identifiera. Din Amazon-butik som säljer i USA kan till exempel ha namnet `Amazon Store USA`.

1. För **[!UICONTROL Amazon Marketplace Country]** väljer du den region/det land där den här Amazon-säljkanalsbutiken säljer produkter. Alternativ:

   - Amerikas förenta stater
   - Kanada
   - Mexico
   - Storbritannien

1. Gör följande i avsnittet _[!UICONTROL Map your Magento attributes to Amazon]_:

   - För **[!UICONTROL Product ID on the Amazon market]** väljer du det Amazon-attribut som ska mappas till [!DNL Commerce]-attributet som är markerat nedan.

      Detta ID hjälper dig att matcha motsvarande produkter i din [!DNL Commerce]-katalog korrekt.

   - För **[!UICONTROL Map a Magento attribute]** väljer du det [!DNL Commerce]-produktattribut som ska mappas till det Amazon-attribut som valts ovan.

      [Genom att mappa ](./ob-creating-magento-attributes.md) attribut kan du se till att din Amazon-lista matchar motsvarande produkt i  [!DNL Commerce] katalogen.

1. Klicka på **[!UICONTROL Connect]**.

   Dialogrutan stängs och den nya butiken visas med ett bekräftelsemeddelande på sidan [Amazon Sales channel home](./amazon-sales-channel-home.md).

## Anslut en butik till [!DNL Amazon Seller Central]

1. Klicka på **[!UICONTROL Connect store]** på butikskortet på kontrollpanelen för att starta [!DNL Amazon Seller Central] på en ny flik.

1. Ange dina [!DNL Amazon Seller Central]-kontouppgifter och klicka på **[!UICONTROL Sign in]**.

   För att slutföra anslutningen måste du logga in på ditt [!DNL Amazon Seller Central]-konto med inloggningsuppgifterna för den primära användaren (den e-postadress eller telefon som användes för att skapa säljarkontot).

1. Fyll i Amazon Two-Factor Authorization (2FA) genom att ange koden du får från Amazon och klicka på **[!UICONTROL Sign in]**.

1. Markera kryssrutan [!UICONTROL I understand...] på bekräftelsesidan och klicka på **[!UICONTROL Next]**._[!UICONTROL Amazon Marketplace Web Service]_

1. Klicka på **[!UICONTROL Continue]** i _[!UICONTROL You are almost done]_-meddelandet.

   Du har gett Amazon säljkanal behörighet att komma åt och dela data med ditt [!DNL Amazon Seller Central]-konto. Amazon-sidan stängs och ett bekräftelsemeddelande visas.

   Sidan [Startsida för Amazon-försäljningskanal](./amazon-sales-channel-home.md) öppnas med dina Amazon-butikskort.

   Om du vill visa butiksinstrumentpanelen klickar du på **[!UICONTROL View Store]** på butikskortet.

![Amazon säljkanalshem med nytt butikskort](assets/asc-dashboard-after-2fa.png)

Din nya Amazon säljkanalsbutik är nu ansluten till ditt [!DNL Amazon Seller Central]-konto.

![Nästa ](assets/btn-next.png) [**ikonFortsätt att skapa en listregel**](./ob-create-listing-rule.md)
