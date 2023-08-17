---
title: Amazon försäljningskanal - [!UICONTROL Listing Price]
description: Använd inställningarna för listpris för att bestämma priskällan och basprisvärdet (standardpriset) för dina Amazon-listor.
feature: Sales Channels, Products, Price Rules
redirect_from: sales-channels/asc/ob-listing-price.html
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 0%

---

# [!UICONTROL Listing Price]

[!UICONTROL Listing Price] -inställningarna ingår i inställningarna för din butikslista. Du kommer åt listinställningarna via [instrumentpanel för butik](./amazon-store-dashboard.md).

Dessa inställningar definierar vilka [!DNL Commerce] prisattribut att använda som priskälla, vilket är basprisvärdet (standardvärdet) för dina Amazon-listor. De här inställningarna används av [prisregler](./pricing-rule-general-settings.md) för att automatiskt justera ditt Amazon-pris i förhållande till det värde som angetts för _[!UICONTROL Magento Price Source]_.

Du kan konfigurera [prissättning](./price-scope.md) som global eller webbplats. Om ditt prisomfång är inställt på `Global`, finns det en enda priskälla för alla dina butiker/webbplatser. Om ditt prisomfång är inställt på `Website`, använder priskällan reservlogik för webbplatsens pris (om tillgängligt) följt av standardpriset (globalt).

Om en listregel är inställd på att gälla för mer än en webbplats, bestäms ordningen som webbplatsens pris används i av den prioritetsinställning som definieras i dialogrutan [listregel](./listing-rules.md). Med de här reglerna kan du definiera produktpriser i hela katalogen. Se om du använder webbplatsens prisomfång [Katalogprisomfång](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/catalog-price-scope.html).

De alternativ som visas i _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ och _[!UICONTROL Strike Through Price (MSRP)]_inkludera dina konfigurerade prisattribut. Prisattributen är [!DNL Commerce] produktattribut med värdet för katalogindatatypen för butiksägaren satt till `Price`. Se [Attributindatatyper](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/attributes-input-types.html).

## Konfigurera inställningar för listpris {#configure-listing-price-settings}

1. Klicka **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet _[!UICONTROL Listing Price]_.

1. För **[!UICONTROL Magento Price Source]** (obligatoriskt) väljer du ett alternativ.

   Standardvärdet är `Price`. Den här inställningen avgör vilken priskälla som används för dina Amazon-listor. Om du skapar [prisregler](./pricing-products.md)används reglerna på det värde som definieras för det attribut som väljs här. Du kan välja valfritt konfigurerat prisattribut. Men om det valda attributet inte fylls i för en produkt, återgår priskällan för produkten till `Price` när prissättningsregler tillämpas för att fastställa det publicerade priset för Amazon.

1. För **[!UICONTROL Minimum Advertised Price (MAP)**]väljer du ett alternativ.

   Standardvärdet är ingen markering. Den här inställningen aktiverar ett lägsta annonspris (MAP) för en produkt. När du definierar ett prisattribut och ditt listpris för en produkt faller under ditt fastställda minimipris (baserat på din priskälla och dina regler), blir det här värdet MAP för listan. Med den här inställningen kan du implementera [prisregler](./pricing-products.md), samtidigt som du behåller kontrollen över minimipriset för en produkt. Om du vill förhindra att ett listpris blir för lågt väljer du ett prisattribut att använda som din MAP. Om det valda prisfältet inte är definierat för en produkt används dock inte MAP.

