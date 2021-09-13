---
title: Standardprisregelåtgärder
description: Använd standardprisregelåtgärder för att öka eller minska ett listpris för Amazon i förhållande till Commerce-katalogpriset (eller priskällan).
exl-id: 91df6ef3-852b-478b-8b01-51dd437dd4f9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Åtgärder för standardprisregel

Med en standardprisregelåtgärd kan du öka eller minska ett Amazon-listpris med en viss procentandel eller ett fast belopp i förhållande till katalogpriset [!DNL Commerce] (eller priskällan).

Avsnitt i en standardprisregelåtgärd är:

- [!UICONTROL Select Rule Type]
- [!UICONTROL Price Adjustment]

## Konfigurera prisregelåtgärder

1. Välj `Standard price rule` för **[!UICONTROL Rule Type]**.

   Det här alternativet inaktiverar de andra fälten i _[!UICONTROL Select Rule Type]_-avsnittet.

1. Expandera avsnittet _[!UICONTROL Price Adjustment]_om det behövs.

1. För **[!UICONTROL Price Action]** väljer du ett alternativ för att bestämma hur du vill ändra *[!UICONTROL Magento Price Source]*-värdet (definierat i [listpriset](./listing-price.md)).

   - `Decrease By` - Välj när du vill att värdet ska minskas innan det anges till Amazon.

   - `Increase By` - Välj när du vill att värdet ska ökas innan du publicerar till Amazon.

1. För **[!UICONTROL Apply]** väljer du ett alternativ för att bestämma hur du vill att det definierade *[!UICONTROL Magento Price Source]* som definieras i [listpriset](./listing-price.md)-värdet ska justeras:

   - `Apply as percentage` - Välj när du vill att det definierade  *[!UICONTROL Magento Price Source]* värdet i ditt  [listpris ska ](./listing-price.md) justeras med ett procentvärde

   - `Apply as fixed amount` - Välj när du vill att det definierade  *[!UICONTROL Magento Price Source]* värdet i ditt  [listpris ska ](./listing-price.md) justeras med ett fast belopp.

1. För **[!UICONTROL Adjustment Amount]** (obligatoriskt) anger du det numeriska värdet för prisjusteringen.

   - När *[!UICONTROL Apply]* är `Apply as percentage` anger du procentvärdet (exempel: ange `25` för en prisjustering på 25 %).

   - När *[!UICONTROL Apply]* är `Apply as fixed amount` anger du det numeriska värdet för det fasta beloppet (exempel: ange `25` för en fast prisjustering på $25).

1. Klicka på **[!UICONTROL Save pricing rule]** när du är klar.

![Standardprisregel](assets/ob-price-rule-action-standard-example.png)

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Rule Type] | Välj `Standard price rule`. |
| [!UICONTROL Price Action] | Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill att det definierade  [!DNL Commerce] priskällvärdet ska minskas innan det anges till Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill att det definierade  [!DNL Commerce] priskällvärdet ska höjas innan du publicerar det på Amazon.</li></ul> |
| [!UICONTROL Apply] | Alternativ:<ul><li>**[!UICONTROL Apply as percentage]** - Välj när du vill att det definierade  [!DNL Commerce] priskällvärdet ska justeras i procent.</li><li>**[!UICONTROL Apply as fixed amount]** - Välj när du vill att det definierade  [!DNL Commerce] priskällvärdet ska justeras med ett fast belopp.</li></ul> |
| [!UICONTROL Adjustment Amount] | Obligatoriskt.<br><br>Om du väljer  `Apply as percentage` för  *[!UICONTROL Apply]* anger du procentvärdet (exempel: ange  `25` för en justering på 25 %).<br><br>Om du väljer  `Apply as fixed amount` för  *[!UICONTROL Apply]* anger du det numeriska värdet för det fasta beloppet (exempel: ange  `25` för en fast justering på $25). |
