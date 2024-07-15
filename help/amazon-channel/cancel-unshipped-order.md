---
title: Avbryta en olevererad Amazon-beställning
description: Avbryt en väntande eller delvis levererad beställning (ej levererad) via ditt Amazon [!DNL Seller Central] konto.
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# Avbryta en olevererad Amazon-beställning

Amazon-beställningar kan bara avbrytas om de har statusen `Unshipped`. Om ordern är väntande eller delvis levererad (ej levererad), kan beställningen endast annulleras via ditt [!DNL Amazon Seller Central]-konto. Om artikeln har levererats måste returer och utbyten också hanteras i ditt [!DNL Amazon Seller Central]-konto.

>[!NOTE]
>
>För andra uppgifter än att annullera en order:
>
>- Om du har [orderimport](./order-settings.md) aktiverat hanteras beställningar i arbetsflödet för [[!DNL Commerce] beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).
>- Om [orderimport](./order-settings.md) är inaktiverad måste du hantera dina beställningar i [!DNL Amazon Seller Central].

## Avbryt en order i statusen `Unshipped`

1. Klicka på **[!UICONTROL View Store]** på butikskortet.

1. Klicka på ett ordernummer i avsnittet _[!UICONTROL Recent Orders]_på kontrollpanelen för butik.

   Sidan _[!UICONTROL Amazon Order Details]_visas.

1. Klicka på **[!UICONTROL Cancel Order]** i sidhuvudsfältet.

   Det här alternativet visas bara för order med statusen `Unshipped`.

1. Välj ett alternativ för **[!UICONTROL Reason for cancellation]**.

1. Klicka på **[!UICONTROL Confirm]**.

   Ordern avbryts och statusen uppdateras till `Canceled` i orderinformationen.

Annulleringsmeddelandet skickas till ditt [!DNL Amazon Seller Central]-konto och kunden som är kopplad till ordern meddelas också. Statusen för motsvarande [!DNL Commerce]-order, om någon, ändras till `Complete`.
