---
title: Visa Amazon-beställningar
description: Visa dina order på Amazon Marketplace i Adobe Commerce eller Magento Open Source Admin.
exl-id: d7811604-8e15-4d1a-a0e7-9fa61c61ef5d
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Visa Amazon-order

Det finns två sätt att visa dina Amazon-beställningar: _[!UICONTROL Recent Orders]_och_[!UICONTROL All Orders]_.

Båda alternativen visar grundläggande beställningsinformation från Amazon, inklusive:

- Inköpsdatum
- Ordernummer
- Status
- Köparens namn
- Summa
- Orderanteckningar

_[!UICONTROL All Orders]_vy lägger till filtreringsalternativ för sökningar efter ordning.

>[!NOTE]
>
>Förutom kolumnen _[!UICONTROL Order Notes]_fylls tabellen_[!UICONTROL Amazon orders]_ i med orderinformation som den har fått från Amazon. Kolumnen _Orderanteckningar_ uppdateras av [!DNL Commerce] som orderprocesser.

## Senaste order

Du kan visa de senaste beställningarna i _[!UICONTROL Recent Orders]_-delen av [butiksinstrumentpanelen](./amazon-store-dashboard.md).

![Senaste order](assets/amazon-recent-orders-imported.png)

### Visa de senaste Amazon-beställningarna

1. Klicka på **[!UICONTROL View Store]** på ett butikskort.

1. Visa dina beställningar i _[!UICONTROL Recent Orders]_-avsnittet.

1. Om du vill visa orderinformation klickar du på Amazon ordernummer i kolumnen _[!UICONTROL Order Number]_.

   Sidan _[!UICONTROL Amazon Order Details]_för ordern öppnas.

## Visa alla order

Du kan visa alla dina Amazon-beställningar på _[!UICONTROL Amazon orders]_-sidan (kallas även_[!UICONTROL All Orders]_-vyn). Tabellen Amazon Orders liknar _[!UICONTROL Recent Orders]_-avsnittet på kontrollpanelen för butiker, men du kan visa alla dina Amazon-beställningar och begränsa din beställningslista med följande filteralternativ:

- [!UICONTROL Purchase Date (range)]
- [!UICONTROL Order Number]
- [!UICONTROL Buyer's Name]
- [!UICONTROL Total (range)]
- [!UICONTROL Status]

![Amazon beställningar](assets/amazon-orders-list-all.png)

### Se alla Amazon-order

1. Klicka på **[!UICONTROL View Store]** på ett butikskort.

1. Klicka på **[!UICONTROL All Orders]** i avsnittet _[!UICONTROL Recent Orders]_.

1. Om du vill begränsa listan eller söka efter ett visst ordernummer fyller du i **[!UICONTROL Filter by]**-parametrarna och klickar på **[!UICONTROL Apply filters]**.

1. Om du vill visa orderinformation klickar du på Amazon ordernummer i kolumnen _[!UICONTROL Order Number]_.

   Sidan _[!UICONTROL Amazon Order Details]_för ordern öppnas.

## Använda filter

Du kan använda filter i din orderlista i avsnittet _[!UICONTROL Filter by]_. Gör dina val och klicka på&#x200B;**[!UICONTROL Apply filters]**. De filter du använder visas ovanför stödrastret för beställningar.

![Filter för att visa Amazon-order](assets/amazon-orders-filter-view.png)

### Ändra använda filter

- Du kan lägga till eller ändra dina filter i _[!UICONTROL Filter by]_-avsnittet. Klicka på&#x200B;**[!UICONTROL Apply filters]**för att uppdatera ordningslistan och filteralternativen som visas ovanför rutnätet.

- Du kan ta bort filter, antingen ett i taget, genom att klicka på `x` för filtret eller alla samtidigt genom att klicka på **[!UICONTROL Clear all filters]**. När du tar bort ett filter uppdateras sorteringslistan och filteralternativen som visas ovanför rutnätet för order.

- Om orderlistan är lång kan du använda sidnumreringskontrollerna under rutnätet för att visa fler order.

>[!TIP]
>
>Några tips om ordervyn:
>
>- Om du har flera Amazon Store-integreringar kan det behövas en uppdatering av sidvyn när du växlar mellan butiksvyer för att uppdatera både orderlistan och sidnumreringsvyn för den aktuella butiken.
>- Vid sortering efter kolumn gäller sorteringen endast den aktuella listvyn. Det är bäst att filtrera listan och sedan sortera sidan som du visar.
>- Beroende på bredden på visningsfönstret kan överlappande text visas i kolumnerna. Om du vill expandera kolumnerna så att texten radbryts, breddar du fönstervyn.
>- Filtrera efter heltal vid filtrering med _[!UICONTROL Total]_. Om du anger ett decimalvärde kan det orsaka fel i resultatet.


### Standardkolumner

| Kolumn | Beskrivning |
|---|---|
| [!UICONTROL Filter by] | Endast tillgängligt i vyn _[!UICONTROL All Orders]_.<br>Beställningslistan begränsas av:<ul><li>`Purchase Date (range)`</li><li>`Order Number`</li><li>`Buyer's Name`</li><li>`Total (range)`</li><li>`Status`</li></ul> |
| [!UICONTROL Purchase Date] | Datum för köpet, enligt Amazon. |
| [!UICONTROL Order Number] | Ordernumret som genereras av och tas emot från Amazon. Klicka på länken om du vill visa skärmen för beställningsinformation för Amazon. |
| [!UICONTROL Status] | Beställningens status, enligt Amazon. Alternativ: `Error` / `Pending` / `Shipped` / `Canceled` / `Completed` / `Unshipped` / `PartiallyShipped` / `PendingAvailability` |
| [!UICONTROL Buyer's Name] | Namnet på den person som beställde, enligt Amazon. |
| [!UICONTROL Grand Total] | Orderns totala valutavärde, enligt Amazon. |
| [!UICONTROL Order Notes] | Den senaste åtgärden som spelats in för ordern när den bearbetas i [!DNL Commerce]. Informationen omfattar, men är inte begränsad till, beställningsfel och uppdateringar av orderbearbetning.<br>**Obs**: Det här fältet uppdateras av  [!DNL Commerce] som orderprocesserna. |
