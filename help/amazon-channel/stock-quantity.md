---
title: Lager/kvantitet
description: Uppdatera inställningarna för Stock/Kvantitet om du vill styra synkroniseringen av produktkvantitetsinformation från din Commerce Store till ditt [!DNL Amazon Seller Central] konto.
redirect_from: /sales-channels/asc/ob-stock-quantity.html
exl-id: a8b7ab6c-393c-43c6-b5ef-68845177edff
source-git-commit: 632157839130461869345724bdfc03b306a4f613
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Lager/kvantitet

*[!UICONTROL Stock/Quantity]* -inställningarna ingår i inställningarna för din butikslista. Du kommer åt listinställningarna från [butiksdashboard](./amazon-store-dashboard.md).

De här inställningarna används för att synkronisera produktkvantitetsinformationen från [!DNL Commerce]-butiken till kvantiteten på ditt [!DNL Amazon Seller Central]-konto. Det här verktyget är kraftfullt och kan användas för ytterligare annonsering genom att visa köparens snabbhet samtidigt som lagret hålls organiserat. En del handlare kan till exempel ha 150 artiklar av en viss SKU i lager och vill vara säkra på att Amazon kunder kan köpa hela sitt lager. Andra handlare kanske bara vill ta med ett objekt i taget för att skapa en känsla av brist för slutanvändaren. I det här fallet anger du *[!UICONTROL Maximum Listed Quantity]* till `1`.

Kvantitet är ett regionalt attribut och baseras på inställningen **[!UICONTROL Amazon Marketplace Country]** som definieras under [butiksintegrering](./store-integration.md). När en produkts kvantitet ändras påverkar ändringen alla Amazon-listor som delar [!DNL Amazon Seller SKU] i Amazon butiker som säljer i samma land. En ändring av ett delat [!DNL Amazon Seller SKU]-värde i USA påverkar inte dina Amazon-butiker som konfigurerats för ett annat land. Din första Amazon-butik som är integrerad (med det äldsta skapandedatumet) styr prioriteten i kvantitetsinställningarna.

>[!NOTE]
>
>För användare av Adobe Commerce och Magento Open Source 2.3.x stöder Amazon försäljningskanal användningen av lagerhanteringstillägget utan ytterligare konfigurationer. Se [Hantera lager](https://docs.magento.com/user-guide/v2.3/catalog/inventory-management.html){:target=&quot;_blank&quot;}.

## Konfigurera inställningar för lager/kvantitet {#configure-stock--quantity-settings}

1. Klicka på **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet **[!UICONTROL Stock / Quantity]**.

1. För **[!UICONTROL Out-of-Stock Threshold]** (obligatoriskt) anger du ett numeriskt värde för den lägsta kvantiteten av en produkt för att produkten ska kunna tas upp på förteckningen över Amazon.

   Standardvärdet är `0`. Om din [!DNL Commerce]-produkt blir mindre än detta antal är respektive Amazon-lista inte tillgänglig för försäljning via Amazon.

1. För **[!UICONTROL Maximum Listed Quantity]** (obligatoriskt) anger du ett numeriskt värde för den kvantitet du vill visa i din Amazon-lista.

   Den här inställningen visar alla Amazon-listor som är berättigade till det angivna värdet. När en artikel säljs ändras inte Amazon listkvantitet. Den tillgängliga kvantiteten i listan använder alltid det här värdet, även när den faktiska produktkvantiteten är högre eller lägre. Den här inställningen används vanligtvis när du inte hanterar produktlager. Du kan till exempel ha en produkt med en kvantitet på 80 i din [!DNL Commerce]-katalog. Med inställningen `10` visar Amazon-listan alltid ett tillgängligt antal `10` och ändras inte när produkten säljs.

1. För **[!UICONTROL "Do Not Manage Stock" Quantity]** (obligatoriskt) anger du ett kvantitetsvärde som ska visas för dina Amazon-listor.

   Amazon kräver att du publicerar en tillgänglig kvantitet. För [!DNL Commerce]-produkter som inte är inställda på att hantera stockar men som du vill visa på Amazon, publiceras listan med tillgänglig kvantitet som anges här.

1. Klicka på **[!UICONTROL Save listing settings]** när du är klar.

![Inställningar för lager/kvantitet](assets/amazon-stock-quantity.png)

| Fält | Beskrivning |
|---|---|
| [!UICONTROL Out-of-Stock Threshold] | Ange ett numeriskt värde för den lägsta kvantiteten av en produkt för att produkten ska kunna tas med i listan över Amazon (standardvärdet är `0`).<br><br>Om din  [!DNL Commerce] produktbeställning är lägre än detta nummer är respektive Amazon-lista inte tillgänglig för försäljning via Amazon. |
| [!UICONTROL Maximum Listed Quantity] | Ange ett numeriskt värde för den kvantitet du vill visa i din Amazon-lista.<br><br>När en artikel säljs återpubliceras den kvantitet som anges här. Den här inställningen används vanligtvis när du inte hanterar produktlager.<br><br>Du kan t.ex. ange värdet för Maximalt antal i listan som  `10`. Den faktiska kvantiteten för en produkt är `80`. Eftersom du har angett det här värdet som `10` visas alltid den tillgängliga mängden `10` i Amazon. Tillgänglig kvantitet visas alltid med det definierade värdet, även när lagerkvantiteten är lägre. |
| [!UICONTROL "Do Not Manage Stock" Quantity] | Ange ett värde för visningsmängden för dina Amazon-listor.<br><br>Amazon kräver att du publicerar en tillgänglig kvantitet. För [!DNL Commerce]-produkter som inte är inställda på att hantera Stock men som du vill lista dem på Amazon, publiceras listan med den tillgängliga kvantiteten av värdet som anges här. |

**Snabb åtkomst**  -  [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)

## Exempel: Maximal kvantitet

När en artikel säljs är den här kvantiteten försedd med Amazon lista.

Om du till exempel anger *[!UICONTROL Maximum Listed Quantity]* som `12` visar Amazon-listan kvantiteten 12 trots att produkten har [!DNL Commerce] kvantiteten 80:

![Exempel på maximal listats kvantitet 1](assets/amazon-max-listed-quantity.png)

Om du anger *[!UICONTROL Maximum Listed Quantity]* som `1` listas alla produkter som uppfyller kraven med kvantiteten `1`. När en artikel säljs letar systemet efter din [!DNL Commerce]-produkt och, om det finns ytterligare lager, litar på artikeln på Amazon med kvantiteten `1`.

Det här alternativet kan vara värdefullt för produkter som vanligtvis beställs med en kvantitet på 1. Det är också mycket angeläget för kunderna när de tittar på din Amazon-lista.

![Exempel på maximal listats kvantitet 2](assets/amazon-max-listed-quantity-1.png)
