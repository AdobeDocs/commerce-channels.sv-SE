---
title: Orderinställningar
description: Använd orderinställningarna för att bestämma hur Amazon-beställningar importeras till och bearbetas i din Commerce Store.
redirect_from: /sales-channels/asc/ob-order-settings.html
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '1377'
ht-degree: 0%

---

# Orderinställningar

Orderinställningarna anger om och hur Amazon-beställningar ska importeras till och bearbetas i [!DNL Commerce] och kan öppnas på [instrumentpanel för butik](./amazon-store-dashboard.md).

Inställningarna för orderimport är inställda på `Enabled` som standard, vilket innebär att dina Amazon-beställningar visas på kontrollpanelen för butiker och skapar motsvarande [!DNL Commerce] beställningar. Importerade order kan hanteras i [!DNL Commerce] [Beställningar](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} arbetsflöde.

>[!NOTE]
>
>Oberoende av orderinställningar importeras inte Amazon-beställningar som fanns före butiksintegreringen.

Efter [butiksintegrering](./store-integration.md) är klart kan du ändra dina orderinställningar. Om du ställer in orderinställningarna på `Disabled`visas Amazon-beställningar på butikens kontrollpanel, men måste hanteras i [!DNL Amazon Seller Central] konto.

När en beställning skapas på Amazon importeras den inte direkt till [!DNL Commerce]. Amazon tilldelar en `Pending` status för nyligen skapade order. När Amazon har verifierat ordern och betalningsmetoden ändras orderns status till `Unshipped`. Den här statusändringen utlöser orderimporten och [!DNL Commerce] skapar en matchande, motsvarande ordning.

