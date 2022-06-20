---
title: Hantera Walmart Marketplace-anslutning
description: Uppdatera API-autentiseringsuppgifterna för att auktorisera anslutningen mellan en [DNL! Commerce]-butiksvyn och [!DNL Walmart Marketplace]. Anslutningen krävs för att ansluta Commerce-produktlistor och synkronisera lager-, pris-, order- och leveransdata mellan Commerce och Walmart.
source-git-commit: 97128dcf45d7672e958c771f88389aba40c6e39e
workflow-type: tm+mt
source-wordcount: '126'
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
