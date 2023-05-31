---
title: "Introduktion till [!DNL Amazon Sales Channel]"
description: "[!DNL Amazon Sales Channel] gör det möjligt för handlare att smidigt sälja produkter i [!DNL Amazon Marketplace]."
redirect_from: /sales-channels/amazon/amazon-sales-channel.html
exl-id: a4a6f446-7029-4c92-bce3-5b857cc33056
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Introduktion till [!DNL Amazon Sales Channel]

Som Adobe Commerce eller Magento Open Source kan du använda [!DNL Amazon Sales Channel] för att integrera butikerna med världens största globala shoppingplats. Det här tillägget möjliggör Amazon försäljning genom att ansluta [!DNL Commerce] med [!DNL Amazon Seller Central] och erbjuder både automatisering och synkronisering av katalog- och orderdata. Hantera alla Amazon-listor, implementera enkla eller intelligenta prisregler och underhålla order och lager i en enda [!DNL Commerce] kontrollpanel.

Efter [onboarding](./amazon-onboarding-home.md), [!DNL Commerce] blir ett&quot;centralt kommandocentral&quot; för hantering och styrning av dina Amazon-listor, -beställningar och -lager samt priser för din Amazon-butik. [Integrering med Store](./store-integration.md) ansluter [!DNL Commerce] -instans och Amazon för att synkronisera data mellan båda plattformarna. Amazon säljkanal:

- [Inbyggt](./amazon-onboarding-home.md) och integrera en eller flera [!DNL Amazon Seller Central] konton hos Adobe Commerce eller Magento Open Source.

- Importera och synkronisera befintliga Amazon-listor och matcha med produkter i [!DNL Commerce] katalog, skapa en centraliserad produktkatalog.

- Skapa och hantera Amazon-listor för produkter i [!DNL Commerce] katalog.

- Visa och leverera (leverans) order i [!DNL Commerce] och Amazon, synkning av orderstatus, betalning och återbetalningsinformation.

- Visa loggar för analys och fel för [konkurrenskraftiga priser](./competitive-price-analysis.md), [liständringar](./listing-changes-log.md)och [kommunikationsfrågor](./communication-errors-log.md).

I Amazon butiker kan du visa och hantera alla dessa funktioner, kontoinformation, listor, beställningar med mera via Amazon försäljningskanal [hemsida](./amazon-sales-channel-home.md).

## Kampanjer och priser

Med [!DNL Amazon Sales Channel] kan du:

- Synkronisera Amazon listpriser till [!DNL Commerce] katalogpris (eller alternativt prisattribut).

