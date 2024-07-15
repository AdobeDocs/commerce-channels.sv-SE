---
title: Visa och hantera beställningar från  [!DNL Channel Manager]
description: 'Visa och hantera [!DNL Walmart Marketplace] beställningar med [!DNL Channel Manager] för Adobe Commerce och Magento Open Source.'
feature: Sales Channels, Orders
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Visa och spåra beställningar från [!DNL Channel Manager]

[!DNL Walmart Marketplace] orderdata för [!DNL Commerce] produkter synkroniseras automatiskt till [!DNL Channel Manager] efter att [!DNL Walmart] har bearbetat ordern.

På [!DNL Commerce]-sidan utlöser en lyckad synkronisering följande åtgärder:

- [!DNL Channel Manager] skickar en orderbekräftelse till Walmart.

- En motsvarande [!DNL Commerce]-ordning skapas från Walmart-ordningen.

- Den uppdaterade orderinformationen visas på kontrollpanelen för [!DNL Channel Manager] order.

I butiksadministratören kan du visa orderdata från [!DNL Channel Manager] genom att öppna butiken för säljkanaler och välja **[!UICONTROL Orders]**.

![Vyn Kanalhanterarorder som hanterar [!DNL Walmart Marketplace] order](assets/orders-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Det kan ta upp till 35 minuter för en [!DNL Walmart Marketplace]-order att visas i listan [!DNL Channel Manager]-order. [!DNL Walmart] tar ca 30 minuter att bearbeta inkommande order och skicka dem till [!DNL Channel Manager]. När Channel Manager har tagit emot beställningen tar det ytterligare fem minuter att skapa och visa beställningen i Adobe Commerce eller Magento Open Source.

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
<td>Sortera vyn genom att välja ett av [!UICONTROL Order Status]-korten.</td>
</tr>
<tr>
<td>Statusinformation</td>
<td>Innehåller information om orderfel och returbegäranden. Om du vill visa returinformation och återbetalningsstatus för en order markerar du texten <strong>[!UICONTROL Return requested]</strong> så att kontrollpanelen [!UICONTROL Returns] öppnas.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Om du vill visa orderdetaljer markerar du [!DNL Commerce]-ordernumret i tabellen [!UICONTROL Order]. Använd sedan [!DNL Commerce] ordningsalternativ för att bearbeta ordern.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Om du vill ändra kanalkonfigurationen väljer du kanal-Walmart-anslutningsreferenser, mappade attribut eller leveransidentifierare. Inställningarna markerar [!DNL Commerce]-ordningsnumret i tabellen [!UICONTROL Order]. Använd sedan [!DNL Commerce] ordningsalternativ för att bearbeta ordern.</td>
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
<td>Inköpsordernumret som tilldelats ordern i [!DNL Walmart Marketplace]. När en order först importeras till [!DNL Channel Manager] visas bara ordernumret för [!DNL Walmart]. När ordningen [!DNL Commerce] skapas lagras ordernumret [!DNL Walmart] i produktattributet [!UICONTROL External ID].</td>
</tr>
<tr>
<td>[!DNL Commerce] Ordernr</td>
<td>Numret som tilldelats den [!DNL Commerce]-ordning som skapats från ordningen [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>Objekt</td>
<td>Antal beställda objekt på [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Order Value]</td>
<td>Total kostnad för beställda artiklar.</td>
</tr>
<tr>
<td>[!UICONTROL Ordered]</td>
<td>Det datum då ordern skickades till [!DNL Walmart Marketplace] konverterades till den lokala tidszonen.</td>
</tr>
<tr>
<td>[!UICONTROL Ship By (timezone)]</td>
<td>Det datum som ordern måste levereras av för att uppfylla [!DNL Walmart Marketplace] krav som konverterats till den lokala tidszonen.
</td>
</tr>
<tr>
<td>[!UICONTROL Deliver By (timezone)]</td>
<td>Det datum som ordern måste levereras till kunden för att uppfylla [!DNL Walmart Marketplace]-krav som konverterats till den lokala tidszonen.</td>
</tr>
<tr>
<td>[!UICONTROL Ship Method]</td>
<td>Leveransmetoden [[!DNL Walmart Marketplace]](https://sellerhelp.walmart.com/s/guide?language=en_US&amp;article=000007893%29 har valts för ordern.</td>
</tr>
<tr>
<td>[!UICONTROL Last Update]</td>
<td>Tidsstämpel som anger den senaste gången orderdata uppdaterades i [!DNL Channel Manager] konverterades till lokal tidszon.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Anger den aktuella orderstatusen i orderarbetsflödet [!DNL Commerce]. Den initiala statusen för en order som importerats från [!DNL Walmart Marketplace] är _Open_. Ytterligare statusuppdateringar inträffar när [!DNL Commerce] order bearbetas och [!DNL Channel Manager] synkroniserar leveranser, partiell leverans och annulleringsuppdateringar för [!DNL Walmart Marketplace].</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>Ger mer detaljerad information om beställningar med fel eller återbetalningsbegäranden.</td>
</tr>
</table>

## Orderstatus

[!UICONTROL Order Status] innehåller information om det aktuella tillståndet för [!DNL Walmart Marketplace] order som hanteras från Adobe Commerce eller Magento Open Source. Orderstatusuppdateringar inträffar när [!DNL Channel Manager] tar emot uppdaterad orderinformation från antingen [!DNL Walmart Marketplace] eller [!DNL Commerce] ordersystemet. Order kan ha följande status:

- **[!UICONTROL Shipped]** - Beställningar som har skickats från butiken [!DNL Commerce]. När ordern levereras skickar [!DNL Channel Manager] en uppdatering till [!DNL Walmart Marketplace] för att uppdatera leveransstatusen på Walmart och ange orderspårningsnumret för leveransen. När en order har skickats kan orderartiklarna delvis eller helt återbetalas om Walmart utfärdar ett returformulär för godkännande av försäljning. Se [Återbetalningar och återbetalningar](return-refund-orders.md).

- **[!UICONTROL Partially Shipped]** - Beställningar med artiklar markerade som levererade och andra som väntar på att skickas. När artiklar i orderleveransen skickas en uppdatering till [!DNL Walmart Marketplace] från [!DNL Channel Manager] för att uppdatera leveransstatusen till _[!DNL Partially Shipped]_på Walmart och ange orderspårningsnumret för leveransen.

- **[!UICONTROL Canceled]** - Beställningar som har annullerats från [!DNL Commerce]-butiken.

  När orderannulleringen har slutförts uppdateras lagerkvantiteten [!DNL Commerce] så att returnerade artiklar visas. Sedan synkroniserar [!DNL Channel Manager] uppdateringen till [!DNL Walmart Marketplace].

- **[!UICONTROL Return requested]** - Om Walmart Marketplace begär en retur för orderartiklar som har skickats visas en `Return requested`-länk i kolumnen [!UICONTROL Status details]. Om du väljer länken öppnas kontrollpanelen [!UICONTROL Returns] för att visa returen och hantera återbetalningsprocessen.

- **[!UICONTROL Error]** - Beställningar med fel. Fel kan uppstå när en orderuppdateringsåtgärd misslyckas. Det kan till exempel uppstå fel om [!DNL Channel Manager] inte kan ta emot en ny order från Walmart. De kan också inträffa om [!DNL Channel Manager] inte kan skicka en orderleverans eller en annulleringsuppdatering till [!DNL Walmart Marketplace]. Om en åtgärd misslyckas visas beställningens _Error_-status på sidan Beställningar. Mer information finns i [Åtgärda orderfel](process-orders.md#fix-shipping-and-cancelation-errors).

- **[!UICONTROL Status details]**-Tillhandahåller mer information om orderfel som inträffar på grund av t.ex. saknad information eller ogiltiga värden, felaktig leveransinformation eller en misslyckad orderannullering. Beskrivningen hjälper till att avgöra om fel uppstod i instansen [!DNL Commerce] eller i [!DNL Walmart Marketplace].

>[!NOTE]
>
>Om orderartiklar skickas i flera leveranser, återspeglar orderstatusen i [!DNL Channel Manager] den senaste tillgängliga orderstatusen. Om till exempel det första objektet skickas och inga fel returneras när orderuppdateringarna synkroniseras med [!DNL Channel Manager] och [!DNL Walmart Marketplace], är [!DNL Channel Manager] orderstatusen _[!UICONTROL Partially Shipped]_. Om en andra artikel skickas och [!DNL Channel Manager] returnerar ett fel uppdateras orderstatusen till_[!UICONTROL Error]_.

## Granska beställningar

1. Öppna sidan [!UICONTROL Channel Manager Marketplace Stores] genom att välja **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** i Admin.

1. Öppna butiksvyn genom att markera ögonikonen i en butikspostrad.

1. Om du vill visa orderinformation väljer du *[!UICONTROL *Orders]**.

1. Hämta information om ordningen och identifiera nästa steg genom att kontrollera kolumnen **[Status](#order-status)**.

## Granska orderdetaljer

När en beställning har tagits emot från marknadsplatsen och importerats till din säljkanalsbutik använder du beställnings-ID:t [!DNL Commerce] för att visa orderinformationen i Adobe Commerce.

I **[!UICONTROL Orders]** väljer du **[!UICONTROL Commerce Order Number]** för att öppna [!DNL Commerce]-ordningsinformationen.

![Commerce orderdetaljvy för en [!DNL Walmart Marketplace] order ](assets/order-detail-with-external-order-id.png){width="600" zoomable="yes"}

I Commerce Store har beställningar som importerats från [!DNL Walmart Marketplace] följande ytterligare information i orderdata:

- **Betalningsinformation och leveransmetod**-Beställningar som importeras från Walmart innehåller följande värden för betalnings- och leveransfält:

   - **[!UICONTROL Offline Channel Payment]** - Anger att orderbetalningen behandlas offline av [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]** - Visar [!DNL Walmart Marketplace]-ordernumret.

   - **[!UICONTROL Channel Shipping - Value]**-Anger att leveransavgifter hanteras via [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]** - Det här fältet visas bara om en ordning som importerats från [!DNL Walmart Marketplace] har avbrutits. Orsaker till annullering är:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

- **Artiklar som beställts** - I det här avsnittet listas orderobjekten på alla Commerce-beställningar. Kolumnen [!UICONTROL Qty] innehåller statushistorik för orderobjekt. Om en order till exempel har fakturerats, skickats och återbetalats kan du se statusövergångarna.

  ![Statushistorik för sorterad artikel i orderdetaljer [!DNL Walmart Marketplace] order](assets/order-detail-status-history.png){width="600" zoomable="yes"}

Visa information om artikelfaktura och återbetalning genom att välja alternativen [!UICONTROL Invoice] och [!UICONTROL Credit Memo] på navigeringsmenyn. Du kan även komma åt kreditnotan direkt från kontrollpanelen [[!UICONTROL Returns]](return-refund-orders.md) i din säljkanalsbutik.
