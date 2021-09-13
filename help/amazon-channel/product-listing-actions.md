---
title: Produktlistningsåtgärder
description: Använd inställningarna för Produktlistningsåtgärder för att definiera hur din Commerce-katalog interagerar med Amazon.
redirect_from: /sales-channels/asc/ob-product-listing-actions.html: 
exl-id: c7d3f22c-05c6-4826-99eb-543bac462cf8
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 568
ht-degree: 0%

---

# Produktlistningsåtgärder

Inställningarna för produktlistningsåtgärder ingår i inställningarna för din butikslista. Du kommer åt listinställningarna från [butiksdashboard](./amazon-store-dashboard.md).

De här inställningarna definierar hur katalogen interagerar med Amazon. Dessa inställningar:

- Ange om dina [!DNL Commerce]-katalogprodukter som uppfyller Amazon behörighetskrav automatiskt skickas till ditt [!DNL Amazon Seller Central]-konto för att skapa listor.

- Ange standardhanteringstid för en order. Det här värdet anger hur många dagar som krävs för att bearbeta och skicka en beställning. Om någon t.ex. väljer 2-dagars frakt börjar inte transporttiden förrän bearbetningen är klar och paketen skickas till en fraktfirma. Den totala leveranstiden är (hanteringstid + transporttid + helgdagar).

## Konfigurera inställningar

1. Klicka på **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet _[!UICONTROL Product Listing Actions]_.

1. Välj ett alternativ för **[!UICONTROL Automatic List Action]** (obligatoriskt):

   - `Automatically List Eligible Products` - (Standard) Välj när du vill att dina  [!DNL Commerce] katalogprodukter (som uppfyller Amazon behörighetskrav) automatiskt ska publiceras till Amazon och skapa Amazon-listor.

   - `Do Not Automatically List Eligible Products` - Välj när du vill välja rätt  [!DNL Commerce] katalogprodukter manuellt och skapa Amazon-listor. När du väljer det här alternativet visas katalogprodukter som uppfyller dina listvillkor och innehåller all nödvändig information på fliken [_[!UICONTROL Ready to List]_](./ready-to-list.md) för manuell publicering till Amazon.

1. För **[!UICONTROL Default Handling Time]** (obligatoriskt) anger du antalet dagar som behövs för produktionstiden före leverans.

   Standardvärdet är `2` dagar.

   >[!NOTE]
   >
   >Detta standardvärde för ledtider gäller endast för Amazon-listor som skapats via Amazon försäljningskanal. Alla Amazon-listor som skapades i ditt [!DNL Amazon Seller Central]-konto använder den standardhanteringstid som angetts i Amazon.

1. Klicka på **[!UICONTROL Save listing settings]** när du är klar.

![Produktlistningsåtgärder](assets/amazon-product-listing-actions.png)

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Automatic List Action] | Alternativ:<ul><li>**[!UICONTROL Automatically List Eligible Products]** - (Rekommenderas) Välj när du vill att  [!DNL Commerce] katalogprodukter (som uppfyller Amazon behörighetskrav) automatiskt ska publiceras till Amazon och skapa Amazon-listor. När du väljer det här alternativet visas inte fliken [_[!UICONTROL Ready to List]_](./ready-to-list.md). </li><li>**[!UICONTROL Do Not Automatically List Eligible Products]** - Välj när du vill välja rätt  [!DNL Commerce] katalogprodukter manuellt och skapa Amazon-listor. När du väljer det här alternativet visas katalogprodukter som uppfyller dina listvillkor och innehåller all nödvändig information på fliken [_[!UICONTROL Ready to List]_](./ready-to-list.md) för manuell publicering.</li></ul> |
| [!UICONTROL Default Handling Time] | Det numeriska värdet som representerar det antal dagar som det i allmänhet tar dig att bearbeta och leverera beställningarna. Standardvärdet är `2`. Det här värdet används för Amazon-listor som skapats i [!DNL Commerce] och publicerats till Amazon. Standardhanteringstiden för Amazon-listor innan de integreras med [!DNL Commerce] påverkas inte av den här inställningen.<br><br>Det värde som definieras i Amazon försäljningskanal ersätter inte den standardhanteringstid som definieras i en befintlig Amazon-lista. När en **[!UICONTROL Handling Time Override]** är aktiverad och sedan tas bort återställs hanteringstiden för en order till det värde som definieras här.<br><br>Om du har produkter som har olika hanteringstider kan du skapa en åsidosättning av hanteringstid på den produktspecifika nivån. Du kan hantera åsidosättningar av hanteringstid på fliken [_[!UICONTROL Overrides]_](./overrides.md), vilket ger dig flexibilitet att hantera leveransen av produkten. Om det inte finns någon åsidosättning av hanteringstid i [!DNL Commerce] för en produkt, är standardtiden för hantering det värde som definieras i Amazon lista.<br><br>Hantera tid är ett regionalt attribut. När värdet ändras för en lista påverkar ändringen alla listor som delar [!DNL Amazon Seller SKU] i alla Amazon-butiker som finns för samma region (definieras i [butiksintegrering](./store-integration.md)). Om du ändrar värdet för en delad [!DNL Amazon Seller SKU] i Nordamerika påverkas inte samma produkter som finns i en butik med en annan definierad region. Butiken för regionen med det äldsta skapandedatumet styr prioriteten för standardinställningarna för hanteringstid. |

**Snabb åtkomst**  -  [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
