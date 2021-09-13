---
title: Lägg till prisregler
description: Använd prisregler för att hantera listpriser på Amazon Marketplace för din Commerce-produktkatalog.
exl-id: 37ecf25a-7b47-4f6d-a4bb-2f306f7b5997
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Lägg till prisregler

Prisreglerna kan konfigureras och ändras när som helst efter att butiken har integrerats. Prisreglerna ingår i [listinställningarna](./listing-settings.md) och kan nås på [butikspanelen](./amazon-store-dashboard.md).

## Standardprisregel

Med en standardprisregelåtgärd kan du öka eller minska ett Amazon-listpris med en viss procentandel eller ett fast belopp i förhållande till **[!UICONTROL Magento Price Source*]* som är definierat i [listpriset](./listing-price.md).

### Lägg till en standardprisregel

1. Klicka på **[!UICONTROL Pricing rules]** på butikens kontrollpanel.

1. Klicka på **[!UICONTROL Add new pricing rule]**.

1. Fyll i **[[!UICONTROL General Settings]](./pricing-rule-general-settings.md)** för regeln.

1. Fyll i **[[!UICONTROL Price Rule Conditions]](./pricing-rule-conditions.md)** för regeln.

1. Fyll i **[[!UICONTROL Price Rule Actions]](./standard-price-rules.md)** för regeln.

1. Klicka på **[!UICONTROL Save pricing rule]** när du är klar.

## Intelligent regel för omprissättning

En intelligent regel för omprissättning använder Amazon konkurrenters priser för att fastställa ert pris. Konkurrenterna är andra säljare som listar samma produkter som du listar på Amazon.

### Lägg till en intelligent regel för omprissättning

1. Klicka på **[!UICONTROL Pricing rules]** på butikens kontrollpanel.

1. Klicka på **[!UICONTROL Add new pricing rule]**.

1. Fyll i **[[!UICONTROL General Settings]](./pricing-rule-general-settings.md)** för regeln.

1. Fyll i **[[!UICONTROL Price Rule Conditions]](./pricing-rule-conditions.md)** för regeln.

1. Fyll i **[!UICONTROL Price Rule Actions]** för regeln.

   - [[!UICONTROL Select Rule Typ]e](./intelligent-repricing-rules.md)

   - [[!UICONTROL Competitor Conditional Variances]](./competitor-conditional-variances.md)

   - [[!UICONTROL Price Adjustment]](./price-adjustment.md)

   - [[!UICONTROL Floor Price]](./floor-price.md)

   - [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

1. Klicka på **[!UICONTROL Save pricing rule]** när du är klar.
