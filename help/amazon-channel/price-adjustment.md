---
title: Prisjustering
description: Konfigurera prisjusteringar för att definiera prisberäkningen när du har identifierat priskällan för Amazon-konkurrenten.
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Prisjustering

>[!NOTE]
>
>Avsnittet Prisjustering skiljer sig något åt för reglerna för Standard och Intelligent prissättning. **[!UICONTROL Match Competitor Price]** är bara tillgängligt under  _[!UICONTROL Price Action]_när **[!UICONTROL Rule Type]**är inställt på  `Intelligent repricing rule`.

Avsnitt i en intelligent regel för återprissättning omfattar:

- [Välj regeltyp](./intelligent-repricing-rules.md)
- [Villkorsavvikelser för konkurrenter](./competitor-conditional-variances.md)
- Prisjustering
- [Baspris](./floor-price.md)
- [Valfritt takpris](./optional-ceiling-price.md)

Prisjusteringen definierar prisberäkningen när du har identifierat konkurrentens priskälla.

## Konfigurera prisjustering

Definiera prisjusteringen i avsnittet _[!UICONTROL Price Adjustment]_.

1. Välj ett alternativ för **[!UICONTROL Price Action]**:

   - `Decrease By` - Välj när du vill att det definierade priskällvärdet ska justeras nedåt, vilket skapar ett lägre pris för regeln, innan det anges i Amazon.

   - `Increase By` - Välj när du vill att det definierade priskällvärdet ska justeras uppåt, vilket skapar ett högre pris för regeln, innan det anges i Amazon.

   - `Match Competitor Price` - (Endast regel för intelligent omprissättning) Välj när du vill ändra ditt Amazon-pris så att det matchar det  [lägsta ](./lowest-competitor-pricing.md) konkurrentpriset, baserat på din konkurrents feedback- och variansparametrar. Om `Match Competitor Price` anges tas fälten _[!UICONTROL Apply]_och_[!UICONTROL Adjustment Amount]_ bort.

1. Välj ett alternativ för **[!UICONTROL Apply]**:

   - `Apply as percentage` - Välj när du vill att det definierade  **[!UICONTROL Magento Price Source]** värdet i  [listpriset ska ](./listing-price.md) justeras med ett procenttal.

   - `Apply as fixed amount` - Välj när du vill att det definierade  **[!UICONTROL Magento Price Source]** värdet i  [listpriset ska ](./listing-price.md) justeras med ett fast belopp.

1. För **[!UICONTROL Adjustment Amount]** (obligatoriskt) anger du det numeriska värdet för prisjusteringen.

   - När **[!UICONTROL Apply]** är `Apply as percentage` anger du procentvärdet (exempel: ange `25` för en justering på 25 %).

   - När **[!UICONTROL Apply]** är `Apply as fixed amount` anger du det numeriska värdet för det fasta beloppet (exempel: ange `25` för en fast justering på $25).

![Intelligent regel för omprissättning - prisjustering](assets/amazon-price-adjustment.png)

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Price Action] | Välj en prisjusteringsåtgärd. Alternativ:<br>**[!UICONTROL Decrease By]**- Välj när du vill att det definierade _[!UICONTROL Magento Price Source]_som definieras i [listpriset](./listing-price.md) ska justeras nedåt, vilket skapar ett lägre pris för regeln, innan det anges till Amazon.<br>**[!UICONTROL Increase By]**- Välj när du vill att det definierade_[!UICONTROL Magento Price Source]_ värdet i  [ ](./listing-price.md) listpriset ska justeras upp, vilket skapar ett högre pris för regeln, innan det läggs upp på Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Endast regel för intelligent omprissättning) Välj när du vill ändra ditt Amazon-pris så att det matchar det  [lägsta ](./lowest-competitor-pricing.md) konkurrentpriset, baserat på din konkurrents feedback- och variansparametrar. När du väljer det här alternativet tas fälten _Använd_ och _Justeringsmängd_ bort. |
| [!UICONTROL Apply] | Alternativ:<br>**[!UICONTROL Apply as percentage]**- Välj när du vill att det definierade _[!UICONTROL Magento Price Source]_som definieras i [listpriset](./listing-price.md) ska justeras med ett procenttal.<br>**[!UICONTROL Apply as fixed amount]**- Välj när du vill att det definierade_[!UICONTROL Magento Price Source]_ värdet i  [listpriset ska ](./listing-price.md) justeras med ett fast belopp. |
| [!UICONTROL Adjustment Amount] | Obligatoriskt.<br>Om du väljer  `Apply as percentage` för  **[!UICONTROL Apply]** anger du procentvärdet (exempel: ange  `25` för en justering på 25 %).<br>Om du väljer  `Apply as fixed amount` för  **[!UICONTROL Apply]** anger du det numeriska värdet för det fasta beloppet (exempel: ange  `25` för en fast justering på $25). |
