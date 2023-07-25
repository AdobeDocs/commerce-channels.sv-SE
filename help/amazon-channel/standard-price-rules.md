---
title: Amazon försäljningskanal - Standardprisregelåtgärder
description: Använd standardprisregelåtgärder för att öka eller minska ett listpris för Amazon i förhållande till Commerce-katalogpriset (eller priskällan).
feature: Sales Channels, Price Rules
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Åtgärder för standardprisregel

Med en standardprisregelåtgärd kan du öka eller minska ett Amazon-listpris med en viss procentandel eller ett fast belopp i förhållande till [!DNL Commerce] katalogpris (eller priskälla).

Avsnitt i en standardprisregelåtgärd är:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Konfigurera prisregelåtgärder

1. För **[!UICONTROL Rule Type]**, välja `Standard price rule`.

   Det här alternativet inaktiverar de andra fälten i dialogrutan _[!UICONTROL Select Rule Type]_-avsnitt.

1. Expandera _[!UICONTROL Price Adjustment]_vid behov.

1. För **[!UICONTROL Price Action]** väljer du ett alternativ som bestämmer hur du vill ändra *[!UICONTROL Magento Price Source]* (definieras i [Listpris](./listing-price.md)).

   - `Decrease By` - Välj när du vill att värdet ska minskas innan det anges till Amazon.

   - `Increase By` - Välj när du vill att värdet ska ökas innan du publicerar till Amazon.

1. För **[!UICONTROL Apply]** väljer du ett alternativ som bestämmer hur du vill ha den definierade *[!UICONTROL Magento Price Source]* definieras i [Listpris](./listing-price.md) värde som ska justeras:

   - `Apply as percentage` - Välj när du vill ha den definierade *[!UICONTROL Magento Price Source]* definieras i [Listpris](./listing-price.md) värde justerat med ett procenttal

   - `Apply as fixed amount` - Välj när du vill ha den definierade *[!UICONTROL Magento Price Source]* definieras i [Listpris](./listing-price.md) värdet justerat med ett fast belopp.

1. För **[!UICONTROL Adjustment Amount]** (obligatoriskt), ange det numeriska värdet för prisjusteringen.

   - När *[!UICONTROL Apply]* är inställd på `Apply as percentage`anger du procentvärdet (exempel: enter `25` för en prisjustering på 25 %).

   - När *[!UICONTROL Apply]* är inställd på `Apply as fixed amount`anger du det numeriska värdet för det fasta beloppet (exempel: enter `25` för en fast prisjustering på 25 USD).

1. När du är klar klickar du på **[!UICONTROL Save pricing rule]**.

![Standardprisregel](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | Välj `Standard price rule`. |
| [!UICONTROL Price Action] | Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill ha den definierade [!DNL Commerce] Priskällvärdet som ska minskas innan det anges i Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill ha den definierade [!DNL Commerce] Priskällvärde som ska ökas innan det anges till Amazon.</li></ul> |
| [!UICONTROL Apply] | Alternativ:<ul><li>**[!UICONTROL Apply as percentage]** - Välj när du vill ha den definierade [!DNL Commerce] priskällvärdet justerat med ett procenttal.</li><li>**[!UICONTROL Apply as fixed amount]** - Välj när du vill ha den definierade [!DNL Commerce] Priskällvärdet justerat med ett fast belopp.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obligatoriskt.<br><br>Om du väljer `Apply as percentage` for *[!UICONTROL Apply]* anger du procentvärdet (exempel: enter `25` för en justering på 25 %).<br><br>Om du valde `Apply as fixed amount` for *[!UICONTROL Apply]* anger du det numeriska värdet för det fasta beloppet (exempel: enter `25` för en fast justering på 25 USD). |
