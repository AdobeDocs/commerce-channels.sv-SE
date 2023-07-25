---
title: Amazon försäljningskanal - [!UICONTROL Price Adjustment]
description: Konfigurera prisjusteringar för att definiera prisberäkningen när du har identifierat priskällan för Amazon-konkurrenten.
feature: Sales Channels, Price Rules
exl-id: 60569b37-2a6d-40ef-bcec-2c3a132a07e0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# [!UICONTROL Price Adjustment]

>[!NOTE]
>
>Avsnittet Prisjustering skiljer sig något åt för reglerna för Standard och Intelligent prissättning. **[!UICONTROL Match Competitor Price]** är endast tillgängligt under _[!UICONTROL Price Action]_när **[!UICONTROL Rule Type]**är inställd på `Intelligent repricing rule`.

Avsnitt i en intelligent regel för återprissättning omfattar:

- [Välj regeltyp](./intelligent-repricing-rules.md)
- [Villkorsavvikelser för konkurrenter](./competitor-conditional-variances.md)
- Prisjustering
- [Baspris](./floor-price.md)
- [Valfritt takpris](./optional-ceiling-price.md)

Prisjusteringen definierar prisberäkningen när du har identifierat konkurrentens priskälla.

## Konfigurera prisjustering

Definiera prisjusteringen i _[!UICONTROL Price Adjustment]_-avsnitt.

1. För **[!UICONTROL Price Action]** väljer du ett alternativ:

   - `Decrease By` - Välj när du vill att det definierade priskällvärdet ska justeras nedåt, vilket skapar ett lägre pris för regeln, innan det anges i Amazon.

   - `Increase By` - Välj när du vill att det definierade priskällvärdet ska justeras uppåt, vilket skapar ett högre pris för regeln, innan det anges i Amazon.

   - `Match Competitor Price` - (Endast regel för intelligent omprissättning) Välj när du vill ändra ditt Amazon-pris så att det matchar [lägsta konkurrent](./lowest-competitor-pricing.md) baserat på konkurrentens feedback och avvikelseparametrar. När inställt på `Match Competitor Price`, _[!UICONTROL Apply]_och_[!UICONTROL Adjustment Amount]_ fält tas bort.

1. För **[!UICONTROL Apply]** väljer du ett alternativ:

   - `Apply as percentage` - Välj när du vill ha den definierade **[!UICONTROL Magento Price Source]** definieras i [Listpris](./listing-price.md) justeras med ett procenttal.

   - `Apply as fixed amount` - Välj när du vill ha den definierade **[!UICONTROL Magento Price Source]** definieras i [Listpris](./listing-price.md) justerat med ett fast belopp.

1. För **[!UICONTROL Adjustment Amount]** (obligatoriskt), ange det numeriska värdet för prisjusteringen.

   - När **[!UICONTROL Apply]** är inställd på `Apply as percentage`anger du procentvärdet (exempel: enter `25` för en justering på 25 %).

   - När **[!UICONTROL Apply]** är inställd på `Apply as fixed amount`anger du det numeriska värdet för det fasta beloppet (exempel: enter `25` för en fast justering på 25 USD).

![Intelligent regel för omprissättning - prisjustering](assets/amazon-price-adjustment.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Välj en prisjusteringsåtgärd. Alternativ:<br>**[!UICONTROL Decrease By]**- Välj när du vill ha den definierade _[!UICONTROL Magento Price Source]_definieras i [Listpris](./listing-price.md) som ska justeras ned, vilket skapar ett lägre pris för regeln, innan den tas upp på Amazon.<br>**[!UICONTROL Increase By]**- Välj när du vill ha den definierade_[!UICONTROL Magento Price Source]_ definieras i [Listpris](./listing-price.md) som ska justeras upp, vilket skapar ett högre pris för regeln, innan den tas upp i Amazon.<br>**[!UICONTROL Match Competitor Price]**- (Endast regel för intelligent omprissättning) Välj när du vill ändra ditt Amazon-pris så att det matchar [lägsta konkurrent](./lowest-competitor-pricing.md) baserat på konkurrentens feedback och avvikelseparametrar. När du väljer det här alternativet visas _Använd_ och _Justeringsbelopp_ fält tas bort. |
| [!UICONTROL Apply] | Alternativ:<br>**[!UICONTROL Apply as percentage]**- Välj när du vill ha den definierade _[!UICONTROL Magento Price Source]_definieras i [Listpris](./listing-price.md) justeras med ett procenttal.<br>**[!UICONTROL Apply as fixed amount]**- Välj när du vill ha den definierade_[!UICONTROL Magento Price Source]_ definieras i [Listpris](./listing-price.md) justerat med ett fast belopp. |
| [!UICONTROL Adjustment Amount] | Obligatoriskt.<br>Om du valde `Apply as percentage` for **[!UICONTROL Apply]** anger du procentvärdet (exempel: enter `25` för en justering på 25 %).<br>Om du valde `Apply as fixed amount` for **[!UICONTROL Apply]** anger du det numeriska värdet för det fasta beloppet (exempel: enter `25` för en fast justering på 25 USD). |
