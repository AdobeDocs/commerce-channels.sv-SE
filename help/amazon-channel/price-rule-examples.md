---
title: Amazon säljkanal - Exempel på prisregel
description: Se de här exemplen baserat på vanliga scenarier för att få hjälp med att utforma prisregler för listor från Amazon.
feature: Sales Channels, Price Rules
exl-id: 4d9717ba-4ad6-468d-b4ca-99f8620b60b4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 2%

---

# Exempel på prisregler

## Exempel på standardprisregler

### Ignorera efterföljande regler

Möjligheten att ignorera efterföljande regler är en bra funktion i prissättningsreglerna som förhindrar att flera olika prisregler staplas och ger oönskade ytterligare rabatter. Om du vill ignorera efterföljande regler måste en prisregel använda de prioriteter som anges i _[!UICONTROL Priority]_avsnitt i [Allmänna inställningar för prisregel](./pricing-rule-general-settings.md).

If **[!UICONTROL Discard Subsequent Rules]** är inställd på `Yes`gäller dock inte reglerna med lägre prioritet (högre nummer) för de produkter som omfattas.

Det finns till exempel tre prisregler:

| Exempel | Regelnamn | Prioritet | Ignorera efterföljande regel |
|---------|-----------------------|----------|-------------------------|
| 1 | 10 % rabatt på produkter | 1 | Nej |
| 2 | $2 av försäljningen | 2 | Ja |
| 3 | 5 % rabatt på alla produkter | 3 | Nej |

I det här scenariot gäller regel 1 och 2 för de produkter som omfattas. Regel nr 3 gäller endast berättigade produkter som inte finns i regel nr 2 eftersom den har lägre prioritet än exempel nr 2 och **[!UICONTROL Discard Subsequent Rules]** är inställd på `Yes`. Så de produkter som ingår i säljkategorin får 10 % rabatt och 2 USD rabatt på Amazon listpris.

### Använda två standardprisregler

| Fält | Inställning - regel 1 | Inställning - regel 2 |
|--------------------------------|---------------------|-----------------------|
| [!UICONTROL Rule Name] | Regel-1 | Regel 2 |
| [!UICONTROL Priority] | 1 | 2 |
| [!UICONTROL Rule Type] | Standardprisregel | Standardprisregel |
| [!UICONTROL Price action] | Minska med | Minska med |
| [!UICONTROL Apply] | Använd som procentsats | Använd som fast belopp |
| [!UICONTROL Adjustment Amount] | 10 | 10 |

#### Produkt 1

Pris: 45,49 USD

Tillämpad regel 1: $45,49 x (0,9) = $40,94

Tillämpad regel 2: $40.94 - $10.00 = $30.94

Slutpriset efter regel 1 och regel 2 ska tillämpas: 30,94 USD

#### Produkt 2

Pris: 47,76 USD

Tillämpad regel 1: $47.76 x (0.9) = $42.98

Tillämpad regel 2: $42.98 - $10.00 = $32.98

Slutpriset efter regel 1 och regel 2 ska tillämpas: 32,98 USD

## Exempel på regel för intelligent omprissättning

### Buy Box pris med rörlig priskälla = pris

| Fält | Inställning |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | Regel-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Intelligent regel för omprissättning |
| [!UICONTROL Competitor Price Source] | Använd&quot;Buy Box&quot;-pris |
| [!UICONTROL Price Action] | Matcha konkurrentpris |
| [!UICONTROL Floor Price Source] | Pris |
| [!UICONTROL Floor Price Action] | Matcha |

#### Produkt 1

Pris: $15

[Buy Box](./buy-box-competitor-pricing.md) pris från Amazon: 10 dollar

På grund av [Buy Box](./buy-box-competitor-pricing.md) priset är lägre än det ursprungliga priset, produkten anges till det ursprungliga priset.

Det slutliga priset efter att regeln har tillämpats: $15

#### Produkt 2

