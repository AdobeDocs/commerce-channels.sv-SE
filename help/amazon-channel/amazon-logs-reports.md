---
title: Loggar och arkivrapporter
description: Använd loggarna och lagra rapporter för att se vad som händer i din Adobe Commerce eller Magento Open Source store och i era Amazon Marketplace-listor.
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Loggar och butiksrapporter

Tillägget för Amazon-försäljningskanalen innehåller värdefulla loggar och butiksrapporter som gör att du kan visa ändringar som påverkar dina Amazon listor och beställningar. Du kan använda de här rapporterna för att se vad som händer i din butik och för att förstå olika liststatusar.

Inga åtgärder är tillgängliga för loggarna eller butiksrapporterna, eftersom de bara är granskningsfunktioner.

Följande loggar kan nås från [butikspanelen](./amazon-store-dashboard.md).

- I loggen [Listing Changes Log](./listing-changes-log.md) visas de ändringar som har gjorts i ditt Amazon Seller-konto som en spegling av inställningarna för din Amazon försäljningskanal.

- Loggen [Kommunikationsfel](./communication-errors-log.md) visar alla rapporterade kommunikationsfel med Amazon.

Följande butiksspecifika rapporter finns på [butiksdashboard](./amazon-store-dashboard.md).

- Rapporten [Konkurrenskursanalys](./competitive-price-analysis.md) visar att ditt Amazon _landade pris_ (listpris plus leveranspris) i relation till priset [på Buy Boxen](./buy-box-competitor-pricing.md) och [lägsta konkurrent](./lowest-competitor-pricing.md).

- Rapporten [Listing Improvements](./listing-improvements.md) visar alla föreslagna listförbättringar som Amazon erbjuder för den valda butiken.

>[!TIP]
>
>Du kan även kontrollera loggfilen för ytterligare information när felsökning behövs. Se [administratörsinställningar för försäljningskanal](./sales-channel-settings.md). Synkroniseringsloggning för Amazon-försäljningskanal skrivs till filen `{Commerce Root}/var/log/channel_amazon.log` och kan visas i [utvecklarläge](https://docs.magento.com/user-guide/magento/installation-modes.html){target=&quot;_blank&quot;}.
