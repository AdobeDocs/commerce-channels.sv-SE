---
title: '"Hantera [!DNL Walmart Marketplace] Beställningar"'
description: '"Visa och hantera [!DNL Walmart Marketplace] order med [!DNL Channel Manager] för Adobe Commerce och Magento Open Source."'
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: e3b12c9ce1ad4b5be17284e98956a773d7ccca24
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Hantera [!DNL Walmart Marketplace] order

[!DNL Walmart Marketplace] order för [!DNL Commerce] produktlistor synkroniseras automatiskt till [!DNL Channel Manager] efter [!DNL Walmart] bearbetar ordern. När synkroniseringen är klar kan du visa orderinformation genom att välja **[!UICONTROL Orders]** från den anslutna kanalbutiksvyn i [!DNL Channel Manager].

![Vyn Kanalhanterarorder som ska hanteras [!DNL Walmart Marketplace] order](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Det kan ta upp till 35 minuter i en [!DNL Walmart Marketplace] ordningen som visas i [!DNL Channel Manager] orderlista. [!DNL Walmart] tar ca 30 minuter att bearbeta inkommande order och skicka dem till [!DNL Channel Manager]. När Channel Manager har tagit emot beställningen tar det ytterligare fem minuter att skapa och visa beställningen i Adobe Commerce eller Magento Open Source.

## Granska beställningar

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** för att öppna [!UICONTROL Channel Manager Marketplace Stores] sida.

1. Öppna butiksvyn genom att välja pennikonen i en butikspostrad.

1. Om du vill visa orderinformation väljer du *[!UICONTROL *Orders]**.

1. Hämta information om beställningen och avgöra vilka steg som ska utföras genom att kontrollera **[Status](#about-order-status)** för att få information om beställningarna.

## Visa orderdetaljer

När en beställning har tagits emot från marknadsplatsen och importerats till Adobe Commerce eller Magento Open Source använder du [!DNL Commerce] Order-ID för att visa ordern i Adobe Commerce.

Från **[!UICONTROL Orders]** väljer du **[!UICONTROL Commerce Order Number]** för att öppna [!DNL Commerce] orderdetaljer.

![Detaljvy för handelsorder för en [!DNL Walmart Marketplace] order](assets/order-detail-with-external-order-id.png)

### Beställningskontroller och kolumnbeskrivningar

I följande tabeller beskrivs de kontroller och kolumner som är tillgängliga för beställningar.

**Kontroller för[!UICONTROL Orders]**
| **Kontroll**                    | **Beskrivning**                                                                                                                                               | |—|—| | [!UICONTROL Filter orders]     | Sortera vyn genom att välja ett av alternativen [!UICONTROL Order Status] kort.                                                                                        | | Information om felmeddelande | Hovra över [!UICONTROL Error Status] om du vill se ett detaljerat felmeddelande.                                                                      | | [!UICONTROL View order detail] | Om du vill visa orderdetaljer väljer du [!DNL Commerce] ordernummer i [!UICONTROL Order] tabell. Använd sedan [!DNL Commerce] orderalternativ för att bearbeta ordern. |

**Kolumnbeskrivningar**

| Fält | Beskrivning |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL  Walmart Order Number] | Inköpsordernummer som tilldelats ordern i [!DNL Walmart Marketplace]. När en order importeras till [!DNL Channel Manager], bara [!DNL Walmart] ordernummer visas. När [!DNL Commerce] order skapas, [!DNL Walmart] ordernumret lagras i [!UICONTROL External ID] produktattribut. |
| [!DNL Commerce]  Ordernummer | Numret som tilldelats [!DNL Commerce]  order som skapats från [!DNL Walmart Marketplace] beställa. |
| Objekt | Antal beställda artiklar [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Total kostnad för beställda artiklar. |
| [!UICONTROL Date Created] | Det datum då ordern skapades den [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Datum då ordern måste levereras av för att uppfylla [!DNL Walmart Marketplace] krav. |
| [!UICONTROL Deliver By Date] | Datum då ordern måste levereras till kunden för att kunna mötas [!DNL Walmart Marketplace] krav. |
| [!UICONTROL Last Update At] | Tidsstämpel som anger senaste gången orderdata uppdaterades i [!DNL Channel Manager] |
| [!UICONTROL Status] | Anger aktuell orderstatus i [!DNL Commerce] orderarbetsflöde. Statusen uppdateras när du har lagt till produkter i [!DNL Channel Manager] och när du matchar produkter på [!DNL Walmart Marketplace]. Om en åtgärd misslyckas visas felstatusen i listan. När du har åtgärdat felet [!DNL Channel Manager] försöker utföra åtgärden igen och uppdaterar statusen. |
| [!UICONTROL Error Description] | Ger mer detaljerad information om beställningar med en *Fel* status. |

### Om orderstatus


[!UICONTROL Order Status] innehåller information om det aktuella läget för [!DNL Walmart Marketplace] beställningar som hanteras från Adobe Commerce eller Magento Open Source. Uppdateringar av orderstatus när [!DNL Channel Manager] får uppdaterad orderinformation från antingen [!DNL Walmart Marketplace] eller [!DNL Commerce] ordersystem. Order kan ha följande status:

* **[!UICONTROL Open]**-Beställningar från [!DNL Walmart Marketplace] som kan granskas och behandlas i Adobe Commerce eller Magento Open Source.

   Efter att kunden beställt en produkt från [!DNL Walmart Marketplace]kan det ta upp till 35 minuter för den öppna ordern att visas i orderarbetsytan för den anslutna kanalen. [!DNL Commerce] tar ca 30 minuter att bearbeta inkommande order och skicka dem till [!DNL Channel Manager]. När Channel Manager tar emot beställningen tar det ytterligare fem minuter att skapa och visa [!DNL Commerce] beställa.

* **[!UICONTROL Processed]**-Beställningar som har skickats, annullerats eller återbetalats från [!DNL Commerce] butik.

   Om du vill visa alla levererade, annullerade och återfinansierade order väljer du **Behandlad** statuskort.

* **[!UICONTROL Canceled]**-Beställningar som har avbrutits från [!DNL Commerce] butik.

   När ordern har annullerats [!DNL Commerce] Uppdateringar av lagerkvantitet för att spegla returnerade artiklar. Sedan [!DNL Channel Manager] synkroniserar uppdateringen till [!DNL Walmart Marketplace].

* **[!UICONTROL Refunded]**-Beställningar som har återbetalats från [!DNL Commerce] butik.

   När återbetalningen är klar [!DNL Commerce] Uppdateringar av lagerkvantitet för att spegla återförda artiklar. Sedan [!DNL Channel Manager] synkroniserar uppdateringen till [!DNL Walmart Marketplace].

* **[!UICONTROL Error]**- Beställningar som innehåller fel. Fel kan uppstå när en orderuppdateringsåtgärd misslyckas. Exempel: fel uppstår om [!DNL Channel Manager] kan inte ta emot en ny beställning från Walmart. De kan också inträffa om [!DNL Channel Manager] kan inte skicka en orderleverans eller en annulleringsuppdatering till [!DNL Walmart Marketplace].

* **[!UICONTROL Error description]**-Innehåller detaljerad information om orderfel som inträffar på grund av t.ex. saknad information eller ogiltiga värden, felaktig leveransinformation eller misslyckad orderannullering. Beskrivningen hjälper till att avgöra om fel uppstod i [!DNL Commerce] eller på [!DNL Walmart Marketplace].