Pris: $5

[Buy Box](./buy-box-competitor-pricing.md) pris från Amazon: 10 dollar

På grund av [Buy Box](./buy-box-competitor-pricing.md) priset är högre än det ursprungliga priset, produkten anges på [Buy Box](./buy-box-competitor-pricing.md) pris.

Det slutliga priset efter att regeln har tillämpats: 10 dollar

### Buy Box pris med rörlig priskälla = Pris och en prissänkning på 20 %

| Fält | Inställning |
|--------------------------------------|----------------------------|
| [!UICONTROL Rule Name] | Regel-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Intelligent regel för omprissättning |
| [!UICONTROL Competitor Price Source] | Använd&quot;Buy Box&quot;-pris |
| [!UICONTROL Price Action] | Matcha konkurrentpris |
| [!UICONTROL Floor Price Source] | Pris |
| [!UICONTROL Floor Price Action] | Minska med |
| [!UICONTROL Apply] | Använd som en procentandel |
| [!UICONTROL Floor Adjustment Amount] | 20 |

#### Produkt 1

Pris: $20

Beräknat golvpris: $16

[Buy Box](./buy-box-competitor-pricing.md) pris från Amazon: $15

På grund av [Buy Box](./buy-box-competitor-pricing.md) priset är lägre än beräknat [Baspris](./floor-price.md)finns produkten på Beräknad [Baspris](./floor-price.md).

Det slutliga priset efter att regeln har tillämpats: $16

#### Produkt 2

Pris: $15

Beräknat [Baspris](./floor-price.md): $12

[Buy Box](./buy-box-competitor-pricing.md) pris från Amazon: $15

På grund av [Buy Box](./buy-box-competitor-pricing.md) priset är större än beräknat [Baspris](./floor-price.md), visas produkten på [Buy Box](./buy-box-competitor-pricing.md) pris.

Det slutliga priset efter att regeln har tillämpats: $15

#### Produkt 3

Pris: $17

Beräknat golvpris: 13,60 USD

[Buy Box](./buy-box-competitor-pricing.md) pris från Amazon: $15

På grund av [Buy Box](./buy-box-competitor-pricing.md) priset är större än beräknat [Baspris](./floor-price.md), visas produkten på [Buy Box](./buy-box-competitor-pricing.md) pris.

Det slutliga priset efter att regeln har tillämpats: $15

### Lägsta pris med alla konkurrenters priser och använd alla konkurrenters produktvillkor

| Fält | Inställning |
|----------------------------------------|-----------------------------------------|
| [!UICONTROL Rule Name] | Regel-1 |
| [!UICONTROL Priority] | 1 |
| [!UICONTROL Rule Type] | Intelligent regel för omprissättning |
| [!UICONTROL Competitor Price Source] | Använd lägsta konkurrentpris |
| [!UICONTROL Minimum Positive Feedback] | Alla konkurrentpriser |
| [!UICONTROL Conditional Variance] | Använd alla konkurrentens produktvillkor |
| [!UICONTROL Price Action] | Matcha konkurrentpris |
| [!UICONTROL Floor Price Source] | Pris |
| [!UICONTROL Floor Price Action] | Matcha |

| Pris | Villkor |
|-------|-----------------|
| $17 | Nytt |
| $15 | Nytt |
| $14 | Används. Mycket bra |
| $13 | Används. Bra |

#### Produkt 1

Pris: 10 dollar

Villkor: Nytt

Eftersom det lägsta konkurrentpriset för det nya villkoret är 15 USD anges produkten till 15 USD.

Det slutliga priset efter att regeln har tillämpats: $15

#### Produkt 2

Pris: 10 dollar

Villkor: Används. Godtagbart

På grund av [lägsta konkurrentpris](./lowest-competitor-pricing.md) för villkoret Använt är 13 USD anges produkten till 13 USD.

Det slutliga priset efter att regeln har tillämpats: $13

