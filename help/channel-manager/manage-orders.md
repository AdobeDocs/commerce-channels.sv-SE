---
title: Visa och hantera order från [!DNL Channel Manager]'
description: Visa och hantera [!DNL Walmart Marketplace] beställningar med [!DNL Channel Manager] för Adobe Commerce och Magento Open Source."
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Visa och spåra beställningar från [!DNL Channel Manager]

[!DNL Walmart Marketplace] beställa data för [!DNL Commerce] produkter synkroniseras automatiskt till [!DNL Channel Manager] efter [!DNL Walmart] bearbetar ordern.

På [!DNL Commerce] en lyckad synkronisering utlöser följande åtgärder:

- [!DNL Channel Manager] skickar en orderbekräftelse till Walmart.

- En motsvarande [!DNL Commerce] ordern skapas från Walmart-ordningen.

- Den uppdaterade orderinformationen visas på [!DNL Channel Manager] Kontrollpanel för beställningar.

I storefront Admin kan du visa orderdata från [!DNL Channel Manager] genom att öppna säljkanalsbutiken och välja **[!UICONTROL Orders]**.

![Vyn Kanalhanterarorder som ska hanteras [!DNL Walmart Marketplace] order](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Det kan ta upp till 35 minuter i en [!DNL Walmart Marketplace] ordningen som visas i [!DNL Channel Manager] orderlista. [!DNL Walmart] tar ca 30 minuter att bearbeta inkommande order och skicka dem till [!DNL Channel Manager]. När Channel Manager har tagit emot beställningen tar det ytterligare fem minuter att skapa och visa beställningen i Adobe Commerce eller Magento Open Source.

## Beställningskontroller och kolumnbeskrivningar

I följande tabeller beskrivs de kontroller och kolumner som är tillgängliga för beställningar.

**Kontroller för[!UICONTROL Orders]**

<table>
<tr>
<td><strong>Kontroll</strong></td>
<td><strong>Beskrivning</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter orders]</td>
<td>Sortera vyn genom att välja ett av alternativen [!UICONTROL Order Status] kort.</td>
</tr>
<tr>
<td>Statusinformation</td>
<td>Innehåller information om orderfel och returbegäranden. Om du vill visa returinformation och återbetalningsstatus för en order väljer du <strong>[!UICONTROL Return requested]</strong> text för att öppna [!UICONTROL Returns] kontrollpanel.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Om du vill visa orderdetaljer väljer du [!DNL Commerce] ordernummer i [!UICONTROL Order] tabell. Använd sedan [!DNL Commerce] orderalternativ för att bearbeta ordern.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Om du vill ändra kanalkonfigurationen väljer du autentiseringsuppgifter för kanal Walmart-anslutning, mappade attribut eller leveransidentifierare. Inställningarna väljer [!DNL Commerce] ordernummer i [!UICONTROL Order] tabell. Använd sedan [!DNL Commerce] orderalternativ för att bearbeta ordern.</td>
</tr>
</table>


**Kolumnbeskrivningar**

