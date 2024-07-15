---
title: 'Intelligent Repricing Rule: Optional Ceiling Price'
description: Använd de valfria takprisinställningarna för att skydda ditt högsta produktpris mot de intelligenta prisregler som hanterar dina Amazon-listor.
feature: Sales Channels, Price Rules
exl-id: edc40e6b-e71f-41a3-8d5f-8bb73ada42a3
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Intelligent regel för omprissättning: valfritt takpris

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

   Välj ditt [!DNL Commerce] [produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) som anger din relativa takgräns. Om du t.ex. inte vill att ditt Amazon-pris ska gå över MSRP för ditt objekt väljer du attributet `Manufacturer's Suggested Retail Price`.

1. Välj ett alternativ för **[!UICONTROL Ceiling Price Action]**.

   - `Decrease By` - Välj när du vill att det definierade _[!UICONTROL Ceiling Price Source]_-värdet ska justeras nedåt, vilket skapar ett lägre takpris för regeln, innan det visas i Amazon.

   - `Increase By` - Välj när du vill att det definierade _[!UICONTROL Ceiling Price Source]_-värdet ska justeras uppåt, vilket skapar ett högre takpris för regeln, innan det visas i Amazon.

   - `Match` - Välj när du inte vill att listpriset ska fluktuera över det definierade _[!UICONTROL Ceiling Price Source]_-värdet. När `Match` anges inaktiveras fälten_[!UICONTROL Apply]_ och _[!UICONTROL Ceiling Adjustment Amount]_.

1. Använd **[!UICONTROL Apply]** som `Apply as percentage`.

1. För **[!UICONTROL Ceiling Adjustment Price]** anger du det numeriska värdet för procentvärdet för att justera ditt _[!UICONTROL Ceiling Price Source]_-värde.

I det här exemplet sätts taket till 2 % under artikelns minimipris.

![Intelligent ompriseringsregel - valfritt takpris](assets/ob-intelligent-price-rule-ceiling.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Ceiling Price Source] | Välj det [!DNL Commerce] [produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html) som anger din relativa takgräns. Om du t.ex. inte vill att priset på din produktlista ska ligga över minimipriset för ditt objekt väljer du attributet `Manufacturer's Suggested Retail Price`. |
| [!UICONTROL Ceiling Price Action] | Välj en prisjustering. Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Välj när du vill att det definierade _[!UICONTROL Ceiling Price Source]_-värdet ska justeras nedåt, vilket skapar ett lägre takpris för regeln, innan det visas i Amazon.</li><li>**[!UICONTROL Increase By]** - Välj när du vill att det definierade _[!UICONTROL Ceiling Price Source]_-värdet ska justeras uppåt, vilket skapar ett högre takpris för regeln, innan det visas i Amazon.</li><li>**[!UICONTROL Match]** - Välj när du inte vill att listpriset ska fluktuera över det definierade _[!UICONTROL Ceiling Price Source]_-värdet. När `Match` anges inaktiveras fälten_[!UICONTROL Apply]_ och _[!UICONTROL Ceiling Adjustment Amount]_.</li></ul> |
| [!UICONTROL Apply] | **[!UICONTROL Apply as percentage]** - en procentuell justering i förhållande till värdet _[!UICONTROL Ceiling Price Source]_. |
| [!UICONTROL Ceiling Price Adjustment] | Ange det numeriska värdet för procentvärdet för att justera ditt _[!UICONTROL Ceiling Price Source]_-värde. |
