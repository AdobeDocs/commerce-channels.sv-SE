---
title: Om Amazon försäljningskanal
description: Använd Amazon-tillägget för säljkanaler för att smidigt integrera Adobe Commerce eller Magento Open Source med ditt Amazon Seller Central-konto.
exl-id: 11752491-d0da-4ff7-a0a7-d17d4fa1bfc9
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Om Amazon försäljningskanal

Kanalhanteraren för Adobe Commerce erbjuder tillägget för Amazon-försäljningskanal, som sömlöst integrerar din [!DNL Commerce]-administratör med ditt [!DNL Amazon Seller Central]-konto. Efter [introduktion](./amazon-onboarding-home.md) blir [!DNL Commerce] ett centralt kommandocenter för hantering och styrning av listor, order och lager för Amazon samt priser för din Amazon-butik.

[Store-](./store-integration.md) integrationer kopplar samman din  [!DNL Commerce] instans och Amazon för att synkronisera data mellan båda plattformarna. Amazon säljkanal:

- [Anlita ](./amazon-onboarding-home.md) och integrera ett eller flera  [!DNL Amazon Seller Central] konton med Adobe Commerce eller Magento Open Source.

- Importera och synkronisera dina befintliga Amazon-listor och matcha dem med produkter i din [!DNL Commerce]-katalog, vilket skapar en centraliserad produktkatalog.

- Skapa och hantera Amazon-listor för produkter i din [!DNL Commerce]-katalog.

- Visa och slutför beställningar (leverans) i [!DNL Commerce] och Amazon, synkning av orderstatus, betalning och återbetalningsinformation.

- Visa loggar för analyser och fel för [konkurrenskraftiga priser](./competitive-price-analysis.md), [liständringar](./listing-changes-log.md) och [kommunikationsproblem](./communication-errors-log.md).

I Amazon butiker kan du visa och hantera alla dessa funktioner, kontoinformation, listor, order med mera på Amazon säljkanal [hemsida](./amazon-sales-channel-home.md).

## Kampanjer och priser

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Synkronisera Amazon listpris till [!DNL Commerce] katalogpris (eller alternativt prisattribut).

- Aktivera MSRP [genomstrykningspris](./listing-price.md#configure-listing-price-settings) i dina Amazon-listor för att öka kundvärdesanspråken.

- Aktivera och hantera [lägsta annonspris (MAP)](./listing-price.md#configure-listing-price-settings) i dina Amazon-listor.

- Konfigurera ytterligare [moms](./listing-price.md#configure-listing-price-settings) i dina Amazon-priser.

- Ange ett anpassat värde för &quot;tillgängligt antal&quot; i dina [inställningar för lager/kvantitet](./stock-quantity.md#configure-stock--quantity-settings) som ska visas med dina Amazon-listor för att öka köparens trängsel.

## Prisregler

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Skapa staplingsbara, flexibla och komplexa [prisregler](./pricing-products.md) för att hantera dina Amazon-priser för daglig försäljning eller säsongskampanjer.

- Skapa [floor](./floor-price.md) och [tak](./optional-ceiling-price.md) för att skydda dina lägsta och högsta priser.

- Skapa och hantera [smarta omprisregler](./intelligent-repricing-rules.md) som automatiskt anpassar din produktprissättning i förhållande till andra Amazon-konkurrenter ([lägsta konkurrent](./lowest-competitor-pricing.md) och [Buy Box](./buy-box-competitor-pricing.md) pris).

## Katalogflödeshantering

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Importera dina befintliga Amazon-listor (produkter) och matcha med befintliga eller skapa produkter i din [!DNL Commerce]-katalog.

- Publicera dina [!DNL Commerce]-produkter på Amazon för att skapa Amazon-listor.

- Skapa [åsidosättningar](./creating-editing-overrides.md) för att ange ett individuellt meddelande om pris, hanteringstid, villkor och säljaranteckningar.

- Importera och mappa [attribut](./attributes-view.md) från dina Amazon-listor så att de automatiskt matchar produkter i din [!DNL Commerce]-katalog.

- Ställ in flera sökparametrar så att de matchar Amazon-listor i din [!DNL Commerce]-katalog.

- Definiera [listregler](./listing-rules.md) för att avgöra vilken av dina [!DNL Commerce]-produkter som kan listas på Amazon.

- Ange en standardtid för [hantering](./product-listing-actions.md) för dina nya Amazon-listor.

- Matcha listvillkoren baserat på ett [!DNL Commerce]-attribut.

- Lägg till säljaranteckningar för varje villkorstyp (valfritt).

- Implementera tröskelvärden för antal när du importerar Amazon-listor till din [!DNL Commerce]-katalog.

- Visa rekommenderade [listförbättringar](./listing-improvements.md).

## Orderhantering och kundtjänst

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Support och bearbetning av beställningar i Amazon och [!DNL Commerce].

- [Importera ](./order-settings.md#configure-order-settings) våra Amazon-order till  [!DNL Commerce] eller lämna dem i Amazon.

- Definiera vilka av dina [!DNL Commerce] webbplatshögar som ska kopplas till dina Amazon-beställningar för import och hantering av beställningar.

- Visa, avbryt och skicka beställningar från [!DNL Commerce] och/eller Amazon beroende på dina [leveransinställningar](./fulfilled-by.md).

- Mappa din Amazon-orderstatus till anpassad status inom [!DNL Commerce] (valfritt).

- Visa och hantera orderfel för att lösa problem och få kontakt med kunderna.

- Skicka orderspårningsdata till ditt [!DNL Amazon Seller Central]-konto.

- [Avbryt ](./cancel-unshipped-order.md) beställningar och välj ett orsakssvar.

- Visa [beställningsinformationen](./amazon-store-dashboard.md) för dina Amazon-order.

## Rapportering

Med tillägget [!DNL Amazon Sales Channel] kan du granska rapportinformation om:

- Listor efter status för aktiv, inaktiv, giltig och ofullständig.

- Beställningar som väntar på leverans.

- De senaste beställningarna.

- Amazon [med en lista ändras loggen](./listing-changes-log.md) för att granska ändringar av produkt-/listfeed (till exempel pris och kvantitet).

- Produkt [Buy Box](./buy-box-competitor-pricing.md) Konkurrentprisdata.

- Produkt [Lägsta konkurrentpris](./lowest-competitor-pricing.md) data.

## Stöd för global försäljning

Med tillägget [!DNL Amazon Sales Channel] kan du:

- Hantera flera [!DNL Amazon Marketplace]-regioner (länder).

- Stöd för flera valutor med [[!DNL Commerce] valutakonverteringsverktyget](https://docs.magento.com/user-guide/stores/currency-configuration.html){target=&quot;_blank&quot;}.

- Hantera leveranser från era produktplatser och Amazon leveranscentra.

## Kundhantering

Bygg din [!DNL Commerce] kunddatabas genom att [importera kunddata](./order-settings.md#configure-order-settings) som är kopplade till dina Amazon-beställningar. Utöka er marknadsföringspotential med den här expanderade listan över kunder via [!DNL Amazon Marketplace]-listor och [!DNL Commerce] butiker.
