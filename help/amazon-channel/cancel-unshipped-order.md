---
title: Avbryt en olevererad order
description: Avbryt en väntande eller delvis levererad beställning (ej levererad) via ditt Amazon [!DNL Seller Central] konto.
exl-id: a6df09b7-7f62-47e5-a2d3-1761802255d0
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---

# Avbryt en ej levererad order

Beställningar från Amazon kan bara avbrytas om de har statusen `Unshipped`. Om ordern är väntande eller delvis levererad (ej levererad) kan beställningen endast annulleras via ditt [!DNL Amazon Seller Central]-konto. Om artikeln har levererats måste returer och börser också hanteras i ditt [!DNL Amazon Seller Central]-konto.

>[!NOTE]
>
>För andra uppgifter än att annullera en order:
>
>- Om du har [aktiverat orderimport](./order-settings.md) hanteras beställningar i [[!DNL Commerce] orderarbetsflödet](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.
>- Om [orderimport](./order-settings.md) är inaktiverad måste du hantera dina beställningar i [!DNL Amazon Seller Central].


## Avbryt en beställning i `Unshipped`-status

1. Klicka på **[!UICONTROL View Store]** på butikskortet.

1. Klicka på ett ordernummer i avsnittet _[!UICONTROL Recent Orders]_på kontrollpanelen för butik.

   Sidan _[!UICONTROL Amazon Order Details]_visas.

1. Klicka på **[!UICONTROL Cancel Order]** i rubrikfältet.

   Det här alternativet visas bara för order med statusen `Unshipped`.

1. Välj ett alternativ för **[!UICONTROL Reason for cancellation]**.

1. Klicka på **[!UICONTROL Confirm]**.

   Ordern avbryts och statusen uppdateras till `Canceled` i orderinformationen.

Annulleringsmeddelandet skickas till ditt [!DNL Amazon Seller Central]-konto och kunden som är kopplad till ordern meddelas också. Statusen för motsvarande [!DNL Commerce]-ordning, om någon, ändras till `Complete`.
