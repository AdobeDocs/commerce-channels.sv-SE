---
title: Amazon försäljningskanal - Standardprisregelåtgärder
description: Använd standardprisregelåtgärder för att öka eller minska ett listpris för Amazon i förhållande till katalogpriset för Commerce (eller priskällan).
feature: Sales Channels, Price Rules
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Åtgärder för standardprisregel

Med en standardprisregelåtgärd kan du öka eller minska ett Amazon-listpris med en viss procentandel eller ett fast belopp i förhållande till katalogpriset [!DNL Commerce] (eller priskällan).

Avsnitt i en standardprisregelåtgärd är:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Konfigurera prisregelåtgärder

1. Välj `Standard price rule` för **[!UICONTROL Rule Type]**.

   Det här alternativet inaktiverar de andra fälten i avsnittet _[!UICONTROL Select Rule Type]_.

1. Expandera avsnittet _[!UICONTROL Price Adjustment]_om det behövs.

1. För **[!UICONTROL Price Action]** väljer du ett alternativ som bestämmer hur du vill ändra värdet *[!UICONTROL Magento Price Source]* (som definieras i ditt [listpris](./listing-price.md)).

   - `Decrease By` - Välj när du vill att värdet ska minskas innan det visas i Amazon.

   - `Increase By` - Välj när du vill att värdet ska ökas innan det visas i Amazon.

1. För **[!UICONTROL Apply]** väljer du ett alternativ som avgör hur du vill att det definierade *[!UICONTROL Magento Price Source]* som definieras i ditt [listpris](./listing-price.md) ska justeras:

   - `Apply as percentage` - Välj när du vill att det definierade *[!UICONTROL Magento Price Source]* som definieras i ditt [listpris](./listing-price.md)-värde ska justeras med ett procentvärde

   - `Apply as fixed amount` - Välj när du vill att det definierade *[!UICONTROL Magento Price Source]* som definieras i värdet för [listpris](./listing-price.md) ska justeras med ett fast belopp.

1. För **[!UICONTROL Adjustment Amount]** (obligatoriskt) anger du det numeriska värdet för prisjusteringen.

   - När *[!UICONTROL Apply]* är inställt på `Apply as percentage` anger du procentvärdet (exempel: ange `25` för en prisjustering på 25 %).

   - När *[!UICONTROL Apply]* är inställt på `Apply as fixed amount` anger du det numeriska värdet för det fasta beloppet (exempel: ange `25` för en fast prisjustering på $25).

1. Klicka på **[!UICONTROL Save pricing rule]** när du är klar.

![Standardprisregel](assets/ob-price-rule-action-standard-example.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | Välj `Standard price rule`. |
| [!UICONTROL Price Action] | Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill att det definierade [!DNL Commerce]-priskällvärdet ska minskas innan det visas i Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill att det definierade [!DNL Commerce]-priskällvärdet ska ökas innan det listas i Amazon.</li></ul> |
| [!UICONTROL Apply] | Alternativ:<ul><li>**[!UICONTROL Apply as percentage]** - Välj när du vill att det definierade [!DNL Commerce]-priskällvärdet ska justeras med ett procenttal.</li><li>**[!UICONTROL Apply as fixed amount]** - Välj när du vill att det definierade [!DNL Commerce]-priskällvärdet ska justeras med ett fast belopp.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obligatoriskt.<br><br>Om du väljer `Apply as percentage` för *[!UICONTROL Apply]* anger du procentvärdet (exempel: ange `25` för en justering på 25 %).<br><br>Om du väljer `Apply as fixed amount` för *[!UICONTROL Apply]* anger du det numeriska värdet för det fasta beloppet (exempel: ange `25` för en fast justering på $25). |
