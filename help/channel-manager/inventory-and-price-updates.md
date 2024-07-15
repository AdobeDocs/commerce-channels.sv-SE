---
title: Lager- och prisuppdateringar
description: '[!DNL Channel Manager] synkroniserar lager- och prisuppdateringar mellan  [!DNL Commerce] butiken och [!DNL Walmart Marketplace] så att du kan hantera dina säljkanalsåtgärder från  [!DNL Commerce] administratören'
feature: Sales Channels, Merchandising, Inventory, Tools and External Services
role: Leader, Admin, User
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Uppdatera lager och priser

[!DNL Channel Manager] spårar lager och priser för produkter i produktkatalogen [!DNL Commerce] och synkroniserar uppdateringar till den anslutna försäljningskanalen och [!DNL Walmart Marketplace]. Synkroniseringsåtgärden ser till att produktlistor återspeglar aktuell lagerkvantitet och aktuella priser.


>[!IMPORTANT]
>
>När [!DNL Channel Manager] har installerats och konfigurerats synkroniseras alla lager-, pris- och orderuppdateringar automatiskt. Om du redan säljer på Walmart Marketplace måste du inaktivera alla andra integreringar som uppdaterar produkt- och orderdata. Verifiera sedan att lagernivåerna och priserna i [!DNL Commerce]-butiken är korrekta och matchar data i [!DNL Walmart Marketplace] innan du ansluter [!DNL Channel Manager] till den aktiva marknadsplatsen.


## Lageruppdateringar

När produktlagernivåerna ändras i [!DNL Commerce] synkroniserar [!DNL Channel Manager] uppdateringar till [!DNL Walmart Marketplace]. Det kan ta upp till 10 minuter för lageruppdateringar att synkronisera över försäljningskanalen till [!DNL Walmart marketplace].

* **Uppdateringar av lagerkvantitet i produktkatalog** - När [!DNL Commerce] lagerkvantitet ändras på grund av [manuella ändringar av lagerkvantitet](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html), återbetalningar eller annulleringar, synkroniserar [!DNL Channel Manager] ändringen till anslutna kanaler och [!DNL Walmart Marketplace].

* **Minska lagerkvantiteten för att återspegla [!DNL Walmart Marketplace] order** - Efter att en [!DNL Walmart Marketplace]-order synkroniseras till [!DNL Channel Manager] skickar [!DNL Channel Manager] uppdateringen till [!DNL Commerce]-ordersystemet. [!DNL Commerce] justerar lagerkvantiteter baserat på ordningen. Den uppdaterade kvantiteten synkroniseras sedan till [!DNL Walmart Marketplace]. Tills synkroniseringsåtgärderna är slutförda kan du se olika kvantiteter i säljkanalslistorna och [!DNL Walmart].

>[!IMPORTANT]
>
>Efter att en [!DNL Walmart Marketplace]-order synkroniseras med [!DNL Channel Manager] uppdateras lagerkvantiteter och orderinformation endast för återbetalningar och annulleringar som initierats från [!DNL Commerce]. Om en order återbetalas eller annulleras från [!DNL Walmart marketplace], bearbetar du ändringen från [!DNL Commerce] för att se till att lagerkvantiteter och orderinformation för [!DNL Commerce] är korrekta.

## Prisuppdateringar

När produktpriset ändras i [!DNL Commerce] synkroniserar [!DNL Channel Manager] uppdateringen till [!DNL Walmart Marketplace]. Det kan ta upp till fem minuter innan prisändringen visas i listan [!DNL Walmart Marketplace].

### Hantera priser för en ansluten produkt

1. Välj **[!UICONTROL Catalog > Products]** från [!UICONTROL Admin].
1. Leta reda på produkten som ska uppdateras i produktrutnätet och välj **[!UICONTROL Edit]**.
1. Granska och uppdatera priset efter behov.
1. **[!UICONTROL Save]** ändringen.

Hjälp om hur du hanterar produktpriskonfigurationen i [!DNL Commerce] finns i [Hantera priser](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
