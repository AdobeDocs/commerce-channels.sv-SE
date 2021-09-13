---
title: Amazon Fulfillment Workflows
description: Uppfyllandet av en beställning från en Amazon-lista följer en specifik sekvens från beställning som skickas till leverans.
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon arbetsflöden för leveranser

## Exempel: fullgjord av handlare

| Steg | Beskrivning |
|----|----|
| 3 | **En order som uppfyller handelskraven läggs på Amazon.** Amazon tilldelar status till  `Pending` tills kundens kreditkortsinformation har verifierats. Beställningar med statusen `Pending` importeras automatiskt till Amazon försäljningskanal, men visas inte på fliken _[!UICONTROL Orders]_. |
| 2 | **Ordern verifieras av Amazon.** När det är verifierat ändrar Amazon status till  `Unshipped`. Med den här statusändringen uppdateras ordern i Amazon försäljningskanal och visas på fliken _[!UICONTROL Orders]_. |
| 1 | **Orderinformationen uppdateras.** Amazon försäljningskanal uppdaterar orderinformationen med pris, e-post och kundnamn. Under den här uppdateringen skapar Amazon-ordern motsvarande [!DNL Commerce]-ordning på orderhanteringssidan. Ordernumret [!DNL Commerce] visas med orderinformationen på fliken _[!UICONTROL Orders]_. |
| 4 | **Ett nytt kundkonto skapas.** Om den konfigureras i dina orderinställningar och kunden inte finns i din  [!DNL Commerce] databas, skapas en ny kund i din  [!DNL Commerce] databas med motsvarande kundinformation från Amazon-beställningen. Om du väljer `No Customer Creation (guest)` i dina orderinställningar följer ordningen gästprocessen [!DNL Commerce] och skapar inte en kund i din databas. Om ditt [!DNL Commerce]-system är integrerat med ett ERP/OMS/WMS hämtas ordern efter integreringen av en ny order som placeras och skapas i [!DNL Commerce]. |
| 5 | **Ordern skickas.** På sidan för  [!DNL Commerce] orderbehandling skickar du ordern och lägger till ett spårningsnummer. När alla objekt är markerade med en `Shipped`-status:<ul><li>Statusen för ordningen [!DNL Commerce] ändras till `Complete`.</li><li>Statusen för Amazon säljkanalsorder ändras till `Shipped`.</li><li>Spårningsnumret synkroniseras med Amazon och orderns status i Amazon ändras till `Shipped`.</li><li>Leveransmeddelanden skickas till kunden via Amazon, inte från [!DNL Commerce] (enligt Amazon regler). |

## Exempel: Uppfylls av Amazon (FBA)

| Steg | Beskrivning |
|---|---|
| 3 | **En Amazon-beställning görs på Amazon.** |
| 2 | **Ordern importeras.** Ordern importeras inte till Amazon försäljningskanal förrän ordern har tilldelats  `Shipped` status av Amazon. Eftersom Amazon har lager för den här produkten förhindrar den att det stör lagerställets-/lagerhanteringen. |
| 1 | **Orderinformationen uppdateras.** Om den är konfigurerad i dina  [orderinställningar](./order-settings.md) skapar Amazon-ordern motsvarande  [!DNL Commerce] order och skapas som en order med statusen  `Complete`. |
