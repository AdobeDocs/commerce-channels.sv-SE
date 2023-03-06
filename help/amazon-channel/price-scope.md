---
title: Prisområde
description: Använd Commerce pricing för att hantera priser utifrån flera webbplatser eller globalt.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Prisområde

[!DNL Commerce] tillhandahåller konfiguration för [prissättning](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} to be set to `Global` or `Website`. If pricing is set to `Global`, there is a single price source for all websites. If pricing is set to `Website`, your websites can vary their pricing across and also have a fallback default pricing value. See [Catalog Price](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){target="_blank"} i den centrala Commerce-användarhandboken.

Om du ändrar katalogprisomfånget från `Global` till `Website`ändras också alla pristypattribut till `Website`. Se [Lägga till webbplatser](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){target="_blank"}.

När man väljer ett webbplatspris finns det två priskällor:

- Webbplatspriset
- Standardpriset (fallback)

För integreringen av Amazon-försäljningskanaler, baserat på din [listregler](./listing-rules.md)kan du mappa produkter från flera webbplatser till en enda [!DNL Amazon Marketplace] Land (definieras under [butiksintegrering](./store-integration.md)). Kartläggningen introducerar dock problemet med vilket pris som ska publiceras om produkten finns på flera webbplatser med olika priser.