1. För **[!UICONTROL Strike Through Price (MSRP)]** väljer du ett alternativ.

   Standardvärdet är ingen markering. Den här inställningen avgör vilket prisattribut som används som tillverkarens rekommenderade försäljningspris för en produkt. Om ditt listpris är lägre än det angivna minimipriset (MSRP) visas din lista i Amazon med en genomgång av minimipriset (MSRP) med det lägre listpriset tillsammans med det beräknade&quot;Spara&quot;-beloppet och procentandelen. Om det valda prisfältet inte är definierat för en produkt, beräknas dock inte MSRP.

   >[!NOTE]
   >
   >Den här inställningen gäller endast listor som har vunnit [Buy Box](./buy-box-competitor-pricing.md) position. Buy Boxen delas ut av Amazon till den säljare som har den produkt som vanligtvis anges till det bästa priset, tillsammans med andra faktorer som FBA/Prime-leverans, tillgänglighet och säljarens resultat.

1. För **Tillämpa mervärdesskatt (moms)** väljer du ett alternativ:

   - `Disabled` - (Standard) Välj när du inte vill tillgodoräkna dig moms.

   - `Enabled` - Välj när du vill tillgodoräkna dig moms. moms används vanligtvis som moms i europeiska länder och läggs till i det slutliga priset i Amazon. moms inte tillämpas på slutpriset för listor som används inom en regel för intelligent prissättning, såvida inte [lägsta pris](./floor-price.md) är träffad.

   >[!NOTE]
   >
   >Företag i EU måste skicka fakturor till köpare, så att kunden kan överföra skatt. Du kan antingen generera dessa fakturor och beräkna momsen själv eller använda en momsberäkningstjänst som Amazon momsberäkningstjänst. Amazon rekommenderar att du registrerar dig för [Amazon momskalkyleringstjänst](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;). Om du väljer en annan metod ansvarar du för att momssatsen efterlevs.>
   >
   >Det kan ta 10-14 dagar för Amazon att verifiera och aktivera momsberäkningstjänstkontot.

1. För **[!UICONTROL VAT Percentage]** anger du momssatsen.

   Standardvärdet är `0.00`. Det här värdet används för att beräkna momsbeloppet som ska läggas till listpriset. If `10.2` anges läggs 10,20 % moms på ditt listpris. Det här fältet är inaktiverat när fältet Använd moms är inställt på `Disabled`.

1. **(Endast UK Stores)** För **[!UICONTROL Amazon Product Tax Code (PTC)]** väljer du ett alternativ:

   - `Do Not Manage PTC` - (Standard) Välj om du använder en momsberäkningstjänst från tredje part eller redan har alla dina skatteberäkningar konfigurerade i [!DNL Amazon Seller Central] konto. När du väljer det här alternativet skickar Amazon försäljningskanal ingen produktskattekod till din [!DNL Amazon Seller Central] konto.

   - `Set Default PTC` - Välj om du har en universell produktskattekod (PTC) som du vill använda för alla produkter. När du väljer det här alternativet måste du slutföra _[!UICONTROL Default PTC]_.

      - För **[!UICONTROL Default PTC]** anger du den PTC som ska användas som standard för alla Amazon-listor. Om din standard-PTC är inställd i [!DNL Amazon Seller Central] lämna fältet tomt. Ändringar som görs i det här fältet påverkar inte befintliga Amazon-listor. Om du vill ändra standard-PTC för en befintlig lista måste listan vara [avslutad](./end-listings-manually.md) och en ny lista skapas.

   >[!NOTE]
   >
   >Om du använder Amazon momsberäkningstjänst måste du känna till momskategorin för dina produkter. En PTC-kod är Amazon ID-kod för skattekategori för B2B-inköp i EU. Se [Amazon produktskattekod](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}.

1. För **[!UICONTROL Currency Conversion]** väljer du ett alternativ.

   Standardvärdet är `Disabled`. Dessa alternativ beror på [!DNL Commerce] [valuta](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) inställningar. Om det inte finns några tillgängliga alternativ ställer du in valutainställningarna.

1. När du är klar klickar du på **[!UICONTROL Save listing settings]**.

![Listpris](assets/amazon-listing-price.png){width="500" zoomable="yes"}

