---
title: "[!DNL (B2B) Business Price] för Amazon-listor"
description: Du kan visa dina [!DNL Commerce] butiksprodukter på Amazon Business-webbplatsen (B2B) genom att aktivera företag i ditt Amazon [!DNL Seller Central] konto.
role: Admin
level: Intermediate
feature: Sales Channels, Configuration, B2B, Tools and External Services, Merchandising, Integration
exl-id: 12a6cb2d-7a22-4b6d-9e94-ce91d564f42f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# [!DNL (B2B) Business Price] för Amazon-listor

(B2B) Affärsprisinställningarna ingår i dina butiksinställningar. Du kommer åt listinställningarna från [Amazon Store-instrumentpanelen](./amazon-store-dashboard.md).

[!DNL Amazon Business] är en marknadsplats som är exklusiv för Amazon registrerade affärskonton och endast är tillgänglig i USA, Frankrike, Tyskland och Storbritannien. Om marknadsplatsen tillåter B2B-företagspriser kan den redigeras i dina listinställningar.

[!DNL B2B Business Pricing] tillåter handlare med affärskonton att köpa från varandra med förväntat resultat för Amazon shoppingupplevelse. Med B2B-priser kan företag erbjuda nivåindelade priser baserat på inköpskvantiteten.

För att dina produkter ska kunna listas på webbplatsen [!DNL Amazon Business (B2B)] måste du först aktivera företag i ditt [!DNL Amazon Seller Central]-konto. Mer information om B2B-funktionen finns i [Amazon: B2B Central](https://sellercentral.amazon.com/gp/help/G202161480/){target="_blank"} (kräver Seller Central-inloggning).

## Konfigurera inställningar för [!DNL (B2B) Business Price]

1. Klicka på **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet _[!UICONTROL (B2B) Business Price]_.

1. Välj ett alternativ för **[!UICONTROL Enable Business Pricing]**.

   - `Disabled` - (Standard) Välj när du inte vill aktivera försäljning från företag till företag. Alla andra fält i det här avsnittet inaktiveras när de väljs.

   - `Enabled` - Välj när du vill aktivera försäljning från företag till företag. När det här alternativet är aktiverat sätts företagspriset till samma pris som listpriset när alla prisregler har tillämpats. Affärspriset följer webbplatsens prisnivå, om detta är aktiverat. Ett företagspris får inte vara mindre än $1.

1. Välj ett alternativ för **[!UICONTROL Enable Tiered Pricing]**.

   - `Disabled` - (Standard) Välj när du vill ha samma listpris för alla orderkvantiteter. När du väljer det här alternativet inaktiveras alla _[!UICONTROL Pricing Level]_-fält i det här avsnittet.

   - `Enabled` - Välj när du vill aktivera prisjusteringar baserat på orderkvantitet. När du väljer det här alternativet aktiveras _[!UICONTROL Pricing Level]_-fälten.

1. Slutför inställningarna för **[!UICONTROL Pricing Level]**.

   Du kan definiera upp till fem inställningar för kvantitet/rabatt som anger nivåpriset för dina företagslistor. På varje rad anger du tröskelvärdet för kvantitet och den rabattprocent som ska användas. Om du till exempel anger `5` i det första fältet på den första raden och `5` i det andra fältet får priset 5 % rabatt när ett annat företag köper minst 5.

1. Klicka på **[!UICONTROL Save listing settings]** när du är klar.

![Amazon Business Pricing (B2B)](assets/amazon-business-pricing.png){width="500" zoomable="yes"}

| Fält | Beskrivning |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Business Pricing] | Alternativ: <ul><li>**[!UICONTROL Disabled]** - (Standard) Välj när du inte vill aktivera affärsförsäljning. När du väljer det här alternativet inaktiveras alla andra fält i det här avsnittet.</li><li>**[!UICONTROL Enabled]** - Välj när du vill aktivera ditt företag för affärsförsäljning. När du väljer det här alternativet sätts företagspriset till samma pris som listpriset när alla prisregler har tillämpats. Affärspriset följer webbplatsens prisnivå, om detta är aktiverat. Ett företagspris får inte vara mindre än $1.</li></ul> |
| [!UICONTROL Enable Tiered Pricing] | (Obligatoriskt) Alternativ: <ul><li>**[!UICONTROL Disabled]** - (Standard) Välj när du vill ha samma listpris för alla orderkvantiteter. När du väljer det här alternativet inaktiveras alla _[!UICONTROL Pricing Level]_-fält i det här avsnittet.</li><li>**[!UICONTROL Enabled]** - Välj när du vill aktivera priser som justeras baserat på orderkvantitet. När du väljer det här alternativet aktiveras _[!UICONTROL Pricing Level]_-fälten.</li></ul> |
| [!UICONTROL Pricing Level One-Five (qty/discount)] | När nivåpriser är aktiverade kan du definiera upp till fem kvantitet-/rabattinställningar som anger nivåpriset för dina företagslistor. På varje rad anger du tröskelvärdet för kvantitet och den rabattprocent som ska användas. Om du till exempel anger `5` i det första fältet på den första raden och `5` i det andra fältet, får priset 5 % rabatt när ett annat företag köper minst fem. |

**Snabbåtkomst** - [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
