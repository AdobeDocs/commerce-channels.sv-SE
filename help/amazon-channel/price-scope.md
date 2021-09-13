---
title: Prisområde
description: Använd Commerce pricing för att hantera priser utifrån flera webbplatser eller globalt.
exl-id: 24a1eac1-d579-4063-a33c-71969bc2b4b9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Prisområde

[!DNL Commerce] innehåller konfiguration för  [prisomfånget](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;} som ska anges till  `Global` eller  `Website`. Om priset är `Global` finns det en enda priskälla för alla webbplatser. Om du anger `Website` som pris kan dina webbplatser variera sina priser och dessutom få ett standardpris som reserv. Se [Katalogpris](https://docs.magento.com/user-guide/configuration/catalog/catalog.html#price){:target=&quot;_blank&quot;} i huvudanvändarhandboken för Commerce.

Om du ändrar katalogprisomfånget från `Global` till `Website` ändras även alla pristypsattribut till `Website`. Se [Lägga till webbplatser](https://docs.magento.com/user-guide/stores/stores-all-create-website.html){:target=&quot;_blank&quot;}.

När man väljer ett webbplatspris finns det två priskällor:

- Webbplatspriset
- Standardpriset (fallback)

För integreringen av Amazon-försäljningskanaler, baserat på dina [listregler](./listing-rules.md), kan du mappa produkter från flera webbplatser till ett enda [!DNL Amazon Marketplace]-land (definierat under [butiksintegrering](./store-integration.md)). Kartläggningen introducerar dock problemet med vilket pris som ska publiceras om produkten finns på flera webbplatser med olika priser.
