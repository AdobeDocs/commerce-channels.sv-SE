---
title: Hantera Walmart Marketplace-anslutning
description: '''Uppdatera API-autentiseringsuppgifterna för att auktorisera anslutningen mellan en [DNL! Commerce]-butiksvyn och [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] produktlistor och synkronisera lager, pris, order och leveransdata mellan [!DNL Commerce] och Walmart.'
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Kartlägg transportföretag

Innan du [processorderförsändelser](process-orders.md#ship-an-order) for [!DNL Walmart Marketplace] beställningar, karta Walmart rekommenderade fraktföretag till motsvarande fraktfirma i [!DNL Commerce] så att leveransdata kan synkroniseras mellan [!DNL Walmart] och [!DNL Commerce].

Commerce-transportföretag som inte mappar till en föredragen leverantör är märkta som *[!UICONTROL Other Carrier]* på [!DNL Walmart].

**Förutsättningar**

Granska [Krav för Walmart](walmart-requirements.md) för [!DNL Marketplace Seller account].

## Uppdatera anslutningsautentiseringsuppgifter

1. På [!UICONTROL Listings] sidan för säljkanalsbutiken, välj **[!UICONTROL Channel Settings]**.

1. På **[!UICONTROL Channel Settings]**, markera **[!UICONTROL Walmart Connection]**.

1. Om du vill ändra autentiseringsuppgifterna väljer du **[!UICONTROL Change Credentials]**

   ![Uppdatera Walmart API-autentiseringsuppgifter för att auktorisera anslutningen](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. Ange **[!UICONTROL Walmart Client ID]** och **[!UICONTROL Walmart Client Secret]**.

1. Välj **[!UICONTROL Save]** för att tillämpa konfigurationen.
