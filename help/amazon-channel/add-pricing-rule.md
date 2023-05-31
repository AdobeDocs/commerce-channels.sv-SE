---
title: Lägg till Amazon prisregler
description: Använd prisregler för att hantera listpriser på Amazon Marketplace för din Commerce-produktkatalog.
exl-id: 37ecf25a-7b47-4f6d-a4bb-2f306f7b5997
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---

# Lägg till Amazon prisregler

Prisreglerna kan konfigureras och ändras när som helst efter att butiken har integrerats. Prisreglerna ingår i [Listinställningar](./listing-settings.md) och kan öppnas i [instrumentpanel för butik](./amazon-store-dashboard.md).

## Standardprisregel

Med en standardprisregelåtgärd kan du öka eller minska ett Amazon-listpris med en viss procentandel eller ett fast belopp i förhållande till **[!UICONTROL Magento Price Source*]* definieras i [Listpris](./listing-price.md).

### Lägg till en standardprisregel

1. Klicka **[!UICONTROL Pricing rules]** på butikens kontrollpanel.

1. Klicka **[!UICONTROL Add new pricing rule]**.

1. Slutför **[[!UICONTROL General Settings]](./pricing-rule-general-settings.md)** för regeln.

1. Slutför **[[!UICONTROL Price Rule Conditions]](./pricing-rule-conditions.md)** för regeln.

1. Slutför **[[!UICONTROL Price Rule Actions]](./standard-price-rules.md)** för regeln.

1. När du är klar klickar du på **[!UICONTROL Save pricing rule]**.

## Intelligent regel för omprissättning

En intelligent regel för omprissättning använder Amazon konkurrenters priser för att fastställa ert pris. Konkurrenterna är andra säljare som listar samma produkter som du listar på Amazon.

### Lägg till en intelligent regel för omprissättning

1. Klicka **[!UICONTROL Pricing rules]** på butikens kontrollpanel.

1. Klicka **[!UICONTROL Add new pricing rule]**.

1. Slutför **[[!UICONTROL General Settings]](./pricing-rule-general-settings.md)** för regeln.

1. Slutför **[[!UICONTROL Price Rule Conditions]](./pricing-rule-conditions.md)** för regeln.

1. Slutför **[!UICONTROL Price Rule Actions]** för regeln.

   - [[!UICONTROL Select Rule Typ]e](./intelligent-repricing-rules.md)

   - [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)

   - [[!UICONTROL Price Adjustment]](./price-adjustment.md)

   - [[!UICONTROL Floor Price]](./floor-price.md)

   - [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

1. När du är klar klickar du på **[!UICONTROL Save pricing rule]**.
