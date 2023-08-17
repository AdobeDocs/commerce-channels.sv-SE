---
title: Förinställda uppgifter för [!DNL Amazon sales channel]
description: Granska de uppgifter som ska utföras innan du integrerar din Adobe Commerce- eller Magento Open Source-butik i Amazon Sales Channel.
role: Admin, Developer
feature: Sales Channels, Install, Configuration
exl-id: eb9d9136-925f-4b20-9d65-b166173f434b
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# Förinställda uppgifter för [!DNL Amazon sales channel]

Före [Butiksintegrering](./store-integration.md)måste du se till att [!DNL Amazon Seller Central] konto och [!DNL Commerce] kontot är klart för integrering. Det finns några nödvändiga förinställningsuppgifter för att integrera.

När du ställer in din första Amazon-butik i Amazon försäljningskanal visas en lista med konfigurationsuppgifter. Vi rekommenderar att du granskar dessa uppgifter innan du [lägg till en Amazon-butik](./store-integration.md). När du har lagt till din första butik kan du granska dessa uppgifter i vyn Utbildning och förberedelse i Amazon försäljningskanal [hemsida](./amazon-sales-channel-home.md).

## 1. Aktivera bakgrundsuppgifter i [!DNL Commerce]

Alla produkter och data synkroniserade mellan [!DNL Commerce] och Amazon hanteras av en [cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html). När du slutför uppgifter som att lägga till eller uppdatera listor och ta emot beställningar skickas och tar emot data mellan [!DNL Commerce] backend och din [!DNL Amazon Seller Central] konto.

