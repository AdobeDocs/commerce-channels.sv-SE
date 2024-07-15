---
title: Bearbeta order
description: 'Instruktioner för frakt och annullering [!DNL Walmart Marketplace] av beställningar från Adobe Commerce och Magento Open Source.'
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Bearbeta order

När [!DNL Walmart Marketplace] order har bekräftats och skickats till [!DNL Channel Manager] använder du [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#orders-workspace) för att bearbeta ordern.

Kanalhanteraren synkroniserar uppdateringar till [!DNL Walmart Marketplace] för att säkerställa att orderstatus och leveransinformation från [!DNL Commerce] matchar data som spåras i [!DNL Walmart Marketplace].

* **Beställningsleveranser**-Walmart kräver ett spårningsnummer för alla leveranser. Om några artiklar inte finns i lager kan du skapa partiella leveranser för att skicka artiklar som är tillgängliga just nu. När du har skickat leveransen synkroniseras orderuppdateringarna med [!DNL Walmart Marketplace]. Sedan meddelar Walmart sina kunder om orderstatus och leveransinformation.

* **Orderannulleringar**-När du avbryter en [!DNL Walmart Marketplace]-beställning kräver Walmart en orsak till annullering som ingår i det beställningsannulleringsmeddelande som skickas till kunden. Orsaken till annulleringen visas också i informationen om orderbetalningar i [!DNL Commerce]. När du har skickat annulleringen synkroniseras lageruppdateringarna till [!DNL Walmart Marketplace]. Sedan meddelar Walmart sina kunder om orderstatus och leveransinformation.

  I butiken måste du annullera hela ordern. [!DNL Commerce] tillåter inte partiella annulleringar.

* **Återbetalningsbegäran**- Om en returbegäran från Walmart Marketplace begärs för en levererad order innehåller [!UICONTROL Status details] en länk till returen. Returer och återbetalningar hanteras från kontrollpanelen [Returer](return-refund-orders.md).

När Commerce-beställningar bearbetas och [!DNL Channel Manager] synkroniserar leveranser, partiell leverans och annulleringsuppdateringar för [!DNL Walmart Marketplace] slutförs orderbearbetningen. Returbegäranden och återbetalningar för levererade order hanteras från kontrollpanelen [Returnerar](return-refund-orders.md).

>[!NOTE]
>
> Det kan ta upp till fem minuter för orderuppdateringar att synkronisera till [!DNL Walmart Marketplace]. Om du vill kontrollera orderstatus går du tillbaka till sidan [!DNL Channel Manager] Beställningar.

## Leverera en beställning

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** i Admin.

1. Öppna butiksvyn genom att välja ögonikonen för en säljkanalsbutik.

1. Om du vill visa [!DNL Walmart Marketplace] order väljer du **[!UICONTROL Orders]**.

1. Öppna beställningen som ska levereras genom att välja **[!UICONTROL Commerce Order Number]** i tabellen Beställningar.

1. Skapa och skicka en leverans för hela eller delar av en order genom att välja **[!UICONTROL Ship]**.

   ![Commerce orderdetaljvy för en [!DNL Walmart Marketplace] order ](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

   * Välj en fraktfirma och lägg till ett spårningsnummer genom att välja **[!UICONTROL Add tracking number]**.

     ![Commerce orderdetaljvy för en [!DNL Walmart Marketplace] order ](assets/order-shipment-add-tracking-number.png){width="600" zoomable="yes"}

   * Fyll i resten av leveransformuläret efter behov. Mer information finns i [[!DNL Shipping an Order]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-ship.html).

1. När du har skickat leveransen spårar du [orderstatusen](manage-orders.md#about-order-status) i [!DNL Channel Manager] för att verifiera att uppdateringarna skickades till [!DNL Walmart Marketplace].

När en order har skickats kan du bearbeta fullständiga eller partiella återbetalningar från [!DNL Channel Manager] för artiklar som ingår i ordern baserat på returbegäranden som har tagits emot från [!DNL Walmart Marketplace]. Se [Retur- och återbetalningsorder](return-refund-orders.md).

## Avbryt en beställning

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** i Admin.

1. Öppna butiksvyn genom att välja ögonikonen för en butikskanal.

1. Om du vill visa [!DNL Walmart Marketplace] order väljer du *[!UICONTROL Orders]**.

1. Öppna [orderdetaljsidan](manage-orders.md#view-order-detail) i tabellen Beställningar genom att välja **[!UICONTROL Commerce Order Number]** för ordern som ska avbrytas.

   ![Commerce orderdetaljvy för en[!DNL Walmart Marketplace]order](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

1. Avbryt beställningen.

   * Välj **Avbryt** på menyn Orderdetaljer.

   * Markera **[!UICONTROL Cancellation reason]** i formuläret [!UICONTROL Cancel Order].

   ![Commerce orderdetaljvy för en [!DNL Walmart Marketplace] order ](assets/cancel-order-reason-selector.png){width="600" zoomable="yes"}

   * Välj **[!UICONTROL Cancel Order]**.

1. När du har skickat annulleringen spårar du [orderstatusen](manage-orders.md#about-order-status) i [!DNL Channel Manager] för att verifiera att uppdateringarna skickades till [!DNL Walmart Marketplace].

## Åtgärda orderfel

Fel kan uppstå under ordersynkroniseringsprocessen från [!DNL Walmart Marketplace] eller under orderuppdateringsprocessen för leveranser, partiella leveranser och annulleringar.

Om synkroniseringsåtgärden för en leverans-, partiell leverans- eller annulleringsuppdatering misslyckas visas status _Fel_ för ordern på sidan [!DNL Channel Manager] Beställningar. Om du vill vara säker på att leveransinformation och information om annullering av order visas korrekt i Walmart Marketplace-kontot måste du manuellt uppdatera ordern i din [!DNL Walmart Marketplace]-butik.


