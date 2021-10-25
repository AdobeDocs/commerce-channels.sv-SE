---
title: Prisområde
description: Använd Commerce pricing för att hantera priser utifrån flera webbplatser eller globalt.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Prisområde

[!DNL Commerce] tillhandahåller konfiguration för [prissättning](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target=&quot;_blank&quot;} ska anges till `Global` eller `Website`. Om priset är inställt på `Global`, finns det en enda priskälla för alla webbplatser. Om priset är inställt på `Website`kan dina webbplatser variera sina priser och dessutom ha ett standardpris. Se [Katalogpris](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target=&quot;_blank&quot;} i användarhandboken för kärnhandeln.

Om du ändrar katalogprisomfånget från `Global` till `Website`ändras också alla pristypattribut till `Website`. Se [Lägga till webbplatser](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target=&quot;_blank&quot;}.

När man väljer ett webbplatspris finns det två priskällor:

- Webbplatspriset
- Standardpriset (fallback)

För integreringen av Amazon-försäljningskanaler, baserat på din [listregler](./listing-rules.md)kan du mappa produkter från flera webbplatser till en enda [!DNL Amazon Marketplace] Land (definieras under [butiksintegrering](./store-integration.md)). Kartläggningen introducerar dock problemet med vilket pris som ska publiceras om produkten finns på flera webbplatser med olika priser.
