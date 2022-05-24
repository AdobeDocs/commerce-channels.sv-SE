---
title: Lager- och prisuppdateringar
description: '''[!DNL Channel Manager] synkroniserar lager- och prisuppdateringar mellan Commerce Store och [!DNL Walmart Marketplace] så att du kan hantera dina säljkanalsåtgärder från din Commerce Admin'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: 71ad5e3bc9ff6b909943a161472e4db7d375683f
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Uppdatera lager och priser

[!DNL Channel Manager] spårar lager och priser för produkter i [!DNL Commerce] produktkatalog och synkroniserar uppdateringar till den anslutna försäljningskanalen och [!DNL Walmart Marketplace]. Synkroniseringen ser till att produktlistor återspeglar aktuell lagerkvantitet och aktuella priser.

## Lageruppdateringar

När produktlagernivåer ändras i [!DNL Commerce], [!DNL Channel Manager] synkroniserar uppdateringar till försäljningskanalen och till [!DNL Walmart Marketplace]. Det kan ta upp till 10 minuter för lageruppdateringar att synkronisera över försäljningskanalen till [!DNL Walmart marketplace].

* **Uppdateringar av lagerkvantitet i produktkatalog**—When [!DNL Commerce] lagerkvantitet ändras på grund av [manuella ändringar av lagerkvantitet](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html), återbetalningar eller uppsägningar, [!DNL Channel Manager] synkroniserar ändringen till anslutna kanaler och [!DNL Walmart Marketplace].

* **Minska lagerkvantiteten för att spegla [!DNL Walmart Marketplace] order**—Efter [!DNL Walmart Marketplace] order synkas till [!DNL Channel Manager], [!DNL Channel Manager] skickar uppdateringen till [!DNL Commerce] ordersystem. [!DNL Commerce] justerar lagerkvantiteter baserat på ordern. Sedan synkroniseras den uppdaterade kvantiteten till [!DNL Walmart Marketplace]. Tills synkroniseringsåtgärderna är slutförda kan du se olika kvantiteter i säljkanalslistorna och [!DNL Walmart].

>[!IMPORTANT]
>
>Efter [!DNL Walmart Marketplace] order synkas till [!DNL Channel Manager], lagerkvantiteter och orderinformation uppdateras endast för återbetalningar och annulleringar som initieras från [!DNL Commerce]. Om en order återbetalas eller annulleras från [!DNL Walmart marketplace], bearbeta ändringen från [!DNL Commerce] säkerställa att [!DNL Commerce] lagerkvantiteter och orderinformation.

## Prisuppdateringar

När produktpriset ändras i [!DNL Commerce], [!DNL Channel Manager] synkroniserar uppdateringen till [!DNL Walmart Marketplace]. Det kan ta upp till fem minuter innan prisändringen visas i [!DNL Walmart Marketplace] lista.

### Hantera priser för en publicerad produkt

1. Från [!UICONTROL Admin], markera **[!UICONTROL Catalog > Products]**.
1. Leta reda på produkten som ska uppdateras och välj **[!UICONTROL Edit]**.
1. Granska och uppdatera priset efter behov.
1. **[!UICONTROL Save]** förändringen.

Om du vill ha hjälp med att hantera produktpriskonfigurationen i [!DNL Commerce], se [Hantera priser](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
