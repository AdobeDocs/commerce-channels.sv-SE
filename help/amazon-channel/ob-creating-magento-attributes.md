---
title: Skapa [!DNL Commerce] Attribut för Amazon
description: Innan du slutför Amazon process för registrering av säljkanaler måste du se till att du har de [!UICONTROL Commerce] produktattribut.
exl-id: eebad794-c171-40a3-aa24-d5509e2b5797
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Skapa [!DNL Commerce] Attribut för Amazon

Innan du börjar prenumerera på [!DNL Amazon Seller Central] konton, det är bäst att lägga till [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/stores/attributes-product.html){target="_blank"} för att kartlägga produktlistor. När du är klar med introduktionen kan du hantera dina produktattribut via [Attribut](./managing-attributes.md) -fliken i [Amazon säljkanal - startsida](./amazon-sales-channel-home.md) sida.

Dessa instruktioner beskriver hur du skapar [!DNL Commerce] för Amazon ASIN och Amazon Condition. Vi rekommenderar att du skapar ytterligare attribut som Amazon EAN, Amazon ISBN och Amazon UPC. Du kan också skapa ett Amazon Price-attribut om du vill använda ditt Amazon-pris som en priskälla för prisregler. Dessa attribut används när du konfigurerar dina lista- och prisinställningar under introduktionen. Använd även dessa attribut när du skapar Amazon-listor och när du uppdaterar och synkroniserar [!DNL Commerce] katalogisera med dina Amazon-listor.

Med inställningarna för katalogsökning kan du ange matchande sökparametrar som hjälper dig att mappa berättigande [!DNL Commerce] produkter med Amazon. När det mappas aktiverar Amazon åtgärder som rör priser, kvantitet, åsidosättningar samt order- och produktsynkronisering.

Om du definierar dessa värden ökar risken för exakta matchningar, vilket minimerar behovet av att manuellt matcha produktlistor senare. Lägg till attribut som en del av din introduktion [förinställningsuppgifter](./amazon-pre-setup-tasks.md)har Amazon försäljningskanal större potential att automatiskt matcha dina produkter vid introduktion och synkronisering av produktdata mellan Amazon och [!DNL Commerce] efter introduktionen.

Om du bara skapar attributet Amazon ASIN (utan att lägga till ASIN-värden per produkt) kan du [!DNL Commerce] kanske inte matchar dina Amazon-listor automatiskt. Du kan matcha dina produkter manuellt med _Store Review_. Manuell matchning skapar dock inte de dataelement som behövs för att dela och synkronisera dina produktdata.

>[!IMPORTANT]
>
>Om du uppdaterar ett ASIN, UPC eller något annat dataelement för en manuellt matchad produkt måste du uppdatera informationen på båda platserna: din [!DNL Commerce] katalogen och listan i [!DNL Amazon Seller Central] konto.

## Skapa produktattributet för Amazon ASIN

1. Logga in på [!DNL Commerce] Admin.

1. Klicka **[!UICONTROL Stores]** i den vänstra menyn.

1. I _[!UICONTROL Attributes]_avsnitt, klicka **[!UICONTROL Product]**.

1. Om du vill öppna attributegenskaperna klickar du på **[!UICONTROL Add New Attribute]**.

1. För **[!UICONTROL Default Label]**, ange `Amazon ASIN` (namnet på attributet).

1. För **[!UICONTROL Catalog Input Type for Store Owner]**, välja `Text Field`.

1. För **[!UICONTROL Values Required]**, välja `No`.

   Även om det krävs ett Amazon ASIN för att visa en produkt i Amazon, kanske vissa av katalogprodukterna inte finns med i Amazon.

1. Expandera _[!UICONTROL Advanced Attribute Properties]_och ange alternativ:

   - För **[!UICONTROL Attribute Code]**, ange `amazon_asin`.

   - För **[!UICONTROL Scope]**, välja `Global`.

   - För **[!UICONTROL Unique Value]**, välja `No`.

   - För **[!UICONTROL Input Validation for Store Owner]**, välja `None`.

   - För **[!UICONTROL Add to Column Options]**, välja `Yes`.

   - För **[!UICONTROL Use in Filter Options]**, välja `Yes`.

1. Klicka **[!UICONTROL Save Attribute]**.

![Amazon ASIN-attribut](assets/creating-asin-attribute.png)

## Skapa Amazon Condition-produktattributet

1. Logga in på [!DNL Commerce] Admin.

1. Klicka **[!UICONTROL Stores]** i den vänstra menyn.

1. I _[!UICONTROL Attributes]_avsnitt, klicka **[!UICONTROL Product]**.

1. Om du vill öppna attributegenskaperna klickar du på **[!UICONTROL Add New Attribute]**.

1. För **[!UICONTROL Default Label]**, ange `Amazon Condition` (namnet på attributet).

1. För **[!UICONTROL Catalog Input Type for Store Owner]**, välja `Dropdown`.

   The _[!UICONTROL Manage Options (Values of your Attribute)]_visas.

1. För **[!UICONTROL Values Required]**, välja `No`.

1. För **[!UICONTROL Manage Options (Values for your Attribute)]** lägger du till alla villkorsalternativ.

   Standardvillkoren för Amazon är:

   - `New: Refurbished: Used`
   - `Like New: Used`
   - `Very Good: Used`
   - `Good: Used`
   - `Acceptable: Collectible`
   - `Like New; Collectible`
   - `Very Good: Collectible`
   - `Good: Collectible; Acceptable`

1. Klicka **[!UICONTROL Add Option]**.

1. Välj **[!UICONTROL Is Default]** för villkoret som du vill använda som standardval.

1. I _[!UICONTROL Admin]_anger du texten för etiketten för villkoret som du lägger till (till exempel `New`, `Used`och `Used-Like New`)

1. Klicka **[!UICONTROL Add Option]** om du vill lägga till fler alternativ efter behov.

1. Expandera _[!UICONTROL Advanced Attribute Properties]_och ange alternativen.

   - För **[!UICONTROL Attribute Code]**, ange `amazon_condition`.

   - För **[!UICONTROL Scope]**, välja `Global`.

   - För **[!UICONTROL Unique Value]**, välja `No`.

   - För **[!UICONTROL Input Validation for Store Owner]**, välja `None`.

   - För **[!UICONTROL Add to Column Options]**, välja `Yes`.

   - För **[!UICONTROL Use in Filter Options]**, välja `Yes`.

1. Klicka **[!UICONTROL Save Attribute]**.

![Amazon Condition-attribut](assets/creating-amazon-condition-attribute.png)

![Nästa ikon](assets/btn-next.png) [**Fortsätt lägga till eller verifiera API-nyckel**](./amazon-verify-api-key.md)
