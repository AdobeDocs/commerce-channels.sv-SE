---
title: Retur- och återbetalningsorder
description: "Instruktioner för att helt eller delvis återbetala returansökningar som erhållits från [!DNL Walmart Marketplace] från [!DNL Channel Manager] för Adobe Commerce och Magento Open Source."
source-git-commit: e9d2f53a955956a2b5086649d9ac18cc982ef4e3
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# Retur- och återbetalningsorder

När en köpare begär en retur av orderartiklar som köpts via [!DNL Walmart Marketplace], Walmart skapar en returbegäran. [!DNL Channel Manager] övervakar Marketplace-kanalen för dessa begäranden och synkroniserar automatiskt returbegärandeinformationen till Channel Manager.

På Commerce-sidan startar returbegäran följande arbetsflöde:

1. Channel Manager skapar en motsvarande returbegäran med mottagen status och lägger till det returnerade ID-numret ([!UICONTROL RMA #]) till [!UICONTROL Returns] kontrollpanel. På [!DNL Orders] kontrollpanelen, statusinformation för den order som är associerad med returuppdateringarna som innehåller en [!UICONTROL Return requested] för att visa och bearbeta returen.

1. Handläggarna bearbetar den återbetalning som är kopplad till returen genom att skapa en kreditnota efter [Adobe Commerce arbetsflöde för återbetalning](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow). Alla återbetalningar behandlas med offlinemetoden.

1. [!DNL Channel Manager] skickar en återbetalningsuppdatering till Walmart Marketplace så att returstatusen kan uppdateras för att återspegla den slutförda återbetalningen från Adobe Commerce.

I Store Admin kan du visa och bearbeta returer från Channel Manager genom att öppna butiken för säljkanaler och välja **[!UICONTROL Returns]**.

![Kanalhanteraren returnerar kontrollpanelen för att bearbeta återbetalningar för returbegäranden som tagits emot från [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png)

>[!NOTE]
>
>Du kan bara bearbeta återbetalningar för levererade order. I [!DNL Channel Manager]måste orderstatusen vara [!UICONTROL Shipped]. I [!DNL Walmart Marketplace] Säljarkonto, ordern måste vara [!UICONTROL Delivered].

## Returnerar kontroller och kolumnbeskrivningar

I följande tabeller beskrivs de kontroller och kolumner som är tillgängliga för [!DNL Channel Manager] returneras.

**Kontroller för[!UICONTROL Returns]**

<table>
<tr>
<td><strong>Kontroll</strong></td>
<td><strong>Beskrivning</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>Filtrera vyn genom att välja ett av [!UICONTROL Return Status] kort.</td>
</tr>
<tr>
<td>Statusinformation</td>
<td>För returposter med [!UICONTROL Received] eller [!UICONTROL Refunded] status kan du skapa eller visa kreditnotan för återbetalningen genom att markera den länkade texten i kolumnen Statusdetaljer.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Om du vill visa orderdetaljer väljer du [!DNL Commerce] ordernummer i [!UICONTROL Order] för att öppna handelsordern.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Om du vill ändra kanalkonfigurationen väljer du autentiseringsuppgifter för kanal Walmart-anslutning, mappade attribut eller leveransidentifierare. Inställningarna väljer [!DNL Commerce] ordernummer i [!UICONTROL Order] tabell. Använd sedan [!DNL Commerce] orderalternativ för att bearbeta ordern.</td>
</tr>
</table>

**Kolumnbeskrivningar**

<table>
<tr>
<td><strong>Fält</strong></td>
<td><strong>Beskrivning</strong></td>
</tr>
<tr>
<td>[!UICONTROL RMA #]</td>
<td>Returnumret för Merchandise-auktorisering som är associerat med returbegäran som tagits emot från [!DNL Walmart Marketplace]. Det här numret genereras av Walmart Marketplace [!UICONTROL Returns] när returprocessen initieras.</td>
</tr>
<tr>
<td>[!DNL Commerce] Ordernr</td>
<td>The [!DNL Commerce] ordernummer som är associerat med artiklarna som ingår i returbegäran från Walmart Marketplace. Visa orderinformation genom att välja ordernummer.</td>
</tr>
<tr>
<td>Begärd</td>
<td>Datumet då returen begärdes den [!DNL Walmart Marketplace]
konverteras till lokal tid.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>Datumet då returen måste återbetalas av för att uppfylla [!DNL Walmart Marketplace] [requirements](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) konverterad till lokal tid.</td>
</tr>
<tr>
<td>[!UICONTROL Items]</td>
<td>Visar SKU och kvantitet för varje artikel i returen.</td>
</tr>
<tr>
<td>[!UICONTROL Refund amount]</td>
<td>Det totala värdet som ska återbetalas för de returnerade artiklarna.</td>
</tr>
<tr>
<td>[!UICONTROL Status]</td>
<td>Anger aktuell returstatus i [!DNL Commerce] returarbetsflöde-<i>Mottaget</i>, <i>Avrundad</i>, eller <i>Fel</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>För mottagna och återbetalningsbara returtransaktioner ger statusinformation en länk för att komma åt kreditnotan för bearbetning av återbetalning. Om ett fel inträffar under [!DNL Channel Manager] synkroniseringsprocess mellan Adobe Commerce och [!DNL Walmart marketplace], innehåller det här fältet felbeskrivningen.</td>
</tr>
</table>

## Returstatus

[!UICONTROL Return Status] innehåller information om det aktuella läget för [!DNL Walmart Marketplace] returbegäranden som hanteras från Adobe Commerce eller Magento Open Source.

Returnera statusuppdateringar när [!DNL Channel Manager] tar emot en returbegäran från [!DNL Walmart Marketplace] eller när [!DNL Commerce] kreditnota skapas för att bearbeta återbetalningen för de returnerade artiklarna.

Returer kan ha följande statusar:

* **[!UICONTROL Received]**-Detta är den inledande statusen för returbegäran som tagits emot från [!DNL Walmart Marketplace] butik. Handlaren kan bearbeta återbetalningen för returen genom att välja **[!UICONTROL Create credit memo]** i [!UICONTROL Status details].

* **[!UICONTROL Refunded]**- Anger att en kreditnota har skapats för att utfärda en återbetalning för de returnerade artiklarna. Handlare kan visa återbetalningsinformation genom att välja **[!UICONTROL View credit memo]** i [!UICONTROL Status details].

* **[!UICONTROL Error]**—Returnera begäranden som innehåller fel. Fel kan uppstå när returbegäran från Walmart saknar eller har felaktiga data. Eller om [!DNL Channel Manager] kan inte skicka meddelandet om återbetalningsuppdatering till Walmart.

## Returscenarier

I följande scenarier beskrivs hur du utfärdar återbetalningar för olika typer av returbegäranden från [!DNL Channel Manager].

* **Fullständig radbrytning**- Om returbegäran från Walmart Marketplace gäller alla artiklar i ordern ska du uppdatera kreditfakturakvantiteten så att alla artiklar återbetalas.

* **Delvis retur**-Om returbegäran från Walmart Marketplace bara gäller vissa orderartiklar, ska du bara uppdatera kreditfakturakvantiteten för de artiklar som ska återbetalas.

* **Återbetalning har redan återbetalats genom Walmart Marketplace**-I vissa fall behandlas en återbetalning på [!DNL Walmart Marketplace] innan du bearbetar returen i Channel Manager. Om en handelsorder t.ex. inte återbetalas inom den 48-timmars bearbetningsperiod för återbetalning som krävs av Walmart, återbetalar Walmart ordern automatiskt. När detta inträffar synkroniserar Channel Manager fortfarande returbegäran till Adobe Commerce så att du kan bearbeta returen och utfärda kreditnotan. Det här arbetsflödet ser till att orderdetaljerna i [!DNL Commerce] matchar orderinformationen i Walmart Marketplace.

>[!NOTE]
>
> Det kan ta upp till fem minuter innan återbetalningsuppdateringar synkroniseras till [!DNL Walmart Marketplace]. Du kan kontrollera den aktuella returstatusen på [!DNL Channel Manager] [!UICONTROL Returns] kontrollpanel.

## Bearbeta en återbetalningsbegäran

1. Öppna [!UICONTROL Returns] kontrollpanel för er säljkanalsbutik.

   * Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Öppna butiksvyn genom att välja ögonikonen för en säljkanalsbutik.

   * Du kan granska returerna genom att välja **[!UICONTROL Returns]** -fliken.

      Du kan även komma åt returinformation från [!UICONTROL Orders] sida. Sök efter [!UICONTROL Shipped] order som har en returbegäran. Välj sedan `Return requested` i [!UICONTROL Status Details] -kolumn för att visa och bearbeta begäran.

1. Hitta en retur med *[!UICONTROL Received]* status.

1. Granska listan över orderartiklar och kvantitet som ska återbetalas i kolumnen Artiklar.

1. Bearbeta återbetalningen genom att utfärda en kreditnota.

   * Från [!UICONTROL Status Details] kolumn, markera **[!UICONTROL Create credit memo]** för att öppna sidan Orderinformation i [!DNL Commerce].

      Om ordern inte har fakturerats visas ett felmeddelande på sidan Orderinformation som uppmanar dig att skapa en. Välj **[!UICONTROL Create invoice]**. Sedan [skapa och spara fakturan](https://docs.magento.com/user-guide/sales/invoices.html).

   * På sidan Orderinformation väljer du **[!UICONTROL Credit Memo]**.

   * I [!UICONTROL Items to Refund] i [!UICONTROL Credit Memo], uppdatera **[!UICONTROL Qty to refund]** och **[!UICONTROL Return to Stock]** Information om de artiklar som ingår i returbegäran.

      Se till att bara returnera de objekt som anges i returbegäran.

   * Om du vill lägga till en kommentar anger du texten i **[!UICONTROL Credit Memo Comments]**

   * Välj **[!UICONTROL Refund Offline]**.

När återbetalningen är slutförd [!DNL Channel Manager] uppdaterar returstatus i dialogrutan [!UICONTROL Returns] kontrollpanel till [!UICONTROL Refunded] och synkroniserar uppdateringen till Walmart för att uppdatera returstatusen på Marketplace.


## Visa återbetalningsinformation för en retur

Du kan visa information om returbegäranden och återbetalningsbehandling från [!UICONTROL Returns] kontrollpanel.

1. Öppna kontrollpanelen Returnerar för din säljkanalsbutik.

   * Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]**.

   * Öppna butiksvyn genom att välja ögonikonen för en säljkanalsbutik.

   * Välj **[!UICONTROL Returns]**.

1. Visa återfinansierade order genom att välja **[!UICONTROL Refunded]** statuskort.

1. Visa återbetalningsinformation för en retur genom att välja **[!UICONTROL View credit memo]**.

   ![Kreditnota som återför returnerade artiklar för en [!DNL Walmart Marketplace] order](assets/refund-credit-memo-for-marketplace-order.png)

>[!NOTE]
>
>När en order har återbetalats [!UICONTROL Orders] Kontrollpanelen visar inte returinformation. Om du vill visa returinformation använder du [!DNL Channel Manager] Returnerar instrumentpanelen. Mer detaljerad information om retur och återbetalning finns också på sidan Orderdetaljer.

## Åtgärda returfel

Fel kan uppstå när returinformationen tas emot från [!DNL Walmart Marketplace]eller när [!DNL Channel Manager] synkroniserar statusuppdateringar från [!DNL Commerce] till [!DNL Walmart Marketplace].

Om synkroniseringsåtgärden för en returuppdatering misslyckas, visas [!DNL Channel Manager] Returnerar en instrumentpanel som visar *[!UICONTROL Error]* status för returposten. För att säkerställa att retur- och återbetalningsinformation återspeglas korrekt i Walmart Marketplace-kontot måste du uppdatera beställningen manuellt i [!DNL Walmart Marketplace] butik.


