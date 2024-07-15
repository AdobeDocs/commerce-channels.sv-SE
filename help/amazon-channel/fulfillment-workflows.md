---
title: Amazon arbetsflöden för leveranser
description: Uppfyllandet av en beställning från en Amazon-lista följer en specifik sekvens från beställning som skickas till leverans.
feature: Sales Channels, Orders, Shipping/Delivery
exl-id: 30dd9f97-9193-4c98-bded-e5d8d35b0d05
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---

# Amazon arbetsflöden för leveranser

## Exempel: uppfyllt av handlare

| Steg | Beskrivning |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **En order som uppfyller handelskraven läggs på Amazon.** Amazon tilldelar statusen `Pending` tills kundens kreditkortsinformation har verifierats. Beställningar med statusen `Pending` importeras automatiskt till Amazon-försäljningskanal, men visas inte på fliken _[!UICONTROL Orders]_. |
| 2 | **Beställningen verifieras av Amazon.** När det verifieras ändrar Amazon statusen till `Unshipped`. Med den här statusändringen uppdateras ordern i Amazon försäljningskanal och visas på fliken _[!UICONTROL Orders]_. |
| 3 | **Beställningsinformationen uppdateras.** Amazon försäljningskanal uppdaterar orderinformationen med pris, e-postadress och kundnamn. Under den här uppdateringen skapar Amazon-ordern motsvarande [!DNL Commerce]-ordning på orderhanteringssidan. Ordernumret [!DNL Commerce] visas med orderinformationen på fliken _[!UICONTROL Orders]_. |
| 4 | **Ett nytt kundkonto skapas.** Om den har konfigurerats i dina orderinställningar och kunden inte finns i din [!DNL Commerce]-databas skapas en ny kund i din [!DNL Commerce]-databas med motsvarande kundinformation från Amazon-beställningen. Om du väljer `No Customer Creation (guest)` i dina orderinställningar följer ordningen [!DNL Commerce]-gästprocessen och skapar inte en kund i din databas. Om ditt [!DNL Commerce]-system nu är integrerat med ett ERP/OMS/WMS hämtas ordern efter integreringen av en ny order som placeras och skapas i [!DNL Commerce]. |
| 5 | **Ordern skickas.** På sidan [!DNL Commerce] för orderbearbetning skickar du ordern och lägger till ett spårningsnummer. När alla objekt har markerats med statusen `Shipped`:<ul><li>Statusen för ordningen [!DNL Commerce] ändras till `Complete`.</li><li>Status för Amazon-försäljningskanalorder ändras till `Shipped`.</li><li>Spårningsnumret synkroniseras med Amazon och orderns status i Amazon ändras till `Shipped`.</li><li>Leveransmeddelanden skickas till kunden via Amazon, inte från [!DNL Commerce] (enligt Amazon policyer). |

## Exempel: uppfyllt av Amazon (FBA)

| Steg | Beskrivning |
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | **En Amazon-genomförd beställning placeras på Amazon.** |
| 2 | **Ordern importeras.** Ordern importeras inte till Amazon försäljningskanal förrän ordern har tilldelats statusen `Shipped` av Amazon. Eftersom Amazon har lager för den här produkten förhindrar den att det stör lagerställets-/lagerhanteringen. |
| 3 | **Beställningsinformationen uppdateras.** Om den är konfigurerad i dina [orderinställningar](./order-settings.md) skapar Amazon-ordningen motsvarande [!DNL Commerce]-ordning och skapas som en order med statusen `Complete`. |
