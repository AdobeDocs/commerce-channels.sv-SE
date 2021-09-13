---
title: Listpris
description: Använd inställningarna för listpris för att bestämma priskällan och basprisvärdet (standardpriset) för dina Amazon-listor.
redirect_from: /sales-channels/asc/ob-listing-price.html: 
exl-id: d97d81fa-c298-423f-9072-050ee72e707e
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: 1509
ht-degree: 0%

---

# Listpris

[!UICONTROL Listing Price] -inställningarna ingår i inställningarna för din butikslista. Du kommer åt listinställningarna från [butiksdashboard](./amazon-store-dashboard.md).

De här inställningarna definierar vilket [!DNL Commerce] prisattribut som ska användas som priskälla, vilket är basprisvärdet (standard) för dina Amazon-listor. De här inställningarna används av dina [prisregler](./pricing-rule-general-settings.md) för att automatiskt justera ditt Amazon listpris i förhållande till det värde som angetts för _[!UICONTROL Magento Price Source]_.

Du kan konfigurera ditt [prisområde](./price-scope.md) som globalt eller som en webbplats. Om ditt prisomfång är `Global` finns det en enda priskälla för alla dina butiker/webbplatser. Om ditt prisomfång är inställt på `Website` använder priskällan reservlogik för webbplatspriset (om tillgängligt) följt av standardpriset (globalt).

