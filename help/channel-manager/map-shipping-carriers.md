---
title: Kartlägg transportföretag
description: Mappningsattribut för matchning av [DNL! Commerce]-produkter till befintlig [!DNL Walmart Marketplace] listor och synkronisera data mellan [!DNL Channel Manager] och [!DNL Walmart].
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: aff38e59771fb973b789450b1a7b9552a7a809ff
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Kartlägg transportföretag

Innan du [processorderförsändelser](process-orders.md#ship-an-order) for [!DNL Walmart Marketplace] beställningar, karta Walmart rekommenderade fraktföretag till motsvarande fraktfirma i [!DNL Commerce] så att leveransdata kan synkroniseras mellan [!DNL Walmart] och [!DNL Commerce].

Commerce-transportföretag som inte mappar till en föredragen leverantör är märkta som *[!UICONTROL Other Carrier]* på Walmart.

**Förutsättningar**

Utför följande uppgifter innan du mappar transportföretag:

1. Granska [Bärarmetoder och bästa leveransmetoder för leverans i tid](https://sellerhelp.walmart.com/s/guide?article=000009473) för Walmart Marketplace.

1. Verifiera [[!UICONTROL Shipping Carrier]](https://docs.magento.com/user-guide/shipping/carriers.html) och [!UICONTROL Shipping Settings] i din [!DNL Commerce] lagra för att säkerställa att du har optimerat konfigurationen för [!DNL Walmart Marketplace sales].

## Kartlägg transportföretag

1. På [!UICONTROL Listings] sidan för säljkanalsbutiken, välj **[!UICONTROL Settings]**.

1. Från **[!UICONTROL Map Attributes]**, markera **[!UICONTROL Shipping Carriers]**.

   ![Kartlägg transportföretag](assets/map-shipping-carriers.png)

1. För varje [!DNL Walmart] önskad leverantör visas. Välj [!DNL Commerce] transportföretagets namn i listrutan om transportföretaget är tillgängligt.

1. Välj **[!UICONTROL Save]** för att tillämpa konfigurationen.
