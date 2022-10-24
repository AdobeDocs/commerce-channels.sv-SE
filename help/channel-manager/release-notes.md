---
title: '''[!DNL Store Fulfillment by Walmart Commerce Technologies] Versionsinformation'
description: "Den senaste versionsinformationen för [!DNL Channel Manager] från Adobe Commerce."
source-git-commit: e9d2f53a955956a2b5086649d9ac18cc982ef4e3
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# [!DNL Channel Manager] Versionsinformation

I versionsinformationen beskrivs den första versionen av [!DNL Channel Manager] och innehåller:

![Nytt](../assets/new.svg) Nya funktioner
![Korrigerat problem](../assets/fix.svg) Korrigeringar och förbättringar
![Känt fel](../assets/bug.svg) Kända fel


## v1.1.0

![Nytt](../assets/new.svg)<!--CHAN-5204--> **Returer och återbetalningar**- Nu kan du bearbeta returleveranser och återbetalningsprocesser på Walmart Marketplace för beställningar som skickas via en Adobe Commerce- och Magento Open Source Channel Manager-butik. Information och uppdateringar om returer och återbetalningar synkroniseras mellan Walmart och Adobe Commerce så att aktuella data är tillgängliga i båda [!DNL Commerce] storefront och [!DNL Walmart Marketplace]. Se [Retur- och återbetalningsorder](return-refund-orders.md).

![Fast](../assets/fix.svg)<!--CHAN-5661--> Korrigerade `Class Magento\SalesDataExporter\MOdel\OrdersFeed does not exist` fel som uppstod vid omsynkronisering av kanalhanterarens orderdata med `bin/magento saas:resync --feed orders` -kommando. Felet löstes genom att kanalhanterarens paketberoenden uppdaterades för modulen Säljdataexport, som fick ett nytt namn `magento/module-sales-data-exporter` till `magento/module-sales-orders-data-exporter`.

## v1.0.0

Inledande version, kompatibel med följande Commerce-versioner:

* Open Source (CE): 2.4.x
* Adobe Commerce (EE): 2.4.x
* Adobe Commerce for Cloud (ECE): 2.4.x
* Stabilitet: Stabil