Om en listregel är inställd på att gälla för mer än en webbplats, bestäms ordningen som webbplatspriset används i av den prioritetsinställning för webbplatsen som definieras i [listregeln](./listing-rules.md). Med de här reglerna kan du definiera produktpriser i hela katalogen. Om du vill se om du använder webbplatsens prisomfång läser du [Katalogens prisomfång](https://docs.magento.com/user-guide/catalog/catalog-price-scope.html){target=&quot;_blank&quot;}.

De alternativ som listas i _[!UICONTROL Magento Price Source]_,_[!UICONTROL Minimum Advertised Price (Map)]_ och _[!UICONTROL Strike Through Price (MSRP)]_innehåller dina konfigurerade prisattribut. Prisattributen är [!DNL Commerce] produktattribut med värdet `Price` för Catalog Input Type för Store Owner. Se [Attributindatatyper](https://docs.magento.com/user-guide/stores/attributes-input-types.html){target=&quot;_blank&quot;}.

## Konfigurera inställningar för listpris {#configure-listing-price-settings}

1. Klicka på **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet _[!UICONTROL Listing Price]_.

1. Välj ett alternativ för **[!UICONTROL Magento Price Source]** (obligatoriskt).

   Standardvärdet är `Price`. Den här inställningen avgör vilken priskälla som används för dina Amazon-listor. Om du skapar [prisregler](./pricing-products.md) tillämpas reglerna på det värde som definieras för det attribut som väljs här. Du kan välja valfritt konfigurerat prisattribut. Om det valda attributet inte fylls i för en produkt, kommer standardpriset för produkten att vara `Price` när prisregler tillämpas för att fastställa det publicerade listpriset för Amazon.

1. Välj ett alternativ för **[!UICONTROL Minimum Advertised Price (MAP)**].

   Standardvärdet är ingen markering. Den här inställningen aktiverar ett lägsta annonspris (MAP) för en produkt. När du definierar ett prisattribut och ditt listpris för en produkt faller under ditt fastställda minimipris (baserat på din priskälla och dina regler), blir det här värdet MAP för listan. Med den här inställningen kan du implementera [prisregler](./pricing-products.md), samtidigt som du behåller kontrollen över minimipriset för en produkt. Om du vill förhindra att ett listpris blir för lågt väljer du ett prisattribut att använda som din MAP. Om det valda prisfältet inte är definierat för en produkt används dock inte MAP.

1. Välj ett alternativ för **[!UICONTROL Strike Through Price (MSRP)]**.

   Standardvärdet är ingen markering. Den här inställningen avgör vilket prisattribut som används som tillverkarens rekommenderade detaljhandelspris (MSRP) för en produkt. Om ditt listpris är lägre än det angivna minimipriset (MSRP) visas din lista i Amazon med en genomgång av minimipriset (MSRP) med det lägre listpriset tillsammans med det beräknade&quot;Spara&quot;-beloppet och procentandelen. Om det valda prisfältet inte är definierat för en produkt, beräknas dock inte MSRP.

   >[!NOTE]
   >
   >Den här inställningen gäller endast för listor som har vunnit [Buy Boxen](./buy-box-competitor-pricing.md)-positionen. Buy Boxen delas ut av Amazon till den säljare som har den produkt som vanligtvis anges till det bästa priset, tillsammans med andra faktorer som FBA/Prime-leverans, tillgänglighet och säljarens resultat.

1. Välj ett alternativ för **Använd mervärdesskatt (moms)**:

   - `Disabled` - (Standard) Välj när du inte vill tillgodoräkna dig moms.

   - `Enabled` - Välj när du vill tillgodoräkna dig moms. moms används vanligtvis som moms i europeiska länder och läggs till i det slutliga priset i Amazon. moms gäller inte slutpriset för listor som används inom en regel för intelligent prissättning, såvida inte [lägsta pris](./floor-price.md) nås.
   >[!NOTE]
   >
   >Företag i EU måste skicka fakturor till köpare, så att kunden kan överföra skatt. Du kan antingen generera dessa fakturor och beräkna momsen själv eller använda en momsberäkningstjänst som Amazon momsberäkningstjänst. Amazon rekommenderar att du registrerar dig för [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources?ref_=asuk_soa_rd&amp;){target=&quot;_blank&quot;}. Om du väljer en annan metod ansvarar du för att momssatsen efterlevs.>
   >
   >Det kan ta 10-14 dagar för Amazon att verifiera och aktivera momsberäkningstjänstkontot.

1. I **[!UICONTROL VAT Percentage]** anger du momssatsen.

   Standardvärdet är `0.00`. Det här värdet används för att beräkna momsbeloppet som ska läggas till listpriset. Om `10.2` anges läggs 10,20 % moms på ditt listpris. Det här fältet är inaktiverat när fältet Använd mervärdesskatt (moms) är inställt på `Disabled`.

1. **(Endast UK Stores)** Välj ett alternativ  **[!UICONTROL Amazon Product Tax Code (PTC)]** för:

   - `Do Not Manage PTC` - (Standard) Välj om du använder en momsberäkningstjänst från tredje part eller redan har alla dina skatteberäkningar konfigurerade i ditt  [!DNL Amazon Seller Central] konto. När du väljer det här alternativet skickar Amazon försäljningskanal ingen produktskattekodsinformation till ditt [!DNL Amazon Seller Central]-konto.

   - `Set Default PTC` - Välj om du har en universell produktskattekod (PTC) som du vill använda för alla dina produkter. När du väljer det här alternativet måste du slutföra _[!UICONTROL Default PTC]_.

      - I **[!UICONTROL Default PTC]** anger du den standardPTC som ska användas för alla Amazon-listor som är berättigade. Om din standard-PTC är inställd i ditt [!DNL Amazon Seller Central]-konto lämnar du det här fältet tomt. Ändringar som görs i det här fältet påverkar inte befintliga Amazon-listor. Om du vill ändra standard-PTC för en befintlig lista måste listan vara [avslutad](./end-listings-manually.md) och en ny lista skapas.
   >[!NOTE]
   >
   >Om du använder Amazon momsberäkningstjänst måste du känna till momskategorin för dina produkter. En PTC-kod är Amazon ID-kod för skattekategori för B2B-inköp i EU. Se [Amazon produktskattekod](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}.

1. Välj ett alternativ för **[!UICONTROL Currency Conversion]**.

   Standardvärdet är `Disabled`. Dessa alternativ beror på dina [!DNL Commerce] [valutainställningar](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;}. Om det inte finns några tillgängliga alternativ ställer du in valutainställningarna.

1. Klicka på **[!UICONTROL Save listing settings]** när du är klar.

![Listpris](assets/amazon-listing-price.png)

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Magento Price Source] | Bestämmer priskällan som används när du skapar dina Amazon-listor. Standardvärdet är `Price`. Om du väljer ett annat attribut, till exempel `Amazon Price` eller `Special Price`, används det definierade värdet för attributet för din Amazon-lista. Om det markerade attributet inte definieras används `Price`. |
| [!UICONTROL Minimum Advertised Price (MAP)] | Attributet [!DNL Commerce] för MAP-priser. Om du väljer MAP-alternativet anges ditt Amazon-pris automatiskt till MAP-priset om listpriset är lägre än MAP-priset. |
| [!UICONTROL Strike Through Price (MSRP)] | Attributet [!DNL Commerce] som representerar MSRP-priset. Om ditt Amazon listpris är lägre än MSRP visas en genomgång av MSRP-priset och listpriset. Den här inställningen används även för att beräkna&quot;Spara&quot;-beloppet och procentandelen, men den här funktionen gäller bara för listor som har vunnit [Buy Boxen](./buy-box-competitor-pricing.md)-positionen. |
| [!UICONTROL Apply Value Added Tax (VAT)] | moms används av säljare i EU.<br><br>Välj  `Disabled` om du inte vill att moms ska läggas till listpriserna.<br><br>Välj  `Enabled` och ange sedan momsprocenten för moms på dina listpriser. |
| [!UICONTROL VAT Percentage] | Definiera den procentandel som ska användas för att beräkna momsbeloppet som ska läggas till i listpriset för dina Amazon-listor. <br><br>Om du anger  `5`en moms på 5 % tillämpas på det slutliga börspriset när alla prisregler har tillämpats. Moms gäller inte slutpriset för listor som används i en intelligent prisregel, såvida inte [floor](./floor-price.md) eller [taket](./optional-ceiling-price.md) nås. |
| [!UICONTROL Amazon Product Tax Code (PTC)] | (Visas endast för butiker i Storbritannien) Anger om Amazon försäljningskanal skickar produktskattekodsinformation till ditt [!DNL Amazon Seller Central]-konto. <br><br>Välj  **Hantera inte** PTC om du använder en tredjepartstjänst för momsberäkning eller redan har alla dina momsberäkningar konfigurerade i ditt  [!DNL Amazon Seller Central] konto. När det här alternativet anges skickar Amazon försäljningskanal ingen produktskattekodsinformation till ditt [!DNL Amazon Seller Central]-konto.<br><br>Välj  **Ange standard-** PTC om du har en universell produktskattekod som du vill använda för alla produkter.<br><br>Se  [Amazon produktskattekod](https://sellercentral.amazon.com/gp/help/help.html?itemID=G200794510&amp;language=en_US){target=&quot;_blank&quot;}. |
| [!UICONTROL Default PTC] | Visas endast när **Amazon Product Tax Code (PTC)** är inställt på `Set Default PTC`. Ange den PTC som ska användas som standard för alla Amazon-listor. Om din standard-PTC är inställd i ditt [!DNL Amazon Seller Central]-konto lämnar du det här fältet tomt. <br><br>Ändringar som görs i det här fältet påverkar inte befintliga listor. Listan måste vara [avslutad](./end-listings-manually.md) och en ny lista måste skapas för att ändringen ska börja gälla. |
| [!UICONTROL Currency Conversion] | Gör att din standardvaluta för [!DNL Commerce]-butiken kan konvertera korrekt till din standardvaluta i Amazon för att publicera dina listpriser i rätt valuta. Valutakonverteringen baseras alltid på din [!DNL Commerce] standardvaluta.<br><br>Du kan fortfarande visa dina standardvalutor  [!DNL Commerce] och Amazon-valutor när andra valutor är tillgängliga. Om din standardvaluta för [!DNL Commerce] matchar din standardvaluta för Amazon låter du Valutakonvertering vara inaktiverat.<br><br>Om din  [!DNL Commerce] standardvaluta till exempel är CAD (kanadensiska dollar) och Amazon standardvaluta är USD, måste du aktivera Valutakonvertering och välja Konverteringsränta CAD till USD. Alternativen som presenteras baseras på de inbyggda [!DNL Commerce] valutakonverteringarna. Om du inte ser det alternativ du söker efter kan du [ställa in valutan i [!DNL Commerce]](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}. |

**Snabb åtkomst**  -  [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