- [Aktivera [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html).

- För maximala prestanda [set [!DNL Commerce] cron](https://experienceleague.adobe.com/docs/commerce-admin/config/advanced/system.html) att köras en gång var femte minut.

## 2. Skapa [!DNL Amazon Seller Central] konto

Innan du börjar konfigurera din Amazon-försäljningskanal måste du ha en aktiv [!DNL Amazon Seller Central] konto. Om du inte har något Amazon Seller-konto i [Nordamerika (USA, CA, MX)](https://sell.amazon.com/){target="_blank"} or [European (UK)](https://sell.amazon.co.uk/sell-online/beginners-guide){target="_blank"} kan du slutföra konfigureringen av Amazon säljarkonto.

Amazon försäljningskanal kräver [!DNL Professional Seller] konto på [!DNL Amazon Seller Central]. Amazon debiterar en månadsprenumeration och tar ut avgifter för försäljningen. Se [Amazon: Välj din säljplan](https://sell.amazon.com/pricing.html){target="_blank"}.

## 3. Kontrollera att du är en godkänd Amazon-återförsäljare

För att kunna integrera måste du ha en godkänd [!DNL Amazon Seller Central] konto. Ditt konto får inte ha några begränsningar för produkter eller kategorier. Vissa produkter och kategorier måste godkännas innan du kan skapa listor. Granska Amazon policyer för godkännande av kategori och produkt för att säkerställa att produkterna godkänns. Se [Amazon: Kategorier och produkter som måste godkännas](https://sellercentral.amazon.com/gp/help/200333160){target="_blank"} (Inloggning till Seller Central krävs).

Det är också viktigt att du har konfigurerat följande i [!DNL Amazon Seller Central] konto:

- Se till att returpolicyn är lika bra som eller bättre än Amazon returpolicy. Se [Amazon: Returpolicy](https://www.amazon.com/gp/help/customer/display.html){target="_blank"}.

- Kontrollera att skatteinställningarna är konfigurerade. Se [Amazon: Skattepolicy](https://sellercentral.amazon.com/gp/help/external/help.html){target="_blank"} (Inloggning till Seller Central krävs).

- Kontrollera att leveransmetoderna är korrekt konfigurerade. Så här ställer du in leveransmetoder som [!DNL Commerce] erbjuds kunderna att utföra dina Amazon-beställningar, uppdatera [Amazon: Leveransinställningar](https://sellercentral.amazon.com/sbr/ref=xx_shipset_dnav_xx#shipping_templates){target="_blank"} i [!DNL Amazon Seller Central] konto.

## 4. Se till att momsen är konfigurerad för butikerna

(Används främst av brittiska säljare.) Amazon rekommenderar att du registrerar dig för [Amazon momskalkyleringstjänst](https://sell.amazon.co.uk/learn/vat-resources#vat-services-on-amazon){target="_blank"}. Om du väljer en annan metod ansvarar du för att momssatsen efterlevs.

>[!NOTE]
>
>Det kan ta 10-14 dagar för Amazon att verifiera och aktivera momsberäkningstjänstkontot.

## 5. Öka antalet automatiska katalogmatchningar

Vid introduktionen använder Amazon säljkanal produktattribut för att matcha dina befintliga Amazon-listor (om tillämpligt) med befintliga produkter i din [!DNL Commerce] katalog. Efter introduktionen används dessa produktattribut för att publicera [!DNL Commerce] katalogobjekt till en Amazon-lista och för att synkronisera produktdata mellan [!DNL Commerce] och Amazon.

Att ha det högsta antalet [!DNL Commerce] produkter som automatiskt matchar Amazon listor bör du skapa en uppsättning produktattribut för [!DNL Commerce] katalog. Innan du konfigurerar din Amazon-återförsäljare bör du lägga till [!DNL Commerce] produktattribut som matchar dessa Amazon-attribut, till exempel: ASIN, EAN, ISBN, UPC eller GCID. Se [Skapa ett produktattribut i [!DNL Commerce]](./ob-creating-magento-attributes.md).

## 6. Konfigurera valuta och konvertering (efter behov)

Om din Amazon-butik använder en annan valuta än den som konfigurerats för din [!DNL Commerce] butik, [aktivera valutan](https://experienceleague.adobe.com/docs/commerce-admin/config/general/currency-setup.html) och ange [valutakurs](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-update.html).

## 7. Skapa ett produktvillkorsattribut (efter behov)

Om dina Amazon-listor innehåller mer än ett produktvillkor (till exempel _new_, _används_, eller _gillar nya_), skapa en [!DNL Commerce] och tilldela villkorsvärden. Du måste mappa det här attributet under introduktionen till Amazon Condition-produktattributet. Se [Skapa attribut för Amazon](./ob-creating-magento-attributes.md).

## 8. Konfigurera [!DNL Amazon Seller Central] leveranssätt

Information om hur du ställer in leveransmetoder för att utföra dina Amazon-beställningar finns i _Inställningar och leveransinställningar_ i [!DNL Amazon Seller Central] konto.

## Ytterligare konfigurationer

När ditt Amazon-konto är konfigurerat och aktivt finns det flera [!DNL Commerce] rekommendationer som hjälper till att effektivisera Amazon process för registrering av säljkanaler.

### Granska och notera produkter som du vill utesluta

Du kanske inte vill att vissa produkter ska listas på Amazon. Amazon försäljningskanal har en listregelmotor som används för att avgöra vilka produkter som är berättigade att publicera till Amazon. [Listregler](./listing-rules.md) kan du välja vilka delmängder av produkter som ska publiceras (eller inte publiceras) till [!DNL Amazon Seller Central] konto, t.ex. per kategori eller genom att definiera ett eller flera produktattribut. Gilla [!DNL Commerce] [katalog](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) eller [kundvagn](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) prisregler, produktattribut som används för att ta upp Amazon-produkter måste ha **[!UICONTROL Use for Promo Rule Conditions]** ange till `Yes`. Se **[!UICONTROL Use for Promo Rule Conditions]** in [Produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

### Ställ in [!DNL Amazon Seller Central] region till inaktiv

För att underlätta felfri dataövergång under integreringen rekommenderar vi att du ställer in Amazon-regionen på `Inactive` status i Inställningar > Kontoinformation > Semesterinställningar. När installationen är klar ändrar du status tillbaka till `Active` i Amazon.

![Nästa ikon](assets/btn-next.png) [**Fortsätt till Skapa [!DNL Commerce] Attribut**](./ob-creating-magento-attributes.md)
