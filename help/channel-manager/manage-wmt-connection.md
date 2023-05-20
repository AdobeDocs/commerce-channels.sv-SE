---
title: Hantera Walmart Marketplace-anslutning
description: '''Uppdatera API-autentiseringsuppgifterna för att auktorisera anslutningen mellan en [DNL! Commerce]-butiksvyn och [!DNL Walmart Marketplace]. The connection is required to connect [!DNL Commerce] produktlistor och synkronisera lager, pris, order och leveransdata mellan [!DNL Commerce] och Walmart.'
exl-id: 817b1b58-a57e-4c8d-b08f-1ce3bec15bc3
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Kartlägg transportföretag

Innan du [processorderförsändelser](process-orders.md#ship-an-order) for [!DNL Walmart Marketplace] beställningar, karta Walmart rekommenderade fraktföretag till motsvarande fraktfirma i [!DNL Commerce] så att leveransdata kan synkroniseras mellan [!DNL Walmart] och [!DNL Commerce].

Commerce-transportföretag som inte mappar till en föredragen leverantör är märkta som *[!UICONTROL Other Carrier]* på [!DNL Walmart].

**Förutsättningar**

Granska [Krav för Walmart](walmart-requirements.md) för [!DNL Marketplace Seller account].

## Uppdatera anslutningsreferenser

1. På [!UICONTROL Listings] sidan för säljkanalsbutiken, välj **[!UICONTROL Channel Settings]**.

1. På **[!UICONTROL Channel Settings]**, markera **[!UICONTROL Walmart Connection]**.

1. Om du vill ändra inloggningsuppgifterna väljer du **[!UICONTROL Change Credentials]**

   ![Uppdatera Walmart API-autentiseringsuppgifter för att auktorisera anslutningen](assets/update-connection-credentials.png)

1. Ange **[!UICONTROL Walmart Client ID]** och **[!UICONTROL Walmart Client Secret]**.

1. Välj **[!UICONTROL Save]** för att tillämpa konfigurationen.
