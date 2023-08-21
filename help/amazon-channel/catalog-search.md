---
title: Katalogsökning efter Amazon-listor
description: Om du vill ange attributmatchning som hjälper dig att mappa kvalificerade Commerce-katalogprodukter med Amazon-listor uppdaterar du inställningarna för katalogsökning.
feature: Sales Channels, Search, Catalog Management, Products, Configuration
exl-id: 9fcaa924-cba3-498f-8e21-1a1f91b1ad04
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# Katalogsökning efter Amazon-listor

_Katalogsökning_ -inställningarna ingår i inställningarna för din butikslista. Du kommer åt listinställningarna via [instrumentpanel för butik](./amazon-store-dashboard.md).

Med de här inställningarna kan du ange attributmatchning som hjälper dig att mappa berättigande [!DNL Commerce] produkter med Amazon. När det mappas aktiverar Amazon åtgärder som rör priser, kvantitet, åsidosättningar samt order- och produktsynkronisering.

Om du definierar dessa mappningsvärden ökar risken för exakta matchningar, vilket minimerar behovet av att manuellt matcha produktlistor. Lägg till attributen som en del av [Åtgärder före installation](./amazon-pre-setup-tasks.md)har Amazon försäljningskanal större potential att automatiskt matcha dina produkter vid introduktion och synkronisering av produktdata mellan Amazon och [!DNL Commerce].

Om du bara skapar attributet Amazon ASIN (utan att lägga till ASIN-värden per produkt) kan du [!DNL Commerce] kanske inte matchar dina Amazon-listor automatiskt. Du kan [tilldela manuellt](./creating-assigning-catalog-products.md) dina produkter. Manuell matchning skapar dock inte de dataelement som behövs för att dela och synkronisera dina produktdata.

>[!IMPORTANT]
>
>Om du manuellt matchade en produkt och vill uppdatera ett ASIN-, UPC- eller andra dataelement för produkten måste du uppdatera informationen på två ställen. Uppdatera den i [!DNL Commerce] i din Amazon-katalog [!DNL Amazon Seller Central] konto.

Det är bäst att mappa dessa attribut och värden om de är tillgängliga. Du behöver inte slutföra mappningen, men det är bra för produktmatchning och krävs för korrekt katalogsynkronisering mellan Amazon och [!DNL Commerce].

Om du vill lägga till attribut finns mer information i [Skapa produktattribut för Amazon Matching](./ob-creating-magento-attributes.md).

## Konfigurera [!UICONTROL Catalog Search] inställningar

1. Klicka **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet _[!UICONTROL Catalog Search]_.

1. För **[!UICONTROL ASIN]** väljer du det produktattribut du skapade för Amazon ASIN-värdet.

   An ASIN ([!DNL Amazon Standard Identification Number]) är ett unikt block med tio bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när artikeln överförs till sin katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln.

1. För **[!UICONTROL EAN]** väljer du det produktattribut du skapade för Amazon EAN-värdet.

   Det europeiska artikelnumret (EAN) är en streckkodsstandard, en 12- eller 13-siffrig produktidentifieringskod. Varje EAN identifierar unikt produkten, tillverkaren och dess attribut. Vanligtvis trycks EAN på en produktetikett eller förpackning som streckkod. Amazon kräver EAN-koder för att förbättra kvaliteten på sökresultaten och på katalogen. Du kan få EAN-nummer från tillverkaren.

1. För **[!UICONTROL GCID]** väljer du det produktattribut du skapade för Amazon GCIN-värdet.

   GCID (Global Catalog Identifier) är ett ID för produkter som inte har någon UPC-kod eller ISBN. Med Amazon varumärkestrogister kan du registrera dig som varumärkesägare och skapa ett unikt ID för produkter.

1. För **[!UICONTROL ISBN]** väljer du det produktattribut du skapade för Amazon ISBN-värdet.

   ISBN (International Standard Book Number) är en unik streckkod för affärsboksidentifierare. Varje ISBN-kod identifierar en bok unikt. En ISBN har antingen tio eller 13 siffror. Alla ISBN som tilldelats efter 1 januari 2007 har 13 siffror.

1. För **[!UICONTROL UPC]** väljer du det produktattribut du skapade för Amazon UPC-värdet.

   Universal Product Code (UPC) är en 12-siffrig streckkod som används i stor utsträckning för detaljhandelsförpackningar i USA.

1. För **[!UICONTROL General Search]** väljer du det produktattribut som du vill använda för en allmän sökmatchning.

   Det här attributet kan du välja att matcha [!DNL Commerce] till rätt Amazon-lista. Allmän sökning använder nyckelordssökningar från din katalog. Därför bör du använda en [!DNL Commerce] attribut som innehåller relevanta nyckelord, t.ex. produkt-SKU eller produktnamn. Allmän sökning kan returnera många möjliga träffar, och i sådana fall kan du välja lämplig Amazon-lista bland de möjliga matchningarna. En vanlig markering för det här fältet är `Product Name`.

1. När du är klar klickar du på **[!UICONTROL Save listing settings]**.

![Katalogsökning](assets/amazon-catalog-search.png){width="500" zoomable="yes"}

| Fält | Beskrivning |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL ASIN] | Ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt.<br><br>ASIN står för [!DNL Amazon Standard Identification Number]. Ett ASIN är ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när artikeln överförs till sin katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln. |
| [!UICONTROL EAN (European Article Number)] | En 12- eller 13-siffrig produktidentifieringskod. Det europeiska artikelnumret (EAN) är en streckkodsstandard, en 12- eller 13-siffrig produktidentifieringskod. Varje EAN identifierar unikt produkten, tillverkaren och dess attribut. Vanligtvis trycks EAN på en produktetikett eller förpackning som streckkod. Amazon kräver EAN-koder för att förbättra kvaliteten på sökresultaten och på katalogen. Du kan få EAN-nummer från tillverkaren. |
| [!UICONTROL GCID (Global Catalog Identifier)] | GCID (Global Catalog Identifier) är ett ID för produkter som inte har någon UPC-kod eller ISBN. Med Amazon varumärkestrogister kan du registrera dig som varumärkesägare och skapa ett unikt ID för produkter som inte har en UPC eller ISBN. |
| [!UICONTROL ISBN (International Standard Book Number)] | En 10- eller 13-siffrig unik streckkod för affärsboksidentifierare. ISBN (International Standard Book Number) är en unik streckkod för affärsboksidentifierare. Varje ISBN-kod identifierar en bok unikt. En ISBN har antingen tio eller 13 siffror. Alla ISBN som tilldelats efter 1 januari 2007 har 13 siffror. |
| UPC (Universal Product Code) | En tolvsiffrig streckkod. Universal Product Code (UPC) är en 12-siffrig streckkod som används i stor utsträckning för detaljhandelsförpackningar i USA. |
| [!UICONTROL General Search] | Välj ett attribut. Det här attributet kan du välja att matcha [!DNL Commerce] till rätt Amazon-lista. Allmän sökning använder nyckelordssökningar från din katalog. Därför bör du använda en [!DNL Commerce] attribut som innehåller relevanta nyckelord, t.ex. produkt-SKU eller produktnamn. Allmän sökning kan returnera många möjliga träffar, och i sådana fall kan du välja lämplig Amazon-lista bland de möjliga matchningarna. En vanlig markering för det här fältet är `Product Name`. |

**Snabb åtkomst** - [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
