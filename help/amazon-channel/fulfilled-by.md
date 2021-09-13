---
title: Fullgjord av
description: Använd inställningarna för Fulifyllt av för att bestämma hur beställningarna från Amazon-listorna uppfylls (skickas).
redirect_from: /sales-channels/asc/ob-fulfilled-by.html: 
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 618
ht-degree: 0%

---

# Fullgjord av

_[!UICONTROL Fulfilled By]_-inställningarna ingår i inställningarna för din butikslista. Du kommer åt listinställningarna från [butiksdashboard](./amazon-store-dashboard.md).

Dessa inställningar definierar den part som slutför (eller levererar) beställningar. Om alla dina beställningar har utförts på ett och samma sätt kan du välja mellan handlare (du) eller Amazon. Om du planerar att utföra beställningar från olika platser och använda Amazon är det bäst att använda det tredje alternativet och konfigurera ett [!DNL Commerce]-produktattribut.

- **[!UICONTROL Fulfilled by Merchant]** - Välj om du, handlaren, ska utföra alla order. När en order placeras dras lagret från din [!DNL Commerce]-katalog.

- **[!UICONTROL Fulfilled by Amazon]** - Välj om Amazon uppfyller alla beställningar. Med det här alternativet dras produktlager inte av från din [!DNL Commerce]-katalog när en beställning görs. Lager för Amazon levererade order lagras och dras av från lagerställena. Innan du tilldelar det här alternativet måste du verifiera i ditt [!DNL Amazon Seller Central]-konto att dina produkter är berättigade till _Fulfilled By Amazon_ (FBA). FBA-inventering hanteras direkt via ditt [!DNL Amazon Seller Central]-konto. Med den här leveransmetoden delar inte Amazon försäljningskanal kvantitetsuppdateringar mellan [!DNL Commerce] och Amazon. Därför är inte alla marknadsföringsverktyg som beskrivs i Kvantitetsinställningarna tillgängliga i Amazon försäljningskanal.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Om dina produkter kan uppfyllas av dig och Amazon kan du skapa ett  [!DNL Commerce] produktattribut med värden för Fulfill By Merchant och Fulfill by Amazon. Om du anger det här värdet per produkt visas vem som slutför beställningarna.

Fulfillment-metoden är ett regionalt attribut och baseras på inställningen **[!UICONTROL Amazon Marketplace Country]** som definierats under [butiksintegrering](./store-integration.md). När en ändring görs påverkar ändringen alla Amazon-listor som delar [!DNL Amazon Seller SKU] i Amazon butiker som säljer i samma region (enligt definitionen i _[!UICONTROL Amazon Marketplace Country]_under [butiksintegrering](./store-integration.md)). En ändring av en delad [!DNL Amazon Seller SKU] i USA påverkar inte dina Amazon-arkiv som är inställda för en annan region (som definieras under butiksintegreringen).

>[!NOTE]
>
>När en beställning har slutförts av Amazon (FBA) och beställningen har importerats, kan du visa exempeldata för vissa fält i beställningsinformationen. Se [Amazon orderinformation](./amazon-order-details.md).

## Konfigurera [!UICONTROL Fulfilled By]-inställningarna {#configure-fulfilled-by-settings}

1. Klicka på **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet _[!UICONTROL Fulfilled By]_.

1. För **[!UICONTROL Product Fulfilled By]** väljer du vem som uppfyller (levererar) ordern:

   - `Fulfilled by Merchant` - Merchant slutför order.

   - `Fulfilled by Amazon` - Amazon lagerställe slutför beställningen.

   - `Assign Fulfilled By Using Magento Product Attribute` - Ett  [!DNL Commerce] attribut anger vem som slutför beställningen per produkt.

      Om du väljer det här alternativet väljer du det [!DNL Commerce]-attribut som du vill mappa i **[!UICONTROL Fulfilled by Attribute]**.

1. Klicka på **[!UICONTROL Save listing settings]** när du är klar.

![Inställningarna Fulifyllda](assets/amazon-fulfilled-by.png)

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Product Fulfilled By] | Alternativ:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Välj om du har slutfört beställningarna. När en order placeras dras lagret från din [!DNL Commerce]-katalog. När en ny produkt skapas tilldelas leveransmetoden för Merchant Fulfill.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Välj om Amazon uppfyller beställningarna. Med den här leveransmetoden dras produktlager inte av från din [!DNL Commerce]-katalog när en beställning görs. När en produkt skapas skapas den med _[!UICONTROL Fulfilled by Amazon (FBA)]_som hämtningstyp. Se till att dina produkter är berättigade till FBA-leverans inom ditt [!DNL Amazon Seller Central]-konto. FBA-inventering hanteras även direkt via ditt [!DNL Amazon Seller Central]-konto. Med den här leveransmetoden skickas inte kvantitetsuppdateringar ut i förhållande till din [!DNL Commerce]-katalog, så du kan inte använda några av de marknadsföringsverktyg som beskrivs i [Inställningar för Stock/Kvantitet](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Välj om du har ett befintligt  [!DNL Commerce] attribut som avgör om det uppfylls av handlaren eller uppfylls av Amazon. När **[!UICONTROL Fulfilled by Attribute]** är valt aktiveras det.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Välj det [!DNL Commerce]-attribut som används för att bestämma leveransmetoden.<br><br>Om attributet till exempel är  _Fulfilled_ Byte och du väljer attributvärdet som  _[!UICONTROL Fulfilled By Merchant]_eller_[!UICONTROL Fulfilled By Amazon (FBA)]_ använder systemet det värdet som hämtningstyp för en ny produkt. Som handlare bör du se till att dina produkter är berättigade till FBA-leverans inom ditt [!DNL Amazon Seller Central]-konto. FBA-inventering hanteras även direkt via ditt Amazon-säljarkonto.<br><br>Alternativen beror på vilka attribut du har konfigurerat för dina Amazon-produkter. |

**Snabb åtkomst**  -  [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
