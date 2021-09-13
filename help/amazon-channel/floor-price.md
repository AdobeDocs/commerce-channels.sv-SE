---
title: '"Intelligent Repricing Rule: Pris på golv'
description: Använd inställningarna för lägsta pris för att fastställa det lägsta priset för en intelligent prisregel för att hantera dina Amazon-listor.
exl-id: e00cac95-eef8-4d4d-b578-287a91f54bdf
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---

# Intelligent ompriseringsregel: lägsta pris

Avsnitt i en intelligent regel för återprissättning omfattar:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [!UICONTROL Floor Price]
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

Inställningarna för [lägsta pris](./floor-price.md) skyddar automatiskt ditt lägsta produktpris mot reglerna för intelligent prissättning. Använd de här inställningarna för att ange ett golv (lägsta pris) för dina smarta prisregler och se till att dina produkter inte listas under ett önskat pris.

Attributen för golvpris baseras på webbplatsens omfång om din [!DNL Commerce]-butik använder webbplatsens prisomfång. Se [Prisomfång](./price-scope.md).

Golvpriset används bara när **[!UICONTROL Rule Type]** är `Intelligent repricing rule`.

## Konfigurera golvpris

Definiera den lägsta prisinställningen i avsnittet _[!UICONTROL Floor Price]_.

1. Välj ett priskällattribut för **[!UICONTROL Floor Price Source]**.

   Välj det [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){target=&quot;_blank&quot;} som anger din relativa golvgräns. Om du t.ex. inte vill att priset på din Amazon ska gå under kostnaden för artikeln väljer du attributet *Kostnad*.

1. Välj ett alternativ för **[!UICONTROL Floor Price Action]**.

   - `Decrease By` - Välj när du vill att det definierade  _[!UICONTROL Floor Price Source]_värdet ska justeras nedåt, vilket skapar ett lägre minimipris för regeln, innan det anges i Amazon.

   - `Increase By` - Välj när du vill att det definierade  _[!UICONTROL Floor Price Source]_värdet ska justeras uppåt, vilket skapar ett högre golvpris för regeln, innan du listar till Amazon.

   - `Match` - Välj när du inte vill att listpriset ska fluktuera under det definierade  _[!UICONTROL Floor Price Source]_värdet. Om `Match` anges är fälten_[!UICONTROL Apply]_ och _[!UICONTROL Floor Adjustment Amount]_inaktiverade.

1. Låt **[!UICONTROL Apply]** vara `Apply as percentage` som standard.

1. För **[!UICONTROL Floor Adjustment Price]** anger du det numeriska värdet för procentvärdet för att justera _[!UICONTROL Floor Price Source]_-värdet.

I det här exemplet sätts minimipriset till 3 % över kostnaden för artikeln.

![Exempel på regel för intelligent omprissättning - lägsta pris](assets/ob-intelligent-pricde-rule-floor-price.png)

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Floor Price Source] | Välj det [!DNL Commerce]-attribut som anger din relativa golvgräns (lägsta pris). Om du t.ex. inte vill att priset på ditt Amazon-konto ska gå under kostnaden för ditt objekt väljer du attributet `Cost`. |
| [!UICONTROL Floor Price Action] | Välj en prisjusteringsåtgärd. Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill att det definierade  _[!UICONTROL Floor Price Source]_värdet ska justeras nedåt, vilket skapar ett lägre minimipris för regeln, innan det anges i Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill att det definierade  _[!UICONTROL Floor Price Source]_värdet ska justeras uppåt, vilket skapar ett högre golvpris för regeln, innan du listar till Amazon.</li><li>**[!UICONTROL Match]** - Välj när du inte vill att listpriset ska fluktuera under det definierade  _[!UICONTROL Floor Price Source]_värdet. När du väljer det här alternativet inaktiveras fälten_[!UICONTROL Apply]_ och _[!UICONTROL Floor Adjustment Amount]_.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - en procentuell justering i förhållande till  _[!UICONTROL Floor Price Source]_värdet. |
| [!UICONTROL Floor Adjustment Amount] | Ange det numeriska värdet för procentvärdet för att justera _[!UICONTROL Floor Price Source]_-värdet. |
