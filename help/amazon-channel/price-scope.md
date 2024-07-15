---
title: Amazon försäljningskanal - prisomfång
description: Använd Commerce prissättning för att hantera priser utifrån flera webbplatser eller globalt.
feature: Sales Channels, Price Rules
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Prisområde

[!DNL Commerce] tillhandahåller konfiguration för ditt [prisområde](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) som ska anges till `Global` eller `Website`. Om priset anges till `Global` finns det en enda priskälla för alla webbplatser. Om priset är inställt på `Website` kan dina webbplatser variera sina priser och även ha ett standardreservprisvärde (se [Prisomfång](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)).

Om du ändrar katalogprisomfånget från `Global` till `Website` ändras även alla pristypattribut till `Website`. Se [Lägga till webbplatser](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

När man väljer ett webbplatspris finns det två priskällor:

- Webbplatspriset
- Standardpriset (fallback)

För integreringen av Amazon-försäljningskanaler, baserat på dina [listregler](./listing-rules.md), kan du mappa produkter från flera webbplatser till ett enda [!DNL Amazon Marketplace]-land (definieras under [butiksintegrering](./store-integration.md)). Kartläggningen introducerar dock problemet med vilket pris som ska publiceras om produkten finns på flera webbplatser med olika priser.
