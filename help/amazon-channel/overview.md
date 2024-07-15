---
title: "Introduktion till  [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] gör det möjligt för handlare att sömlöst sälja produkter i  [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
role: Admin, User, Leader
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Introduktion till [!DNL Amazon Sales Channel]

Som Adobe Commerce- eller Magento Open Source-handlare kan du använda tillägget [!DNL Amazon Sales Channel] för att integrera dina butiker med världens största globala shoppingplats. Det här tillägget möjliggör Amazon försäljning genom att ansluta [!DNL Commerce] till ditt [!DNL Amazon Seller Central]-konto och tillhandahålla både automatisering och synkronisering av katalog- och orderdata. Hantera alla Amazon-listor fullständigt, implementera enkla eller intelligenta prisregler och underhålla dina order och lager via en enda [!DNL Commerce]-kontrollpanel.

Efter [introduktion](./amazon-onboarding-home.md) blir [!DNL Commerce] ett&quot;centralt kommandocenter&quot; för att hantera och kontrollera dina Amazon-listor, -beställningar och -lager samt priser för din Amazon-butik. [Store-integrering](./store-integration.md) ansluter din [!DNL Commerce]-instans och Amazon för att synkronisera data mellan båda plattformarna. Med Amazon säljkanal kan ni

- [Inbyggt](./amazon-onboarding-home.md) och integrera ett eller flera [!DNL Amazon Seller Central]-konton med Adobe Commerce eller Magento Open Source.

- Importera och synkronisera dina befintliga Amazon-listor och matcha med produkter i din [!DNL Commerce]-katalog, så skapas en centraliserad produktkatalog.

- Skapa och hantera Amazon-listor för produkter i [!DNL Commerce]-katalogen.

- Visa och slutför beställningar (leverans) i [!DNL Commerce] och Amazon, synkronisering av orderstatus, betalning och återbetalningsinformation.

- Visa loggar för analyser och fel för [konkurrenskraftiga priser](./competitive-price-analysis.md), [listning av ändringar](./listing-changes-log.md) och [kommunikationsproblem](./communication-errors-log.md).

Gå till dina Amazon-butiker för att visa och hantera alla dessa funktioner, kontoinformation, listor, beställningar och annat på Amazon säljkanals [hemsida](./amazon-sales-channel-home.md).

## Kampanjer och priser

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Synkronisera Amazon listpris till [!DNL Commerce] katalogpris (eller alternativt prisattribut).

