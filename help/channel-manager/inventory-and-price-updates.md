---
title: Lager- och prisuppdateringar
description: '''[!DNL Channel Manager] synkroniserar lager- och prisuppdateringar mellan Commerce Store och [!DNL Walmart Marketplace] så att du kan hantera dina säljkanalsåtgärder från din Commerce Admin'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a1944052f02968c36495275cd5ddfb2ca43ce967
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Lager- och prisuppdateringar

[!DNL Channel Manager] spårar lager och priser för produkter i kanalbutiken. När lager eller priser ändras synkroniseras uppdateringarna med båda [!DNL Channel Manager] och [!DNL Walmart Marketplace] för att återspegla aktuell lagerkvantitet och priser i produktlistor.

## Lageruppdateringar

När lagernivåerna ändras synkroniserar Channel Manager uppdateringar mellan Commerce och Walmart Marketplace för att säkerställa att kanalhanteraren och Walmart Marketplace har rätt lagerkvantitet.

Det kan ta upp till 10 minuter för lageruppdateringar att synkronisera mellan kanalhanteraren och marknadsplatsen.

* **Uppdateringar av lagerkvantitet i produktkatalog**-När butikskvantiteten ändras på grund av [manuella ändringar av lagerkvantitet](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html), återbetalningar eller annulleringar synkroniserar Channel Manager ändringen till anslutna kanaler och [!DNL Walmart Marketplace].

* **Minska lagerkvantiteten för att återspegla Walmart Marketplace-order**-Efter att en Walmart Marketplace-order har synkroniserats med kanalhanteraren skickas uppdateringen till handelsordersystemet. Handel justerar lagerkvantiteter baserat på ordern. Därefter synkroniseras den uppdaterade kvantiteten till Walmart Marketplace. Tills synkroniseringen är klar kan du se kvantitetsskillnader mellan kanalhanteraren och Marketplace.

>[!IMPORTANT]
>
> Efter att en Walmart Marketplace-order har synkroniserats med Channel Manager uppdateras lagerkvantiteter och orderinformation endast för återbetalningar och annulleringar som initierats från Commerce. Om en order återbetalas eller annulleras från Walmart Marketplace ska du bearbeta ändringen från Commerce för att säkerställa att lagret i Commerce är korrekt och att orderinformationen är korrekt.

## Prisuppdateringar

När produktpriset ändras i Commerce synkroniseras uppdateringen från [!DNL Commerce] produktkatalog till [!DNL Walmart Marketplace]. Det kan ta upp till fem minuter för marknadsplatsen att visa prisförändringarna.

### Hantera priser för en publicerad produkt

1. Från [!UICONTROL Admin], markera **[!UICONTROL Catalog > Products]**.
1. Leta reda på produkten som ska uppdateras och välj **[!UICONTROL Edit]**.
1. Granska och uppdatera priset efter behov.
1. **[!UICONTROL Save]** förändringen.

Mer information om hur du hanterar produktpriskonfigurationen i Commerce finns i [Hantera priser](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
