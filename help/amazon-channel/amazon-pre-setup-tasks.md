---
title: Åtgärder före installation
description: Granska de uppgifter som ska utföras innan du integrerar din Adobe Commerce eller Magento Open Source store i Amazon Sales Channel.
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# Åtgärder före installation

Innan du [Store-integrering](./store-integration.md) måste du se till att ditt [!DNL Amazon Seller Central]-konto och ditt [!DNL Commerce]-konto är klara för integreringen. Det finns några nödvändiga förinställningsuppgifter för att integrera.

När du ställer in din första Amazon-butik i Amazon försäljningskanal visas en lista med konfigurationsuppgifter. Vi rekommenderar att du granskar dessa uppgifter innan du [lägger till en Amazon-butik](./store-integration.md). När du har lagt till din första butik kan du granska dessa uppgifter i vyn Utbildning och förberedelse i Amazon försäljningskanal [hemsida](./amazon-sales-channel-home.md).

## 1. Aktivera bakgrundsuppgifter i [!DNL Commerce]

Alla produkter och data som synkroniseras mellan [!DNL Commerce] och Amazon hanteras av ett [cron-jobb](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}. När du slutför uppgifter som att lägga till eller uppdatera listor och ta emot beställningar skickas och tar emot data mellan din [!DNL Commerce]-backend och ditt [!DNL Amazon Seller Central]-konto.

