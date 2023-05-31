---
title: Amazon försäljningskanal - Produktlistningsåtgärder
description: Använd inställningarna för Produktlistningsåtgärder för att definiera hur din Commerce-katalog interagerar med Amazon.
redirect_from: /sales-channels/asc/ob-product-listing-actions.html
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Produktlistningsåtgärder

Inställningarna för produktlistningsåtgärder ingår i inställningarna för din butikslista. Du kommer åt listinställningarna via [instrumentpanel för butik](./amazon-store-dashboard.md).

De här inställningarna definierar hur katalogen interagerar med Amazon. Dessa inställningar:

- Ange om [!DNL Commerce] katalogprodukter som uppfyller Amazon behörighetskrav skickas automatiskt till [!DNL Amazon Seller Central] för att skapa listor.

- Ange standardhanteringstid för en order. Det här värdet anger hur många dagar som krävs för att bearbeta och skicka en beställning. Om någon t.ex. väljer 2-dagars frakt börjar inte transporttiden förrän bearbetningen är klar och paketen skickas till en fraktfirma. Den totala leveranstiden är (hanteringstid + transporttid + helgdagar).

## Konfigurera inställningar

1. Klicka **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera _[!UICONTROL Product Listing Actions]_-avsnitt.

1. För **[!UICONTROL Automatic List Action]** (obligatoriskt) väljer du ett alternativ:

   - `Automatically List Eligible Products` - (Standard) Välj när du vill ha [!DNL Commerce] katalogprodukter (som uppfyller Amazon behörighetskrav) för att automatiskt publicera till Amazon och skapa Amazon-listor.

   - `Do Not Automatically List Eligible Products` - Välj när du manuellt vill välja rätt [!DNL Commerce] katalogprodukter och skapa Amazon-listor. När du väljer det här alternativet visas katalogprodukter som uppfyller dina listvillkor och innehåller all nödvändig information på [_[!UICONTROL Ready to List]_](./ready-to-list.md) för manuell publicering på Amazon.

1. För **[!UICONTROL Default Handling Time]** (obligatoriskt), ange antalet dagar som behövs för produktionstiden före leverans.

   Standardvärdet är `2` dagar.

   >[!NOTE]
   >
   >Detta standardvärde för ledtider gäller endast för Amazon-listor som skapats via Amazon försäljningskanal. Alla Amazon-listor som har skapats i [!DNL Amazon Seller Central] kontot använder den standardhanteringstid som anges i Amazon.

1. När du är klar klickar du på **[!UICONTROL Save listing settings]**.

![Produktlistningsåtgärder](assets/amazon-product-listing-actions.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Automatic List Action] | Alternativ:<ul><li>**[!UICONTROL Automatically List Eligible Products]** - (Rekommenderas) Välj när du vill ha [!DNL Commerce] katalogprodukter (som uppfyller Amazon behörighetskrav) för att automatiskt publicera till Amazon och skapa Amazon-listor. När du väljer det här alternativet visas [_[!UICONTROL Ready to List]_](./ready-to-list.md) visas inte. </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** - Välj när du manuellt vill välja berättigande [!DNL Commerce] katalogprodukter och skapa Amazon-listor. När du väljer det här alternativet visas katalogprodukter som uppfyller dina listvillkor och innehåller all nödvändig information på [_[!UICONTROL Ready to List]_](./ready-to-list.md) för manuell publicering.</li></ul> |
| [!UICONTROL Default Handling Time] | Det numeriska värdet som representerar det antal dagar som det i allmänhet tar dig att bearbeta och leverera beställningarna. Standardvärdet är `2`. Det här värdet används för Amazon-listor som skapas i [!DNL Commerce] och publiceras i Amazon. Standardhanteringstiden för Amazon-listor innan integrering med [!DNL Commerce] påverkas inte av den här inställningen.<br><br>Det värde som definieras i Amazon försäljningskanal ersätter inte den standardhanteringstid som definieras i en befintlig Amazon-lista. När en **[!UICONTROL Handling Time Override]** aktiveras och tas sedan bort, återställs hanteringstiden för en order till det värde som definieras här.<br><br>Om du har produkter som har olika hanteringstider kan du skapa en åsidosättning av hanteringstid på den produktspecifika nivån. Du kan hantera åsidosättningar av hanteringstid i [_[!UICONTROL Overrides]_](./overrides.md) -fliken, vilket ger dig flexibilitet att hantera leveransen. Om det inte finns någon åsidosättning av hanteringstid i [!DNL Commerce] för en produkt är standardvärdet för hanteringstid det värde som definieras i Amazon lista.<br><br>Hantera tid är ett regionalt attribut. När värdet ändras för en lista påverkar ändringen alla listor som delar [!DNL Amazon Seller SKU] i alla Amazon-butiker som finns för samma region (definieras på [butiksintegrering](./store-integration.md)). Om du ändrar värdet för en delad [!DNL Amazon Seller SKU] i Nordamerika påverkar inte samma produkter som finns i en butik med ett annat definierat område. Butiken för regionen med det äldsta skapandedatumet styr prioriteten för standardinställningarna för hanteringstid. |

**Snabb åtkomst** - [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
