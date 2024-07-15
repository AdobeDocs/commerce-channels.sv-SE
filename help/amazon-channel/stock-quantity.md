---
title: Amazon-Sales Channel - [!UICONTROL Stock/Quantity]
description: Uppdatera inställningarna för Stock/Kvantitet om du vill styra synkroniseringen av produktkvantitetsinformation från din Commerce-butik till ditt [!DNL Amazon Seller Central] konto.
feature: Sales Channels, Inventory
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# [!UICONTROL Stock/Quantity]

*[!UICONTROL Stock/Quantity]*-inställningarna ingår i inställningarna för din butikslista. Du kommer åt listinställningarna från [butiksinstrumentpanelen](./amazon-store-dashboard.md).

De här inställningarna används för att synkronisera produktkvantitetsinformationen från din [!DNL Commerce]-butik till kvantiteten på ditt [!DNL Amazon Seller Central]-konto. Det här verktyget är kraftfullt och kan användas för ytterligare annonsering genom att visa köparens snabbhet samtidigt som lagret hålls organiserat. En del handlare kan till exempel ha 150 artiklar av en viss SKU i lager och vill vara säkra på att Amazon kunder kan köpa hela sitt lager. Andra handlare kanske bara vill ta med ett objekt i taget för att skapa en känsla av brist för slutanvändaren. I det här fallet anger du *[!UICONTROL Maximum Listed Quantity]* till `1`.

Kvantitet är ett regionalt attribut och baseras på inställningen **[!UICONTROL Amazon Marketplace Country]** som definieras under [butiksintegrering](./store-integration.md). När en ändring görs av en produkts kvantitet påverkar ändringen alla Amazon-listor som delar [!DNL Amazon Seller SKU] i dina Amazon-butiker som säljer i samma land. En ändring av en delad [!DNL Amazon Seller SKU] i USA påverkar inte dina Amazon-butiker som konfigurerats för ett annat land. Din första Amazon-butik som är integrerad (med det äldsta skapandedatumet) styr prioriteten i kvantitetsinställningarna.

>[!NOTE]
>
>För användare av Adobe Commerce och Magento Open Source 2.3.x stöder Amazon försäljningskanal användning av Inventory management-tillägget utan ytterligare konfiguration. Se [Hantera lager](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){target="_blank"}.

## Konfigurera inställningar för lager/kvantitet {#configure-stock--quantity-settings}

1. Klicka på **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet **[!UICONTROL Stock / Quantity]**.

1. För **[!UICONTROL Out-of-Stock Threshold]** (obligatoriskt) anger du ett numeriskt värde för den lägsta kvantiteten av en produkt för att produkten ska kunna tas med i listan över Amazon-produkter.

   Standardvärdet är `0`. Om ditt [!DNL Commerce]-produktlager blir lägre än detta nummer är respektive Amazon-lista inte tillgänglig för försäljning via Amazon.

1. För **[!UICONTROL Maximum Listed Quantity]** (obligatoriskt) anger du ett numeriskt värde för den kvantitet som du vill visa i din Amazon-lista.

   Den här inställningen visar alla Amazon-listor som är berättigade till det angivna värdet. När en artikel säljs ändras inte Amazon listkvantitet. Den tillgängliga kvantiteten i listan använder alltid det här värdet, även när den faktiska produktkvantiteten är högre eller lägre. Den här inställningen används vanligtvis när du inte hanterar produktlager. Du kan till exempel ha en produkt med en kvantitet på 80 i din [!DNL Commerce]-katalog. Med inställningen `10` visar Amazon-listan alltid en tillgänglig kvantitet på `10` och ändras inte när produkten säljs.

1. För **[!UICONTROL "Do Not Manage Stock" Quantity]** (obligatoriskt) anger du ett kvantitetsvärde som ska visas för dina Amazon-listor.

   Amazon kräver att du publicerar en tillgänglig kvantitet. För [!DNL Commerce]-produkter som inte är inställda på att hantera lager men som du vill lista dem på Amazon, publiceras listan med tillgänglig kvantitet som anges här.

1. Klicka på **[!UICONTROL Save listing settings]** när du är klar.

![Inställningar för Stock/kvantitet](assets/amazon-stock-quantity.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Out-of-Stock Threshold] | Ange ett numeriskt värde för den lägsta kvantiteten av en produkt för att produkten ska kunna tas med i listan över Amazon (standardvärdet är `0`).<br><br>Om din [!DNL Commerce]-produktstruktur blir lägre än detta nummer är respektive Amazon-lista inte tillgänglig för försäljning via Amazon. |
| [!UICONTROL Maximum Listed Quantity] | Ange ett numeriskt värde för den kvantitet du vill visa i din Amazon-lista.<br><br>När en artikel säljs återpubliceras den kvantitet som anges här av Amazon. Den här inställningen används vanligtvis när du inte hanterar produktlager.<br><br>Du kan t.ex. ange värdet för Högsta antal listade kvantiteter som `10`. Den faktiska kvantiteten för en produkt är `80`. Eftersom du har angett det här värdet till `10` visas alltid den tillgängliga kvantiteten `10` i Amazon-listan. Tillgänglig kvantitet visas alltid med det definierade värdet, även när lagerkvantiteten är lägre. |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Ange ett värde för visningsmängden för dina Amazon-listor.<br><br>Amazon kräver att du publicerar en tillgänglig kvantitet. För [!DNL Commerce]-produkter som inte är inställda på att hantera lager men som du vill lista dem på Amazon, publiceras listan med den tillgängliga kvantiteten av värdet som anges här. |

**Snabbåtkomst** - [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## Exempel: Maximal listat kvantitet

När en artikel säljs är den här kvantiteten försedd med Amazon lista.

Om du till exempel anger *[!UICONTROL Maximum Listed Quantity]* som `12` visas kvantiteten 12 i Amazon-listan, även om produkten har en [!DNL Commerce] kvantitet på 80:

![Exempel på maximal listad kvantitet ](assets/amazon-max-listed-quantity.png){width="300"}

Om du anger *[!UICONTROL Maximum Listed Quantity]* som `1` listas alla berättigade produkter med kvantiteten `1`. När en artikel säljs letar systemet efter din [!DNL Commerce]-produkt och, om det finns ytterligare lager, litar på artikeln på Amazon med kvantiteten `1`.

Det här alternativet kan vara värdefullt för produkter som vanligtvis beställs med en kvantitet på 1. Det är också mycket angeläget för kunderna när de tittar på din Amazon-lista.

![Exempel på maximal listad kvantitet 2](assets/amazon-max-listed-quantity-1.png){width="300"}