- Aktivera [genomstrykningspris](./listing-price.md#configure-listing-price-settings) för MSRP i dina Amazon-listor för att öka kundvärdesanspråken.

- Aktivera och hantera [lägsta kampanjpris (MAP)](./listing-price.md#configure-listing-price-settings) i dina Amazon-listor.

- Konfigurera ytterligare [moms](./listing-price.md#configure-listing-price-settings) i dina Amazon-priser.

- Ange ett anpassat värde för &quot;tillgängligt antal&quot; i dina [lager-/kvantitetsinställningar](./stock-quantity.md#configure-stock--quantity-settings) som ska visas med dina Amazon-listor för att öka köparens trängsel.

## Prisregler

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Skapa staplingsbara, flexibla och komplexa [prisregler](./pricing-products.md) för att hantera dina Amazon-priser för daglig försäljning eller säsongskampanjer.

- Skapa [golv](./floor-price.md)- och [tak](./optional-ceiling-price.md)-priser för att skydda dina lägsta och högsta priser.

- Skapa och hantera [smarta omprisregler](./intelligent-repricing-rules.md) som automatiskt justerar dina produktpriser i förhållande till andra Amazon-konkurrenter ([lägsta konkurrent](./lowest-competitor-pricing.md) och [Buy Box](./buy-box-competitor-pricing.md) pris).

## Katalogflödeshantering

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Importera dina befintliga Amazon-listor (produkter) och matcha med befintliga eller skapa produkter i din [!DNL Commerce]-katalog.

- Publish dina [!DNL Commerce]-produkter till Amazon för att skapa Amazon-listor.

- Skapa [åsidosättningar](./creating-editing-overrides.md) om du vill ange ett individuellt meddelande om pris, hanteringstid, villkor och säljaranteckningar.

- Importera och mappa [attribut](./attributes-view.md) från dina Amazon-listor så att de automatiskt matchar produkter i din [!DNL Commerce]-katalog.

- Ange flera sökparametrar så att de matchar Amazon-listor i din [!DNL Commerce]-katalog.

- Definiera [listregler](./listing-rules.md) för att avgöra vilka av dina [!DNL Commerce] produkter som är berättigade att listas i Amazon.

- Ange en standardhanteringstid [för ](./product-listing-actions.md) för dina nya Amazon-listor.

- Matcha listvillkoren baserat på ett [!DNL Commerce]-attribut.

- Lägg till säljaranteckningar för varje villkorstyp (valfritt).

- Implementera tröskelvärden för antal när du importerar Amazon-listor till din [!DNL Commerce]-katalog.

- Visa rekommenderade [listförbättringar](./listing-improvements.md).

## Orderhantering och kundtjänst

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Support och bearbeta beställningar i Amazon och [!DNL Commerce].

- [Importera](./order-settings.md#configure-order-settings) dina Amazon-beställningar till [!DNL Commerce] eller lämna dem i Amazon.

- Definiera vilka av dina [!DNL Commerce]-webbplatslager som ska kopplas till dina Amazon-beställningar för import och hantering av beställningar.

- Visa, avbryt och skicka beställningar från [!DNL Commerce] och/eller Amazon beroende på dina [leveransinställningar](./fulfilled-by.md).

- Mappa din Amazon-orderstatus till anpassad status inom [!DNL Commerce] (valfritt).

- Visa och hantera orderfel för att lösa problem och få kontakt med kunderna.

- Skicka orderspårningsdata till ditt [!DNL Amazon Seller Central]-konto.

- [Avbryt beställningar](./cancel-unshipped-order.md) och välj ett orsakssvar.

- Visa [beställningsinformationen](./amazon-store-dashboard.md) för dina Amazon-beställningar.

## Rapportering

Med tillägget [!DNL Amazon Sales Channel] kan du granska rapportinformation om:

- Listor efter status för aktiv, inaktiv, giltig och ofullständig.

- Beställningar som väntar på leverans.

- De senaste beställningarna.

- Amazon [lista ändrar logg](./listing-changes-log.md) för att granska ändringar i produkt-/listfeed (som pris och kvantitet).

- Prissättningsdata för produkt [Buy Box](./buy-box-competitor-pricing.md).

- Produktens [lägsta konkurrentpris](./lowest-competitor-pricing.md)-data.

## Stöd för global försäljning

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Hantera flera [!DNL Amazon Marketplace] regioner (länder).

- Stöd för flera valutor med [Commerce valutakonfigurationsverktyg](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- Hantera leveranser från era produktplatser och Amazon leveranscentra.

## Kundhantering

Bygg din [!DNL Commerce]-kunddatabas genom att [importera kunddata](./order-settings.md#configure-order-settings) som är kopplad till dina Amazon-beställningar. Utöka er marknadsföringspotential med hjälp av den här utökade listan över kunder via [!DNL Amazon Marketplace]-listor och [!DNL Commerce] Store.


Det är enkelt att komma igång. En kort introduktionsprocess hjälper dig att skapa ett [!DNL Amazon Seller Central]-konto och integrera det med din Amazon-återförsäljare och din [!DNL Commerce]-katalog för att hantera Amazon listor, beställningar, lager och uppfyllelse. En central kontrollpanel visar statusuppdateringar för alla era Amazon-butiker-integreringar och Amazon-listor. Nå nya kunder i den globala [!DNL Amazon Marketplace] med förenklade och automatiserade processer - helt utan eller med lite kostnad och arbete för att konfigurera ett nytt system.

När du har integrerat ditt [!DNL Amazon Seller Central]-konto kan du med [!DNL Amazon Sales Channel]-tillägget hantera dina konton och synkronisera data mellan [!DNL Commerce] och Amazon. Det gör att du kan skapa listor, hantera kampanjer, ange priser och hantera lager och leveranser direkt via [!DNL Commerce]-administratören. Dessa alternativ inkluderar prisregler som övervakar Amazon priser för samma artikel och automatiskt anpassar priserna så att de blir mer konkurrenskraftiga.

