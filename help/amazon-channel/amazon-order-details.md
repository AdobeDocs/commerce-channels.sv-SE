---
title: Beställningsinformation för Amazon
description: Läs mer om dina Amazon Marketplace-beställningar i Adobe Commerce eller Magento Open Source Admin.
feature: Sales Channels, Orders
exl-id: a85bb6b3-817d-4859-a815-41777f4b8667
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Beställningsinformation för Amazon

![Beställningsinformation för Amazon](assets/amazon-order-details-header.png){width="600" zoomable="yes"}

## Visa beställningsinformation för Amazon

1. Klicka på **[!UICONTROL View Store]** på butikskortet.

1. Klicka på ett ordernummer i avsnittet _[!UICONTROL Recent Orders]_.

   Sidan _[!UICONTROL Amazon Order Details]_öppnas.

>[!NOTE]
>
>Om du har aktiverat orderimport i dina [orderinställningar](./order-settings.md) och ordningen [uppfylls av Amazon (FBA)](./fulfilled-by.md) kan du se exempeldata för vissa fält i orderinformationen. Amazon skickar inte följande data för FBA-beställningar.
>
> - `AddressType`
> - `AddressLine1`
> - `AddressLine2`
> - `AddressLine3`
> - `BuyerName`
> - `Phone`
> - `PurchaseOrderNumber`
> - `RecipientName`
> - `CustomizedURL`
> - `GiftMessageText`

### Fliken Order and Shipping Details

Fliken _[!UICONTROL Order and Shipping Details]_visar detaljerad orderinformation som tagits emot från Amazon.

>[!IMPORTANT]
>
>Amazon godkänner icke-standardadressinformation som inte kan importeras till Amazon försäljningskanal, vilket förhindrar att delstat-/landskoderna uppdateras korrekt för vissa order. Följande fält kan redigeras i orderinformationen för att korrigera adressfel:
>
>- `Shipping address 1`
>- `Shipping address 2`
>- `Shipping address 3`
>- `Shipping city`
>- `Shipping region`
>- `Shipping postal code`
>- `Shipping country`
>
>Glöm inte att klicka på **Spara ordning** när du har redigerat.

![Beställnings- och leveransinformation](assets/amazon-order-details.png){width="600" zoomable="yes"}

### Fliken Orderposter

Fliken _[!UICONTROL Order Items]_visar alla objekt som är associerade med Amazon-beställningen, enligt Amazon.

![Beställningsinformation](assets/amazon-order-item-details.png){width="600" zoomable="yes"}

### Fliken Spårning

På fliken _[!UICONTROL Tracking]_visas spårningsinformation som är kopplad till Amazon-beställningen.

![Spårningsinformation](assets/amazon-order-tracking-details.png){width="600" zoomable="yes"}