- [ [!DNL Commerce] Aktivera](https://docs.magento.com/user-guide/system/cron.html){target=&quot;_blank&quot;}.

- [Ange [!DNL Commerce] cron](https://docs.magento.com/user-guide/configuration/advanced/system.html){target=&quot;_blank&quot;} så att den körs en gång var femte minut för maximala prestanda.

## 2. Skapa ditt [!DNL Amazon Seller Central]-konto

Innan du börjar konfigurera din Amazon-försäljningskanal måste du ha ett aktivt [!DNL Amazon Seller Central]-konto. Om du inte har något Amazon Seller-konto i [Nordamerika (USA, CA, MX)](https://sell.amazon.com/){target=&quot;_blank&quot;} eller [Europa (UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target=&quot;_blank&quot;} kan du slutföra konfigurationen av Amazon Seller-konto.

Amazon försäljningskanal kräver ett [!DNL Professional Seller]-konto på [!DNL Amazon Seller Central]. Amazon debiterar en månadsprenumeration och tar ut avgifter för försäljningen. Se [Amazon: Välj din försäljningsplan](https://sell.amazon.com/pricing.html){target=&quot;_blank&quot;}.

## 3. Se till att du är en godkänd Amazon-återförsäljare

För att kunna integrera måste du ha ett godkänt [!DNL Amazon Seller Central]-konto. Ditt konto får inte ha några begränsningar för produkter eller kategorier. Vissa produkter och kategorier måste godkännas innan du kan skapa listor. Granska Amazon policyer för godkännande av kategori och produkt för att säkerställa att produkterna godkänns. Se [Amazon: Kategorier och produkter som kräver godkännande](https://sellercentral.amazon.com/gp/help/200333160){target=&quot;_blank&quot;} (Inloggning till Seller Central krävs).

Det är också viktigt att du har konfigurerat följande i ditt [!DNL Amazon Seller Central]-konto:

- Se till att returpolicyn är lika bra som eller bättre än Amazon returpolicy. Se [Amazon: Returprincip](https://www.amazon.com/gp/help/customer/display.html){target=&quot;_blank&quot;}.

- Kontrollera att skatteinställningarna är konfigurerade. Se [Amazon: Skattepolicyer](https://sellercentral.amazon.com/gp/help/external/help.html){target=&quot;_blank&quot;} (Inloggning till Seller Central krävs).

- Kontrollera att leveransmetoderna är korrekt konfigurerade. Uppdatera [Amazon för att konfigurera leveransmetoder som [!DNL Commerce] erbjuds kunder att utföra dina Amazon-beställningar: Leveransinställningar](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target=&quot;_blank&quot;} i ditt [!DNL Amazon Seller Central]-konto.

## 4. Se till att momsen är konfigurerad för butikerna

(Används främst av brittiska säljare.) Amazon rekommenderar att du registrerar dig för [Amazon VAT Calculation Service](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target=&quot;_blank&quot;}. Om du väljer en annan metod ansvarar du för att momssatsen efterlevs.

>[!NOTE]
>
>Det kan ta 10-14 dagar för Amazon att verifiera och aktivera momsberäkningstjänstkontot.

## 5. Öka antalet automatiska katalogmatchningar

Under introduktionen använder Amazon försäljningskanal produktattribut för att matcha dina befintliga Amazon-listor (om tillämpligt) med befintliga produkter i din [!DNL Commerce]-katalog. Efter introduktionen används de här produktattributen för att publicera dina [!DNL Commerce]-katalogobjekt till en Amazon-lista och för att synkronisera produktdata mellan [!DNL Commerce] och Amazon.

Om du vill att det högsta antalet [!DNL Commerce]-produkter automatiskt ska matcha Amazon-listor bör du skapa en uppsättning produktattribut för din [!DNL Commerce]-katalog. Innan du konfigurerar Amazon säljkanalsbutik bör du lägga till [!DNL Commerce]-produktattribut som matchar dessa Amazon-attribut, till exempel: ASIN, EAN, ISBN, UPC eller GCID. Se [Skapa ett produktattribut i [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Konfigurera valuta och konvertering (efter behov)

Om din Amazon-butik använder en annan valuta än den som är konfigurerad för ditt [!DNL Commerce]-arkiv, [aktiverar du valutan](https://docs.magento.com/user-guide/configuration/general/currency-setup.html){target=&quot;_blank&quot;} och anger [valutakonverteringssatsen](https://docs.magento.com/user-guide/stores/currency-update.html){target=&quot;_blank&quot;}.

## 7. Skapa ett produktvillkorsattribut (efter behov)

Om dina Amazon-listor innehåller fler än ett produktvillkor (till exempel _new_, _used_ eller _som new_) skapar du ett [!DNL Commerce]-attribut och tilldelar villkorsvärden. Du måste mappa det här attributet under introduktionen till Amazon Condition-produktattributet. Se [Skapa attribut för Amazon](./ob-creating-magento-attributes.md).

## 8. Konfigurera leveransmetoden för [!DNL Amazon Seller Central]

Information om hur du ställer in leveransmetoder för att utföra dina Amazon-beställningar finns i [Inställningar och leveransinställningar][10] i ditt [!DNL Amazon Seller Central]-konto.

## Ytterligare konfigurationer

När ditt Amazon-konto är konfigurerat och aktivt finns det flera [!DNL Commerce] rekommendationer som hjälper till att effektivisera processen för att ta steget över till Amazon säljkanal.

### Granska och notera produkter som du vill utesluta

Du kanske inte vill att vissa produkter ska listas på Amazon. Amazon försäljningskanal har en listregelmotor som används för att avgöra vilka produkter som är berättigade att publicera till Amazon. [Med ](./listing-rules.md) listlinjaler kan du välja vilka delmängder av produkter som ska publiceras (eller inte publiceras) till ditt  [!DNL Amazon Seller Central] konto, t.ex. efter kategorival eller genom att definiera ett eller flera produktattribut. Precis som [!DNL Commerce] [katalog](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;} eller [kundvagn](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){target=&quot;_blank&quot;} måste de produktattribut som används för att visa Amazon-produkter ha **[!UICONTROL Use for Promo Rule Conditions]** inställt på `Yes`. Se **[!UICONTROL Use for Promo Rule Conditions]** i [Produktattribut](https://docs.magento.com/user-guide/stores/attributes-product.html){target=&quot;_blank&quot;}.

### Ange att din [!DNL Amazon Seller Central]-region ska vara inaktiv

För att underlätta felfri dataövergång under integreringen rekommenderar vi att du ställer in din Amazon-region till `Inactive`-status i Inställningar > Kontoinformation > Vacationsinställningar. Se [Amazon: Liststatus för semester][11]. När installationen är klar ändrar du statusen till `Active` i Amazon.

![Nästa ](assets/btn-next.png) [**ikonFortsätt till Skapa  [!DNL Commerce] attribut**](./ob-creating-magento-attributes.md)