### Intelligent regel för omprissättning som kombinerar takpris, valutakonvertering och moms

| Fält | Inställning |
|-----------------------------------|---------------|
| [!UICONTROL VAT] | 10% |
| [!UICONTROL Ceiling price source] | $10 |
| [!UICONTROL Currency conversion] | 1,25 euro:1 USD |

[Takpris](./optional-ceiling-price.md) På den europeiska (moms) marknaden: $10 x 1.25 = $12.50

När [tak](./optional-ceiling-price.md) på den europeiska marknaden (moms) beräknas och läggs momsen till.

Slutpris efter moms: $12.50 x (1.1) = $13.75

### Kombinera flera prisregler, takpris, valutakonvertering och moms

#### Intelligent prisregel (från föregående exempel)

| Fält | Inställning |
|----------------------|---------------|
| Prioritet | 1 |
| moms | 10% |
| Tak priskälla | $10 |
| Valutakonvertering | 1,25 euro:1 USD |

[Takpris](./optional-ceiling-price.md) På den europeiska (moms) marknaden: $10 x 1.25 = $12.50

Slutpris efter moms: $12.50 x (1.1) = $13.75

#### Standardprisregel

| Fält | Inställning |
|--------------------------------|-----------------------|
| [!UICONTROL Priority] | 2 |
| [!UICONTROL Price Action] | Öka med |
| [!UICONTROL Apply] | Använd som fast belopp |
| [!UICONTROL Adjustment Amount] | $5.00 |

När [tak](./optional-ceiling-price.md) är träffad tillämpas standardprisregeln ovanpå regeln om intelligent prissättning.

Slutpris efter att standardprisregeln har tillämpats: $13.75 + $5.00 = $18.75

### Prisjustering

I det här exemplet definieras det mest konkurrenskraftiga priset genom att titta på Amazon [konkurrentens lägsta pris](./lowest-competitor-pricing.md) med 95 % positiv feedback och minst 1 000 feedback-granskningar.

![Exempel på prisjustering](assets/amazon-price-adjustment-example.png){width="600" zoomable="yes"}

När sökningen har utförts baserat på de här parametrarna återgår priset till 25 dollar.

Här är tre olika [prisregelåtgärd](./pricing-rule-actions.md) baserat på det lägsta priset.

| Fält | Beskrivning |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Price Action] | Alternativ:<ul><li>**[!UICONTROL Decrease By]** - Det här alternativet minskar ditt listpris i förhållande till [lägsta konkurrentpris](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Increase By]** - Det här alternativet ökar ditt listpris i förhållande till [lägsta konkurrentpris](./lowest-competitor-pricing.md).</li><li>**[!UICONTROL Match Competitor Price]** - Det här alternativet ändrar ditt Amazon-pris så att det matchar det lägsta priset baserat på parametrarna. I exemplet är Amazon listpris 25 dollar.</li></ul> |
| [!UICONTROL Apply] | Alternativ: Använd som procentsats / Använd som fast belopp |
| [!UICONTROL Adjustment Amount] | Numeriskt värde för att definiera procentandelen eller det fasta beloppet för den rabatt som ska tillämpas. <br>Dessa val resulterar i att det lägsta priset sätts till 0,01 USD lägre. |

### Golvpris

| Fält | Inställning |
|--------------------------------------|---------------------|
| [!UICONTROL Floor Price Source] | Kostnad = $5 |
| [!UICONTROL Floor Price Action] | Öka med |
| [!UICONTROL Apply] | Använd som procentsats |
| [!UICONTROL Floor Adjustment Amount] | 5 |

[Golvpris](./floor-price.md) beräkning = rörlig priskälla `$5` x Justeringsbelopp för golv `5%` = $5,25

När regeln om intelligent prissättning tillämpas, tillåter den att listpriset är lägre än 5,25 USD för den här specifika produkten när kostnaden är 5 USD.