- Aktivera MSRP [genomslagspriser](./listing-price.md#configure-listing-price-settings) i era Amazon-listor för att öka kundvärdesanspråken.

- Aktivera och hantera [Lägsta kampanjpris (MAP)](./listing-price.md#configure-listing-price-settings) i dina Amazon-listor.

- Konfigurera ytterligare [Moms](./listing-price.md#configure-listing-price-settings) till Amazon priser.

- Ange ett anpassat värde för&quot;tillgänglig kvantitet&quot; i [Inställningar för lager/kvantitet](./stock-quantity.md#configure-stock--quantity-settings) att visa med dina Amazon-listor för att öka köparens trängsel.

## Prisregler

Med [!DNL Amazon Sales Channel] kan du:

- Skapa stackningsbara, flexibla och komplexa [prisregler](./pricing-products.md) för att hantera era Amazon-priser för daglig försäljning eller säsongskampanjer.

- Skapa [floor](./floor-price.md) och [tak](./optional-ceiling-price.md) priser för att skydda dina lägsta och högsta priser.

- Skapa och hantera [regler för intelligent reprisering](./intelligent-repricing-rules.md) som automatiskt anpassar sina produktpriser i förhållande till andra Amazon-konkurrenter ([lägsta konkurrent](./lowest-competitor-pricing.md) och [Buy Box](./buy-box-competitor-pricing.md) pris).

## Katalogflödeshantering

Med [!DNL Amazon Sales Channel] kan du:

- Importera dina befintliga Amazon-listor (produkter) och matcha befintliga produkter eller skapa produkter i [!DNL Commerce] katalog.

- Publicera [!DNL Commerce] till Amazon för att skapa Amazon-listor.

- Skapa [åsidosättningar](./creating-editing-overrides.md) för att ange ett individuellt pris, hanteringstid, villkor och säljarens anteckningsmeddelande.

- Importera och mappa produkt [attributes](./attributes-view.md) från dina Amazon-listor så att de automatiskt matchar produkterna i [!DNL Commerce] katalog.

- Ange flera sökparametrar så att de matchar Amazon-listor [!DNL Commerce] katalog.

- Definiera [listregler](./listing-rules.md) för att avgöra vilken av [!DNL Commerce] kan listas på Amazon.

- Ange som standard [hanteringstid](./product-listing-actions.md) för dina nya Amazon-listor.

- Matcha listvillkoren baserat på en [!DNL Commerce] -attribut.

- Lägg till säljaranteckningar för varje villkorstyp (valfritt).

- Implementera tröskelvärden för antal när du importerar Amazon-listor till [!DNL Commerce] katalog.

- Visa rekommenderad [förbättringar av listor](./listing-improvements.md).

## Orderhantering och kundtjänst

Med [!DNL Amazon Sales Channel] kan du:

- Support och bearbetning av beställningar i Amazon och [!DNL Commerce].

- [Importera](./order-settings.md#configure-order-settings) dina Amazon-order [!DNL Commerce] eller lämna dem i Amazon.

- Ange vilken av dina [!DNL Commerce] webbutiker som kan kopplas till dina Amazon-beställningar för import och hantering av beställningar.

- Visa, annullera och skicka beställningar från [!DNL Commerce] och/eller Amazon beroende på [uppfyllandeinställningar](./fulfilled-by.md).

- Omvandla din Amazon-orderstatus till anpassad status inom [!DNL Commerce] (valfritt).

- Visa och hantera orderfel för att lösa problem och få kontakt med kunderna.

- Skicka orderspårningsdata till [!DNL Amazon Seller Central] konto.

- [Avbryt beställningar](./cancel-unshipped-order.md) och välja ett svar på orsaken.

- Visa [senaste order](./amazon-store-dashboard.md) information om dina Amazon-beställningar.

## Rapportering

Med [!DNL Amazon Sales Channel] kan du granska rapportinformation om:

- Listor efter status för aktiv, inaktiv, giltig och ofullständig.

- Beställningar som väntar på leverans.

- De senaste beställningarna.

- Amazon [blogg om ändringar](./listing-changes-log.md) för att granska produkt-/listningsändringar (såsom pris och kvantitet).

- Produkt [Buy Box](./buy-box-competitor-pricing.md) Konkurrentpriser.

- Produkt [Lägsta konkurrentpris](./lowest-competitor-pricing.md) data.

## Stöd för global försäljning

Med [!DNL Amazon Sales Channel] kan du:

- Hantera flera [!DNL Amazon Marketplace] regioner (länder).

- Stöd för flera valutor med [Konfigurationsverktyg för Commerce-valuta](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/currency/currency-configuration.html).

- Hantera leveranser från era produktplatser och Amazon leveranscentra.

## Kundhantering

Bygg [!DNL Commerce] kunddatabas per [importera kunddata](./order-settings.md#configure-order-settings) som är kopplade till dina Amazon-beställningar. Utöka er marknadsföringspotential med hjälp av den här utökade listan över kunder i er [!DNL Amazon Marketplace] listor och [!DNL Commerce] storefront.


Det är enkelt att komma igång. En kort introduktionsprocess hjälper dig att skapa en [!DNL Amazon Seller Central] och integrera med er Amazon-återförsäljare och [!DNL Commerce] katalog för att hantera Amazon listor, beställningar, lager och leveranser. En central kontrollpanel visar statusuppdateringar för alla era Amazon-butiker-integreringar och Amazon-listor. Nå nya kunder globalt [!DNL Amazon Marketplace] med förenklade och automatiserade processer - allt till lite eller ingen del av kostnaden och arbetet med att skapa ett nytt system.

När du har integrerat [!DNL Amazon Seller Central] konto, [!DNL Amazon Sales Channel] kan du hantera dina konton och synkronisera data mellan [!DNL Commerce] och Amazon. Det gör att ni kan skapa listor, hantera kampanjer, ange priser och hantera lager och leveranser direkt via [!DNL Commerce] Admin. Dessa alternativ inkluderar prisregler som övervakar Amazon priser för samma artikel och automatiskt anpassar priserna så att de blir mer konkurrenskraftiga.

