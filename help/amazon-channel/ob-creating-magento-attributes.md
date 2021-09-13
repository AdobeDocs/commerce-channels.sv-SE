---
title: Skapa [!DNL Commerce] attribut för Amazon
description: Innan du slutför Amazon introduktionsprocess för säljkanaler måste du kontrollera att du har de [!UICONTROL Commerce] produktattribut du behöver.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# Skapa [!DNL Commerce]-attribut för Amazon

Innan du börjar prenumerera på dina [!DNL Amazon Seller Central]-konton bör du lägga till [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/stores/attributes-product.html){:target=&quot;_blank&quot;} för att mappa dina produktlistor. När du är klar med introduktionen kan du hantera dina produktattribut via fliken [Attribut](./managing-attributes.md) på sidan [Amazon Sales channel home](./amazon-sales-channel-home.md).

I dessa anvisningar beskrivs hur du skapar [!DNL Commerce]-attribut för Amazon ASIN och Amazon Condition. Vi rekommenderar att du skapar ytterligare attribut som Amazon EAN, Amazon ISBN och Amazon UPC. Du kan också skapa ett Amazon Price-attribut om du vill använda ditt Amazon-pris som en priskälla för prisregler. Dessa attribut används när du konfigurerar dina lista- och prisinställningar under introduktionen. Använd även dessa attribut när du skapar Amazon-listor och när du uppdaterar och synkroniserar din [!DNL Commerce]-katalog med dina Amazon-listor.

Med inställningarna för katalogsökning kan du ange matchande sökparametrar som hjälper dig att mappa [!DNL Commerce]-produkter som är berättigade med Amazon listor. När det mappas aktiverar Amazon åtgärder som rör priser, kvantitet, åsidosättningar samt order- och produktsynkronisering.

Om du definierar dessa värden ökar risken för exakta matchningar, vilket minimerar behovet av att manuellt matcha produktlistor senare. Genom att lägga till attributen som en del av din introduktion [före konfigureringsuppgifter](./amazon-pre-setup-tasks.md) har Amazon säljkanal en större potential för automatisk matchning av dina produkter vid introduktion och synkronisering av produktdata mellan Amazon och [!DNL Commerce] efter introduktionen.

Om du bara skapar attributet Amazon ASIN (utan att lägga till ASIN-värden per produkt) kanske dina [!DNL Commerce]-produkter inte automatiskt matchar dina Amazon-listor. Du kan matcha dina produkter manuellt med _Store Review_. Manuell matchning skapar dock inte de dataelement som behövs för att dela och synkronisera dina produktdata.

>[!IMPORTANT]
>
>Om du uppdaterar ett ASIN, UPC eller något annat dataelement för en manuellt matchad produkt måste du uppdatera informationen på båda platserna: din [!DNL Commerce]-katalog och listan i ditt [!DNL Amazon Seller Central]-konto.

## Skapa produktattributet för Amazon ASIN

1. Logga in i din [!DNL Commerce]-administratör.

1. Klicka på **[!UICONTROL Stores]** på den vänstra menyn.

1. Klicka på **[!UICONTROL Product]** i _[!UICONTROL Attributes]_-avsnittet.

1. Klicka på **[!UICONTROL Add New Attribute]** om du vill öppna attributegenskaperna.

1. I **[!UICONTROL Default Label]** anger du `Amazon ASIN` (namnet på attributet).

1. Välj `Text Field` för **[!UICONTROL Catalog Input Type for Store Owner]**.

1. Välj `No` för **[!UICONTROL Values Required]**.

   Även om det krävs ett Amazon ASIN för att visa en produkt i Amazon, kanske vissa av katalogprodukterna inte finns med i Amazon.

1. Expandera avsnittet _[!UICONTROL Advanced Attribute Properties]_och ange alternativen:

   - Ange `amazon_asin` för **[!UICONTROL Attribute Code]**.

   - Välj `Global` för **[!UICONTROL Scope]**.

   - Välj `No` för **[!UICONTROL Unique Value]**.

   - Välj `None` för **[!UICONTROL Input Validation for Store Owner]**.

   - Välj `Yes` för **[!UICONTROL Add to Column Options]**.

   - Välj `Yes` för **[!UICONTROL Use in Filter Options]**.

1. Klicka på **[!UICONTROL Save Attribute]**.

![Amazon ASIN-attribut](assets/creating-asin-attribute.png)

## Skapa Amazon Condition-produktattributet

1. Logga in i din [!DNL Commerce]-administratör.

1. Klicka på **[!UICONTROL Stores]** på den vänstra menyn.

1. Klicka på **[!UICONTROL Product]** i _[!UICONTROL Attributes]_-avsnittet.

1. Om du vill öppna attributegenskaperna klickar du på **[!UICONTROL Add New Attribute]**.

1. I **[!UICONTROL Default Label]** anger du `Amazon Condition` (namnet på attributet).

1. Välj `Dropdown` för **[!UICONTROL Catalog Input Type for Store Owner]**.

   Avsnittet _[!UICONTROL Manage Options (Values of your Attribute)]_visas.

1. Välj `No` för **[!UICONTROL Values Required]**.

1. För **[!UICONTROL Manage Options (Values for your Attribute)]** lägger du till de olika villkorsalternativen.

   Standardvillkoren för Amazon är:

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. Klicka på **[!UICONTROL Add Option]**.

1. Välj alternativet **[!UICONTROL Is Default]** för villkoret som du vill ska vara standardvalet.

1. I kolumnen _[!UICONTROL Admin]_anger du texten för etiketten för villkoret som du lägger till (till exempel `New`, `Used` och `Used-Like New`)

1. Klicka på **[!UICONTROL Add Option]** om du vill lägga till fler alternativ efter behov.

1. Expandera avsnittet _[!UICONTROL Advanced Attribute Properties]_och ange alternativen.

   - Ange `amazon_condition` för **[!UICONTROL Attribute Code]**.

   - Välj `Global` för **[!UICONTROL Scope]**.

   - Välj `No` för **[!UICONTROL Unique Value]**.

   - Välj `None` för **[!UICONTROL Input Validation for Store Owner]**.

   - Välj `Yes` för **[!UICONTROL Add to Column Options]**.

   - Välj `Yes` för **[!UICONTROL Use in Filter Options]**.

1. Klicka på **[!UICONTROL Save Attribute]**.

![Amazon Condition-attribut](assets/creating-amazon-condition-attribute.png)

![Nästa ](assets/btn-next.png) [**ikonFortsätt till Lägg till eller verifiera API-nyckel**](./amazon-verify-api-key.md)
