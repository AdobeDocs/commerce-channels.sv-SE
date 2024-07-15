---
title: Introduktion till  [!DNL Channel Manager]
description: 'Lär dig hur du installerar och använder [!DNL Channel Manager] för att integrera Adobe Commerce- och Magento Open Source-butiker med Walmart Marketplace och skapa en försäljningskanal för att hantera marknadsplatslistor, priser, lager och försäljning smidigt från din Commerce Admin.'
role: Leader, Admin, User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 850aece134084e108b324a964d7d834042c7ddfd
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# Introduktion till [!DNL Channel Manager]

[!DNL Channel Manager] hjälper handlare att öka försäljningen, nå nya kunder, effektivisera säljprocesserna och spara tid genom att integrera en Adobe Commerce- eller Magento Open Source-produktkatalog med [!DNL Walmart Marketplace].

![[!DNL Channel Manager] tilläggsadministratörsvy](assets/channel-manager-home.png){width="700" zoomable="yes"}

[!DNL Channel Manager] har stöd för Adobe Commerce- eller Magento Open Source-handlare som vill sälja på [!DNL Walmart Marketplace] genom att utöka [!DNL Commerce]-administratören. Med [!DNL Channel Manager] installerat kan butiksadministratörer och driftspersonal hantera [!DNL Walmart Marketplace] försäljning, lager och produktpriser sömlöst från Commerce-miljön.

Den utökade administratören effektiviserar åtgärderna eftersom handlarna kan använda samma arbetsflöden och processer för att hantera försäljningen från både [!DNL Commerce] butiker och Walmart Marketplace.

När du har installerat och konfigurerat [!DNL Channel Manager] kan du använda följande funktioner för att hantera försäljningsorder på Walmart Marketplace:

* **Listhantering** - Anslut enkelt produktlistor genom att matcha produkter från din [!DNL Commerce]-katalog med befintliga [!DNL Walmart Marketplace]-listor.

* **Inventory management**-Artiklar i handlarens säljarkonto synkroniseras automatiskt och uppdateras från [!DNL Commerce] för att säkerställa korrekta lagernivåer.

* **Prisuppdateringar** - Behåll rätt priser för marknadsplatslistor med automatisk prissynkronisering. När priset ändras i Adobe Commerce återspeglas ändringarna på marknaden.

* **Beställningshantering** - När nya order skapas på marknadsplatsen synkroniserar [!DNL Channel Manager] order med Adobe Commerce och skickar orderbekräftelser till marknadsplatsen. Denna källangivelse säkerställer att lagret reserveras för varje order. Det sista steget är att skapa motsvarande order i Order Management-systemet [!DNL Commerce] för bearbetning.

* **Leveranshantering** - När order markeras som levererade i Adobe Commerce skickas leveransuppdateringen till [!DNL Walmart Marketplace]. Detta meddelande säkerställer att säljarna uppfyller sina SLA-krav och att kunderna får meddelanden om leveransuppdateringar för sina aktuella order.

* **Annulleringar** - När beställningar annulleras i Adobe Commerce skickar [!DNL Channel Manager] uppdaterad orderinformation till marknadsplatsen för att replikera åtgärden för motsvarande marknadsplatsorder. När orderannulleringen har slutförts synkroniseras [!DNL Commerce]-lagerkvantitetsuppdateringarna automatiskt för att återspegla returnerade artiklar och lageruppdateringar till [!DNL Walmart Marketplace].

* **Returnerar och återbetalas** - När Walmart Marketplace begär en retur av objekt som beställts via försäljningskanalen för Adobe Commerce eller Magento Open Source, skickar [!DNL Channel Manager] returbegärandeinformationen till Commerce säljkanalsbutik för att replikera returbegäran. Återbetalningen kan sedan behandlas med offlinemetoden [!DNL Commerce] [ReturnWorkflow](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memos.html#refund-workflow) . När återbetalningen är klar synkroniserar [!DNL Channel Manager] uppdateringen till Walmart så att returstatusen på marknadsplatssäljarkontot kan uppdateras för att återspegla återbetalningen.

## Förväntad fördröjning för [!DNL Channel Manager]-åtgärder

Datasynkroniseringsprocesserna mellan [!DNL Channel Manager] och ett länkat [!DNL Walmart Marketplace]-arkiv kräver en stund. Granska den förväntade bearbetningstiden för [!DNL Channel Manager]-åtgärder för att hjälpa till att planera säljkanalsåtgärder.

**Uppskattad fördröjning för [!DNL Channel Manager] åtgärder**

| **Åtgärd** | **Beskrivning** | **Förväntad fördröjning** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Lägg till produkter i [!DNL Channel Manager] | Välj produkter från produktkatalogen [!DNL Commerce] och importera dem till [!DNL Channel Manager]. | **Upp till fem minuter**-Om du väljer många produkter, till exempel en hel produktkatalog, tar importen längre tid. |
| Matcha produkter på [!DNL Walmart Marketplace] | Välj produktlistor i [!DNL Channel Manager] och skicka till Walmart för matchning. | **Upp till 30 minuter**-Om du väljer många produkter tar matchningsprocessen längre tid beroende på vald kvantitet. |
| Lageruppdateringar | När lagerkvantiteten ändras i Commerce synkroniserar [!DNL Channel Manager] uppdateringen till Walmart. | **Upp till 10 minuter** |
| Prisuppdateringar | När ett produktpris ändras synkroniserar [!DNL Channel Manager] uppdateringen till Walmart. | **Upp till fem minuter** |
| Ordna synkroniseringar från Walmart till [!DNL Commerce] | Kunden beställer en [!DNL Commerce]-produkt på Walmart Marketplace. Walmart skickar ordern till [!DNL Channel Manager]. Ordningen visas på orderkontrollpanelen. | **Upp till 30 minuter** |
| Beställning skapad i [!DNL Commerce] Order Management | [!DNL Channel Manager] skapar ordningen [!DNL Commerce] från Walmart-ordningen och uppdaterar orderkontrollpanelen så att den innehåller ordernumret [!DNL Commerce]. | **Upp till fem minuter** |
| Leveransstatusuppdatering i [!DNL Commerce] Order Management | När en order levereras från Commerce uppdaterar [!DNL Channel Manager] leveransstatusen på orderkontrollpanelen och skickar uppdateringen till Walmart Marketplace så att kunden kan meddelas. | **Upp till fem minuter** |
| Uppdatering av annullering av order i Commerce Order Management | När en order annulleras från Commerce uppdaterar [!DNL Channel Manager] orderstatusen på orderkontrollpanelen och skickar uppdateringen till Walmart Marketplace så att kunden kan meddelas. När orderannulleringen har slutförts uppdateras lagerkvantiteten [!DNL Commerce] så att returnerade artiklar visas. Sedan synkroniserar [!DNL Channel Manager] uppdateringen till [!DNL Walmart Marketplace]. | **Upp till fem minuter** |