| Fält | Beskrivning |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Magento Price Source] | Bestämmer priskällan som används när du skapar dina Amazon-listor. Standardvärdet är `Price`. Om du väljer ett annat attribut, till exempel `Amazon Price` eller `Special Price`används det definierade värdet för attributet för din Amazon-lista. Om det valda attributet inte är definierat, `Price` används. |
| [!UICONTROL Minimum Advertised Price (MAP)] | The [!DNL Commerce] för MAP-priser. Om du väljer MAP-alternativet anges ditt Amazon-pris automatiskt till MAP-priset om listpriset är lägre än MAP-priset. |
| [!UICONTROL Strike Through Price (MSRP)] | The [!DNL Commerce] som representerar MSRP-priser. Om ditt Amazon listpris är lägre än MSRP visas en genomgång av MSRP-priset och listpriset. Den här inställningen används även för att beräkna&quot;Spara&quot;-beloppet och procentandelen, men den här funktionen gäller bara för listor som har vunnit [Buy Box](./buy-box-competitor-pricing.md) position. |
| [!UICONTROL Apply Value Added Tax (VAT)] | moms används av säljare i EU.<br><br>Välj `Disabled` om du inte vill att moms ska läggas till listpriserna.<br><br>Välj `Enabled` och ange momsprocenten för moms på dina noteringspriser. |
| [!UICONTROL VAT Percentage] | Definiera den procentandel som ska användas för att beräkna momsbeloppet som ska läggas till i listpriset för dina Amazon-listor. <br><br>Om du anger `5`kommer en moms på 5 % att tillämpas på det slutliga börspriset när alla prisregler har tillämpats. Moms gäller inte slutpriset för listor som används inom en regel för intelligent prissättning, såvida inte [floor](./floor-price.md) eller [tak](./optional-ceiling-price.md) är träffad. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Visas endast för butiker i Storbritannien) Anger om Amazon försäljningskanal skickar produktskattekodsinformation till din [!DNL Amazon Seller Central] konto. <br><br>Välj **Hantera inte PTC** om du använder en tredjepartstjänst för momsberäkning eller redan har alla dina momsberäkningar konfigurerade i [!DNL Amazon Seller Central] konto. När du väljer det här alternativet skickar Amazon försäljningskanal ingen information om produktskattekod till din [!DNL Amazon Seller Central] konto.<br><br>Välj **Ange standard-PTC** om du har en universell produktskattekod som du vill använda för alla dina produkter.<br><br>Se [Amazon produktskattekod](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target="_blank"}. |
| [!UICONTROL Default PTC] | Endast visas när **Amazon Product Tax Code (PTC)** är inställd på `Set Default PTC`. Ange den PTC som ska användas som standard för alla Amazon-listor. Om din standard-PTC är inställd i [!DNL Amazon Seller Central] lämna fältet tomt. <br><br>Ändringar som görs i det här fältet påverkar inte befintliga listor. Listan måste vara [avslutad](./end-listings-manually.md) och en ny lista som skapats för att ändringen ska börja gälla. |
| [!UICONTROL Currency Conversion] | Tillåter [!DNL Commerce] lagra standardvaluta för att konvertera till din standardvaluta i Amazon och publicera dina priser i rätt valuta. Valutakonverteringen baseras alltid på din [!DNL Commerce] standardvaluta.<br><br>Du kan fortfarande visa din standardinställning [!DNL Commerce] och Amazon-valutor när andra valutor är tillgängliga. Om din standard [!DNL Commerce] Valutan matchar din standardvaluta för Amazon. Lämna Valutakonvertering inaktiverat.<br><br>Om [!DNL Commerce] Standardvalutan är CAD (Canadian Dollars) och Amazon standardvaluta är USD. Du måste aktivera valutakonvertering och välja Konverteringsgrad CAD till USD. Alternativen som presenteras baseras på den inbyggda [!DNL Commerce] valutakonverteringar. Om du inte ser det alternativ du letar efter [ställa in valutan i [!DNL Commerce]](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html). |

**Snabb åtkomst** - [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
