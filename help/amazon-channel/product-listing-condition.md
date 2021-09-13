---
title: Villkor för produktlista
description: 'Använd inställningarna för produktlistvillkor för att mappa dina Commerce-produkter till ett Amazon-produktvillkor, till exempel"Nytt" eller"Renoverat".'
redirect_from: /sales-channels/asc/ob-product-listing-condition.html: 
exl-id: f37ce3cf-7bfc-4dee-931e-a603008a71b8
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 526
ht-degree: 0%

---

# Villkor för produktlista

Villkorsinställningarna för produktlistor ingår i dina inställningar för butikslista. Du kan komma åt listinställningarna på [butikspanelen](./amazon-store-dashboard.md).

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
>Om du säljer förnyade (renoverade) produkter måste du registrera dig för [!DNL Amazon Renewed Program]. Se [Förnyade produkter](./renewed-products.md).

Om din katalog innehåller produkter med olika villkor (till exempel Ny, Används och Återanvänd) måste du välja **[!UICONTROL Assign Condition Using Product Attribute]**. Med den här inställningen kan du mappa ditt [!DNL Commerce]-villkorsattribut och -värden till villkoren i din Amazon-lista.

Under [Förinställningsuppgifter](./amazon-pre-setup-tasks.md) uppmuntras du att skapa ett [!DNL Commerce]-produktattribut för en produkts villkor. Om du erbjuder produkter under olika förhållanden och du inte har skapat något villkorsattribut läser du [Skapa ett produktattribut i [!DNL Commerce]](./ob-creating-magento-attributes.md). När villkorsattributet har skapats kan du tilldela ett villkorsvärde till var och en av dina produkter i din [!DNL Commerce]-katalog.

## Konfigurera inställningar

1. Klicka på **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet **[!UICONTROL Product Listing Condition]**.

1. Välj ett alternativ för **[!UICONTROL Listing Product Condition]**.

   Välj ett av Amazon standardvillkor för ditt globala villkorsvärde för alla dina listor. Standardinställningen är `New`.

   Om du har produkter/listor som har olika villkor väljer du `Assign Condition Using Product Attribute` för att definiera dina produktvillkorsinställningar i de ytterligare fält som visas.

1. För **villkorsattribut** väljer du [!DNL Commerce]-attributet för att mappa värden för vart och ett av Amazon standardvillkorsattribut.

   Om du har produkter i `Used`- eller `Collectible`-villkoret men inte ytterligare skiljer dig åt, kan du mappa till ett enda `Used`- eller `Collectible`-Amazon-villkor och lämna de andra tomma. Den här metoden mappar alla dina `Used`- eller `Collectible`-villkor till det enskilda Amazon-villkoret Används eller Hämtbart.

   Du har till exempel ett enda `Used`-villkor för dina produkter. Vid mappning väljer du om du vill mappa till Amazon-villkoret `Used; Like New`, `Used; Very Good`, `Used; Good` eller `Used; Acceptable`. Fyll bara i fältet för det Amazon-villkor som du vill använda och lämna de andra `Used`-alternativen inställda på `--Select Option--`. I exempelbilden mappas alla [!DNL Commerce]-produkter i `Used`-villkoret till Amazon `Used; Very Good`-villkoret.

   Du kan också ange beskrivande text för villkoren, förutom `New`.

1. Klicka på **[!UICONTROL Save listing settings]** när du är klar.

![Villkor för produktlista](assets/amazon-product-listing-condition.png)

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Listing Product Condition] | Villkor för produktlistor. Alternativ: `New` / `Refurbished` / `Used: Like New` / `Used: Very Good` / `Used: Good` / `Used: Acceptable` / `Collectible: Like New` / `Collectible: Very Good` / `Collectible: Good` / `Collectible: Acceptable` / `Assign Condition Using Product Attribute`<br><br>Om du säljer ett enstaka produktvillkor väljer du något av Amazon standardvillkoren. Om din [!DNL Commerce]-katalog innehåller produkter under olika förhållanden väljer du `Assign Condition Using Product Attribute`. |
| [!UICONTROL Condition Attribute] | Attributet [!DNL Commerce] som definierar villkoret för dina produkter. Markera det Magneto-attribut som du skapade för att mappa till Amazon villkorsattribut. I [Exempel på förinställningsuppgifter](./ob-creating-magento-attributes.md) rekommenderar du att du namnger den som `Amazon Condition`. När du väljer det här alternativet visas ytterligare fält för att mappa Amazon standardvillkor. |
| [!UICONTROL Additional Condition fields] | För vart och ett av standardvillkoren för Amazon väljer du motsvarande villkor. Alternativen är villkorsetiketterna som du lade till när du [skapade ditt Amazon-villkorsattribut](./ob-creating-magento-attributes.md).<br><br>Om du har produkter i  `Used` eller  `Collectible` villkor men inte gör någon ytterligare skillnad kan du mappa till ett enskilt  `Used` eller  `Collectible` Amazon-villkor och lämna de andra tomma. Den här metoden mappar alla `Used`- eller `Collectible`-villkor till det enskilda Amazon-villkoret Används eller Hämtbart. |

**Snabb åtkomst**  -  [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
