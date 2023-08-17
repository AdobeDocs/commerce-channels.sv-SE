---
title: Hantera Amazon-beställningar
description: Du kan aktivera orderimport i dina orderinställningar för att enklare hantera dina Amazon-beställningar från din Commerce Admin.
feature: Sales Channels, Orders
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Hantera Amazon-beställningar

Du kan se din beställningsinformation från Amazon i _[!UICONTROL Recent Orders]_i [instrumentpanel för butik](./amazon-store-dashboard.md) eller på_[!UICONTROL Amazon orders]_ (kallas även _[!UICONTROL All Orders]_vy).

Hur du hanterar dina Amazon-beställningar beror på om orderimporten är aktiverad eller inaktiverad i [Orderinställningar](./order-settings.md#configure-order-settings).

## Med orderimport aktiverad

Efter [butiksintegrering](./store-integration.md), [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) inställningen är `Enabled` som standard. Med den här inställningen motsvarar [!DNL Commerce] beställningar skapas för dina Amazon-beställningar och kan hanteras i [[!DNL Commerce] Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) arbetsflöde.

>[!NOTE]
>
>Oberoende av inställningarna för orderimport beställer Amazon som fanns i [!DNL Amazon Seller Central] kontot före [butiksintegrering](./store-integration.md) importeras inte.

Importerade Amazon-beställningar hanteras i [[!DNL Commerce] Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) arbetsflöde, precis som ditt andra [!DNL Commerce] butiker. Klicka på Amazon ordernummer i dialogrutan *[!UICONTROL Order Number]* kolumn för att öppna ordningen i [[!DNL Commerce] orderprocess](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). Se [Visa Amazon-beställningar](./amazon-orders-all.md).

### Beställningsimportprocess

När en beställning görs på Amazon och [beställ import](./order-settings.md) är aktiverat startar följande process.

| Ändra | Åtgärder |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En beställning görs på Amazon. | <ul><li>Amazon anger orderstatus till `Pending`.</li><li>Orderinformation skickas till [!DNL Commerce].</li><li>Ordern läggs till i [_Amazon beställningar_ table](./amazon-orders-all.md) med `Pending` status.</li></ul> |
| Amazon ändrar orderstatus till `Unshipped`. | <ul><li>Statusändringen skickas till [!DNL Commerce].</li><li>I [_Amazon beställningar_ table](./amazon-orders-all.md), ändras orderstatusen till `Unshipped`.</li><li>I [[!DNL Commerce] orderarbetsflöde](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), en motsvarande [!DNL Commerce] order skapas med `Processing` status.</li></ul> |
| I [[!DNL Commerce] orderarbetsflöde](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), [!DNL Commerce] ordern behandlas och statusen ändras till `Shipped`. | <ul><li>I [_Amazon beställningar_ table](./amazon-orders-all.md), ändras orderstatusen till `Shipped`.</li><li>Vid nästa kron-jobb ändras orderstatusen till `Complete` i [[!DNL Commerce] orderarbetsflöde](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### Orderspärrar

Det finns några scenarier som förhindrar att motsvarande [!DNL Commerce] beställa. [!DNL Commerce] beställningar skapas inte för beställningar som tas emot när någon av följande utleveranser inträffar.

| Scenario | Lösning |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Objektet finns inte i [!DNL Commerce] katalog. | [Skapa produkten](./creating-assigning-catalog-products.md) i [!DNL Commerce] och [matcha manuellt](./creating-assigning-catalog-products.md) till produkten. |
| Objektet i katalogen är inaktiverat. | Se till att [produktstatus](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) är aktiverat. |
| Den beställda artikeln är inte i lager. | Uppdatera eller konfigurera [produktalternativ](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) för kvantitet och källa. |

När det inte går att importera beställningar visas ett systemmeddelande som liknar följande längst upp på skärmen:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

När problemet är löst kan du [!DNL Commerce] beställningen skapas vid nästa synkronisering.

## Beställningsimporten är inaktiverad

Om du inte vill importera och hantera dina Amazon-beställningar i [!DNL Commerce]kan du ändra [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) ange till `Disabled`. Den här inställningen innebär att när nya order tas emot från Amazon, motsvarar [!DNL Commerce] order skapas inte.

När det är inaktiverat visas orderinformation som tas emot från Amazon i dialogrutan _[!UICONTROL Recent Orders]_-avsnittet på kontrollpanelen för butiker och i_[!UICONTROL All Orders]_ vy. Orderinformationen är skrivskyddad och du måste hantera beställningarna i [!DNL Amazon Seller Central]. Så här öppnar du orderinformationen i [!DNL Amazon Seller Central]klickar du på Amazon ordernummer i dialogrutan _[!UICONTROL Order Number]_kolumn.

Se även [Visa Amazon-beställningar](./amazon-orders-all.md), [Se Amazon orderinformation](./amazon-order-details.md)och [Vanliga orderbearbetningsuppgifter](./common-order-processing.md).
