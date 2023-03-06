---
title: Loggar och arkivrapporter
description: Använd loggarna och lagra rapporter för att se vad som händer i din Adobe Commerce- eller Magento Open Source-butik och i era Amazon Marketplace-listor.
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# Loggar och arkivrapporter

Tillägget för Amazon-försäljningskanalen innehåller värdefulla loggar och butiksrapporter som gör att du kan se ändringarna som påverkar dina Amazon listor och beställningar. Du kan använda de här rapporterna för att se vad som händer i din butik och för att förstå olika liststatusar.

Inga åtgärder är tillgängliga för loggarna eller butiksrapporterna, eftersom de bara är granskningsfunktioner.

Följande loggar kan nås från [instrumentpanel för butik](./amazon-store-dashboard.md).

- The [Ändringslogg för lista](./listing-changes-log.md) visar de ändringar som har gjorts i ditt Amazon Seller-konto som en spegling av dina inställningar för Amazon försäljningskanal.

- The [Logg för kommunikationsfel](./communication-errors-log.md) visar eventuella rapporterade kommunikationsfel med Amazon.

Följande butiksspecifika rapporter finns på [instrumentpanel för butik](./amazon-store-dashboard.md).

- The [Konkurrenskraftprisanalys](./competitive-price-analysis.md) rapporten visar att din Amazon _landat pris_ (noteringspris plus frakt) i förhållande till [Buy Box](./buy-box-competitor-pricing.md) pris och [lägsta konkurrent](./lowest-competitor-pricing.md) pris.

- The [Förbättringar av listor](./listing-improvements.md) rapporten innehåller alla föreslagna listförbättringar som Amazon erbjuder för den valda butiken.

>[!TIP]
>
>Du kan även kontrollera loggfilen för ytterligare information när felsökning behövs. Se [administratörsinställningar för försäljningskanal](./sales-channel-settings.md). Synkroniseringsloggning för Amazon-försäljningskanal skrivs till `{Commerce Root}/var/log/channel_amazon.log` och kan visas i [utvecklarläge](https://docs.magento.com/user-guide/magento/installation-modes.html){target="_blank"}.
