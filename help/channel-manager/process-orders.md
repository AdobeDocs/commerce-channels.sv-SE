---
title: Bearbeta order
description: Instruktioner för frakt och annullering [!DNL Walmart Marketplace] beställningar från Adobe Commerce och Magento Open Source."
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: 638ba8c595652e66aa5f15f5207855c6d2b872d7
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# Bearbeta order

Efter [!DNL Walmart Marketplace] beställningar har bekräftats och skickats till [!DNL Channel Manager]använder du [Hantering av handelsorder](https://docs.magento.com/user-guide/sales/orders-workspace.html) för att bearbeta ordern.

Channel Manager synkroniserar uppdateringar med [!DNL Walmart Marketplace] för att säkerställa orderstatus och leveransinformation från [!DNL Commerce] matchar data som spåras i [!DNL Walmart Marketplace].

* **Beställa försändelser**-Walmart kräver ett spårningsnummer för alla leveranser. Om några artiklar inte finns i lager kan du skapa partiella leveranser för att skicka artiklar som är tillgängliga just nu. När du har skickat leveransen synkroniseras orderuppdateringarna med [!DNL Walmart Marketplace]. Sedan meddelar Walmart sina kunder om orderstatus och leveransinformation.

* **Orderannulleringar**-När du avbryter en [!DNL Walmart Marketplace] order kräver Walmart en orsak till annullering som ingår i det beställningsmeddelande som skickas till kunden. Orsaken till annulleringen visas också i [!DNL Commerce] beställa betalningsinformation. När du har skickat annulleringen synkroniseras lageruppdateringarna med [!DNL Walmart Marketplace]. Sedan meddelar Walmart sina kunder om orderstatus och leveransinformation.

   I butiken måste du annullera hela ordern. [!DNL Commerce] tillåter inte partiella annulleringar.

När handelsorder bearbetas och [!DNL Channel Manager] har synkroniserat försändelse, partiell leverans och annulleringsuppdateringar för [!DNL Walmart Marketplace]är orderbehandlingen slutförd.

>[!NOTE]
>
> Det kan ta upp till fem minuter innan orderuppdateringarna synkroniseras till [!DNL Walmart Marketplace]. Om du vill kontrollera orderstatus går du tillbaka till [!DNL Channel Manager] Sidan Beställningar.

## Leverera en order

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Öppna butiksvyn genom att välja ögonikonen för en säljkanalsbutik.

1. Visa [!DNL Walmart Marketplace] order, välj *[!UICONTROL *Orders]**.

1. Öppna beställningen som ska levereras i tabellen Order (Beställningar) genom att välja **Handelsordernummer**.

1. Skapa och skicka en leverans för hela eller delar av en order genom att välja **[!UICONTROL Ship]**.

   ![Detaljvy för handelsorder för en [!DNL Walmart Marketplace] order](assets/order-detail-with-external-order-id.png)

   * Välj en fraktfirma och lägg till ett spårningsnummer genom att välja **[!UICONTROL Add tracking number]**.

      ![Detaljvy för handelsorder för en [!DNL Walmart Marketplace] order](assets/order-shipment-add-tracking-number.png)


   * Fyll i resten av leveransformuläret efter behov. Se [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) för detaljerade anvisningar.

1. Håll koll på [orderstatus](manage-orders.md#about-order-status) in [!DNL Channel Manager] för att verifiera att uppdateringar skickades till [!DNL Walmart Marketplace].

## Avbryt en beställning

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Öppna butiksvyn genom att välja ögonikonen för en butikskanal.

1. Visa [!DNL Walmart Marketplace] order, välj *[!UICONTROL *Orders]**.

1. I tabellen Order (Beställningar) öppnar du [orderdetaljsida](manage-orders.md#view-order-detail) genom att välja **Handelsordernummer** för ordern att annullera.

   ![Detaljvy för handelsorder för en[!DNL Walmart Marketplace]order](assets/order-detail-with-external-order-id.png)

1. Avbryt ordern.

   * Välj **Avbryt** på menyn Ordningsinformation.

   * På [!UICONTROL Cancel Order] formulär väljer du **Orsak till annullering**.
   ![Detaljvy för handelsorder för en [!DNL Walmart Marketplace] order](assets/cancel-order-reason-selector.png)

   * Välj **Avbryt beställning**.


1. När du har skickat annulleringen spårar du [orderstatus](manage-orders.md#about-order-status) in [!DNL Channel Manager] för att verifiera att uppdateringar skickades till [!DNL Walmart Marketplace].

## Åtgärda orderfel

Fel kan uppstå under ordersynkroniseringsprocessen från [!DNL Walmart Marketplace]eller under orderuppdateringsprocessen för försändelser, partiella leveranser och annulleringar.

Om synkroniseringsåtgärden för en försändelse, delleverans eller annullering misslyckas, kommer [!DNL Channel Manager] På sidan Beställningar visas en _Fel_ status för ordern. Om du vill försäkra dig om att leveransinformation och orderannulleringsinformation visas korrekt i Walmart Marketplace-kontot måste du uppdatera beställningen manuellt i [!DNL Walmart Marketplace] butik.


