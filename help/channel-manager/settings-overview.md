---
title: Översikt över inställningar
description: Läs mer om [!DNL Channel Manager settings] konfigurera autentisering och mappa produktkatalogattribut och transportföretag som krävs för att koordinera försäljningsåtgärder mellan [!DNL Commerce] och [!DNL Walmart Marketplace].'
role: Admin
feature: Sales Channels, Configuration, Merchandising, Shipping/Delivery
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Översikt över inställningar

Försäljningskanalsinställningarna möjliggör kommunikation och datasynkronisering mellan [!DNL Commerce] och [!DNL Walmart Marketplace] så att ni kan hantera [!DNL Walmart Marketplace] försäljningsoperationer från [!DNL Commerce] Admin.

I [!DNL Channel Manager]konfigurerar du vissa inställningar för försäljningskanaler under introduktionsprocessen. Efter introduktionen kan du visa och hantera konfigurationen genom att välja **[!UICONTROL Channel Settings]** från [!UICONTROL Listings] och [!UICONTROL Orders] instrumentpaneler.

* **[Walmart-anslutning](manage-wmt-connection.md)**-Under [!DNL Channel Manager] introduktionsprocess, du tillhandahåller [API-autentiseringsuppgifter](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) från [!DNL Walmart Marketplace] Försäljarkonto att ansluta till [!DNL Commerce] till [!DNL Walmart Marketplace] för kommunikation och datasynkronisering. Om det behövs kan du uppdatera dessa uppgifter från *Kanalinställningar* sida.

* **[Mappa unika identifierare](map-catalog-attributes.md)**-Innan du ansluter listor från [!DNL Commerce] till [!DNL Walmart Marketplace]mappa minst en unik identifierare från [!DNL Commerce] katalog till motsvarande identifierare från Walmart. Det här steget krävs för att matcha [!DNL Commerce] produkter till befintliga [!DNL Walmart] listor och synkronisera produktdata mellan [!DNL Commerce] och [!DNL Walmart].

* **[Kartlägg transportföretag](map-shipping-carriers.md)**-Innan du bearbetar [!DNL Walmart Marketplace] order från [!DNL Commerce]ser du till att kartlägga fraktföretag från [!DNL Commerce] instans till motsvarande bärare på [!DNL Walmart Marketplace].
