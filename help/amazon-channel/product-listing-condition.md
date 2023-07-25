---
title: Amazon försäljningskanal - villkor för produktlista
description: Använd inställningarna för produktlistvillkor för att mappa dina Commerce-produkter till ett Amazon-produktvillkor, till exempel"Nytt" eller"Renoverat".
feature: Sales Channels, Products, Merchandising
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Villkor för produktlista

Villkorsinställningarna för produktlistor ingår i dina inställningar för butikslista. Du kan komma åt listinställningarna på [instrumentpanel för butik](./amazon-store-dashboard.md).

Amazon kräver att en produktlista har ett definierat villkor. Om alla produkter är likadana kan du välja ett av Amazon villkorsalternativ för att representera alla produkter som ditt globala villkorsvärde. Standardvillkoren för Amazon är:

- `New`
- `Refurbished`
- `Used; Like New`
- `Used; Very Good`
- `Used; Good`
- `Used; Acceptable`
- `Collectible; Like New`
- `Collectible; Very Good`
- `Collectible; Good`
- `Collectible; Acceptable`

>[!IMPORTANT]
>
>Om du säljer förnyade (renoverade) produkter måste du registrera dig i [!DNL Amazon Renewed Program]. Se [Förnyade produkter](./renewed-products.md).

Om din katalog innehåller produkter med olika villkor (till exempel Ny, Används och Återanvänd) måste du välja **[!UICONTROL Assign Condition Using Product Attribute]**. Med den här inställningen kan du mappa dina [!DNL Commerce] villkorsattribut och värden till villkoren i din Amazon-lista.

Under [Åtgärder före installation](./amazon-pre-setup-tasks.md)uppmuntras du att skapa en [!DNL Commerce] produktattribut för en produkts villkor. Om du erbjuder produkter under olika förhållanden och inte har skapat något villkorsattribut, se [Skapa ett produktattribut i [!DNL Commerce]](./ob-creating-magento-attributes.md). När villkorsattributet har skapats kan du tilldela ett villkorsvärde till var och en av produkterna i [!DNL Commerce] katalog.

## Konfigurera inställningar

1. Klicka **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera **[!UICONTROL Product Listing Condition]** -avsnitt.

1. För **[!UICONTROL Listing Product Condition]** väljer du ett alternativ.

   Välj ett av Amazon standardvillkor för ditt globala villkorsvärde för alla dina listor. Standardinställningen är `New`.

   Om du har produkter/listor som har olika villkor väljer du `Assign Condition Using Product Attribute` för att definiera dina produktvillkorsinställningar i de ytterligare fält som visas.

1. För **Villkorsattribut** väljer du [!DNL Commerce] för att mappa värden för alla Amazon standardvillkorsattribut.

   Om du har produkter i `Used` eller `Collectible` men du kan inte göra någon ytterligare skillnad, du kan mappa till ett enda `Used` eller `Collectible` Amazon-villkor och lämna de andra tomma. Den här metoden mappar alla `Used` eller `Collectible` villkor till det enskilda Amazon-villkoret Använt eller Hämtbart.

   Du har till exempel en enda `Used` villkor för dina produkter. Vid mappning väljer du om du vill mappa till Amazon-villkoret `Used; Like New`, `Used; Very Good`, `Used; Good`, eller `Used; Acceptable`. Fyll bara i fältet för det Amazon-villkor du vill använda och lämna det andra `Used` alternativ inställda på `--Select Option--`. I exempelbilden är alla [!DNL Commerce] produkter i `Used` villkor mappas till Amazon `Used; Very Good` villkor.

   Du kan även ange beskrivande text för villkoren, förutom `New`.

1. När du är klar klickar du på **[!UICONTROL Save listing settings]**.

![Villkor för produktlista](assets/amazon-product-listing-condition.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Listing Product Condition] | Villkor för produktlistor. Alternativ: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Om du säljer ett enda produktvillkor väljer du något av standardvillkoren för Amazon. Om [!DNL Commerce] katalogen innehåller produkter under olika förhållanden, välj `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | The [!DNL Commerce] -attribut som definierar villkoren för dina produkter. Markera det Magneto-attribut som du skapade för att mappa till Amazon villkorsattribut. I [Exempel på uppgifter före installation](./ob-creating-magento-attributes.md) rekommenderar att du namnger det som `Amazon Condition`. När du väljer det här alternativet visas ytterligare fält för att mappa Amazon standardvillkor. |
| [!UICONTROL Additional Condition fields] | För vart och ett av standardvillkoren för Amazon väljer du motsvarande villkor. Alternativen är villkorsetiketterna som du lade till när du [skapade Amazon-villkorsattribut](./ob-creating-magento-attributes.md).<br><br>Om du har produkter i `Used` eller `Collectible` men du kan inte göra någon ytterligare skillnad, du kan mappa till ett enda `Used` eller `Collectible` Amazon-villkor och lämna de andra tomma. Den här metoden mappar alla `Used` eller `Collectible` villkor till det enskilda Amazon-villkoret Använt eller Hämtbart. |

**Snabb åtkomst** - [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
