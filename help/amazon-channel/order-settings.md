---
title: Amazon orderinställningar
description: Använd orderinställningarna för att ange hur Amazon-beställningar ska importeras till och bearbetas i din Commerce-butik.
feature: Sales Channels, Orders, Inventory, Configuration
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: a93ba31a95f32cc6ea285aed2399255021985693
workflow-type: tm+mt
source-wordcount: '1388'
ht-degree: 0%

---

# Amazon orderinställningar

Orderinställningarna definierar om och hur Amazon-beställningar importeras till och bearbetas i [!DNL Commerce] och kan nås på [butikens kontrollpanel](./amazon-store-dashboard.md).

Inställningarna för orderimport är inställda på `Enabled` som standard, vilket innebär att dina Amazon-beställningar visas på butikens kontrollpanel och att motsvarande [!DNL Commerce]-beställningar skapas. Importerade order kan hanteras i arbetsflödet [!DNL Commerce] [Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

>[!NOTE]
>
>Oberoende av orderinställningar importeras inte Amazon-beställningar som fanns före butiksintegreringen.

När [butiksintegreringen](./store-integration.md) är klar kan du ändra dina orderinställningar. Om du anger orderinställningarna till `Disabled` visas Amazon-beställningar på butikens kontrollpanel, men de måste hanteras i ditt [!DNL Amazon Seller Central]-konto.

När en order skapas på Amazon importeras den inte direkt till [!DNL Commerce]. Amazon tilldelar status `Pending` till nya order. När Amazon har verifierat ordern och betalningsmetoden ändras orderns status till `Unshipped`. Den här statusändringen utlöser orderimporten och [!DNL Commerce] skapar en matchande, motsvarande ordning.

Beställningar som importerats från Amazon kan hanteras i arbetsflödet [!DNL Commerce] [Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Se även [Hantera beställningar](./managing-orders.md).

## Konfigurera orderinställningar {#configure-order-settings}

1. Klicka på **[!UICONTROL Order Settings]** på butikens kontrollpanel.

1. Välj ett alternativ för **[!UICONTROL Import Amazon Orders]** (obligatoriskt):

   - `Disabled` - Välj när du inte vill skapa motsvarande order i [!DNL Commerce] när nya order tas emot från Amazon. När du väljer det här alternativet inaktiveras alla andra fält på den här sidan.

   - `Enabled` - (Standard) Välj när du vill skapa motsvarande [!DNL Commerce]-order när nya order tas emot från Amazon. [!DNL Commerce] order skapas baserat på Amazon status och lagernivåer.

     >[!NOTE]
     >
     >Importera Amazon-beställningar måste anges till `Enabled` för att hantera Amazon-beställningar i arbetsflödet [!DNL Commerce] [beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). Om du anger `Disabled` har dina Amazon-beställningar inget motsvarande [!DNL Commerce]-ordernummer och kan inte hanteras i [!DNL Commerce]. Du hanterar de här beställningarna i ditt [!DNL Amazon Seller Central]-konto.

1. För **[!UICONTROL Import Amazon Orders Into Magento Store]** väljer du vilket [!DNL Commerce]-arkiv som Amazon-beställningarna är kopplade till när motsvarande order skapas i [!DNL Commerce].

   Den här inställningen är som standard Store-vyn för webbplatsen som du valde när du [lade till Amazon Store](./store-integration.md). Om du vill ändra den här inställningen beror listan med alternativ på de [!DNL Commerce]-butiker som du har konfigurerat i konfigurationen. Se [Butiker](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html).

1. Välj ett alternativ för **[!UICONTROL Customer Creation]**:

   - `No Customer Creation (guest)` - (Standard) Välj när du inte vill skapa ett kundkonto i [!DNL Commerce] med importerade kunddata från Amazon-beställningen. När det här alternativet har valts bearbetar [!DNL Commerce] en importerad Amazon-ordning på samma sätt som en gästutcheckning i [!DNL Commerce] bearbetas.

   - `Build New Customer Account` - Välj när du vill skapa ett nytt kundkonto i [!DNL Commerce] med hjälp av kunddata som importerats med Amazon-beställningen. Det här alternativet hjälper er att bygga kunddatabaser utifrån era Amazon-beställningar.

1. Välj ett alternativ för **[!UICONTROL Order Number Source]**:

   - `Build Using Magento Order Number` - (Standard) Välj när du vill skapa ett unikt [!DNL Commerce]-ordernummer för motsvarande Amazon-order med hjälp av det [!DNL Commerce] stegvis tilldelade order-ID:t.

   - `Build Using Amazon Order Number` - Välj när du vill skapa ordernumret för [!DNL Commerce] med hjälp av motsvarande ordernummer som tilldelats av Amazon.

   >[!NOTE]
   >
   >När en order har importerats visas Amazon ordernummer i listan _[!UICONTROL Recent Orders]_på butikens kontrollpanel. Ordernumret [!DNL Commerce] visas när du visar orderinformationen på arbetsytan [!DNL Commerce] [Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

1. Välj ett alternativ för **[!UICONTROL Order Status]** (obligatoriskt):

   - `Default Order Status` - (Standard) Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas din definierade standardorderstatus för nya order. Standardstatus för nya order (om du inte har skapat en anpassad orderstatus för nya order) är `Pending`. Se [Bearbetar beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

   - `Custom Order Status` - Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas en annan status än standardvärdet.

   - `Processing Order Status` - Aktiveras när **[!UICONTROL Order Status]** är inställt på `Custom Order Status`. Välj den status du vill använda för nya order som importeras från Amazon. Alternativen i det här fältet baseras på standardstatusalternativen i [!DNL Commerce]. Se [Beställningsstatus](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Du kan också skapa en anpassad orderstatus som visas här för val. Mer information om hur du skapar en anpassad orderstatus finns i [Anpassad orderstatus](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html#custom-order-status).

1. Klicka på **[!UICONTROL Save order settings]** när du är klar.

![Beställningsinställningar](assets/amazon-order-settings.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | Alternativ:<ul><li>**[!UICONTROL Disabled]** - Välj när du inte vill skapa motsvarande order i [!DNL Commerce] när nya order tas emot från Amazon. När du väljer det här alternativet inaktiveras alla andra fält på den här sidan.</li><li>**[!UICONTROL Enabled]** - (Standard) Välj när du vill skapa motsvarande [!DNL Commerce]-order när nya order tas emot från Amazon. [!DNL Commerce] order skapas baserat på Amazon status och lagernivåer.</li></ul><br><br>`Enabled` måste väljas för att hantera Amazon-beställningar i [!DNL Commerce]. När `Disabled` har valts visas dina Amazon-beställningar på butikens kontrollpanel, men beställningarna måste hanteras på ditt [!DNL Amazon Seller Central]-konto. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Välj vilken [!DNL Commerce]-butik Amazon-beställningarna är kopplade till när de skapas på arbetsytan [!DNL Commerce] [Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) . Den här inställningen är som standard Store-vyn för webbplatsen [!DNL Commerce] som du valde när du [lade till Amazon Store](./store-integration.md). Om du vill ändra den här inställningen beror listan med alternativ på de [!DNL Commerce]-butiker som du har konfigurerat i konfigurationen. Se [Butiker](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/stores.html). |
| [!UICONTROL Customer Creation] | Alternativ:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Standard) Välj när du inte vill skapa ett kundkonto i [!DNL Commerce] med importerade kunddata från Amazon-beställningen. När du väljer det här alternativet instruerar [!DNL Commerce] att bearbeta en importerad Amazon-order på samma sätt som en gästutcheckning bearbetas.</li><li>**[!UICONTROL Build New Customer Account]** - Välj när du vill skapa ett nytt kundkonto i din [!DNL Commerce] kunddatabas med kunddata som importerats med Amazon-beställningen. Med det här alternativet kan du skapa din [!DNL Commerce]-kunddatabas utifrån dina Amazon-beställningar.</li></ul> |
| Beställningsnummer Source | Alternativ:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Standard) Välj när du vill skapa ett unikt [!DNL Commerce]-ordernummer för motsvarande Amazon-order med hjälp av det [!DNL Commerce] stegvis tilldelade order-ID:t. </li><li>**Bygg med Amazon-ordernummer** - Välj när du vill skapa [!DNL Commerce]-ordernumret med hjälp av motsvarande ordernummer som tilldelats av Amazon.</li></ul> |
| Väntande order | Alternativ:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Välj när du inte vill att din [!DNL Commerce]-lagerkvantitet ska påverkas av dina Amazon-beställningar. Välj om du vill använda Amazon för din leveransprocess (FBA). När det här alternativet väljs och du får en Amazon-beställning påverkar den beställda kvantiteten inte din [!DNL Commerce]-lagerkvantitet.</li><li>**[!UICONTROL Reserve Quantity]** - Välj när du vill att orderkvantiteten i Amazon-ordern ska &quot;reserveras&quot; i din [!DNL Commerce]-lagerkvantitet. När du väljer och får en Amazon-beställning kommer den beställda kvantiteten att &quot;reservera&quot; i din [!DNL Commerce]-lagerkvantitet för att förhindra att [!DNL Commerce]-aktien&quot;översäljer&quot;. Den reserverade kvantiteten kan inte köpas via din [!DNL Commerce]-butik.</li></ul> |
| [!UICONTROL Order Status] | Alternativ:<ul><li>**[!UICONTROL Default Order Status]** - (Standard) Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas standardorderstatus för nya order. Standardstatus för nya order (om du inte har skapat en anpassad orderstatus för nya order) är `Pending`. Se [Bearbetar beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).</li><li>**[!UICONTROL Custom Order Status]** - Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas en annan status än standardvärdet. När du väljer det här alternativet kan du välja vilken status du vill använda för nyligen skapade order som importerats från Amazon.**[!UICONTROL Processing Order Status]**</li></ul> |
| [!UICONTROL Processing Orders Status] | Aktiveras när _[!UICONTROL Order Status]_är inställd på `Custom Order Status`. Välj den orderstatus som du vill tilldela nya order. Alternativen i det här fältet beror på standardstatusalternativen i [!DNL Commerce]. Se [Beställningsstatus](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-status.html). Du kan också skapa en anpassad orderstatus som visas här. Mer information om hur du skapar en anpassad orderstatus finns i [Anpassad orderstatus] |

## [!DNL Commerce] orderskapande

[!DNL Commerce] order skapas för Amazon-order baserat på följande status och lagervillkor.

### Skapa order med Inventory management

>[!NOTE]
>
>Stöds endast i integreringar med Adobe Commerce och Magento Open Source 2.3.x.

| Fulfillment Channel | [!DNL Commerce] Lagerstatus | Beställningsstatus för Amazon | Inställning för [!UICONTROL Create Magento Order] | Reserverat lager |
|---------------------|-------------------------------------------|---------------------|-------------------------------------------|--------------------|
| FBA | Inaktuell<br>Inaktuell<br>Hantera inte | Väntande | Nej | Nej |
| FBA | Inaktuell<br>Inaktuell<br>Hantera inte | PendingAvailability | Nej | Nej |
| FBA | Inaktuell<br>Inaktuell<br>Hantera inte | Avbruten | Nej | Nej |
| FBA | Inaktuell<br>Inaktuell<br>Hantera inte | Fel | Nej | Nej |
| FBA | Inaktuell<br>Inaktuell<br>Hantera inte | Olevererad | Nej | Nej |
| FBA | Inaktuell<br>Inaktuell<br>Hantera inte | DelvisLevererad | Nej | Nej |
| FBA | Inbyggd<br>Hantera inte | Levererat | Ja | Nej |
| FBA | Utanför lager | Levererat | Nej | Nej |
| FBM | Inaktuell<br>Inaktuell<br>Hantera inte | Väntande | Nej | Nej |
| FBM | Inaktuell<br>Inaktuell<br>Hantera inte | PendingAvailability | Nej | Nej |
| FBM | Inaktuell<br>Inaktuell<br>Hantera inte | Avbruten | Nej | Nej |
| FBM | Inaktuell<br>Inaktuell<br>Hantera inte | Fel | Nej | Nej |
| FBM | Inbyggd<br>Hantera inte | Olevererad | Ja | Ja |
| FBM | Utanför lager | Olevererad | Nej | Nej |
| FBM | Inbyggd<br>Hantera inte | DelvisLevererad | Ja | Ja |
| FBM | Utanför lager | DelvisLevererad | Nej | Nej |
| FBM | Inbyggd<br>Hantera inte | Levererat | Ja | Ja |
| FBM | Utanför lager | Levererat | Nej | Nej |

>[!NOTE]
>Om en Amazon-order importeras med statusen `Partially Shipped` eller `Shipped` är lagerreservationen som skapas för alla artiklar i ordern. Amazon försäljningskanal kompenserar inte för artiklar som tidigare har levererats.
>
>Om en order har fyllts i av Amazon (FBA) men ett objekt har statusen `out of stock`, kan [!DNL Commerce] inte skapa en motsvarande order. Detta är en begränsning av Inventory management integreringar.
