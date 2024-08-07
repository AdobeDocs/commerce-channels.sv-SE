---
title: 'Intelligent Repricing Rule: Competitor Conditional Variances'
description: Bestäm priset på Amazon baserat på konkurrenternas priser och villkor genom att skapa en intelligent regel för omprissättning.
feature: Sales Channels, Configuration
exl-id: c52230e3-4e47-45bc-80e0-170530f58987
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Regel för intelligent omprisering: Villkorliga avvikelser för konkurrenter

Avsnitt i en intelligent regel för återprissättning omfattar:

- [[!UICONTROL Select Rule Type]](./intelligent-repricing-rules.md)
- [!UICONTROL Competitor Conditional Variances]
- [[!UICONTROL Price Adjustment]](./price-adjustment.md)
- [[!UICONTROL Floor Price]](./floor-price.md)
- [[!UICONTROL Optional Ceiling Price]](./optional-ceiling-price.md)

En intelligent regel för omprissättning använder Amazon konkurrenters priser för att fastställa ert pris. Konkurrenterna är andra säljare som listar samma produkter som du listar på Amazon.

Om det finns en produkt med samma villkor är basmatchningspriset det [lägsta konkurrentpriset](./lowest-competitor-pricing.md) med samma villkor. Om ingen konkurrentprodukt matchar ditt villkor, går basmatchningspriset igenom andra tillgängliga konkurrensvillkor som börjar med New, Refurbished och fortsätter med tillgängliga villkor. När ett villkor har hittats blir basmatchningspriset det lägsta priset i det villkoret.

Om du har en produkt i listan med villkoret `Used; Good` och basmatchningspriset, och en konkurrent har samma produkt i samma villkor till ett lägre pris, används konkurrentpriset. Om en konkurrent inte finns med samma villkor söker systemet efter en konkurrent med nästa villkor, som är `New`. Om en konkurrent hittas med det villkoret används det lägsta priset.

## Konfigurera villkorsavvikelser för konkurrent

Definiera dina villkorsavvikelser i avsnittet _[!UICONTROL Competitor Conditional Variances]_.

Välj ett alternativ för **[!UICONTROL Conditional Variance]**:

- `Use all competitor's product conditions` - (Standard) Välj när du vill att produkten ska jämföras med något tillgängligt villkor (om det inte finns någon matchning för villkoret som du anger).

- `Use Only Matching Competitor's Product Condition` - Välj när du vill att din produkt endast ska jämföras med konkurrentens produkter i samma skick. Om det inte finns någon matchning får produkten priset _Magento i Source_ som definieras i ditt [listpris](./listing-price.md).

- `Apply Variance (if competitor's product condition differs)` - Välj att först försöka jämföra med ditt matchade produktvillkor. Om det inte finns något matchande villkor används en avvikelse (som ett procenttal) i förhållande till ditt produktvillkor och den lägsta konkurrentens villkor.

  När funktionen _[!UICONTROL Apply Variance]_väljs visas ytterligare variansfält för var och en av dina Amazon-villkor. Med den här funktionen kan ni använda smarta regler för omprissättning när ni erbjuder produkter som är i ett annat skick än konkurrenterna. För att förstå beräkningen bakom villkorlig avvikelse måste du först förstå att alla avvikelser bestäms utifrån ett basmatchningspris.

  Villkorliga variansalternativ som visas baseras på dina listinställningar för `Condition` som har mappats till villkorsvärden med ett [!DNL Commerce] [produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). För alla mappade villkor kan du definiera en avvikelseprocent på 1-100. Undantaget är samlarföremål, i vilket fall ett procenttal som är större än 100 kan tillämpas.

![Intelligent ompriseringsregel - villkorliga avvikelser för konkurrent](assets/amazon-competitor-cond-variances.png){width="500" zoomable="yes"}

| Fält | Beskrivning |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Competitor Conditional Variances] | Alternativ: <ul><li>**[!UICONTROL Use all competitor's product conditions]** - Om det inte finns någon matchning för villkoret som du anger produkten med, matchar det här alternativet alla tillgängliga villkor. Först försöker den att matcha ditt villkor och sedan fungerar den från villkoret `New` till `Used; Acceptable`.</li><li>**[!UICONTROL Use only matching competitor's product condition]** - Det här alternativet matchar produktens villkor. Om det inte finns någon matchning får du produktpriserna på _[!UICONTROL Magento Price Source]_.</li><li>>**[!UICONTROL Apply variance (if competitor's product condition differs)]** - Det här alternativet försöker först matcha mot ditt produktvillkor. Om det inte finns något matchande villkor tillämpas en avvikelse (i procent) i förhållande till ditt produktvillkor och den lägsta konkurrentens villkor.</li></ul><br><br>Alternativen för villkorlig avvikelse som visas baserat på dina listinställningar för Villkor som mappas till villkorsvärden med ett [!DNL Commerce] [produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). För alla mappade villkor kan du ange en avvikelseprocent på 1-100. Undantaget är samlarföremål, i vilket fall ett procenttal som är större än 100 kan tillämpas.<br><br>Med den här funktionen kan du använda smarta omprisregler när du erbjuder produkter som är i ett annat skick än dina konkurrenter. För att förstå beräkningen bakom villkorlig avvikelse måste du först förstå att alla avvikelser bestäms utifrån ett basmatchningspris. |

## Beräkna basen för villkorlig avvikelse

- BMC (Base Match Condition Variance) = Avvikelsen för villkoret för din matchningspris. Med hjälp av det tidigare exemplet är BMC variansen för villkoret `New`.
- MCV (Merchant Condition Variance) = Variansen för produktens skick. Med hjälp av det tidigare exemplet är MCV = variansen för villkoret `Used; Good`.
- BMP (Base Match Price) = $7,99 (förklaras ovan)

Formeln för beräkning av villkorlig avvikelsebas är följande:

![formel för beräkning av villkorlig avvikelsebas](assets/amazon-cond-variance-calc-1.png){width="300"}

## Exempel

Inställningar för villkorlig avvikelse är följande:

![exempel på inställningar för villkorlig avvikelse](assets/amazon-cond-variances.png){width="500" zoomable="yes"}

- BMC = 100 (konkurrentvillkor = Nytt)
- MCV = 80 (Affärsvillkor = Använt; Bra)
- BMP = 7,99 USD (basmatchningspris = det lägsta priset för matchande konkurrentvillkor)

![exempel på beräkning av villkorlig avvikelsebas](assets/amazon-cond-variance-calc-2.png){width="300"}

Med hjälp av den villkorliga avvikelsebasberäkningen ovan är din villkorliga avvikelsebas = $6,39. Den här beräkningen är den konkurrentpriskälla som används för dina prisregelåtgärder, vilket förklaras ytterligare i [Prisjustering](./price-adjustment.md).
