---
title: Lager- och prisuppdateringar
description: '''[!DNL Channel Manager] synkroniserar lager- och prisuppdateringar mellan [!DNL Commerce] lagra och [!DNL Walmart Marketplace] så att du kan hantera dina säljkanalsåtgärder via [!DNL Commerce] Administratör'
exl-id: 4dd9fa4a-b12f-4795-a7b2-84ea0fc26aa5
source-git-commit: a3ae579c0eda0c27bf8eab9d0ac12919eaad494b
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Uppdatera lager och priser

[!DNL Channel Manager] spårar lager och priser för produkter i [!DNL Commerce] produktkatalog och synkroniserar uppdateringar till den anslutna försäljningskanalen och [!DNL Walmart Marketplace]. Synkroniseringsåtgärden säkerställer att produktlistor återspeglar aktuell lagerkvantitet och aktuella priser.


>[!IMPORTANT]
>
>Efter [!DNL Channel Manager] installeras och konfigureras, synkroniseras alla lager-, pris- och orderuppdateringar automatiskt. Om du redan säljer på Walmart Marketplace måste du inaktivera alla andra integreringar som uppdaterar produkt- och orderdata. Verifiera sedan lagernivåerna och priserna i [!DNL Commerce] storefront är korrekt och matchar data i [!DNL Walmart Marketplace] innan du ansluter [!DNL Channel Manager] till marknadsplatsen.


## Lageruppdateringar

När produktlagernivåer ändras i [!DNL Commerce], [!DNL Channel Manager] synkroniserar uppdateringar till [!DNL Walmart Marketplace]. Det kan ta upp till 10 minuter för lageruppdateringar att synkronisera över försäljningskanalen till [!DNL Walmart marketplace].

* **Uppdateringar av lagerkvantitet i produktkatalog**—When [!DNL Commerce] lagerkvantitet ändras på grund av [manuella ändringar av lagerkvantitet](https://experienceleague.adobe.com/docs/commerce-admin/inventory/quantities/quantities-assign-per-product.html), återbetalningar eller uppsägningar, [!DNL Channel Manager] synkroniserar ändringen till anslutna kanaler och [!DNL Walmart Marketplace].

* **Minska lagerkvantiteten för att spegla [!DNL Walmart Marketplace] order**—Efter [!DNL Walmart Marketplace] order synkas till [!DNL Channel Manager], [!DNL Channel Manager] skickar uppdateringen till [!DNL Commerce] ordersystem. [!DNL Commerce] justerar lagerkvantiteter baserat på ordern. Sedan synkroniseras den uppdaterade kvantiteten till [!DNL Walmart Marketplace]. Tills synkroniseringsåtgärderna är slutförda kan du se olika kvantiteter i säljkanalslistorna och [!DNL Walmart].

>[!IMPORTANT]
>
>Efter [!DNL Walmart Marketplace] order synkas till [!DNL Channel Manager], lagerkvantiteter och orderinformation uppdateras endast för återbetalningar och annulleringar som initieras från [!DNL Commerce]. Om en order återbetalas eller annulleras från [!DNL Walmart marketplace], bearbeta ändringen från [!DNL Commerce] säkerställa att [!DNL Commerce] lagerkvantiteter och orderinformation.

## Prisuppdateringar

När produktpriset ändras i [!DNL Commerce], [!DNL Channel Manager] synkroniserar uppdateringen till [!DNL Walmart Marketplace]. Det kan ta upp till fem minuter innan prisändringen visas i [!DNL Walmart Marketplace] lista.

### Hantera priser för en ansluten produkt

1. Från [!UICONTROL Admin], markera **[!UICONTROL Catalog > Products]**.
1. Leta reda på produkten som ska uppdateras och välj **[!UICONTROL Edit]**.
1. Granska och uppdatera priset efter behov.
1. **[!UICONTROL Save]** förändringen.

Om du vill ha hjälp med att hantera produktpriskonfigurationen i [!DNL Commerce], se [Hantera priser](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html).
