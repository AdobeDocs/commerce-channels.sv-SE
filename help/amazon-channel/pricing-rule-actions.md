---
title: Amazon försäljningskanal - Prisregelåtgärder
description: Använd prisregelåtgärderna för att definiera justeringsberäkningarna som tillämpas på priskällan för att fastställa Amazon listpris.
feature: Sales Channels, Price Rules
exl-id: c46bd5c2-7994-45b4-ae0c-9e473372c73a
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Prisregelåtgärder

Prisregelåtgärder definierar de justeringsberäkningar som tillämpas på priskällan för att fastställa listpriset.

## Standardprisregel

Med en [standardprisregel](./standard-price-rules.md) kan du öka eller minska ett listpris i Amazon med en viss procentandel eller ett fast belopp i förhållande till katalogpriset [!DNL Commerce] (eller priskällan).

| Avsnitt | Beskrivning |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./standard-price-rules.md) | Ange regeltypen till `Standard price rule`. |
| [[!UICONTROL Price Adjustment]](./standard-price-rules.md) | Definiera justeringsberäkningarna som tillämpas på priskällan för att fastställa listpriset |

## Intelligent regel för omprissättning

En [intelligent regel för omprissättning](./intelligent-repricing-rules.md) använder Amazon konkurrenters priser för att fastställa ditt listpris. Konkurrenterna är andra säljare som listar samma produkter som du listar på Amazon.

| Avsnitt | Beskrivning |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md) | Ange regeltypen till `Intelligent repricing rule` tillsammans med konkurrentprisets Source och feedbackkraven. |
| [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md) | Definiera avvikelser för villkoren för samma produkt som säljs av konkurrenter. |
| [[!UICONTROL Price Adjustment]](./price-adjustment.md) | Definiera justeringsberäkningarna som tillämpas på priskällan för att fastställa listpriset |
| [[!UICONTROL Floor Price]](./floor-price.md) | Definiera det lägsta priset för en produkt för att förhindra att flera prisregler ställer in ett listpris för lågt. |
| [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md) | Definiera det högsta priset för en produkt för att säkerställa att dina priser förblir konkurrenskraftiga. |
