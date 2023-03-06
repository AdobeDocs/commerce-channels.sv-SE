---
title: Avbryt en olevererad order
description: Avbryta en väntande eller delvis levererad beställning via din Amazon [!DNL Seller Central] konto.
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Avbryt en olevererad order

Beställningar från Amazon kan bara avbrytas om de finns i en `Unshipped` status. Om ordern är väntande eller delvis levererad (ej levererad), kan beställningen endast annulleras via [!DNL Amazon Seller Central] konto. Om artikeln har levererats måste returer och utbyten också hanteras i [!DNL Amazon Seller Central] Konto.

>[!NOTE]
>
>För andra uppgifter än att annullera en order:
>
>- Om du har [beställ import](./order-settings.md) aktiverad, beställningar hanteras i [[!DNL Commerce] orderarbetsflöde](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}.
>- If [beställ import](./order-settings.md) är inaktiverat måste du hantera dina beställningar i [!DNL Amazon Seller Central].


## Avbryt en beställning i `Unshipped` status

1. Klicka **[!UICONTROL View Store]** på butikskortet.

1. I _[!UICONTROL Recent Orders]_klickar du på ett ordernummer i butikspanelen.

   The _[!UICONTROL Amazon Order Details]_visas.

1. Klicka **[!UICONTROL Cancel Order]** i rubrikfältet.

   Det här alternativet visas bara för order i `Unshipped` status.

1. För **[!UICONTROL Reason for cancellation]** väljer du ett alternativ.

1. Klicka **[!UICONTROL Confirm]**.

   Ordern annulleras och statusen uppdateras till `Canceled` i orderinformationen.

Meddelandet om att du vill avbryta skickas till [!DNL Amazon Seller Central] och kunden som är kopplad till ordern också meddelas. Status för motsvarande [!DNL Commerce] i förekommande fall, ändra `Complete`.
