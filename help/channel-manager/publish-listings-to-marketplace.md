---
title: Publicera listor till Walmart
description: Publicera listor för Commerce-produkter på Walmart Marketplace för att börja sälja.
source-git-commit: 2a9bd2f8f91e672786c36f5e132f99bcab59dd00
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---

# Publicera listor till Walmart

Precis som andra marknadsplatser tillåter Walmart tredjepartssäljare att lista artiklar som säljs av andra.

Plattformen använder produktidentifierare som UPC och GTIN för att matcha artiklar som redan är till salu.
För matchade produkter uppdateras den befintliga Walmart Marketplace-listan med erbjudandet för Commerce-produkten.
Vanligtvis visas produkter med lägst pris först i resultatet. Men även andra faktorer som granskningar påverkar placeringen.

## Matcha arbetsflöde

När du matchar produkter skickar Channel Manager produktdata till Walmart Marketplace för att söka efter befintliga listor med attributvärden som matchar det mappade Commerce-produktattributet.

Om en matchning hittas uppdateras den befintliga produktlistan så att ditt erbjudande läggs till.

## Förutsättningar

Innan du matchar produkter bör du kontrollera att produktkatalogattributvärdena uppfyller Walmart-kraven och konfigurera attributinställningarna. Se [Konfigurera produktmatchning](map-product-attributes-for-matching.md)

## Välj och matcha produkter

1. Öppna en ansluten försäljningskanal.

1. Från **[!UICONTROL Listings]** väljer du produkter för matchning i *[!UICONTROL Draft]* status.

   ![Välj produkter från listor och skicka för matchning](assets/products-in-marketplace-sales-channel.png)

1. Välj **[!UICONTROL Match Products]**.

   Ett meddelande anger antalet produkter som skickats för matchning.

   ![Skicka produkter till den anslutna försäljningskanalen](assets/products-submit-for-matching.png)

   Det kan ta upp till 30 minuter för Walmart Marketplace att slutföra matchningsåtgärden.

   Status för valda produkter ändras till *[!UICONTROL Processing]* tills matchningsåtgärderna har slutförts. Det kan ta upp till 30 minuter för Walmart Marketplace att slutföra matchningsåtgärden.

## Kontrollera matchningsstatus

1. Välj **Uppdatera produkter** för att uppdatera den senaste produktstatusen.

1. Kontrollera produktstatus.

   När matchningen är klar kan statusen vara *Matcha* eller *Fel*.

   * **[!UICONTROL Match]** anger att produkten matchades. Ditt produkterbjudande publicerades i en befintlig Walmart Marketplace-lista.

   * **[!UICONTROL Error]** anger något av följande:

      * Ett fel uppstod och matchningsåtgärden misslyckades.

      * Ingen matchning hittades.

      * Matchningen hittades, men produkten publicerades som mellanlagrad eftersom [Marketplace-butiken är inte aktiv](walmart-prerequisites.md#walmart-marketplace-store-status).

## Felsöka produktmatchningsfel

Om produktmatchningen misslyckas returnerar Walmart Marketplace en felkod och i Channel Manager visas felstatusen i produktlistinformationen.

Visa felmeddelanden genom att hovra över **Fel** statusetikett. Vanliga fel som returneras är felaktigt formaterade produkt-ID-värden eller nödvändiga attribut saknas.

## Korrigera produkt-ID-värden

| Typ | Beskrivning | Exempel |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, det tolvsiffriga talet inklusive kontrollsiffran.</br></br>Om din UPC har färre än 12 siffror, till exempel UPC-E med 8 siffror, lägger du till</br>inledande nollor för att uppfylla kravet. | Ändra från `45678912345` till `045678912345` |
| GTIN | GTIN-14, det 14-siffriga talet inklusive kontrollsiffran.</br></br>Om ditt GTIN innehåller färre än 14 siffror lägger du till inledande nollor </br>för att uppfylla kraven. | Ändra `456789123456` till `0045678912345` |
| EAN | GTIN-13, det 13-siffriga talet inklusive kontrollsiffran.</br></br>Om EAN har färre än 13 siffror lägger du till radavstånd</br>nollor för att uppfylla kravet. | Ändra från `4567891234` till `0004567891234` |

Mer information om felkoder på Walmart Marketplace finns i [Hjälp för Walmart Seller](https://sellerhelp.walmart.com/s/guide?article=000005844).
