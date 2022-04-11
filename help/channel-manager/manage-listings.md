---
title: Hantera listor
description: Hantera säljkanalslistor för en [!DNL Commerce] lagra med Channel Manager för Adobe Commerce och Magento Open Source.
exl-id: 70999552-9ba7-4b10-a8ee-ee99bc4fe837
source-git-commit: 41a6afec60edbb23492627bd8e80632d3c952caf
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Hantera listor

Hantera produktlistor för en ansluten kanal från [!UICONTROL Listings] i kanalbutiksvyn.

Använd *[!UICONTROL Listings]* arbetsyta för att hantera [!DNL Commerce] produkter som erbjuds till försäljning på Walmart Marketplace. Statusen för en enskild lista visar var produkten finns i [!DNL Channel Manager] arbetsflöde så att du kan avgöra vilka steg som ska utföras och åtgärda eventuella fel.

![Listsida för en ansluten försäljningskanal](assets/products-submit-for-matching.png)

## Visa listor

1. Gå till [!UICONTROL **Marknadsföring** > Kanaler > **Kanalhanteraren**].

1. I listan Kanalbutik väljer du pennikonen i en butikspostrad för att öppna butiksvyn.

1. Välj [!UICONTROL **Listor**].

## Lägg till handelsprodukter i kanalhanteraren

Utför följande uppgifter för att skapa produktsortimentet för Walmart Marketplace-kanalen:

* [Lägg till produkter från din Commerce-produktkatalog i Channel Manager](add-products-to-connected-channel.md)

* [Konfigurera produktmatchning](map-product-attributes-for-matching.md#configure-product-attribute-settings)

## Publicera produkter på Walmart

Du kan skapa produkterbjudanden på Walmart Marketplace med produktmatchning eller genom att överföra produktlistor manuellt för nya produkter. Instruktioner finns i [Publicera listor på Walmart Marketplace](publish-listings-to-marketplace.md) enligt följande avsnitt:

* **[Matcha produkter på Walmart](publish-listings-to-marketplace.md)**-Publicera produktlistor från din kanal till [!DNL Walmart Marketplace] genom att uppdatera befintliga listor som säljer samma produkt. Matchningskriterierna bestäms av [konfiguration för attributmappning](map-product-attributes-for-matching.md) för er kanal.

* **[Överför nya listor manuellt](publish-listings-to-marketplace.md#upload-new-product-listings)-**-För produkter som inte överensstämmer med en befintlig lista på Walmart Marketplace använder du en Walmart-produktkategorimall i Excel för att massöverföra produktlistor.

## Listkontroller och kolumnbeskrivningar

I följande tabeller beskrivs de kontroller och kolumner som är tillgängliga för [!UICONTROL Listings].

**Kontroller för[!UICONTROL Listings]**

| **Kontroll** | **Beskrivning** |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Refresh products] | Uppdaterar visningen med den senaste listan och statusen. |
| [!UICONTROL Add Products] | Öppnar [!UICONTROL Admin Product Catalog] sida för att välja produkter att lägga till [!DNL Walmart Marketplace] eller för att uppdatera produktattribut så att de uppfyller Walmart Marketplace-listkraven. |
| [!UICONTROL Match products on Walmart] | När du har valt en eller flera produkter i utkaststatus väljer du Matcha produkter i Walmart för att kontrollera om det finns produkterbjudanden som kan läggas till i en befintlig [!DNL Walmart Marketplace] lista. |


**Kolumnbeskrivningar**

| **Fält** | **Beskrivning** |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product name] | Namn på produkten från [!DNL Commerce] lagringskatalog. |
| [!UICONTROL SKU (Unique ID)] | Det mappade attribut som används för att matcha produkter på marknadsplatsen. Fältnamnet varierar beroende på den mappade attributkonfigurationen för [!DNL Channel Manager] listor. I det här fallet använder produktmatchningen SKU:n från [!DNL Commerce] katalog där du hittar en [!DNL Walmart Marketplace]  Lista med ett SKU-värde som matchar SKU-värdet från [!DNL Commerce] produktattribut. |
| [!UICONTROL  Quantity] | Belopp som är tillgängligt i Adobe Commerce eller Magento Open Source. |
| [!UICONTROL Price] | Produktpriset från [!DNL Commerce] lagringskatalog. Katalogprisuppdateringarna synkroniseras med kanalhanteraren och skickas sedan till [!DNL Walmart Marketplace]  så att listade artiklar visar aktuellt pris. |
| [!UICONTROL Status] | Anger aktuell orderstatus i [!DNL Commerce] orderarbetsflöde. Statusen uppdateras när du har lagt till produkter i [!DNL Channel Manager] och när ni matchar produkter på marknaden. Om en åtgärd misslyckas visas felstatusen i listan. När du har åtgärdat felet [!DNL Channel Manager] försöker utföra åtgärden igen och uppdaterar statusen. |


### Om liststatus

På arbetsytan Lista visas statusetiketten var en produkt finns i [!DNL Channel Manager] arbetsflöde så att du kan avgöra vilka steg som ska utföras och åtgärda fel. Listor kan ha följande statusetiketter:

* **[!UICONTROL Draft]**-Identifierar produkter som inte har [skickat till [!DNL Walmart] för matchning](publish-listings-to-marketplace.md#match-products).

* **[!UICONTROL Processing]**-Identifierar produkter som skickats in för matchning på [!DNL Walmart Marketplace]. Produkterna finns kvar i *Bearbetar* status tills [!DNL Walmart] returnerar ett HTTP-statusmeddelande som anger om matchningen lyckades eller om ett fel uppstod. Det kan ta upp till 30 minuter innan matchningen slutförs på [!DNL Walmart Marketplace].

* **[!UICONTROL Match]**-Identifierar produkter som matchades korrekt [!DNL Walmart].

   En matchning inträffar när produktattributets värde-UPC-kod till exempel matchar UPC-värdet i en befintlig[!DNL Walmart Marketplace] lista. När en produkt matchar läggs erbjudandet om Commerce-produkt till i den befintliga Walmart-listan.

   Kontrollera [[!UICONTROL Walmart Marketplace Seller Account Items]](https://seller.walmart.com/items-and-inventory/manage-items) kontrollpanel för att granska den uppdaterade produktlistan och verifiera produktinformation, pris och lagerkvantitet.


* **[!UICONTROL Error]**-Identifierar produkter som inte matchats mot en befintlig [!DNL Walmart Marketplace] lista. Visa felinformation genom att hovra över *Fel* statusetikett.

   När du har åtgärdat felet skickar du produkten igen för matchning. Se [Felsöka produktmatchningsfel](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.sz6eji8z9vzy).

* **[!UICONTROL Error - Match in Stage]**-Identifierar produkter som matchar [!DNL Walmart] som inte kan publiceras förrän [!DNL Walmart Marketplace] butiken är live. Produkter med den här statusen publiceras automatiskt när [!DNL Walmart Marketplace] butiken publiceras.