<table>
<tr>
<td>Fält</td>
<td>Beskrivning</td>
</tr>
<tr>
<td>[!UICONTROL Walmart Order #]</td>
<td>Inköpsordernummer som tilldelats ordern i [!DNL Walmart Marketplace]. När en order importeras till [!DNL Channel Manager], bara [!DNL Walmart] ordernummer visas. När [!DNL Commerce] order skapas, [!DNL Walmart] ordernumret lagras i [!UICONTROL External ID] produktattribut.</td>
</tr>
<tr>
<td>[!DNL Commerce] Ordernr</td>
<td>Numret som tilldelats [!DNL Commerce] order som skapats från [!DNL Walmart Marketplace] beställa.</td>
</tr>
<tr>
<td>Objekt</td>
<td>Antal beställda artiklar [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>Total kostnad för beställda artiklar.</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>Datumet då ordern skickades till [!DNL Walmart Marketplace] konverteras till den lokala tidszonen.</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>Datumet då ordern måste levereras av för att uppfylla [!DNL Walmart Marketplace] krav som har konverterats till den lokala tidszonen.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>Datumet då ordern måste levereras till kunden för att uppfylla [!DNL Walmart Marketplace] krav som har konverterats till den lokala tidszonen.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>[[!DNL Walmart Marketplace] Leveranssätt](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 har valts för ordern.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Tidsstämpel som anger senaste gången orderdata uppdaterades i [!DNL Channel Manager] konverteras till lokal tidszon.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Anger aktuell orderstatus i [!DNL Commerce] orderarbetsflöde. Ursprunglig status för en order som importerats från [!DNL Walmart Marketplace] är _Open_. Ytterligare statusuppdateringar sker när [!DNL Commerce] beställningar behandlas och [!DNL Channel Manager] har synkroniserat försändelse, partiell leverans och annulleringsuppdateringar för [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Ger mer detaljerad information om beställningar med fel eller återbetalningsbegäranden.</td>
</tr>
</table>

## Orderstatus

[!UICONTROL Order Status] innehåller information om det aktuella läget för [!DNL Walmart Marketplace] beställningar som hanteras från Adobe Commerce eller Magento Open Source. Uppdateringar av orderstatus när [!DNL Channel Manager] får uppdaterad orderinformation från antingen [!DNL Walmart Marketplace] eller [!DNL Commerce] ordersystem. Order kan ha följande status:

- **[!UICONTROL Shipped]**—Beställningar som har skickats från [!DNL Commerce] butik. När ordern levereras, [!DNL Channel Manager] skickar en uppdatering till [!DNL Walmart Marketplace] för att uppdatera leveransstatus på Walmart och ange orderspårningsnumret för leveransen. När en order har skickats kan orderartiklarna delvis eller helt återbetalas om Walmart utfärdar ett returformulär för godkännande av försäljning. Se [Returer och återbetalningar](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]**—Beställningar med artiklar markerade som levererade och andra som väntar på att skickas. När artiklar i orderleveransen [!DNL Channel Manager] skickar en uppdatering till [!DNL Walmart Marketplace] för att uppdatera leveransstatus till _[!DNL Partially Shipped]_på Walmart och ange orderspårningsnumret för leveransen.

- **[!UICONTROL Canceled]**—Beställningar som har annullerats från [!DNL Commerce] butik.

  När ordern har annullerats [!DNL Commerce] Uppdateringar av lagerkvantitet för att spegla returnerade artiklar. Sedan [!DNL Channel Manager] synkroniserar uppdateringen till [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]**—Om Walmart Marketplace begär en retur för orderartiklar som har skickats, en `Return requested` länken visas i [!UICONTROL Status details] kolumn. När du väljer länken öppnas [!UICONTROL Returns] kontrollpanelen för att visa returen och hantera återbetalningsprocessen.

- **[!UICONTROL Error]**—Beställningar med fel. Fel kan uppstå när en orderuppdateringsåtgärd misslyckas. Exempel: fel uppstår om [!DNL Channel Manager] kan inte ta emot en ny beställning från Walmart. De kan också inträffa om [!DNL Channel Manager] kan inte skicka en orderleverans eller en annulleringsuppdatering till [!DNL Walmart Marketplace]. Om en åtgärd misslyckas visas en _Fel_ status för ordern. Mer information finns i [Åtgärda orderfel](process-orders.md#fix-shipping-and-cancelation-errors).

- **[!UICONTROL Status details]**-Ger mer information om orderfel som inträffar på grund av t.ex. saknad information eller ogiltiga värden, felaktig leveransinformation eller misslyckad orderannullering. Beskrivningen hjälper till att avgöra om fel uppstod i [!DNL Commerce] eller på [!DNL Walmart Marketplace].

>[!NOTE]
>
>Om orderartiklar skickas i flera leveranser visas orderstatusen i [!DNL Channel Manager] återspeglar den senaste tillgängliga orderstatusen. Om till exempel det första objektet skickas och inga fel returneras när orderuppdateringarna synkroniseras med [!DNL Channel Manager] och [!DNL Walmart Marketplace], [!DNL Channel Manager] orderstatus är _[!UICONTROL Partially Shipped]_. Om en andra artikel skickas och [!DNL Channel Manager] returnerar ett fel, orderstatusen uppdateras till_[!UICONTROL Error]_.

## Granska beställningar

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** för att öppna [!UICONTROL Channel Manager Marketplace Stores] sida.

1. Öppna butiksvyn genom att markera ögonikonen i en butikspostrad.

1. Om du vill visa orderinformation väljer du *[!UICONTROL *Orders]**.

1. Hämta information om beställningen och avgöra vilka steg som ska utföras genom att kontrollera **[Status](#order-status)** kolumn.

## Granska orderdetaljer

När en beställning har tagits emot från marknadsplatsen och importerats till din säljkanalsbutik använder du [!DNL Commerce] Beställnings-ID för att visa orderinformationen i Adobe Commerce.

Från **[!UICONTROL Orders]** väljer du **[!UICONTROL Commerce Order Number]** för att öppna [!DNL Commerce] orderdetaljer.

![Detaljvy för handelsorder för en [!DNL Walmart Marketplace] beställa](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

I Commerce Store importerar man order från [!DNL Walmart Marketplace] ha följande ytterligare information i orderuppgifterna:

- **Betalningsinformation och leveranssätt**-Beställningar som importeras från Walmart innehåller följande värden för betalnings- och leveransfält:

   - **[!UICONTROL Offline Channel Payment]**—Anger att orderbetalningen behandlas offline av [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**—Visar [!DNL Walmart Marketplace] ordernummer.

   - **[!UICONTROL Channel Shipping - Value]**-Anger att fraktkostnader hanteras genom [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**-Det här fältet visas bara om en ordning har importerats från [!DNL Walmart Marketplace] avbryts. Orsaker till annullering är:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **Beställda artiklar**- I det här avsnittet visas orderartiklarna på alla handelsorder. The [!UICONTROL Qty] -kolumnen innehåller statushistorik för orderartiklar. Om en order till exempel har fakturerats, skickats och återbetalats kan du se statusövergångarna.

  ![Statushistorik för sorterad artikel för orderdetaljer [!DNL Walmart Marketplace] order](assets/order-detail-status-history.png){width="600" zoomable="yes"}

Visa artikelfaktura och återbetalningsinformation genom att välja [!UICONTROL Invoice] och [!UICONTROL Credit Memo] på navigeringsmenyn. Du kan även komma åt kreditnotan direkt från [[!UICONTROL Returns]](return-refund-orders.md) kontrollpanelen i din säljkanalsbutik.
