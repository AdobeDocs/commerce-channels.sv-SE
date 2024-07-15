---
title: Översikt över inställningar
description: 'Läs mer om  [!DNL Channel Manager settings] för att konfigurera autentisering och mappa produktkatalogattribut och transportföretag som krävs för att koordinera försäljningsåtgärder mellan [!DNL Commerce] och [!DNL Walmart Marketplace].'
role: Admin
feature: Sales Channels, Configuration, Merchandising, Shipping/Delivery
exl-id: 305b3580-bfe2-4fc2-9dc8-fb41f5eaf959
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Översikt över inställningar

Försäljningskanalsinställningarna möjliggör kommunikation och datasynkronisering mellan [!DNL Commerce] och [!DNL Walmart Marketplace] så att du kan hantera [!DNL Walmart Marketplace] säljåtgärder från [!DNL Commerce]-administratören.

I [!DNL Channel Manager] konfigurerar du vissa inställningar för försäljningskanaler under introduktionsprocessen. Efter introduktionen kan du visa och hantera konfigurationen genom att välja **[!UICONTROL Channel Settings]** på kontrollpanelerna [!UICONTROL Listings] och [!UICONTROL Orders].

* **[GåMart-anslutning](manage-wmt-connection.md)**-Under [!DNL Channel Manager]-introduktionsprocessen anger du [API-autentiseringsuppgifter](walmart-requirements.md#generate-a-walmart-marketplace-production-api-key) från ditt [!DNL Walmart Marketplace]-återförsäljarkonto för att ansluta [!DNL Commerce] till [!DNL Walmart Marketplace] för kommunikation och datasynkronisering. Om det behövs kan du uppdatera de här inloggningsuppgifterna från sidan *Kanalinställningar*.

* **[Mappa unika identifierare](map-catalog-attributes.md)** - Innan du ansluter listor från [!DNL Commerce] till [!DNL Walmart Marketplace] måste du mappa minst en unik identifierare från din [!DNL Commerce]-katalog till motsvarande identifierare från Walmart. Det här steget krävs för att matcha [!DNL Commerce] produkter med befintliga [!DNL Walmart]-listor och för att synkronisera produktdata mellan [!DNL Commerce] och [!DNL Walmart].

* **[Mappa transportföretag](map-shipping-carriers.md)**-Innan du bearbetar [!DNL Walmart Marketplace] beställningar från [!DNL Commerce] måste du mappa transportföretag från din [!DNL Commerce]-instans till motsvarande transportföretag på [!DNL Walmart Marketplace].
