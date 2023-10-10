---
title: '[!DNL Channel Manager] Versionsinformation'
description: Den senaste versionsinformationen för [!DNL Channel Manager] från Adobe Commerce.
feature: Sales Channels, Release Notes
exl-id: 8f40ace1-6587-4185-955a-91bc16dee8ce
source-git-commit: 003efd3c1044284a7d2c86db5d3eb1abfb3898ea
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 3%

---

# [!DNL Channel Manager] Versionsinformation

I versionsinformationen beskrivs den första versionen av [!DNL Channel Manager] och innehåller:

![Nytt](../assets/new.svg) Nya funktioner
![Korrigerat problem](../assets/fix.svg) Korrigeringar och förbättringar
![Känt fel](../assets/bug.svg) Kända fel

Se [Kommande versioner](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) om du vill veta mer om releasescheman och support.

Se [Produkttillgänglighet](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) om du vill veta vilka Adobe Commerce-versioner som stöder det här tillägget.

## v2.1.0

*3 oktober 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Channel Manager är nu kompatibelt med [Adobe Commerce version 2.4.7 beta](https://experienceleague.adobe.com/docs/commerce-operations/release/beta.html) releaser.

## v2.0.0

*20 mars 2023*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg)<!--CHAN-5893--> Channel Manager är nu kompatibelt med Adobe Commerce version 2.4.6.

## v1.1.0

*23 november 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg)<!--CHAN-5204--> **Returer och återbetalningar**- Nu kan du bearbeta returleveranser och återbetalningsprocesser på Walmart Marketplace för beställningar som skickas via en Adobe Commerce- och Magento Open Source Channel Manager-butik. Information och uppdateringar om returer och återbetalningar synkroniseras mellan Walmart och Adobe Commerce så att aktuella data är tillgängliga i båda [!DNL Commerce] storefront och [!DNL Walmart Marketplace]. Se [Retur- och återbetalningsorder](return-refund-orders.md).

![Fast](../assets/fix.svg)<!--CHAN-5661--> Korrigerade `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` fel som uppstod vid omsynkronisering av kanalhanterarens orderdata med `bin/magento saas:resync --feed orders` -kommando. Felet löstes genom att kanalhanterarens paketberoenden uppdaterades för modulen Säljdataexport, som fick ett nytt namn `magento/module-sales-data-exporter` till `magento/module-sales-orders-data-exporter`.

## v1.0.0

*14 januari 2022*

[!BADGE Stöds]{type=Informative tooltip="Stöds"}

![Nytt](../assets/new.svg) Inledande version av Channel Manager för allmän tillgänglighet

