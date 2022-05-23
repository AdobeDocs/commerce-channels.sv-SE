---
title: Bearbeta order
description: Instruktioner för frakt och annullering [!DNL Walmart Marketplace] beställningar från Adobe Commerce och Magento Open Source.
source-git-commit: 5670639697550b2d7fee67dd29be9c6278d5782b
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Bearbeta order

Om du använder beställningshanteringen Adobe Commerce och Magento Open Source för att hantera dina [!DNL Commerce] butiksförsäljning, bearbeta [!DNL Walmart Marketplace] order från Commerce med ett liknande arbetsflöde.

När du bearbetar en order i Commerce synkroniserar Channel Manager uppdateringar till [!DNL Walmart Marketplace]. Den här uppdateringen ser till att produktlagret och orderstatusen från Commerce matchar de data som spåras i [!DNL Walmart Marketplace] och meddelar Walmart att skicka orderstatus och leveransinformation till kunderna.

>[!NOTE]
>
> Det kan ta upp till fem minuter innan orderuppdateringarna synkroniseras till [!DNL Walmart Marketplace]. Om du vill kontrollera orderstatus går du tillbaka till [!DNL Channel Manager] Beställningar.

## Leverera en order

När du skickar en order från Commerce använder du [[!DNL Commerce Order Management] leveransarbetsflöde](https://docs.magento.com/user-guide/sales/order-ship.html). När du har skickat ordern synkroniseras uppdateringarna med [!DNL Walmart Marketplace]. Sedan meddelar Walmart sina kunder om orderstatus och leveransinformation.

**Förutsättning**

Kontrollera att [inställningar för leverans av kanaler och konfiguration av transportföretag](map-shipping-carriers.md) träffa [!DNL Walmart Marketplace requirements].

### Skapa och skicka leveransen

När du skickar en [!DNL Walmart Marketplace] beställ från [!DNL Commerce]måste du lägga till ett spårningsnummer. Kunder får spårningsnumret i leveransmeddelandet som de får från [!DNL Walmart].

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** för att öppna [!UICONTROL Channel Manager Marketplace Stores] sida.

1. Öppna butiksvyn genom att välja ögonikonen för en säljkanalsbutik.

1. Visa [!DNL Walmart Marketplace] order, välj *[!UICONTROL *Orders]**.

1. Öppna beställningen som ska levereras i tabellen Order (Beställningar) genom att välja **Handelsordernummer**.

1. Skapa och skicka en leverans för hela eller delar av en order genom att välja **[!UICONTROL Ship]**.

   - Om du vill välja en fraktfirma och lägga till ett spårningsnummer väljer du **[!UICONTROL Add tracking number]**.

   - Fyll i resten av leveransformuläret efter behov. Se [[!DNL Shipping an Order]](https://docs.magento.com/user-guide/sales/order-ship.html) för detaljerade anvisningar.

1. Håll koll på [orderstatus](manage-orders.md#about-order-status) in [!DNL Channel Manager] för att verifiera att uppdateringar skickades till [!DNL Walmart Marketplace].

## Avbryt en beställning

När du avbryter en [!DNL Walmart Marketplace] order, Walmart kräver en annulleringsorsak. När orderannulleringen uppdateras till Walmart inkluderas annulleringsorsaken i det annulleringsmeddelande som skickas till kunden.

Orsaken till annulleringen visas också i [!DNL Commerce] beställa betalningsinformation.

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** för att öppna [!UICONTROL Channel Manager Marketplace Stores] sida.

1. Öppna butiksvyn genom att välja ögonikonen för en butikskanal.

1. Visa [!DNL Walmart Marketplace] order, välj *[!UICONTROL *Orders]**.

1. Öppna sidan med orderinformation i tabellen Order (Beställningar) genom att välja **Handelsordernummer** för ordern att annullera.

   ![Detaljvy för handelsorder för en Walmart Marketplace-order](assets/order-detail-with-external-order-id.png)

1. Avbryt ordern.

   - Välj **Avbryt** på menyn Ordningsinformation.

   - I formuläret Avbryt beställning väljer du **Orsak till annullering**.

      ![Detaljvy för handelsorder för en Walmart Marketplace-order](assets/order-detail-with-external-order-id.png)

   - Välj **Avbryt beställning**.

1. Verifiera att uppdateringar skickades till [!DNL Walmart Marketplace] genom att kontrollera [orderstatus](manage-orders.md#about-order-status) in [!DNL Channel Manager].
