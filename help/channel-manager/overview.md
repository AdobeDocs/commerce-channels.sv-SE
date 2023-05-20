---
title: Introduktion till [!DNL Channel Manager]'
description: "Lär dig hur du installerar och använder [!DNL Channel Manager] att integrera Adobe Commerce och Magento Open Source butiker med Walmart Marketplace och skapa en försäljningskanal för att hantera marknadsplatslistor, priser, lager och försäljning smidigt från er Commerce Admin."
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---


# Introduktion till [!DNL Channel Manager]

[!DNL Channel Manager] hjälper handlare att öka försäljningen, nå nya kunder, effektivisera sin försäljning och spara tid genom att integrera en Adobe Commerce- eller Magento Open Source-produktkatalog med [!DNL Walmart Marketplace].

![[!DNL Channel Manager] tilläggsadministratörsvy](assets/channel-manager-home.png)

[!DNL Channel Manager] stöder de handlare i Adobe Commerce och Magento Open Source som vill sälja vidare [!DNL Walmart Marketplace] genom att utöka [!DNL Commerce] Admin. Med [!DNL Channel Manager] installerat kan arkivadministratörer och driftspersonal hantera [!DNL Walmart Marketplace] försäljning, lager och produktpriser sömlöst från Commerce-miljön.

Den utökade administratören effektiviserar verksamheten eftersom handlarna kan använda samma arbetsflöden och processer för att hantera försäljningen från båda [!DNL Commerce] storefront och Walmart Marketplace.

När du har installerat och konfigurerat [!DNL Channel Manager]kan du använda följande funktioner för att hantera Walmart Marketplace-försäljningsorder:

* **Listhantering**-Koppla enkelt upp produktlistor genom att matcha produkter från [!DNL Commerce] katalog till befintlig [!DNL Walmart Marketplace] listor.

* **Inventory management**-Artiklar i säljarens säljarkonto synkroniseras automatiskt och uppdateras från [!DNL Commerce] för att säkerställa korrekta lagernivåer.

* **Prisuppdateringar**- Behåll korrekt prissättning för marknadsplatslistor med automatisk prissynkronisering. När priset ändras i Adobe Commerce återspeglas ändringarna på marknaden.

* **Orderhantering**- När nya order skapas på marknaden [!DNL Channel Manager] synkroniserar beställningar med Adobe Commerce och skickar beställningsbekräftelser till marknadsplatsen. Denna källangivelse säkerställer att lagret reserveras för varje order. Det sista steget är att skapa motsvarande order i [!DNL Commerce] Orderhanteringssystem för behandling.

* **Leveranshantering**- När beställningar har markerats som levererade i Adobe Commerce skickas leveransuppdateringen till [!DNL Walmart Marketplace]. Detta meddelande säkerställer att säljarna uppfyller sina SLA-krav och att kunderna får meddelanden om leveransuppdateringar för sina aktuella order.

* **Annulleringar**- När beställningar annulleras i Adobe Commerce, [!DNL Channel Manager] skickar uppdaterad orderinformation till marknadsplatsen för att replikera åtgärden för motsvarande marknadsplatsorder. När ordern har annullerats [!DNL Commerce] Uppdateringar av lagerkvantitet för att spegla returnerade artiklar och lageruppdateringar synkroniseras automatiskt till [!DNL Walmart Marketplace].

* **Returer och återbetalningar**- När Walmart Marketplace begär en retur av artiklar som beställts via Adobe Commerce eller Magento Open Source, [!DNL Channel Manager] skickar returbegärandeinformationen till butiken för Commerce-försäljningskanalen för att replikera returbegäran. Därefter kan bidraget bearbetas med [!DNL Commerce] [arbetsflöde för återbetalning](https://docs.magento.com/user-guide/sales/credit-memos.html#refund-workflow), offline-metod. När återbetalningen är slutförd [!DNL Channel Manager] synkroniserar uppdateringen till Walmart så att returstatusen på marknadsplatssäljarkontot kan uppdateras för att återspegla återbetalningen.

## Förväntad fördröjning för [!DNL Channel Manager] operationer

Datasynkroniseringsprocesserna mellan [!DNL Channel Manager] och en länkad [!DNL Walmart Marketplace] butiken behöver lite tid för att slutföra. Granska den förväntade bearbetningstiden för [!DNL Channel Manager] åtgärder för att planera säljkanalsåtgärder.

**Beräknad fördröjning för [!DNL Channel Manager] operationer**

| **Åtgärd** | **Beskrivning** | **Förväntad fördröjning** |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Lägg till produkter i [!DNL Channel Manager] | Välj produkter från [!DNL Commerce] produktkatalog och importera dem till [!DNL Channel Manager]. | **Upp till fem minuter**-Om du väljer många produkter, till exempel en hel produktkatalog, tar importen längre tid. |
| Matcha produkter på [!DNL Walmart Marketplace] | Välj produktlistor i [!DNL Channel Manager] och skicka till Walmart för matchning. | **Upp till 30 minuter**-Om du väljer många produkter tar matchningsprocessen längre tid beroende på vald kvantitet. |
| Lageruppdateringar | När lagerkvantiteten ändras i Commerce [!DNL Channel Manager] synkroniserar uppdateringen till Walmart. | **Upp till 10 minuter** |
| Prisuppdateringar | När ett produktpris ändras [!DNL Channel Manager] synkroniserar uppdateringen till Walmart. | **Upp till fem minuter** |
| Beställ synkroniseringar från Walmart till [!DNL Commerce] | Kundorder [!DNL Commerce] på Walmart Marketplace. Walmart skickar ordern till [!DNL Channel Manager]. Ordningen visas på orderkontrollpanelen. | **Upp till 30 minuter** |
| Ordern skapades i [!DNL Commerce] Orderhantering | [!DNL Channel Manager] skapar [!DNL Commerce] beställa från Walmart-ordningen och uppdaterar orderkontrollpanelen så att den innehåller [!DNL Commerce] ordernummer. | **Upp till fem minuter** |
| Leveransstatusuppdatering i [!DNL Commerce] Orderhantering | När en order skickas från Commerce [!DNL Channel Manager] uppdaterar leveransstatus på orderkontrollpanelen och skickar uppdateringen till Walmart Marketplace så att kunden kan meddelas. | **Upp till fem minuter** |
| Orderannulleringsuppdatering i Hantering av handelsorder | När en order annulleras från Commerce [!DNL Channel Manager] uppdaterar orderstatusen på orderkontrollpanelen och skickar uppdateringen till Walmart Marketplace så att kunden kan meddelas. När ordern har annullerats [!DNL Commerce] Uppdateringar av lagerkvantitet för att spegla returnerade artiklar. Sedan [!DNL Channel Manager] synkroniserar uppdateringen till [!DNL Walmart Marketplace]. | **Upp till fem minuter** |


