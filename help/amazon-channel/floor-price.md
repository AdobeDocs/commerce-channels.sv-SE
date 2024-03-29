---
title: 'Intelligent Repricing Rule: Floor Price'
description: Använd inställningarna för lägsta pris för att fastställa det lägsta priset för en intelligent prisregel för att hantera dina Amazon-listor.
feature: Sales Channels, Price Rules
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Intelligent ompriseringsregel: pris på golv

Avsnitt i en intelligent regel för återprissättning omfattar:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

The [lägsta pris](./floor-price.md) inställningarna automatiskt skyddar ditt lägsta produktpris mot reglerna för intelligenta priser. Använd de här inställningarna för att ange ett golv (lägsta pris) för dina smarta prisregler och se till att dina produkter inte listas under ett önskat pris.

Prisattributen baseras på webbplatsens omfång om [!DNL Commerce] butiken använder webbplatsens prisområde. Se [Prisomfång](./price-scope.md).

Golvpriset används endast när **[!UICONTROL Rule Type]** är inställd på `Intelligent repricing rule`.

## Konfigurera golvpris

Definiera din lägsta prisinställning i dialogrutan _[!UICONTROL Floor Price]_-avsnitt.

1. För **[!UICONTROL Floor Price Source]** väljer du ett priskällattribut.

   Välj [!DNL Commerce] [produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) som anger din relativa golvgräns. Om du t.ex. inte vill att priset på ditt Amazon ska gå under kostnaden för ditt objekt väljer du *Kostnad* -attribut.

1. För **[!UICONTROL Floor Price Action]** väljer du ett alternativ.

   - `Decrease By` - Välj när du vill ha den definierade _[!UICONTROL Floor Price Source]_det värde som ska justeras nedåt, vilket skapar ett lägre minimipris för regeln, innan den tas upp i Amazon.

   - `Increase By` - Välj när du vill ha den definierade _[!UICONTROL Floor Price Source]_värdet som ska justeras uppåt, vilket skapar ett högre minimipris för regeln, innan den tas upp i Amazon.

   - `Match` - Välj när du inte vill att listpriset ska fluktuera under det definierade _[!UICONTROL Floor Price Source]_värde. När inställt på `Match`,_[!UICONTROL Apply]_ och _[!UICONTROL Floor Adjustment Amount]_fält är inaktiverade.

1. Lämna **[!UICONTROL Apply]** standard som `Apply as percentage`.

1. För **[!UICONTROL Floor Adjustment Price]**, ange det numeriska värdet för procentvärdet för att justera _[!UICONTROL Floor Price Source]_värde.

I det här exemplet sätts minimipriset till 3 % över kostnaden för artikeln.

![Exempel på regel för intelligent omprissättning - lägsta pris](assets/ob-intelligent-pricde-rule-floor-price.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Floor Price Source] | Välj [!DNL Commerce] attribut som anger relativ golvgräns (lägsta pris). Om du t.ex. inte vill att priset på ditt Amazon ska gå under kostnaden för ditt objekt väljer du `Cost` -attribut. |
| [!UICONTROL Floor Price Action] | Välj en prisjustering. Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill ha den definierade _[!UICONTROL Floor Price Source]_det värde som ska justeras nedåt, vilket skapar ett lägre minimipris för regeln, innan den tas upp i Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill ha den definierade _[!UICONTROL Floor Price Source]_värdet som ska justeras uppåt, vilket skapar ett högre minimipris för regeln, innan den tas upp i Amazon.</li><li>**[!UICONTROL Match]** - Välj när du inte vill att listpriset ska fluktuera under det definierade _[!UICONTROL Floor Price Source]_värde. När du väljer det här alternativet visas_[!UICONTROL Apply]_ och _[!UICONTROL Floor Adjustment Amount]_fält är inaktiverade.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - en procentuell justering i förhållande till _[!UICONTROL Floor Price Source]_värde. |
| [!UICONTROL Floor Adjustment Amount] | Ange det numeriska värdet för procentvärdet för att justera _[!UICONTROL Floor Price Source]_värde. |
