---
title: Kartlägg transportföretag
description: 'Mappningsattribut för matchning av [DNL! Commerce]-produkter till befintliga [!DNL Walmart Marketplace] listor och synkroniserar data mellan [!DNL Channel Manager] och [!DNL Walmart].'
role: Admin
feature: Sales Channels, Configuration, Shipping/Delivery
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: 4670e9b25a840f86862c9cadaf9e6d3e70330b7d
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Kartlägg transportföretag

Innan du [bearbetar orderleveranser](process-orders.md#ship-an-order) för [!DNL Walmart Marketplace] beställningar ska du mappa Walmart-prioriterade transportföretag till motsvarande transportföretag i [!DNL Commerce] så att leveransdata kan synkroniseras mellan [!DNL Walmart] och [!DNL Commerce].

Commerce-bärare som inte är mappade till en föredragen bärare får etiketten *[!UICONTROL Other Carrier]* på [!DNL Walmart].

**Förutsättningar**

Utför följande uppgifter innan du kartlägger transportföretag:

1. Granska [transportföretagets metoder och Bästa praxis för leverans vid tidpunkt](https://sellerhelp.walmart.com/s/guide?article=000009473) för [!DNL Walmart Marketplace].

1. Verifiera konfigurationen för [[!UICONTROL Shipping Carrier]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/delivery/shipping-carriers/carriers.html) och [[!UICONTROL Shipping Settings]](https://experienceleague.adobe.com/docs/commerce-admin/config/sales/shipping-settings.html) i [!DNL Commerce]-arkivet för att kontrollera att du har optimerat konfigurationen för [!DNL Walmart Marketplace sales].

## Kartlägg transportföretag

1. Välj **[!UICONTROL Channel Settings]** på sidan **[!UICONTROL Listings]** eller **[!UICONTROL Orders]**.

1. På **[!UICONTROL Channel Settings]** väljer du **[!UICONTROL Shipping Carriers]**.

   ![Mappa transportföretag](assets/map-shipping-carriers.png){width="600" zoomable="yes"}

1. För varje [!DNL Walmart] önskad transportör som visas väljer du namnet [!DNL Commerce] i listrutan om transportören är tillgänglig.

1. Välj **[!UICONTROL Save]** om du vill använda konfigurationen.

