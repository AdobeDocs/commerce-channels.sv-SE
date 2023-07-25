---
title: Inställningarna för Amazon-listor har följts
description: Använd inställningarna för Fulifyllt av för att bestämma hur beställningarna från Amazon-listorna uppfylls (skickas).
feature: Sales Channels, Products
exl-id: 240c2198-e23d-40e7-be39-b9a4f78565d2
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Inställningarna för Amazon-listor har följts

_[!UICONTROL Fulfilled By]_-inställningarna ingår i inställningarna för din butikslista. Du kommer åt listinställningarna via [instrumentpanel för butik](./amazon-store-dashboard.md).

Dessa inställningar definierar den part som slutför (eller levererar) beställningar. Om alla dina beställningar har utförts på ett och samma sätt kan du välja mellan handlare (du) eller Amazon. Om du planerar att utföra beställningar från olika platser och använda Amazon är det bäst att använda det tredje alternativet och konfigurera en [!DNL Commerce] produktattribut.

- **[!UICONTROL Fulfilled by Merchant]** - Välj om du, handlaren, ska utföra alla order. När en order läggs dras lagret från [!DNL Commerce] katalog.

- **[!UICONTROL Fulfilled by Amazon]** - Välj om Amazon uppfyller alla beställningar. Med det här alternativet dras produktlager inte av från din [!DNL Commerce] katalog när en order placeras. Lager för Amazon levererade order lagras och dras av från lagerställena. Innan du tilldelar det här alternativet måste du verifiera [!DNL Amazon Seller Central] konto som dina produkter är berättigade till _Fullgjord av Amazon_ (FBA). FBA-inventering hanteras direkt via din [!DNL Amazon Seller Central] Konto. Med den här leveransmetoden delar inte Amazon försäljningskanal kvantitetsuppdateringar mellan [!DNL Commerce] och Amazon. Därför är inte alla marknadsföringsverktyg som beskrivs i Kvantitetsinställningarna tillgängliga i Amazon försäljningskanal.

- **[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Om dina produkter kan uppfyllas av dig och Amazon kan du skapa en [!DNL Commerce] product attribute with values for Fulfill By Merchant and Fulfill by Amazon. Om du anger det här värdet per produkt visas vem som slutför beställningarna.

Fullgörandemetoden är ett regionalt attribut och baseras på **[!UICONTROL Amazon Marketplace Country]** inställning definierad under [butiksintegrering](./store-integration.md). När en ändring görs påverkar ändringen alla Amazon-listor som delar den [!DNL Amazon Seller SKU] i Amazon butiker som säljer i samma region (enligt definition i _[!UICONTROL Amazon Marketplace Country]_under [butiksintegrering](./store-integration.md)). Ändra till en delad [!DNL Amazon Seller SKU] i USA påverkar inte dina Amazon-butiker som är inställda för en annan region (enligt definition under butiksintegreringen).

>[!NOTE]
>
>När en beställning har slutförts av Amazon (FBA) och beställningen har importerats, kan du visa exempeldata för vissa fält i beställningsinformationen. Se [Beställningsinformation för Amazon](./amazon-order-details.md).

## Konfigurera [!UICONTROL Fulfilled By] inställningar {#configure-fulfilled-by-settings}

1. Klicka **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera _[!UICONTROL Fulfilled By]_-avsnitt.

1. För **[!UICONTROL Product Fulfilled By]**, välja vem som ska utföra (leverera) beställningen:

   - `Fulfilled by Merchant` - Merchant slutför order.

   - `Fulfilled by Amazon` - Amazon lagerställe slutför beställningen.

   - `Assign Fulfilled By Using Magento Product Attribute` - A [!DNL Commerce] -attribut anger vem som slutför ordern per produkt.

     Välj [!DNL Commerce] attribut som du vill mappa in **[!UICONTROL Fulfilled by Attribute]**.

1. När du är klar klickar du på **[!UICONTROL Save listing settings]**.

![Inställningarna Fulifyllda](assets/amazon-fulfilled-by.png){width="500" zoomable="yes"}

| Fält | Beskrivning |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product Fulfilled By] | Alternativ:<ul><li>**[!UICONTROL Fulfilled by Merchant]** - (FBM) Välj om du har slutfört beställningarna. När en order läggs dras lagret från [!DNL Commerce] katalog. När en ny produkt skapas tilldelas leveransmetoden för Merchant Fulfill.</li><li>**[!UICONTROL Fulfilled by Amazon]** - (FBA) Välj om Amazon uppfyller beställningarna. Med den här leveransmetoden dras produktlager inte av från din [!DNL Commerce] katalog när en order placeras. När en produkt skapas skapas den med _[!UICONTROL Fulfilled by Amazon (FBA)]_som uppfyllandetyp. Se till att dina produkter är berättigade till FBA-leverans inifrån [!DNL Amazon Seller Central] konto. FBA-inventeringen hanteras också direkt via [!DNL Amazon Seller Central] konto. Med den här leveransmetoden skickas inte kvantitetsuppdateringar ut i förhållande till din [!DNL Commerce] så du inte kan använda några av de marknadsföringsverktyg som beskrivs i [Inställningar för lager/kvantitet](./stock-quantity.md).</li><li>**[!UICONTROL Assign Fulfilled By Using Magento Product Attribute]** - Välj om du har en befintlig [!DNL Commerce] som avgör om den uppfylls av handlaren eller uppfylls av Amazon. När du väljer **[!UICONTROL Fulfilled by Attribute]** aktiverar.</li></ul> |
| [!UICONTROL Fulfilled By Attribute] | Välj [!DNL Commerce] attribut som används för att fastställa leveransmetoden.<br><br>Om attributet till exempel är _Fullgjord av_ och du väljer attributvärdet som `Fulfilled By Merchant` eller `Fulfilled By Amazon (FBA)`används det värdet som hämtningstyp för en ny produkt. Som handlare bör du se till att dina produkter är berättigade till FBA-leveranser inom din [!DNL Amazon Seller Central] konto. FBA-inventering hanteras även direkt via ditt Amazon-säljarkonto.<br><br>Alternativen beror på vilka attribut du har konfigurerat för dina Amazon-produkter. |

**Snabb åtkomst** - [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
