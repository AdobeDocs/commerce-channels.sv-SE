---
title: '"Hantera [!DNL Walmart Marketplace] Beställningar"'
description: '"Visa och hantera [!DNL Walmart Marketplace] order med [!DNL Channel Manager] för Adobe Commerce och Magento Open Source."'
exl-id: c2779c72-4793-445c-858a-867ea8389662
source-git-commit: eb57189ed866fffa064867d1de5ae9db5b32e283
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Hantera [!DNL Walmart Marketplace] order

[!DNL Walmart Marketplace] orderdata för [!DNL Commerce] produkter synkroniseras automatiskt till [!DNL Channel Manager] efter [!DNL Walmart] bearbetar ordern.

På Commerce-sidan utlöser en lyckad synkronisering följande åtgärder:

- [!DNL Channel Manager] skickar en orderbekräftelse till Walmart.

- En motsvarande handelsorder skapas från Walmart-ordern.

- Den uppdaterade orderinformationen visas på [!DNL Channel Manager] Kontrollpanel för beställningar.

I storefront Admin kan du visa orderdata från [!DNL Channel Manager] genom att öppna säljkanalsbutiken och välja **[!UICONTROL Orders]**.

![Vyn Kanalhanterarorder som ska hanteras [!DNL Walmart Marketplace] order](assets/orders-dashboard-view.png)

>[!NOTE]
>
>Det kan ta upp till 35 minuter i en [!DNL Walmart Marketplace] ordningen som visas i [!DNL Channel Manager] orderlista. [!DNL Walmart] tar ca 30 minuter att bearbeta inkommande order och skicka dem till [!DNL Channel Manager]. När Channel Manager har tagit emot beställningen tar det ytterligare fem minuter att skapa och visa beställningen i Adobe Commerce eller Magento Open Source.

## Beställningskontroller och kolumnbeskrivningar

I följande tabeller beskrivs de kontroller och kolumner som är tillgängliga för beställningar.

**Kontroller för[!UICONTROL Orders]**
| **Kontroll**                    | **Beskrivning**                                                                                                                                                                                                                                                                  | |—|—| | [!UICONTROL Filter orders]     | Sortera vyn genom att välja ett av alternativen [!UICONTROL Order Status] kort.                                                                                                                                                                                                           | | Felbeskrivning | Ger mer detaljerad information om beställningar med felstatus.                                                                                                                                                                                                            | | [!UICONTROL View order detail] | Om du vill visa orderdetaljer väljer du [!DNL Commerce] ordernummer i [!UICONTROL Order] tabell. Använd sedan [!DNL Commerce] orderalternativ för att bearbeta ordern.                                                                                                                    | | [!UICONTROL Channel Settings]  | Om du vill ändra kanalkonfigurationen väljer du autentiseringsuppgifter för kanal Walmart-anslutning, mappade attribut eller leveransidentifierare. Inställningarna väljer [!DNL Commerce] ordernummer i [!UICONTROL Order] tabell. Använd sedan [!DNL Commerce] orderalternativ för att bearbeta ordern. |


**Kolumnbeskrivningar**

