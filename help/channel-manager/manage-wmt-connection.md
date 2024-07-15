---
title: Hantera Walmart Marketplace-anslutning
description: 'Uppdatera API-autentiseringsuppgifterna för att auktorisera anslutningen mellan en [DNL! Commerce] butiksvy och  [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] produktlistor och synkronisera lager-, pris-, order- och leveransdata mellan [!DNL Commerce] och Walmart.'
role: Admin, Developer
feature: Sales Channels, Configuration, Shipping/Delivery, Integration
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Kartlägg transportföretag

Innan du [bearbetar orderleveranser](process-orders.md#ship-an-order) för [!DNL Walmart Marketplace] beställningar ska du mappa Walmart-prioriterade transportföretag till motsvarande transportföretag i [!DNL Commerce] så att leveransdata kan synkroniseras mellan [!DNL Walmart] och [!DNL Commerce].

Commerce-bärare som inte är mappade till en föredragen bärare får etiketten *[!UICONTROL Other Carrier]* på [!DNL Walmart].

**Förutsättningar**

Granska [Gå igenom kraven](walmart-requirements.md) för [!DNL Marketplace Seller account].

## Uppdatera anslutningsautentiseringsuppgifter

1. Välj **[!UICONTROL Channel Settings]** på sidan [!UICONTROL Listings] för säljkanalsbutiken.

1. På **[!UICONTROL Channel Settings]** väljer du **[!UICONTROL Walmart Connection]**.

1. Om du vill ändra autentiseringsuppgifterna väljer du **[!UICONTROL Change Credentials]**

   ![Uppdatera Walmart API-autentiseringsuppgifter för att auktorisera anslutningen](assets/update-connection-credentials.png){width="700" zoomable="yes"}

1. Ange **[!UICONTROL Walmart Client ID]** och **[!UICONTROL Walmart Client Secret]**.

1. Välj **[!UICONTROL Save]** om du vill använda konfigurationen.
