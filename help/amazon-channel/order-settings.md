---
title: Orderinställningar
description: Använd orderinställningarna för att bestämma hur Amazon-beställningar importeras till och bearbetas i din Commerce Store.
redirect_from: /sales-channels/asc/ob-order-settings.html: 
exl-id: dc8d0ce1-86a8-4949-b49a-73c5cf62db16
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 1462
ht-degree: 0%

---

# Orderinställningar

Orderinställningarna definierar om och hur Amazon-beställningar importeras till och bearbetas i [!DNL Commerce] och kan nås på [butikspanelen](./amazon-store-dashboard.md).

Inställningarna för orderimport är inställda på `Enabled` som standard, vilket innebär att dina Amazon-beställningar visas på butikens kontrollpanel och att motsvarande [!DNL Commerce]-beställningar skapas. Importerade order kan hanteras i arbetsflödet [!DNL Commerce] [Beställningar](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.

>[!NOTE]
>
>Oberoende av orderinställningar importeras inte Amazon-beställningar som fanns före butiksintegreringen.

När [butiksintegreringen](./store-integration.md) är klar kan du ändra orderinställningarna. Om du anger orderinställningarna till `Disabled` visas Amazon-beställningar på butikens kontrollpanel, men de måste hanteras i ditt [!DNL Amazon Seller Central]-konto.

När en order skapas på Amazon importeras den inte direkt till [!DNL Commerce]. Amazon tilldelar status `Pending` till nya order. När Amazon har verifierat ordern och betalningsmetoden ändras orderns status till `Unshipped`. Den här statusändringen utlöser orderimporten och [!DNL Commerce] skapar en matchande, motsvarande ordning.

Order som importerats från Amazon kan hanteras i [!DNL Commerce] [orderarbetsflödet](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Se även [Hantera beställningar](./managing-orders.md).

## Konfigurera orderinställningar {#configure-order-settings}

1. Klicka på **[!UICONTROL Order Settings]** på butikens kontrollpanel.

1. Välj ett alternativ för **[!UICONTROL Import Amazon Orders]** (obligatoriskt):

   - `Disabled` - Välj när du inte vill skapa motsvarande order i  [!DNL Commerce] när nya order tas emot från Amazon. När du väljer det här alternativet inaktiveras alla andra fält på den här sidan.

   - `Enabled` - (Standard) Välj när du vill skapa motsvarande  [!DNL Commerce] order när nya order tas emot från Amazon. [!DNL Commerce] beställningar skapas baserat på Amazon status och lagernivåer.

      >[!NOTE]
      >
      >Importera Amazon-order måste vara inställt på `Enabled` för att hantera Amazon-order i arbetsflödet [!DNL Commerce] [order](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Om `Disabled` anges har dina Amazon-beställningar inget motsvarande [!DNL Commerce]-ordernummer och kan inte hanteras i [!DNL Commerce]. Du hanterar de här beställningarna i ditt [!DNL Amazon Seller Central]-konto.

1. För **[!UICONTROL Import Amazon Orders Into Magento Store]** väljer du vilket [!DNL Commerce]-arkiv som Amazon-beställningarna är kopplade till när motsvarande order skapas i [!DNL Commerce].

   Den här inställningen är som standard Store-vyn för den webbplats som du valde när du [lade till Amazon store](./store-integration.md). Om du vill ändra den här inställningen beror listan med alternativ på de [!DNL Commerce]-butiker som du har konfigurerat i konfigurationen. Se [Lagrar](https://docs.magento.com/user-guide/stores/stores-all-create-view.html#create-a-new-store-view){:target=&quot;_blank&quot;}.

1. Välj ett alternativ för **[!UICONTROL Customer Creation]**:

   - `No Customer Creation (guest)` - (Standard) Välj när du inte vill skapa ett kundkonto genom att  [!DNL Commerce] använda importerade kunddata från Amazon-beställningen. När du väljer [!DNL Commerce] bearbetas en importerad Amazon-order på samma sätt som en gästutcheckning i [!DNL Commerce].

   - `Build New Customer Account` - Välj när du vill skapa ett nytt kundkonto genom att  [!DNL Commerce] använda kunddata som importerats med Amazon-beställningen. Det här alternativet hjälper er att bygga kunddatabaser utifrån era Amazon-beställningar.

1. Välj ett alternativ för **[!UICONTROL Order Number Source]**:

   - `Build Using Magento Order Number` - (Standard) Välj när du vill skapa ett unikt  [!DNL Commerce] ordernummer för motsvarande Amazon-order med det  [!DNL Commerce] stegvis tilldelade order-ID:t.

   - `Build Using Amazon Order Number` - Välj när du vill skapa  [!DNL Commerce] ordernumret med hjälp av motsvarande ordernummer som tilldelats av Amazon.
   >[!NOTE]
   >
   >När en order har importerats visas Amazon ordernummer i listan _[!UICONTROL Recent Orders]_på butikens kontrollpanel. Ordernumret [!DNL Commerce] visas när du visar orderinformationen på arbetsytan [!DNL Commerce] [Beställningar](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.

1. Välj ett alternativ för **[!UICONTROL Order Status]** (obligatoriskt):

   - `Default Order Status` - (Standard) Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas din definierade standardorderstatus för nya order. Standardstatusen för nya order (om du inte har skapat en anpassad orderstatus för nya order) är `Pending`. Se [Bearbetningsorder](https://docs.magento.com/user-guide/sales/order-processing.html){:target=&quot;_blank&quot;}.

   - `Custom Order Status` - Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas en annan status än standardinställningen.

   - `Processing Order Status` - Aktiveras när  **[!UICONTROL Order Status]** är inställt på  `Custom Order Status`. Välj den status du vill använda för nya order som importeras från Amazon. Alternativen i det här fältet baseras på standardstatusalternativen i [!DNL Commerce]. Se [Beställningsstatus](https://docs.magento.com/user-guide/sales/order-status.html). Du kan också skapa en anpassad orderstatus som visas här för val. Mer information om hur du skapar en anpassad orderstatus finns i [Anpassad orderstatus](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}.

1. Klicka på **[!UICONTROL Save order settings]** när du är klar.

![Orderinställningar](assets/amazon-order-settings.png)

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Import Amazon Orders] | Alternativ:<ul><li>**[!UICONTROL Disabled]** - Välj när du inte vill skapa motsvarande order i  [!DNL Commerce] när nya order tas emot från Amazon. När du väljer det här alternativet inaktiveras alla andra fält på den här sidan.</li><li>**[!UICONTROL Enabled]** - (Standard) Välj när du vill skapa motsvarande  [!DNL Commerce] order när nya order tas emot från Amazon. [!DNL Commerce] beställningar skapas baserat på Amazon status och lagernivåer.</li></ul><br><br>`Enabled` måste väljas för att hantera Amazon-beställningar i  [!DNL Commerce]. När du väljer `Disabled` visas dina Amazon-beställningar på butikens kontrollpanel, men beställningarna måste hanteras i ditt [!DNL Amazon Seller Central]-konto. |
| [!UICONTROL Import Amazon Orders Into Magento Store] | Välj vilket [!DNL Commerce]-arkiv som Amazon-beställningarna är kopplade till när de skapas i arbetsytan [!DNL Commerce] [Beställningar](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}. Den här inställningen är som standard Store-vyn för den [!DNL Commerce]-webbplats som du valde när du [lade till Amazon store](./store-integration.md). Om du vill ändra den här inställningen beror listan med alternativ på de [!DNL Commerce]-butiker som du har konfigurerat i konfigurationen. Se [Lagrar](https://docs.magento.com/user-guide/stores/stores-all-stores.html){:target=&quot;_blank&quot;}. |
| [!UICONTROL Customer Creation] | Alternativ:<ul><li>**[!UICONTROL No Customer Creation (guest)]** - (Standard) Välj när du inte vill skapa ett kundkonto genom att  [!DNL Commerce] använda importerade kunddata från Amazon-beställningen. När du väljer det här alternativet anger du att [!DNL Commerce] ska bearbeta en importerad Amazon-order på samma sätt som en gästutcheckning.</li><li>**[!UICONTROL Build New Customer Account]** - Välj när du vill skapa ett nytt kundkonto i din  [!DNL Commerce] kunddatabas med hjälp av kunddata som importerats med Amazon-beställningen. Med det här alternativet kan du skapa din [!DNL Commerce] kunddatabas utifrån dina Amazon-beställningar.</li></ul> |
| Källa för ordernummer | Alternativ:<ul><li>**[!UICONTROL Build Using Magento Order Number]** - (Standard) Välj när du vill skapa ett unikt  [!DNL Commerce] ordernummer för motsvarande Amazon-order med det  [!DNL Commerce] stegvis tilldelade order-ID:t. </li><li>**Bygg med Amazon ordernummer**  - Välj när du vill skapa  [!DNL Commerce] ordernumret med motsvarande ordernummer som tilldelats av Amazon.</li></ul> |
| Väntande order | Alternativ:<ul><li>**[!UICONTROL Do Not Reserve Quantity]** - Välj när du inte vill att din  [!DNL Commerce] lagerkvantitet ska påverkas av dina Amazon-beställningar. Välj om du vill använda Amazon för din leveransprocess (FBA). När det här alternativet väljs och du får en Amazon-beställning, påverkar den beställda kvantiteten inte din [!DNL Commerce]-lagerkvantitet.</li><li>**[!UICONTROL Reserve Quantity]** - Välj när du vill att orderkvantiteten i Amazon-ordern ska &quot;reserveras&quot; i din  [!DNL Commerce] lagerkvantitet. När du väljer och får en Amazon-beställning kommer den beställda kvantiteten att &quot;reservera&quot; i din [!DNL Commerce]-lagerkvantitet för att förhindra att ditt [!DNL Commerce]-lager &quot;översäljer&quot;. Den reserverade kvantiteten kan inte köpas via din [!DNL Commerce]-butik.</li></ul> |
| [!UICONTROL Order Status] | Alternativ:<ul><li>**[!UICONTROL Default Order Status]** - (Standard) Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas standardorderstatus för nya order. Standardstatusen för nya order (om du inte har skapat en anpassad orderstatus för nya order) är `Pending`. Se [Bearbetningsorder](https://docs.magento.com/user-guide/sales/order-processing.html).</li><li>>**[!UICONTROL Custom Order Status]** - Välj när du vill att nyligen skapade order som importerats från Amazon ska tilldelas en annan status än standardvärdet. När du väljer **[!UICONTROL Processing Order Status]** kan du välja vilken status du vill använda för nya order som importeras från Amazon.</li></ul> |
| [!UICONTROL Processing Orders Status] | Aktiveras när _[!UICONTROL Order Status]_är `Custom Order Status`. Välj den orderstatus som du vill tilldela nya order. Alternativen i det här fältet beror på standardstatusalternativen i [!DNL Commerce]. Se [Beställningsstatus](https://docs.magento.com/user-guide/sales/order-status.html){:target=&quot;_blank&quot;}. Du kan också skapa en anpassad orderstatus som visas här. Mer information om hur du skapar en anpassad orderstatus finns i [Anpassad orderstatus](https://docs.magento.com/user-guide/sales/order-status-custom.html){:target=&quot;_blank&quot;}. |

## [!DNL Commerce] orderskapande

[!DNL Commerce] order skapas för Amazon-order baserat på följande status och lagervillkor.

### Skapa order med lagerhantering

>[!NOTE]
>
>Stöds endast i integreringar med Adobe Commerce och Magento Open Source 2.3.x.

| Fulfillment Channel | [!DNL Commerce] Lagerstatus | Amazon orderstatus | [!UICONTROL Create Magento Order] Inställning | Reserverat lager |
|---|---|---|---|---|
| FBA | Inbyggd<br>Utanför lager<br>Hantera inte | Väntande | Nej | Nej |
| FBA | Inbyggd<br>Utanför lager<br>Hantera inte | PendingAvailability | Nej | Nej |
| FBA | Inbyggd<br>Utanför lager<br>Hantera inte | Avbruten | Nej | Nej |
| FBA | Inbyggd<br>Utanför lager<br>Hantera inte | Fel | Nej | Nej |
| FBA | Inbyggd<br>Utanför lager<br>Hantera inte | Olevererad | Nej | Nej |
| FBA | Inbyggd<br>Utanför lager<br>Hantera inte | DelvisLevererad | Nej | Nej |
| FBA | I lager<br>Hantera inte | Levererat | Ja | Nej |
| FBA | Utanför lager | Levererat | Nej | Nej |
| FBM | Inbyggd<br>Utanför lager<br>Hantera inte | Väntande | Nej | Nej |
| FBM | Inbyggd<br>Utanför lager<br>Hantera inte | PendingAvailability | Nej | Nej |
| FBM | Inbyggd<br>Utanför lager<br>Hantera inte | Avbruten | Nej | Nej |
| FBM | Inbyggd<br>Utanför lager<br>Hantera inte | Fel | Nej | Nej |
| FBM | I lager<br>Hantera inte | Olevererad | Ja | Ja |
| FBM | Utanför lager | Olevererad | Nej | Nej |
| FBM | I lager<br>Hantera inte | DelvisLevererad | Ja | Ja |
| FBM | Utanför lager | DelvisLevererad | Nej | Nej |
| FBM | I lager<br>Hantera inte | Levererat | Ja | Ja |
| FBM | Utanför lager | Levererat | Nej | Nej |

>[!NOTE]
>Om en Amazon-order importeras med statusen `Partially Shipped` eller `Shipped` är lagerreservationen som skapas för alla artiklar i ordern. Amazon försäljningskanal kompenserar inte för artiklar som tidigare har levererats.
>
>Om en order har fyllts i av Amazon (FBA) men ett objekt har `out of stock`-status, kan [!DNL Commerce] inte skapa en motsvarande order. Detta är en begränsning av integreringar av inventeringshantering.
