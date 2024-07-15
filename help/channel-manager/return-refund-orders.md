---
title: Retur- och återbetalningsorder
description: Instruktioner för att utfärda fullständiga eller partiella återbetalningar för returbegäranden som tagits emot från [!DNL Walmart Marketplace] från [!DNL Channel Manager] för Adobe Commerce och Magento Open Source.
feature: Sales Channels, Orders, Shipping/Delivery, Customer Service
exl-id: 45617011-4add-444c-819b-6bb4164d03e4
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# Retur- och återbetalningsorder

När en köpare begär en retur för orderartiklar som köpts via [!DNL Walmart Marketplace] skapar Walmart en returbegäran. [!DNL Channel Manager] övervakar marknadsplatskanalen för dessa begäranden och synkroniserar automatiskt returbegärandeinformationen till kanalhanteraren.

På Commerce-sidan startar returbegäran följande arbetsflöde:

1. Kanalhanteraren skapar en motsvarande returbegäran med mottagen status och lägger till det returnerade ID-numret ([!UICONTROL RMA #]) på kontrollpanelen [!UICONTROL Returns]. På kontrollpanelen [!DNL Orders] innehåller statusinformationen för den order som är associerad med returuppdateringarna en [!UICONTROL Return requested]-länk för att visa och bearbeta returen.

1. Handlare bearbetar den återbetalning som är associerad med returen genom att skapa en kreditnota efter [Adobe Commerce-återbetalningsarbetsflödet](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html). Alla återbetalningar behandlas med offlinemetoden.

1. [!DNL Channel Manager] skickar en återbetalningsuppdatering till Walmart Marketplace så att returstatusen kan uppdateras för att återspegla den slutförda återbetalningen från Adobe Commerce.

I butiksadministratören kan du visa och bearbeta returer från kanalhanteraren genom att öppna säljkanalsbutiken och välja **[!UICONTROL Returns]**.

![Kanalhanteraren returnerar instrumentpanelen för att bearbeta återbetalningar för returbegäranden som tagits emot från [!DNL Walmart Marketplace]](assets/returns-dashboard-view.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Du kan bara bearbeta återbetalningar för levererade order. I [!DNL Channel Manager] måste orderstatusen vara [!UICONTROL Shipped]. I säljarkontot för [!DNL Walmart Marketplace] måste ordern vara [!UICONTROL Delivered].

## Returnerar kontroller och kolumnbeskrivningar

Följande tabeller beskriver de kontroller och kolumner som är tillgängliga för [!DNL Channel Manager] returer.

**Kontroller för[!UICONTROL Returns]**

<table>
<tr>
<td><strong>Kontroll</strong></td>
<td><strong>Beskrivning</strong></td>
</tr>
<tr>
<td>[!UICONTROL Filter returns]</td>
<td>Filtrera vyn genom att välja ett av [!UICONTROL Return Status]-korten.</td>
</tr>
<tr>
<td>Statusinformation</td>
<td>För returposter med statusen [!UICONTROL Received] eller [!UICONTROL Refunded] kan du skapa eller visa kreditnotan för återbetalningen genom att markera den länkade texten i kolumnen Statusdetaljer.</td>
</tr>
<tr>
<td>[!UICONTROL View order detail]</td>
<td>Om du vill visa orderdetaljer väljer du ordernumret [!DNL Commerce] i tabellen [!UICONTROL Order] för att öppna Commerce-ordern.</td>
</tr>
<tr>
<td>[!UICONTROL Channel Settings]</td>
<td>Om du vill ändra kanalkonfigurationen väljer du kanal-Walmart-anslutningsreferenser, mappade attribut eller leveransidentifierare. Inställningarna markerar [!DNL Commerce]-ordningsnumret i tabellen [!UICONTROL Order]. Använd sedan [!DNL Commerce] ordningsalternativ för att bearbeta ordern.</td>
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
<td>Ordernumret [!DNL Commerce] som är associerat med objekten som ingår i returbegäran från Walmart Marketplace. Visa orderinformation genom att välja ordernummer.</td>
</tr>
<tr>
<td>Begärd</td>
<td>Datumet då returen begärdes den [!DNL Walmart Marketplace]
konverteras till lokal tid.</td>
</tr>
<tr>
<td>[!UICONTROL Return By]</td>
<td>Datumet då returen måste återbetalas av för att uppfylla [!DNL Walmart Marketplace] [krav](https://sellerhelp.walmart.com/seller/s/guide?language=en_US&amp;article=000007176f) konverteras till lokal tid.</td>
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
<td>Anger den aktuella returstatusen i [!DNL Commerce] returarbetsflöde-<i>Mottaget</i>, <i>Återgivet</i> eller <i>Fel</i>.</td>
</tr>
<tr>
<td>[!UICONTROL Status Details]</td>
<td>För mottagna och återbetalningsbara returtransaktioner ger statusinformation en länk för att komma åt kreditnotan för bearbetning av återbetalningar. Om ett fel inträffar under synkroniseringsprocessen [!DNL Channel Manager] mellan Adobe Commerce och [!DNL Walmart marketplace] visas felbeskrivningen i det här fältet.</td>
</tr>
</table>

## Returstatus

[!UICONTROL Return Status] innehåller information om det aktuella tillståndet för [!DNL Walmart Marketplace] returbegäranden som hanteras från Adobe Commerce eller Magento Open Source.

Returstatusuppdateringar inträffar när [!DNL Channel Manager] tar emot en returbegäran från [!DNL Walmart Marketplace] eller när kreditnotan [!DNL Commerce] skapas för att bearbeta återbetalningen för de returnerade artiklarna.

Returer kan ha följande statusar:

* **[!UICONTROL Received]**-Detta är den inledande statusen för returbegäran som tagits emot från arkivet [!DNL Walmart Marketplace]. Handlaren kan bearbeta återbetalningen för returen genom att välja **[!UICONTROL Create credit memo]** i [!UICONTROL Status details].

* **[!UICONTROL Refunded]** - Anger att en kreditnota har skapats för att utfärda en återbetalning för de returnerade artiklarna. Handlare kan visa återbetalningsinformation genom att välja **[!UICONTROL View credit memo]** i [!UICONTROL Status details].

* **[!UICONTROL Error]** - Returnera begäranden som innehåller fel. Fel kan uppstå när returbegäran från Walmart saknar eller har felaktiga data. Eller om [!DNL Channel Manager] inte kan skicka meddelandet om återbetalningsuppdatering till Walmart.

## Returscenarier

I följande scenarier beskrivs hur du skickar återbetalningar för olika typer av returbegäranden från [!DNL Channel Manager].

* **Fullständig retur** - Om returbegäran från Walmart Marketplace gäller alla artiklar i ordern, ska du uppdatera kreditfakturakvantiteten så att alla artiklar återbetalas.

* **Delvis retur**- Om returbegäran från Walmart Marketplace bara gäller vissa orderartiklar, ska du bara uppdatera kreditfakturakvantiteten för artiklarna som ska återbetalas.

* **Återbetalningen har redan återbetalats via Walmart Marketplace**-I vissa fall behandlas en återbetalning [!DNL Walmart Marketplace] innan du bearbetar returen i Channel Manager. Om en Commerce-order t.ex. inte återbetalas inom den 48-timmarsperiod som Walmart kräver återbetalas ordern automatiskt av Walmart. När detta inträffar synkroniserar Channel Manager fortfarande returbegäran till Adobe Commerce så att du kan bearbeta returen och utfärda kreditnotan. Det här arbetsflödet säkerställer att orderdetaljen i [!DNL Commerce] matchar orderinformationen i Walmart Marketplace.

>[!NOTE]
>
> Det kan ta upp till fem minuter för återbetalningsuppdateringar att synkronisera till [!DNL Walmart Marketplace]. Du kan kontrollera den aktuella returstatusen från kontrollpanelen [!DNL Channel Manager] [!UICONTROL Returns].

## Bearbeta en återbetalningsbegäran

1. Öppna kontrollpanelen [!UICONTROL Returns] för din säljkanalsbutik.

   * Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** i Admin.

   * Öppna butiksvyn genom att välja ögonikonen för en säljkanalsbutik.

   * Du kan granska returerna genom att välja fliken **[!UICONTROL Returns]**.

     Du kan även komma åt returinformation från sidan [!UICONTROL Orders]. Sök efter [!UICONTROL Shipped] order som har en returbegäran. Markera sedan länken `Return requested` i kolumnen [!UICONTROL Status Details] för att visa och bearbeta begäran.

1. Hitta en retur med statusen *[!UICONTROL Received]* i tabellen Returnerar.

1. Granska listan över orderartiklar och kvantitet som ska återbetalas i kolumnen Artiklar.

1. Bearbeta återbetalningen genom att utfärda en kreditnota.

   * I kolumnen [!UICONTROL Status Details] väljer du **[!UICONTROL Create credit memo]** för att öppna sidan Orderdetaljer i [!DNL Commerce].

     Om ordern inte har fakturerats visas ett felmeddelande på sidan Orderinformation som uppmanar dig att skapa en. Välj **[!UICONTROL Create invoice]**. [Skapa och spara sedan fakturan](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html).

   * Välj **[!UICONTROL Credit Memo]** på sidan Orderinformation.

   * I avsnittet [!UICONTROL Items to Refund] i [!UICONTROL Credit Memo] uppdaterar du **[!UICONTROL Qty to refund]**- och **[!UICONTROL Return to Stock]**-informationen för objekten som ingår i returbegäran.

     Se till att bara returnera de objekt som anges i returbegäran.

   * Om du vill lägga till en kommentar anger du texten i **[!UICONTROL Credit Memo Comments]**

   * Välj **[!UICONTROL Refund Offline]**.

När återbetalningen är klar uppdaterar [!DNL Channel Manager] returstatusen i [!UICONTROL Returns]-kontrollpanelen till [!UICONTROL Refunded] och synkroniserar uppdateringen till Walmart för att uppdatera returstatusen på marknadsplatsen.


## Visa återbetalningsinformation för en retur

Du kan visa information om returbegäranden och återbetalningsbearbetning på kontrollpanelen [!UICONTROL Returns].

1. Öppna kontrollpanelen Returnerar för din säljkanalsbutik.

   * Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** i Admin.

   * Öppna butiksvyn genom att välja ögonikonen för en säljkanalsbutik.

   * Välj **[!UICONTROL Returns]**.

1. Visa återfinansierade order genom att välja statuskortet **[!UICONTROL Refunded]**.

1. Visa återbetalningsinformation för en retur genom att välja **[!UICONTROL View credit memo]**.

   ![Kreditnota för återbetalning av returnerade artiklar för en [!DNL Walmart Marketplace] order ](assets/refund-credit-memo-for-marketplace-order.png){width="600" zoomable="yes"}

>[!NOTE]
>
>När en order har återbetalats visas ingen returinformation på kontrollpanelen [!UICONTROL Orders]. Om du vill visa returinformation använder du kontrollpanelen [!DNL Channel Manager]. Mer detaljerad information om retur och återbetalning finns också på sidan Orderdetaljer.

## Åtgärda returfel

Fel kan uppstå när returinformationen tas emot från [!DNL Walmart Marketplace] eller när [!DNL Channel Manager] synkroniserar statusuppdateringar från [!DNL Commerce] till [!DNL Walmart Marketplace].

Om synkroniseringsåtgärden för en returuppdatering misslyckas, visar kontrollpanelen [!DNL Channel Manager] statusen *[!UICONTROL Error]* för returposten. Om du vill vara säker på att retur- och återbetalningsinformationen återspeglas korrekt i Walmart Marketplace-kontot måste du manuellt uppdatera ordern i din [!DNL Walmart Marketplace]-butik.