| Fält | Beskrivning |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Walmart Order Number] | Inköpsordernummer som tilldelats ordern i [!DNL Walmart Marketplace]. När en order importeras till [!DNL Channel Manager], bara [!DNL Walmart] ordernummer visas. När [!DNL Commerce] order skapas, [!DNL Walmart] ordernumret lagras i [!UICONTROL External ID] produktattribut. |
| [!DNL Commerce] Ordernummer | Numret som tilldelats [!DNL Commerce] order som skapats från [!DNL Walmart Marketplace] beställa. |
| Objekt | Antal beställda artiklar [!DNL Walmart Marketplace]. |
| [!UICONTROL Order Value] | Total kostnad för beställda artiklar. |
| [!UICONTROL Date Ordered] | Datumet då ordern skickades den [!DNL Walmart Marketplace]. |
| [!UICONTROL Ship By Date] | Datum då ordern måste levereras av för att uppfylla [!DNL Walmart Marketplace] krav. |
| [!UICONTROL Deliver By Date] | Datum då ordern måste levereras till kunden för att kunna mötas [!DNL Walmart Marketplace] krav i UTC-format. |
| [!UICONTROL Ship Method] | The [[!DNL Walmart Marketplace] Leveranssätt](https://sellerhelp.walmart.com/s/guide?article=000007893) markerat för ordern. |
| [!UICONTROL Last Update At] | Tidsstämpel som anger senaste gången orderdata uppdaterades i [!DNL Channel Manager] i UTC-format. |
| [!UICONTROL Status] | Anger aktuell orderstatus i [!DNL Commerce] orderarbetsflöde. Ursprunglig status för en order som importerats från [!DNL Walmart Marketplace] är _Öppna_. Ytterligare statusuppdateringar inträffar när handelsorder bearbetas och [!DNL Channel Manager] har synkroniserat försändelse, partiell leverans och annulleringsuppdateringar för [!DNL Walmart Marketplace]. |
| [!UICONTROL Error Description] | Ger mer detaljerad information om beställningar med en _[!UICONTROL Error]_status. |

## Orderstatus


[!UICONTROL Order Status] innehåller information om det aktuella läget för [!DNL Walmart Marketplace] beställningar som hanteras från Adobe Commerce eller Magento Open Source. Uppdateringar av orderstatus när [!DNL Channel Manager] får uppdaterad orderinformation från antingen [!DNL Walmart Marketplace] eller [!DNL Commerce] ordersystem. Order kan ha följande status:

- **[!UICONTROL Shipped]**-Beställningar som har skickats från [!DNL Commerce] butik. När ordern levereras, [!DNL Channel Manager] skickar en uppdatering till [!DNL Walmart Marketplace] för att uppdatera leveransstatus på Walmart och ange orderspårningsnumret för leveransen.

- **[!UICONTROL Partially Shipped]**—Beställningar med artiklar markerade som levererade och andra som väntar på att skickas. När artiklar i orderleveransen [!DNL Channel Manager] skickar en uppdatering till [!DNL Walmart Marketplace] för att uppdatera leveransstatus till delvis levererad vid Walmart och ange orderspårningsnumret för leveransen.

- **[!UICONTROL Canceled]**-Beställningar som har avbrutits från [!DNL Commerce] butik.

   När ordern har annullerats [!DNL Commerce] Uppdateringar av lagerkvantitet för att spegla returnerade artiklar. Sedan [!DNL Channel Manager] synkroniserar uppdateringen till [!DNL Walmart Marketplace].

- **[!UICONTROL Error]**- Beställningar som innehåller fel. Fel kan uppstå när en orderuppdateringsåtgärd misslyckas. Exempel: fel uppstår om [!DNL Channel Manager] kan inte ta emot en ny beställning från Walmart. De kan också inträffa om [!DNL Channel Manager] kan inte skicka en orderleverans eller en annulleringsuppdatering till [!DNL Walmart Marketplace]. Om en åtgärd misslyckas visas en _Fel_ status för ordern. Mer information finns i [Åtgärda orderfel](process-orders.md#fix-shipping-and-cancelation-errors).

- **[!UICONTROL Error description]**-Innehåller detaljerad information om orderfel som inträffar på grund av t.ex. saknad information eller ogiltiga värden, felaktig leveransinformation eller misslyckad orderannullering. Beskrivningen hjälper till att avgöra om fel uppstod i [!DNL Commerce] eller på [!DNL Walmart Marketplace].

>[!NOTE]
>
>Om orderartiklar skickas i flera leveranser visas orderstatusen i [!DNL Channel Manager] återspeglar den senaste orderstatusen som är tillgänglig. Om till exempel det första objektet skickas och inga fel returneras när orderuppdateringarna synkroniseras med [!DNL Channel Manager] och [!DNL Walmart Marketplace], [!DNL Channel Manager] orderstatus är _[!UICONTROL Partially Shipped]_.  Om en andra artikel har levererats och [!Channel Manager] returnerar ett fel, orderstatusen uppdateras till_[!UICONTROL Error]_.

## Granska beställningar

1. Välj **[!UICONTROL Marketing]** > **[!UICONTROL Channel Manager]** för att öppna [!UICONTROL Channel Manager Marketplace Stores] sida.

1. Öppna butiksvyn genom att markera ögonikonen i en butikspostrad.

1. Om du vill visa orderinformation väljer du *[!UICONTROL *Orders]**.

1. Hämta information om beställningen och avgöra vilka steg som ska utföras genom att kontrollera **[Status](#about-order-status)** för att få information om beställningarna.

## Visa orderdetaljer

När en beställning har tagits emot från marknadsplatsen och importerats till Adobe Commerce eller Magento Open Source använder du [!DNL Commerce] Order-ID för att visa ordern i Adobe Commerce.

Från **[!UICONTROL Orders]** väljer du **[!UICONTROL Commerce Order Number]** för att öppna [!DNL Commerce] orderdetaljer.

![Detaljvy för handelsorder för en [!DNL Walmart Marketplace] order](assets/order-detail-with-external-order-id.png)

I Commerce Store importerar man order från [!DNL Walmart Marketplace] ha följande ytterligare information i orderuppgifterna:

- **Betalningsinformation och leveranssätt**-Beställningar som importeras från Walmart innehåller följande värden för betalnings- och leveransfält:

   - **[!UICONTROL Offline Channel Payment]**—Anger att orderbetalningen behandlas offline av [!DNL Walmart Marketplace].

   - **[!UICONTROL External Order Number]**—Visar [!DNL Walmart Marketplace] ordernummer.

   - **[!UICONTROL Channel Shipping - Value]**-Anger att fraktkostnader hanteras genom [!DNL Walmart Marketplace].

   - **[!UICONTROL Cancellation Reason]**-Det här fältet visas bara om en ordning har importerats från [!DNL Walmart Marketplace] har avbrutits. Orsaker till annullering är:

      - [!UICONTROL Price or other listing errors.]
      - [!UICONTROL The item is out of stock.]
      - [!UICONTROL Unavailable carrier or shipping information.]
      - [!UICONTROL Additional information is required by our Credit or Fraud Avoidance department.]

