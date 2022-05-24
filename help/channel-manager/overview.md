---
title: Om [!DNL Channel Manager]
description: Lär dig hur du installerar och använder [!DNL Channel Manager] att integrera Adobe Commerce och Magento Open Source butiker med marknadsplatser från tredje part och skapa en försäljningskanal för att hantera Marketplace-listor, priser, lager och försäljning smidigt från er Commerce Admin.
role: User
level: Intermediate
exl-id: 91265973-d2ad-4925-aa10-260d7e186f20
source-git-commit: 9ccd205ccd4f4b3f4e6b9fed2c4d16893f4b0da8
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Om [!DNL Channel Manager]

[!DNL Channel Manager] hjälper dig att öka försäljningen och nå nya kunder genom att integrera din Adobe Commerce- eller Magento Open Source-produktkatalog med [!DNL Walmart US Marketplace].

![[!DNL Channel Manager] tilläggsadministratörsvy](assets/channel-manager-home.png)

Channel Manager stöder Adobe Commerce- och Magento Open Source-säljare som vill sälja på Walmart Marketplace.

När du har installerat och konfigurerat [!DNL Channel Manager], [!DNL Commerce] Administratören har utökats så att du kan hantera [!DNL Walmart Marketplace] säljåtgärder sömlöst från din handelsmiljö.

* **Listhantering**-Publicera enkelt produktlistor genom att matcha produkter från din Commerce-katalog med befintliga Walmart Marketplace-listor.

* **Inventory management**-Artiklar på handlarens säljarkonto synkroniseras automatiskt och uppdateras från Commerce för att säkerställa korrekta lagernivåer.

* **Prisuppdateringar**-Behåll korrekta priser för marknadsplatslistor med automatisk prissynkronisering. När priset ändras i Adobe Commerce återspeglas ändringarna på marknaden inom 10 minuter.

* **Orderhantering**-När nya order skapas på en marknadsplats synkroniserar Channel Manager order med Adobe Commerce och skickar orderbekräftelser till marknadsplatsen för att säkerställa att lagret reserveras för varje order.

* **Leveranshantering**-När beställningar har markerats som levererade i Adobe Commerce, skickas leveransuppdateringen till [!DNL Walmart Marketplace]. Detta meddelande säkerställer att säljarna uppfyller sina SLA-krav och att kunderna får meddelanden om leveransuppdateringar för sina aktuella order.

* **Annulleringar**-När beställningar annulleras i Adobe Commerce skickar Channel Manager uppdaterad orderinformation till marknadsplatsen för att replikera åtgärden för motsvarande marknadsplatsorder.

## Förväntad fördröjning för kanalhanteraråtgärder

Datasynkroniseringsprocesserna mellan [!DNL Channel Manager] och en länkad [!DNL Walmart Marketplace] butiken behöver lite tid för att slutföra. Granska den förväntade bearbetningstiden för [!DNL Channel Manager] åtgärder för att planera säljkanalsåtgärder.

**Beräknad fördröjning för kanalhanteraråtgärder**

| **Åtgärd** | **Beskrivning** | **Förväntad fördröjning** |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Lägg till produkter i Channel Manager | Välj produkter i Commerce-produktkatalogen och importera dem till Channel Manager. | **Upp till fem minuter**-Om du väljer många produkter, till exempel en hel produktkatalog, tar importen längre tid. |
| Matcha produkter på Walmart Marketplace | Välj produktlistor i Channel Manager och skicka till Walmart för matchning. | **Upp till 30 minuter**-Om du väljer många produkter tar matchningsprocessen längre tid beroende på vald kvantitet. |
| Lageruppdateringar | När lagerkvantiteten ändras i Commerce [!DNL Channel Manager] synkroniserar uppdateringen till Walmart. | **Upp till 10 minuter** |
| Prisuppdateringar | När ett produktpris ändras synkroniserar Channel Manager uppdateringen till Walmart. | **Upp till fem minuter** |
| Beställa synkroniseringar från Walmart till Commerce | Kunden beställer en Commerce-produkt på Walmart Marketplace. Walmart skickar beställningen till kanalhanteraren. Ordningen visas på orderkontrollpanelen. | **Upp till 30 minuter** |
| Ordern har skapats i Hantering av handelsorder | Kanalhanteraren skapar handelsordern från Walmart-ordern och uppdaterar orderkontrollpanelen så att den innehåller handelsordernumret. | **Upp till fem minuter** |

