---
title: Loggar och lagra rapporter för Amazon-listor
description: Använd loggarna och lagra rapporter för att se vad som händer i din Adobe Commerce- eller Magento Open Source-butik och i era Amazon Marketplace-listor.
feature: Sales Channels, Logs
exl-id: 4654f718-d15f-4c3b-b984-ac7b9c29e6c4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Loggar och lagra rapporter för Amazon-listor

Tillägget för Amazon-försäljningskanalen innehåller värdefulla loggar och butiksrapporter som gör att du kan se ändringarna som påverkar dina Amazon listor och beställningar. Du kan använda de här rapporterna för att se vad som händer i din butik och för att förstå olika liststatusar.

Inga åtgärder är tillgängliga för loggarna eller butiksrapporterna, eftersom de bara är granskningsfunktioner.

Följande loggar kan nås från [lagringspanelen](./amazon-store-dashboard.md).

- [Loggen ](./listing-changes-log.md) med listningsändringar visar de ändringar som har gjorts i ditt Amazon Seller-konto som en spegling av inställningarna för din Amazon-försäljningskanal.

- Loggen [Kommunikationsfel ](./communication-errors-log.md) innehåller alla rapporterade kommunikationsfel med Amazon.

Följande butiksspecifika rapporter kan nås från [butiksinstrumentpanelen](./amazon-store-dashboard.md).

- Rapporten [Konkurrenskursanalys](./competitive-price-analysis.md) visar att ditt Amazon _landade pris_ (listpris plus leveranspris) i förhållande till priset [Buy Box](./buy-box-competitor-pricing.md) och [lägsta konkurrentpris](./lowest-competitor-pricing.md).

- Rapporten [Listing Improvements](./listing-improvements.md) visar alla föreslagna listförbättringar som Amazon erbjuder för den valda butiken.

>[!TIP]
>
>Du kan även kontrollera loggfilen för ytterligare information när felsökning behövs. Se [Administrationsinställningar för försäljningskanal](./sales-channel-settings.md). Synkroniseringsloggning för Amazon-försäljningskanal skrivs till filen `{Commerce Root}/var/log/channel_amazon.log` och kan visas i [utvecklarläge](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes).
