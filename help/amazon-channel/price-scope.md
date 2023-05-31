---
title: Amazon försäljningskanal - prisomfång
description: Använd Commerce pricing för att hantera priser utifrån flera webbplatser eller globalt.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Prisområde

[!DNL Commerce] tillhandahåller konfiguration för [prissättning](https://experienceleague.adobe.com/docs/commerce-admin/config/catalog/catalog.html#price) som ska anges till `Global` eller `Website`. Om priset är inställt på `Global`, finns det en enda priskälla för alla webbplatser. Om priset är inställt på `Website`kan dina webbplatser variera sina priser mellan och dessutom ha ett standardpris i reserv (se [Prisområde](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html)).

Om du ändrar katalogprisomfånget från `Global` till `Website`ändras också alla pristypattribut till `Website`. Se [Lägga till webbplatser](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html#add-websites).

När man väljer ett webbplatspris finns det två priskällor:

- Webbplatspriset
- Standardpriset (fallback)

För integreringen av Amazon-försäljningskanaler, baserat på din [listregler](./listing-rules.md)kan du mappa produkter från flera webbplatser till en enda [!DNL Amazon Marketplace] Land (definieras under [butiksintegrering](./store-integration.md)). Kartläggningen introducerar dock problemet med vilket pris som ska publiceras om produkten finns på flera webbplatser med olika priser.
