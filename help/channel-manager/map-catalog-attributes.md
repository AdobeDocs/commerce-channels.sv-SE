---
title: Mappa katalogattribut
description: Mappningsattribut för matchning av [DNL! Commerce]-produkter till befintlig [!DNL Walmart Marketplace] listor och synkronisera data mellan [!DNL Channel Manager] och [!DNL Walmart].
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: 97128dcf45d7672e958c771f88389aba40c6e39e
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Mappa katalogattribut

Innan du ansluter listor från [!DNL Commerce] till [!DNL Walmart Marketplace]måste du mappa minst en unik identifierare från [!DNL Commerce] katalog till motsvarande identifierare från Walmart.

Det här steget krävs för att matcha [!DNL Commerce] produkter till befintliga [!DNL Walmart] listor och synkronisera produktdata mellan [!DNL Commerce] och [!DNL Walmart]. The [!DNL Commerce] produkten måste ha minst ett produktattribut som matchar någon av följande produkt-ID:n (produkt-ID) som krävs av [!DNL Walmart].

**Obligatoriskt [!DNL Walmart] produkt-ID**

| **Godkänd typ** | **Namn** | **Syfte** | **Godtagbara siffror** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Global handelspost | Allmänt ändamål, används världen över | 14 siffror |
| ISBN | Internationellt standardboknummer | Papperskopiering, maskinvaruservice och elektroniska böcker | 10 eller 13 siffror |
| ISSN | Internationellt standardserienummer | 8-siffrigt serienummer som används för att identifiera tidskrifter, tidningar, tidningar och tidskrifter av alla slag som levereras i alla slags medier och elektroniska | 8 siffror |
| UPC | Universell produktkod | Standardspårningskod | 12 siffror |

Om katalogen inte har något matchande attribut, [lägga till eller konvertera ett befintligt katalogattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## Mappa unika identifierare

1. Från **[!UICONTROL Listings]** eller **[!UICONTROL Orders]** sidan för säljkanalsbutiken, välj **[!UICONTROL Channel Settings]**.

1. På **[!UICONTROL Channel Settings]**, markera **[!UICONTROL Shipping Carriers]**.

   - Hitta [!DNL Walmart Marketplace] attribut att mappa.

   - Välj motsvarande attribut i dialogrutan [!DNL Commerce] lagringskatalog.

      Följande exempel mappar [!UICONTROL Walmart Marketplace UPC] attribut till UPC-attributet i produktkatalogen.
   ![Mappningsattribut för produktmatchningsvillkor](assets/products-map-attributes-for-match.png)

   - Välj **[!UICONTROL Save]**.


