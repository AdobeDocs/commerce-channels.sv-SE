---
title: '"Intelligent Repricing Rule: Valfritt takpris'
description: Använd de valfria takprisinställningarna för att skydda ditt högsta produktpris mot de intelligenta prisregler som hanterar dina Amazon-listor.
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Intelligent ompriseringsregel: frivilligt tak

Avsnitt i en intelligent regel för återprissättning omfattar:

- [Välj regeltyp](./intelligent-repricing-rules.md)
- [Villkorsavvikelser för konkurrenter](./competitor-conditional-variances.md)
- [Prisjustering](./price-adjustment.md)
- [Baspris](./floor-price.md)
- Valfritt takpris

De automatiska takprisinställningarna skyddar automatiskt ditt högsta produktpris mot reglerna för intelligent prissättning, vilket gör att du kan sätta ett tak (högsta pris) för dina smarta prisregler.

## Konfigurera det valfria takpriset

Definiera dina valfria inställningar för högsta pris i avsnittet _[!UICONTROL Optional Ceiling Price]_.

1. Välj ett attribut för **[!UICONTROL Ceiling Price Source]**.

   Välj ditt [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;} som anger din relativa takgräns. Om du t.ex. inte vill att ditt Amazon-pris ska ligga över minimipriset för ditt objekt väljer du attributet `Manufacturer's Suggested Retail Price`.

1. Välj ett alternativ för **[!UICONTROL Ceiling Price Action]**.

   - `Decrease By` - Välj när du vill att det definierade  _[!UICONTROL Ceiling Price Source]_värdet ska justeras nedåt, vilket skapar ett lägre takpris för regeln, innan det visas i Amazon.

   - `Increase By` - Välj när du vill att det definierade  _[!UICONTROL Ceiling Price Source]_värdet ska justeras uppåt, vilket skapar ett högre takpris för regeln, innan det visas på Amazon.

   - `Match` - Välj när du inte vill att listpriset ska fluktuera över det definierade  _[!UICONTROL Ceiling Price Source]_värdet. Om `Match` anges är fälten_[!UICONTROL Apply]_ och _[!UICONTROL Ceiling Adjustment Amount]_inaktiverade.

1. Låt **[!UICONTROL Apply]** vara `Apply as percentage` som standard.

1. För **[!UICONTROL Ceiling Adjustment Price]** anger du det numeriska värdet för procentvärdet för att justera _[!UICONTROL Ceiling Price Source]_-värdet.

I det här exemplet sätts taket till 2 % under artikelns minimipris.

![Intelligent regel för omprissättning - valfritt takpris](assets/ob-intelligent-price-rule-ceiling.png)

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Ceiling Price Source] | Välj det [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;} som anger din relativa takgräns. Om du t.ex. inte vill att priset på din produktlista ska ligga över minimipriset för din artikel, väljer du `Manufacturer's Suggested Retail Price`-attributet. |
| [!UICONTROL Ceiling Price Action] | Välj en prisjusteringsåtgärd. Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill att det definierade  _[!UICONTROL Ceiling Price Source]_värdet ska justeras nedåt, vilket skapar ett lägre takpris för regeln, innan det visas i Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill att det definierade  _[!UICONTROL Ceiling Price Source]_värdet ska justeras uppåt, vilket skapar ett högre takpris för regeln, innan det visas på Amazon.</li><li>**[!UICONTROL Match]** - Välj när du inte vill att listpriset ska fluktuera över det definierade  _[!UICONTROL Ceiling Price Source]_värdet. Om `Match` anges är fälten_[!UICONTROL Apply]_ och _[!UICONTROL Ceiling Adjustment Amount]_inaktiverade.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - en procentuell justering i förhållande till  _[!UICONTROL Ceiling Price Source]_värdet. |
| [!UICONTROL Ceiling Price Adjustment] | Ange det numeriska värdet för procentvärdet för att justera _[!UICONTROL Ceiling Price Source]_-värdet. |
