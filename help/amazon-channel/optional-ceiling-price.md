---
title: '"Intelligent Repricing Rule: Valfritt takpris'
description: Använd de valfria takprisinställningarna för att skydda ditt högsta produktpris mot de intelligenta prisregler som hanterar dina Amazon-listor.
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Regel för intelligent omprisering: Valfritt takpris

Avsnitt i en intelligent regel för återprissättning omfattar:

- [Välj regeltyp](./intelligent-repricing-rules.md)
- [Villkorsavvikelser för konkurrenter](./competitor-conditional-variances.md)
- [Prisjustering](./price-adjustment.md)
- [Baspris](./floor-price.md)
- Valfritt takpris

De automatiska takprisinställningarna skyddar automatiskt ditt högsta produktpris mot reglerna för intelligent prissättning, vilket gör att du kan sätta ett tak (högsta pris) för dina smarta prisregler.

## Konfigurera det valfria takpriset

Definiera dina valfria inställningar för högsta pris i _[!UICONTROL Optional Ceiling Price]_-avsnitt.

1. För **[!UICONTROL Ceiling Price Source]** väljer du ett attribut.

   Välj [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} som anger din relativa takgräns. Om du t.ex. inte vill att priset på Amazon ska ligga över minimipriset för ditt objekt väljer du `Manufacturer's Suggested Retail Price` -attribut.

1. För **[!UICONTROL Ceiling Price Action]** väljer du ett alternativ.

   - `Decrease By` - Välj när du vill ha den definierade _[!UICONTROL Ceiling Price Source]_värde som ska justeras nedåt, vilket skapar ett lägre takpris för regeln, innan den tas upp i Amazon.

   - `Increase By` - Välj när du vill ha den definierade _[!UICONTROL Ceiling Price Source]_värde som ska justeras uppåt, vilket skapar ett högre takpris för regeln, innan den tas upp i Amazon.

   - `Match` - Välj när du inte vill att listpriset ska fluktuera över det definierade _[!UICONTROL Ceiling Price Source]_värde. När inställt på `Match`,_[!UICONTROL Apply]_ och _[!UICONTROL Ceiling Adjustment Amount]_fält är inaktiverade.

1. Lämna **[!UICONTROL Apply]** standard som `Apply as percentage`.

1. För **[!UICONTROL Ceiling Adjustment Price]**, ange det numeriska värdet för procentvärdet för att justera _[!UICONTROL Ceiling Price Source]_värde.

I det här exemplet sätts taket till 2 % under artikelns minimipris.

![Intelligent regel för omprissättning - valfritt takpris](assets/ob-intelligent-price-rule-ceiling.png)

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Ceiling Price Source] | Välj [!DNL Commerce] [produktattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){target="_blank"} som anger din relativa takgräns. Om du t.ex. inte vill att priset på din produkt ska ligga över minimipriset för din produkt väljer du `Manufacturer's Suggested Retail Price` -attribut. |
| [!UICONTROL Ceiling Price Action] | Välj en prisjusteringsåtgärd. Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill ha den definierade _[!UICONTROL Ceiling Price Source]_värde som ska justeras nedåt, vilket skapar ett lägre takpris för regeln, innan den tas upp i Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill ha den definierade _[!UICONTROL Ceiling Price Source]_värde som ska justeras uppåt, vilket skapar ett högre takpris för regeln, innan den tas upp i Amazon.</li><li>**[!UICONTROL Match]** - Välj när du inte vill att listpriset ska fluktuera över det definierade _[!UICONTROL Ceiling Price Source]_värde. När inställt på `Match`,_[!UICONTROL Apply]_ och _[!UICONTROL Ceiling Adjustment Amount]_fält är inaktiverade.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - en procentuell justering i förhållande till _[!UICONTROL Ceiling Price Source]_värde. |
| [!UICONTROL Ceiling Price Adjustment] | Ange det numeriska värdet för procentvärdet för att justera _[!UICONTROL Ceiling Price Source]_värde. |