Beställningar som importeras från Amazon kan hanteras i [!DNL Commerce] [orderarbetsflöde](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"}. Se även [Hantera order](./managing-orders.md).

## Konfigurera orderinställningar {#configure-order-settings}

1. Klicka **[!UICONTROL Order Settings]** på butikens kontrollpanel.

1. För **[!UICONTROL Import Amazon Orders]** (obligatoriskt) väljer du ett alternativ:

   - `Disabled` - Välj när du inte vill skapa motsvarande order i [!DNL Commerce] när nya order tas emot från Amazon. När du väljer det här alternativet inaktiveras alla andra fält på den här sidan.

   - `Enabled` - (Standard) Välj när du vill skapa motsvarande [!DNL Commerce] beställningar när nya beställningar tas emot från Amazon. [!DNL Commerce] beställningar skapas baserat på Amazon status och lagernivåer.

      >[!NOTE]
      >
      >Importera Amazon-order måste anges till `Enabled` för att hantera Amazon-beställningar i [!DNL Commerce] [order](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} arbetsflöde. När inställt på `Disabled`har dina Amazon-beställningar inte motsvarande [!DNL Commerce] ordernummer och kan inte hanteras i [!DNL Commerce]. Du hanterar beställningarna i [!DNL Amazon Seller Central] konto.

1. För **[!UICONTROL Import Amazon Orders Into Magento Store]**, välja vilken [!DNL Commerce] lagra de Amazon-order som är kopplade till när motsvarande order skapas i [!DNL Commerce].

   Den här inställningen används som standard för butiksvyn för den webbplats som du valde när du [lade till Amazon Store](./store-integration.md). Om du vill ändra den här inställningen beror listan med alternativ på [!DNL Commerce] lagrar som du har konfigurerat i konfigurationen. Se [Lager](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){target="_blank"}.

1. För **[!UICONTROL Customer Creation]** väljer du ett alternativ:

   - `No Customer Creation (guest)` - (Standard) Välj när du inte vill skapa ett kundkonto i [!DNL Commerce] med importerade kunddata från Amazon-beställningen. När du väljer [!DNL Commerce] bearbetar en importerad Amazon-beställning på samma sätt som en gästutcheckning i [!DNL Commerce].

   - `Build New Customer Account` - Välj när du vill skapa ett nytt kundkonto i [!DNL Commerce] med kunddata som importerats med Amazon-beställningen. Det här alternativet hjälper er att bygga kunddatabaser utifrån era Amazon-beställningar.

1. För **[!UICONTROL Order Number Source]** väljer du ett alternativ:

   - `Build Using Magento Order Number` - (Standard) Välj när du vill skapa en unik [!DNL Commerce] ordernummer för motsvarande Amazon-order med [!DNL Commerce] inkrementellt tilldelat order-ID.

   - `Build Using Amazon Order Number` - Välj när du vill skapa [!DNL Commerce] ordernummer med motsvarande ordernummer som tilldelats av Amazon.
   >[!NOTE]
   >
   >När en beställning har importerats visas Amazon ordernummer i _[!UICONTROL Recent Orders]_-listan på butikspanelen. The [!DNL Commerce] ordernumret visas när beställningsinformationen visas i [!DNL Commerce] [Beställningar](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} arbetsyta.

1. För **[!UICONTROL Order Status]** (obligatoriskt) väljer du ett alternativ:

   - `Default Order Status` - (Standard) Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas din definierade standardorderstatus för nya order. Standardstatusen för nya order (såvida du inte har skapat en anpassad orderstatus för nya order) är `Pending`. Se [Bearbetar order](https://docs.magento.com/user-guide/sales/order-processing.html){target="_blank"}.

   - `Custom Order Status` - Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas en annan status än standardinställningen.

   - `Processing Order Status` - Aktiverad när **[!UICONTROL Order Status]** är inställd på `Custom Order Status`. Välj den status du vill använda för nya order som importeras från Amazon. Alternativen i det här fältet baseras på standardstatusalternativen i [!DNL Commerce]. Se [Orderstatus](https://docs.magento.com/user-guide/sales/order-status.html). Du kan också skapa en anpassad orderstatus som visas här för val. Information om hur du skapar en anpassad orderstatus finns i [Anpassad orderstatus](https://docs.magento.com/user-guide/sales/order-status-custom.html){target="_blank"}.

1. När du är klar klickar du på **[!UICONTROL Save order settings]**.

![Orderinställningar](assets/amazon-order-settings.png)

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Import Amazon Orders] | Alternativ:<ul><li>**[!UICONTROL Disabled]** - Välj när du inte vill skapa motsvarande order i [!DNL Commerce] när nya order tas emot från Amazon. När du väljer det här alternativet inaktiveras alla andra fält på den här sidan.</li><li>**[!UICONTROL Enabled]** - (Standard) Välj när du vill skapa motsvarande [!DNL Commerce] beställningar när nya beställningar tas emot från Amazon. [!DNL Commerce] beställningar skapas baserat på Amazon status och lagernivåer.</li></ul><br><br>`Enabled` måste väljas för att hantera Amazon-beställningar i [!DNL Commerce]. När `Disabled` väljs visas dina Amazon-beställningar på kontrollpanelen, men beställningarna måste hanteras i [!DNL Amazon Seller Central] konto. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Välj vilken [!DNL Commerce] lagra de Amazon-order som är kopplade till när de skapas i [!DNL Commerce] [Beställningar](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} workspace. This setting defaults to the Store View for the [!DNL Commerce] website selected when you [added the Amazon store](./store-integration.md). If you want to change this setting, the list of options depends on the [!DNL Commerce] stores you have set up in your configuration. See [Stores](https://docs.magento.com/user-guide/stores/stores-all-stores.html){target="_blank"}. |
| [!UICONTROL Customer Creation] | Alternativ:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Standard) Välj när du inte vill skapa ett kundkonto i [!DNL Commerce] med importerade kunddata från Amazon-beställningen. När det här alternativet väljs visas [!DNL Commerce] om du vill bearbeta en importerad Amazon-beställning på samma sätt som en gästutcheckning.</li><li>**[!UICONTROL Build New Customer Account]** - Välj när du vill skapa ett nytt kundkonto i ditt [!DNL Commerce] kunddatabas med kunddata som importerats med Amazon-beställningen. Det här alternativet hjälper dig att bygga [!DNL Commerce] kunddatabas från dina Amazon-beställningar.</li></ul> |
| Källa för ordernummer | Alternativ:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Standard) Välj när du vill skapa en unik [!DNL Commerce] ordernummer för motsvarande Amazon-order med [!DNL Commerce] inkrementellt tilldelat order-ID. </li><li>**Bygg med Amazon ordernummer** - Välj när du vill skapa [!DNL Commerce] ordernummer med motsvarande ordernummer som tilldelats av Amazon.</li></ul> |
| Väntande order | Alternativ:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Välj när du inte vill ha [!DNL Commerce] Lagerkvantitet som påverkas av dina Amazon-beställningar. Välj om du vill använda Amazon för din leveransprocess (FBA). När du väljer och får en Amazon-beställning påverkar beställningen inte din [!DNL Commerce] lagerkvantitet.</li><li>**[!UICONTROL Reserve Quantity]** - Välj när du vill att orderkvantiteten i Amazon-ordern ska &quot;reserveras&quot; i din [!DNL Commerce] lagerkvantitet. När du väljer att göra en Amazon-beställning kommer den beställda kvantiteten att &quot;reservera&quot; i din [!DNL Commerce] Lagerkvantitet för att förhindra [!DNL Commerce] aktie från&quot;over selling&quot;. Den reserverade kvantiteten kan inte köpas via din [!DNL Commerce] storefront.</li></ul> |
| [!UICONTROL Order Status] | Alternativ:<ul><li>**[!UICONTROL Default Order Status]** - (Standard) Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas standardorderstatus för nya order. Standardstatusen för nya order (såvida du inte har skapat en anpassad orderstatus för nya order) är `Pending`. Se [Bearbetar order](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]** - Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas en annan status än standardinställningen. När du väljer **[!UICONTROL Processing Order Status]** Med kan du välja vilken status du vill använda för nya order som importeras från Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Aktiverad när _[!UICONTROL Order Status]_är inställd på `Custom Order Status`. Välj den orderstatus som du vill tilldela nya order. Alternativen i det här fältet beror på standardstatusalternativen i [!DNL Commerce]. Se [Orderstatus](https://docs.magento.com/user-guide/sales/order-status.html){target="_blank"}. You can also create a custom order status to show here. To create a custom order status, see [Custom Order Status](https://docs.magento.com/user-guide/sales/order-status-custom.html){target="_blank"}. |

## [!DNL Commerce] orderskapande

[!DNL Commerce] order skapas för Amazon-order baserat på följande status och lagervillkor.

### Skapa order med Inventory management

>[!NOTE]
>
>Stöds endast i integreringar med Adobe Commerce och Magento Open Source 2.3.x.

| Fulfillment Channel | [!DNL Commerce] Lagerstatus | Amazon orderstatus | [!UICONTROL Create Magento Order] Inställning | Reserverat lager |
|---|---|---|---|---|
| FBA | I lager<br>Utanför lager<br>Hantera inte | Väntande | Nej | Nej |
| FBA | I lager<br>Utanför lager<br>Hantera inte | PendingAvailability | Nej | Nej |
| FBA | I lager<br>Utanför lager<br>Hantera inte | Avbruten | Nej | Nej |
| FBA | I lager<br>Utanför lager<br>Hantera inte | Fel | Nej | Nej |
| FBA | I lager<br>Utanför lager<br>Hantera inte | Olevererad | Nej | Nej |
| FBA | I lager<br>Utanför lager<br>Hantera inte | DelvisLevererad | Nej | Nej |
| FBA | I lager<br>Hantera inte | Levererat | Ja | Nej |
| FBA | Utanför lager | Levererat | Nej | Nej |
| FBM | I lager<br>Utanför lager<br>Hantera inte | Väntande | Nej | Nej |
| FBM | I lager<br>Utanför lager<br>Hantera inte | PendingAvailability | Nej | Nej |
| FBM | I lager<br>Utanför lager<br>Hantera inte | Avbruten | Nej | Nej |
| FBM | I lager<br>Utanför lager<br>Hantera inte | Fel | Nej | Nej |
| FBM | I lager<br>Hantera inte | Olevererad | Ja | Ja |
| FBM | Utanför lager | Olevererad | Nej | Nej |
| FBM | I lager<br>Hantera inte | DelvisLevererad | Ja | Ja |
| FBM | Utanför lager | DelvisLevererad | Nej | Nej |
| FBM | I lager<br>Hantera inte | Levererat | Ja | Ja |
| FBM | Utanför lager | Levererat | Nej | Nej |

>[!NOTE]
>Om en Amazon-beställning importeras i en `Partially Shipped` eller `Shipped` status, lagerreservationen som skapas är för alla artiklar i ordern. Amazon försäljningskanal kompenserar inte för artiklar som tidigare har levererats.
>
>Om en beställning har fyllts i av Amazon (FBA) men ett objekt finns i `out of stock` status, [!DNL Commerce] kan inte skapa en motsvarande order. Detta är en begränsning av Inventory management integreringar.
