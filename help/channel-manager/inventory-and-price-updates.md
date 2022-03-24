---
title: Lager- och prisuppdateringar
description: '"[!DNL Channel Manager] synkroniserar lager- och prisuppdateringar mellan Commerce Store och [!DNL Walmart Marketplace] så att du kan hantera dina säljkanalsåtgärder från din Commerce Admin"'
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Lager- och prisuppdateringar

Channel Manager håller reda på lager och priser för publicerade produkter och synkroniserar ändringar till Channel Manager och Walmart Marketplace för att återspegla aktuell lagerkvantitet och priser i produktlistor.**

## Lageruppdateringar

När lagernivåerna ändras synkroniserar Channel Manager uppdateringar mellan Commerce-produktkatalogen och Walmart Marketplace så att både Channel Manager och Walmart Marketplace visar den aktuella lagerkvantiteten.

Det kan ta upp till 5 minuter för lagerändringar att visas i kanalhanteraren och Walmart Marketplace.

* **Uppdateringar av lagerkvantitet i produktkatalog**-Om butikskvantiteten ändras för en produkt som säljer på Walmart på grund av en [manuell ändring av lagerkvantitet](https://docs.magento.com/user-guide/catalog/inventory-product-quantity.html) eller en orderåterbetalning eller annullering synkroniserar Channel Manager ändringen till den anslutna försäljningskanalen och [!DNL Walmart Marketplace].

* **Minska lagerkvantiteten för att återspegla Walmart Marketplace-order**-Efter att en Walmart Marketplace-order har synkroniserats med kanalhanteraren skickas uppdateringen till handelsordersystemet. Handel justerar lagerkvantiteter baserat på ordern. Därefter synkroniseras den uppdaterade kvantiteten till Walmart Marketplace. kan vara några skillnader i lagerkvantitet som visas i kanalhanteraren och Marketplace tills synkroniseringsåtgärderna har slutförts.

>[!IMPORTANT]
>
> Efter att en Walmart Marketplace-order har synkroniserats med Channel Manager uppdateras lagerkvantiteter och annan orderbearbetningsinformation endast för återbetalningar och annulleringar som initierats från Commerce. Om en order återbetalas eller annulleras från Walmart Marketplace, bearbetar du ändringen från Commerce för att se till att Commerce-lagerkvantiteter och orderinformation är korrekta.

## Prisuppdateringar

När produktpriset ändras i Commerce synkroniserar Channel Manager uppdateringen från Commerce-produktkatalogen till Walmart Marketplace. Det kan ta upp till 5 minuter innan lagerändringar visas.

### Hantera priser för en publicerad produkt

1. Från [!UICONTROL Admin], markera **[!UICONTROL Catalog > Products]**.
1. Leta reda på produkten som ska uppdateras och välj **[!UICONTROL Edit]**.
1. Granska och uppdatera priset efter behov.
1. **[!UICONTROL Save]** förändringen.

Channel Manager synkroniserar alla prisuppdateringar till kanalbutiken och [!DNL Walmart Marketplace]. Den här åtgärden kan ta upp till 5 minuter.

Mer information om hur du hanterar produktpriskonfigurationen i Commerce finns i [Hantera priser](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}.
