---
title: 'Intelligent Repricing Rule: Floor Price'
description: Använd inställningarna för lägsta pris för att fastställa det lägsta priset för en intelligent prisregel för att hantera dina Amazon-listor.
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%

---

# Intelligent ompriseringsregel: pris på golv

Avsnitt i en intelligent regel för återprissättning omfattar:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Inställningarna för [lägsta pris](./floor-price.md) skyddar automatiskt ditt lägsta produktpris mot reglerna för intelligent prissättning. Använd de här inställningarna för att ange ett golv (lägsta pris) för dina smarta prisregler och se till att dina produkter inte listas under ett önskat pris.

Attributen för golvpris baseras på webbplatsens omfattning om din [!DNL Commerce]-butik använder webbplatsens prisområde. Se [Prisområde](./price-scope.md).

Golvpriset används bara när **[!UICONTROL Rule Type]** är inställt på `Intelligent repricing rule`.

## Konfigurera golvpris

Definiera den lägsta prisinställningen i avsnittet _[!UICONTROL Floor Price]_.

1. Välj ett priskällattribut för **[!UICONTROL Floor Price Source]**.

   Välj det [!DNL Commerce] [produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) som anger din relativa golvgräns. Om du t.ex. inte vill att ditt Amazon-pris ska gå under kostnaden för din artikel väljer du attributet *Kostnad*.

1. Välj ett alternativ för **[!UICONTROL Floor Price Action]**.

   - `Decrease By` - Välj när du vill att det definierade _[!UICONTROL Floor Price Source]_-värdet ska justeras nedåt, vilket skapar ett lägre minimipris för regeln, innan det visas i Amazon.

   - `Increase By` - Välj när du vill att det definierade _[!UICONTROL Floor Price Source]_-värdet ska justeras uppåt, vilket skapar ett högre lägsta pris för regeln, innan det visas i Amazon.

   - `Match` - Välj när du inte vill att listpriset ska fluktuera under det definierade _[!UICONTROL Floor Price Source]_-värdet. När `Match` anges inaktiveras fälten_[!UICONTROL Apply]_ och _[!UICONTROL Floor Adjustment Amount]_.

1. Använd **[!UICONTROL Apply]** som `Apply as percentage`.

1. För **[!UICONTROL Floor Adjustment Price]** anger du det numeriska värdet för procentvärdet för att justera ditt _[!UICONTROL Floor Price Source]_-värde.

I det här exemplet sätts minimipriset till 3 % över kostnaden för artikeln.

![Exempel på regel för intelligent omprisering - lägsta pris](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | Välj attributet [!DNL Commerce] som anger din relativa golvgräns (lägsta pris). Om du t.ex. inte vill att ditt Amazon-pris ska gå under kostnaden för ditt objekt väljer du attributet `Cost`. |
| [!UICONTROL Floor Price Action] | Välj en prisjustering. Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill att det definierade _[!UICONTROL Floor Price Source]_-värdet ska justeras nedåt, vilket skapar ett lägre minimipris för regeln, innan det visas i Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill att det definierade _[!UICONTROL Floor Price Source]_-värdet ska justeras uppåt, vilket skapar ett högre lägsta pris för regeln, innan det visas i Amazon.</li><li>**[!UICONTROL Match]** - Välj när du inte vill att listpriset ska fluktuera under det definierade _[!UICONTROL Floor Price Source]_-värdet. När du väljer det här alternativet inaktiveras fälten_[!UICONTROL Apply]_ och _[!UICONTROL Floor Adjustment Amount]_.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - en procentuell justering i förhållande till värdet _[!UICONTROL Floor Price Source]_. |
| [!UICONTROL Floor Adjustment Amount] | Ange det numeriska värdet för procentvärdet för att justera ditt _[!UICONTROL Floor Price Source]_-värde. |
