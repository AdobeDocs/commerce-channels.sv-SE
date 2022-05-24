---
title: Bearbeta order
description: Instruktioner för frakt och annullering [!DNL Walmart Marketplace] beställningar från Adobe Commerce och Magento Open Source.
exl-id: 2fdcb348-5c02-464f-a114-16ec657bed6b
source-git-commit: fac4bbd3985e07b919f986c877b8584da797e6fe
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Bearbeta order

Om du använder beställningshanteringen Adobe Commerce och Magento Open Source för att hantera dina [!DNL Commerce] butiksförsäljning kan du bearbeta [!DNL Walmart Marketplace] order från Commerce med samma arbetsflöde.

När du bearbetar en order i Commerce synkroniserar Channel Manager uppdateringar till [!DNL Walmart Marketplace]. Den här uppdateringen ser till att orderstatus och leveransinformation från Commerce matchar de data som spåras i [!DNL Walmart Marketplace].

* **Beställa försändelser**-Walmart kräver ett spårningsnummer för alla leveranser. Du kan skapa partiella leveranser om du inte har lager för alla artiklar i ordern. När du har skickat leveransen synkroniseras orderuppdateringarna med [!DNL Walmart Marketplace]. Sedan meddelar Walmart sina kunder om orderstatus och leveransinformation.

* **Orderannulleringar**-När du avbryter en [!DNL Walmart Marketplace] order kräver Walmart en orsak till annullering som ingår i det beställningsmeddelande som skickas till kunden. Orsaken till annulleringen visas också i [!DNL Commerce] beställa betalningsinformation.

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

   * Välj en fraktfirma och lägg till ett spårningsnummer genom att välja **[!UICONTROL Add tracking number]**.

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


1. När du har skickat annulleringen spårar du [orderstatus](manage-orders.md#about-order-status) in [!DNL Channel Manager] för att verifiera att uppdateringar skickades till [!DNL Walmart Marketplace].
