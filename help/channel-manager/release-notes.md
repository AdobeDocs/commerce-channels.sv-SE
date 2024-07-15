---
title: Versionsinformation för [!DNL Channel Manager]
description: Den senaste versionsinformationen för  [!DNL Channel Manager] från Adobe Commerce.
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Versionsinformation för [!DNL Channel Manager]

Dessa versionsinformation beskriver den första versionen av [!DNL Channel Manager] och innehåller:

![Nya](../assets/new.svg) nya funktioner
![ Åtgärdat problem ](../assets/fix.svg) Korrigeringar och förbättringar
![Kända fel](../assets/bug.svg)

Läs [Kommande releaser](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) om du vill veta mer om releasescheman och support.

Se [Produkttillgänglighet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) om du vill veta vilka Adobe Commerce-versioner som stöder det här tillägget.

## v2.1.0

*3 oktober 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Ny](../assets/new.svg) kanalhanterare är nu kompatibel med [betaversioner av Adobe Commerce version 2.4.7](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html).

## v2.0.0

*20 mars 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Ny](../assets/new.svg)<!--CHAN-5893--> kanalhanterare är nu kompatibel med Adobe Commerce version 2.4.6.

## v1.1.0

*23 november 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg)<!--CHAN-5204--> **Returnerar och återbetalar** - Nu kan du bearbeta returnerings- och återbetalningsprocessen för Walmart Marketplace för order som levereras via en Adobe Commerce- och Magento Open Source Channel Manager-butik. Information och uppdateringar om returer och återbetalningar synkroniseras mellan Walmart och Adobe Commerce så att aktuella data är tillgängliga i både [!DNL Commerce]-butiken och [!DNL Walmart Marketplace]. Se [Retur- och återbetalningsorder](return-refund-orders.md).

![Korrigerat](../assets/fix.svg)<!--CHAN-5661--> `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist`-felet som inträffade när kanalhanterarens orderdata synkroniserades om med kommandot `bin/magento saas:resync --feed orders` har åtgärdats. Felet löstes genom att kanalhanterarens paketberoenden uppdaterades för modulen Säljdataexport, som fick ett nytt namn från `magento/module-sales-data-exporter` till `magento/module-sales-orders-data-exporter`.

## v1.0.0

*14 januari 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Ny](../assets/new.svg) första version av Channel Manager för allmän tillgänglighet

