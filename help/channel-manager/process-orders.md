---
title: Bearbeta order
description: Instruktioner för frakt och annullering [!DNL Walmart Marketplace] beställningar från Adobe Commerce och Magento Open Source.
source-git-commit: 90ccbecd6d1433ae1312d79f7ae2d34c8f381b97
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 0%

---


# Bearbeta order

Om du använder beställningshanteringen Adobe Commerce och Magento Open Source för att hantera dina [!DNL Commerce] butiksförsäljning, process [!DNL Walmart Marketplace] order från Commerce med ett liknande arbetsflöde.

När du bearbetar en order i Commerce synkroniserar Channel Manager uppdateringar till [!DNL Walmart Marketplace]. Den här uppdateringen ser till att orderstatus och leveransinformation från Commerce matchar de data som spåras i [!DNL Walmart Marketplace].

* **Beställa försändelser**-Walmart kräver ett spårningsnummer för alla leveranser. Om lagerkvantiteten inte räcker till för att fylla en hel order skapar du en partiell leverans. När du har skickat leveransen synkroniseras orderuppdateringarna med [!DNL Walmart Marketplace]. Sedan meddelar Walmart sina kunder om orderstatus och leveransinformation.

* **Orderannulleringar**-När du avbryter en [!DNL Walmart Marketplace] order, Walmart kräver en annulleringsorsak. Orsaken till annulleringen ingår i det beställningsannulleringsmeddelande som skickas till kunden. Orsaken till annulleringen visas också i [!DNL Commerce] beställa betalningsinformation.

>[!NOTE]
>
> Det kan ta upp till fem minuter innan orderuppdateringarna synkroniseras till [!DNL Walmart Marketplace]. Om du vill kontrollera orderstatus går du tillbaka till [!DNL Channel Manager] Sidan Beställningar.

## Leverera en order

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Öppna butiksvyn genom att välja ögonikonen för en säljkanalsbutik.

1. Visa [!DNL Walmart Marketplace] order, välj *[!UICONTROL *Orders]**.

1. Öppna beställningen som ska levereras i tabellen Order (Beställningar) genom att välja **Handelsordernummer**.

1. Skapa och skicka en leverans för hela eller delar av en order genom att välja **[!UICONTROL Ship]**.

   ![Detaljvy för handelsorder för en Walmart Marketplace-order](assets/order-detail-with-external-order-id.png)

   * Om du vill välja en fraktfirma och lägga till ett spårningsnummer väljer du **[!UICONTROL Add tracking number]**.

   * Fyll i resten av leveransformuläret efter behov. Se [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) för detaljerade anvisningar.

1. Håll koll på [orderstatus](manage-orders.md#about-order-status) in [!DNL Channel Manager] för att verifiera att uppdateringar skickades till [!DNL Walmart Marketplace].

## Avbryt en beställning

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

1. Öppna butiksvyn genom att välja ögonikonen för en butikskanal.

1. Visa [!DNL Walmart Marketplace] order, välj *[!UICONTROL *Orders]**.

1. Öppna sidan med orderinformation i tabellen Order (Beställningar) genom att välja **Handelsordernummer** för ordern att annullera.

![Detaljvy för handelsorder för en Walmart Marketplace-order](assets/order-detail-with-external-order-id.png)

1. Avbryt ordern.

   * Välj **Avbryt** på menyn Ordningsinformation.

   * På [!UICONTROL Cancel Order] formulär väljer du **Orsak till annullering**.

   ![Detaljvy för handelsorder för en Walmart Marketplace-order](assets/cancel-order-reason-selector.png)

   * Välj **Avbryt beställning**.


1. Verifiera att uppdateringar skickades till [!DNL Walmart Marketplace] genom att kontrollera [orderstatus](manage-orders.md#about-order-status) in [!DNL Channel Manager].
