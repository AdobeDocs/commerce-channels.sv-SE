---
title: Lägg till Amazon prisregler
description: Använd prisregler för att hantera listpriser på Amazon Marketplace för din Commerce-produktkatalog.
role: Admin
feature: Sales Channels, Products, Merchandising
exl-id: 37ecf25a-7b47-4f6d-a4bb-2f306f7b5997
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# Lägg till Amazon prisregler

Prisreglerna kan konfigureras och ändras när som helst efter att butiken har integrerats. Prisreglerna ingår i [listinställningarna](./listing-settings.md) och kan nås på [butikens kontrollpanel](./amazon-store-dashboard.md).

## Standardprisregel

Med en standardprisregelåtgärd kan du öka eller minska ett Amazon-listpris med en viss procentandel eller ett fast belopp i förhållande till **[!UICONTROL Magento Price Source*]* som definieras i ditt [listpris](./listing-price.md).

### Lägg till en standardprisregel

1. Klicka på **[!UICONTROL Pricing rules]** på butikens kontrollpanel.

1. Klicka på **[!UICONTROL Add new pricing rule]**.

1. Slutför **[[!UICONTROL General Settings]](./pricing-rule-general-settings.md)** för regeln.

1. Slutför **[[!UICONTROL Price Rule Conditions]](./pricing-rule-conditions.md)** för regeln.

1. Slutför **[[!UICONTROL Price Rule Actions]](./standard-price-rules.md)** för regeln.

1. Klicka på **[!UICONTROL Save pricing rule]** när du är klar.

## Intelligent regel för omprissättning

En intelligent regel för omprissättning använder Amazon konkurrenters priser för att fastställa ert pris. Konkurrenterna är andra säljare som listar samma produkter som du listar på Amazon.

### Lägg till en intelligent regel för omprissättning

1. Klicka på **[!UICONTROL Pricing rules]** på butikens kontrollpanel.

1. Klicka på **[!UICONTROL Add new pricing rule]**.

1. Slutför **[[!UICONTROL General Settings]](./pricing-rule-general-settings.md)** för regeln.

1. Slutför **[[!UICONTROL Price Rule Conditions]](./pricing-rule-conditions.md)** för regeln.

1. Slutför **[!UICONTROL Price Rule Actions]** för regeln.

   - [[!UICONTROL Select Rule Typ]e](./intelligent-repricing-rules.md)

   - [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)

   - [[!UICONTROL Price Adjustment]](./price-adjustment.md)

   - [[!UICONTROL Floor Price]](./floor-price.md)

   - [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

1. Klicka på **[!UICONTROL Save pricing rule]** när du är klar.
