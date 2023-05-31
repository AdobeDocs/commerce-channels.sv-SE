---
title: Amazon arbetsflöden för leveranser
description: Uppfyllandet av en beställning från en Amazon-lista följer en specifik sekvens från beställning som skickas till leverans.
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon arbetsflöden för leveranser

## Exempel: fullgjord av handlare

| Steg | Beskrivning |
|----|----|
| 1 | **En order som uppfyller handelskraven läggs på Amazon.** Amazon tilldelar status `Pending` tills kundens kreditkortsinformation har verifierats. Beställningar i `Pending` status automatiskt importeras till Amazon försäljningskanal, men visas inte på _[!UICONTROL Orders]_-fliken. |
| 2 | **Ordern verifieras av Amazon.** När det är verifierat ändrar Amazon statusen till `Unshipped`. Med den här statusändringen uppdateras ordern i Amazon försäljningskanal och visas i _[!UICONTROL Orders]_-fliken. |
| 3 | **Orderinformationen uppdateras.** Amazon försäljningskanal uppdaterar orderinformationen med pris, e-post och kundnamn. Under den här uppdateringen skapar Amazon-ordern motsvarande [!DNL Commerce] beställning på orderhanteringssidan. The [!DNL Commerce] ordernumret visas med orderinformationen på _[!UICONTROL Orders]_-fliken. |
| 4 | **Ett nytt kundkonto skapas.** Om den är konfigurerad i dina orderinställningar och kunden inte finns i din [!DNL Commerce] databas skapas en ny kund i din [!DNL Commerce] databas med motsvarande kundinformation från Amazon-beställningen. Om du valde `No Customer Creation (guest)` i orderinställningarna följer ordningen [!DNL Commerce] gästprocess och inte skapa en kund i din databas. Om [!DNL Commerce] systemet är integrerat med ERP/OMS/WMS, beställningen hämtas efter integreringen av en ny order som placeras och skapas inuti [!DNL Commerce]. |
| 5 | **Ordern skickas.** Från [!DNL Commerce] beställningssidan skickar du beställningen och lägger till ett spårningsnummer. När alla objekt är markerade i en `Shipped` status:<ul><li>Status för [!DNL Commerce] beställ ändringar i `Complete`.</li><li>Status för Amazon-försäljningskanalorder ändras till `Shipped`.</li><li>Spårningsnumret synkroniseras med Amazon och orderstatusen i Amazon ändras till `Shipped`.</li><li>Leveransmeddelanden skickas till kunden via Amazon, inte från [!DNL Commerce] (enligt Amazon regler). |

## Exempel: Uppfylls av Amazon (FBA)

| Steg | Beskrivning |
|---|---|
| 1 | **En Amazon-beställning görs på Amazon.** |
| 2 | **Ordern importeras.** Ordern importeras inte till Amazon försäljningskanal förrän ordern har tilldelats `Shipped` status av Amazon. Eftersom Amazon har lager för den här produkten förhindrar den att det stör lagerställets-/lagerhanteringen. |
| 3 | **Orderinformationen uppdateras.** Om den är konfigurerad i [orderinställningar](./order-settings.md)skapar Amazon-ordern motsvarande [!DNL Commerce] beställa och skapa som en order med statusen `Complete`. |
