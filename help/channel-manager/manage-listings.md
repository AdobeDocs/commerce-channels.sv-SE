---
title: Hantera listor
description: 'Hantera säljkanalslistor för en [!DNL Commerce] butik med Channel Manager för Adobe Commerce och Magento Open Source.'
feature: Sales Channels, Merchandising, Products
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Hantera listor

Hantera produktlistor för försäljningskanalen [!DNL Walmart Marketplace] från gränssnittet för kanalhanteraren.

Statusen för en enskild lista visar var produkten finns i arbetsflödet [!DNL Channel Manager] så att du kan bestämma nästa steg och åtgärda eventuella fel.

![Sidan med listor för en ansluten försäljningskanal](assets/listings-dashboard-view.png){width="500" zoomable="yes"}

Du kan utföra följande uppgifter i listvyn.

* Visa aktuella listor
* Sortera och filtrera listorna
* Lägg till produkter
* Matcha produkter
* Status för spårlista
* Granska felbeskrivningen för listor med felstatus

## Visa produktlistor

1. Gå till [!UICONTROL **Marknadsföring** > **Kanalhanteraren**] i Admin.

1. I listan Store väljer du ögonikonen i en butikspostrad för att öppna butiksvyn.

1. Välj [!UICONTROL **Listor**].

1. Sortera *listvyn* genom att välja en kolumnrubrik i tabellen *Lista*.

1. Filtrera vyn *Lista* genom att välja ett av statuskorten.

1. Återställ sorteringsordningen och ta bort filter genom att välja **Uppdatera produkter**.

## Lägg till [!DNL Commerce] produkter i kanalhanteraren

Skapa produktsortimentet för [!DNL Walmart Marketplace]-kanalen genom att utföra följande uppgifter:

* [Lägg till produkter från din [!DNL Commerce] produktkatalog i [!DNL Channel Manager]](add-products-to-channel-store.md)

* [Mappa katalogattribut](map-catalog-attributes.md#configure-product-attribute-settings)

## Matcha produkter på [!DNL Walmart]

Du kan skapa produkterbjudanden på [!DNL Walmart Marketplace] med produktmatchning eller genom att överföra produktlistor manuellt för nya produkter.

* **[Matcha produkter på Walmart](connect-listings-to-marketplace.md)** - Anslut produktlistor från din kanal till [!DNL Walmart Marketplace] genom att uppdatera befintliga listor som säljer samma produkt. Matchningskriterierna bestäms av kanalens [attributmappningskonfiguration](map-catalog-attributes.md).

* **[Överför nya listor manuellt](connect-listings-to-marketplace.md#upload-new-product-listings)** - För produkter som inte matchar en befintlig lista på [!DNL Walmart Marketplace] använder du en Excel-mall för [!DNL Walmart]-produktkategori om du vill överföra produktlistor gruppvis.

## Listkontroller och kolumnbeskrivningar

Följande tabeller beskriver de kontroller och kolumner som är tillgängliga för [!UICONTROL Listings].

**Kontroller för[!UICONTROL Listings]**

| **Kontroll** | **Beskrivning** |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Add Products] | Öppnar sidan [!UICONTROL Admin Product Catalog] där du kan välja vilka produkter som ska läggas till i ditt [!DNL Walmart Marketplace]-sortiment, eller uppdatera produktattribut så att de uppfyller Walmart Marketplace-listkraven. |
| [!UICONTROL Match products on Walmart] | När du har valt en eller flera produkter med statusen [!UICONTROL Draft] väljer du [!UICONTROL Match products on Walmart] för att söka efter produkterbjudanden som kan läggas till i en befintlig [!DNL Walmart Marketplace]-lista. |
| [!UICONTROL Refresh products] | Uppdatera visningen med den senaste listan och statusen. Den här kontrollen återställer även listvyn till standardsorteringsordningen och tar bort eventuella filter. |
| [!UICONTROL Filter by *Status*] | Visa bara listor med en viss status genom att markera ett av statuskorten ovanför tabellen Lista. Ta bort filtret genom att välja **[!UICONTROL Refresh products]**. |
| [!UICONTROL Sort products] | Ändra sorteringsordningen för listning genom att välja en kolumnrubrik. |


**Kolumnbeskrivningar**

| **Fält** | **Beskrivning** |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Namn på produkten från lagringskatalogen [!DNL Commerce]. |
| [!UICONTROL SKU (Unique ID)] | SKU:n som tilldelats produkten i katalogen [!DNL Commerce]. |
| [!UICONTROL  Quantity] | Belopp som är tillgängligt i Adobe Commerce eller Magento Open Source. |
| [!UICONTROL Price] | Produktpriset från butikskatalogen [!DNL Commerce]. Katalogprisuppdateringarna synkroniseras med kanalhanteraren och skickas sedan till [!DNL Walmart Marketplace] så att listade objekt visar det aktuella priset. |
| [!UICONTROL Status] | Anger den aktuella orderstatusen i orderarbetsflödet [!DNL Commerce]. Statusen uppdateras när du har lagt till produkter i [!DNL Channel Manager] och när du matchar produkter på marknadsplatsen. Om en åtgärd misslyckas visas felstatusen i listan. När du har åtgärdat felet gör [!DNL Channel Manager] om åtgärden och uppdaterar statusen. |
| [!UICONTROL Error Description] | Tillhandahåller ytterligare felinformation för produkter med statusen `[!DNL Error]`. |

### Om liststatus

På arbetsytan Lista visar statusetiketten var en produkt finns i arbetsflödet för [!DNL Channel Manager] så att du kan bestämma nästa steg och lösa fel. Listor kan ha följande statusetiketter:

* **[!UICONTROL Draft]**-Identifierar produkter som inte har [skickats till [!DNL Walmart] för matchning](connect-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]** - Identifierar produkter som skickats in för matchning på [!DNL Walmart Marketplace]. Produkterna behåller statusen *Bearbetar* tills [!DNL Walmart] returnerar ett HTTP-statusmeddelande som anger om matchningen lyckades eller om ett fel uppstod. Det kan ta upp till 30 minuter innan matchningen slutförs på [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifierar produkter som matchades på [!DNL Walmart].

  En matchning inträffar när produktattributvärdet - till exempel UPC-koden - matchar UPC-värdet i en befintlig [!DNL Walmart Marketplace]-lista. När en produkt överensstämmer läggs Commerce produkterbjudande till i den befintliga listan.

  Kontrollera kontrollpanelen [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) om du vill granska den uppdaterade produktlistan och verifiera produktinformation, pris och lagerkvantitet.

* **[!UICONTROL Match - Match in Stage]** - Identifierar produkter som matchar [!DNL Walmart] och som inte kan anslutas förrän [!DNL Walmart Marketplace]-butiken är aktiv. Produkter med den här statusen ansluts automatiskt när butiken [!DNL Walmart Marketplace] publiceras.

* **[!UICONTROL Error]** - Identifierar produkter som inte matchats mot en befintlig [!DNL Walmart Marketplace]-lista.

* **[!UICONTROL Error description]** - Tillhandahåller detaljerad information om listfelet.

  När du har åtgärdat felet skickar du produkten igen för matchning. Se [Felsöka produktmatchningsfel](connect-listings-to-marketplace.md#troubleshoot-product-match-errors).
