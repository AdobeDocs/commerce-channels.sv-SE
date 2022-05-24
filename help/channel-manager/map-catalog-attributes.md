---
title: Mappa katalogattribut
description: Mappningsattribut för matchning av [DNL! Commerce]-produkter till befintlig [!DNL Walmart Marketplace] listor och synkronisera data mellan [!DNL Channel Manager] och [!DNL Walmart].
exl-id: 6678d81f-d167-460d-b656-d082d56f670c
source-git-commit: fac4bbd3985e07b919f986c877b8584da797e6fe
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 0%

---

# Mappa katalogattribut

Innan du publicerar listor från [!DNL Commerce] till [!DNL Walmart Marketplace]måste du mappa minst en unik identifierare från [!DNL Commerce] katalog till motsvarande identifierare från Walmart.
Det här steget krävs för att matcha [!DNL Commerce] produkter till befintliga [!DNL Walmart] listor och synkronisera produktdata mellan [!DNL Commerce] och [!DNL Walmart].

För produktmatchning måste Commerce-produkten ha minst ett produktattribut som matchar någon av följande produkt-ID:n (produkt-ID) som krävs av [!DNL Walmart].

**Nödvändiga Walmart-produkt-ID:n**

| **Godkänd typ** | **Namn** | **Syfte** | **Godtagbara siffror** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Global handelspost | Allmänt ändamål, används världen över | 14 siffror |
| ISBN | Internationellt standardboknummer | Papperskopiering, maskinvaruservice och elektroniska böcker | 10 eller 13 siffror |
| ISSN | Internationellt standardserienummer | 8-siffrigt serienummer som används för att identifiera tidskrifter, tidningar, tidningar och tidskrifter av alla slag som levereras i alla slags medier och elektroniska | 8 siffror |
| UPC | Universell produktkod | Standardspårningskod | 12 siffror |

Om katalogen inte har något matchande attribut, [lägga till eller konvertera ett befintligt katalogattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html).

## Mappa unika identifierare

1. På [!UICONTROL Listings] sidan för säljkanalsbutiken, välj **[!UICONTROL Settings]**.

   - Hitta det Walmart Marketplace-attribut du vill mappa.

   - Välj motsvarande attribut i dialogrutan [!DNL Commerce] lagringskatalog.

      I följande exempel mappas UPC-attributet Walmart Marketplace till UPC-attributet i produktkatalogen.
   ![Mappningsattribut för produktmatchningsvillkor](assets/products-map-attributes-for-match.png)
   - Du kan också mappa flera attribut för att öka antalet träffar. Om du mappar fler än ett attribut väljer du ett som **Primär identifierare**. Detta

   - Välj **[!UICONTROL Save]**.


## Uppdatera konfiguration för mappat attribut

Ändra identifieraren för Commerce-produkt för matchande produkter genom att uppdatera inställningarna för mappat attribut.

I stället för att matcha produkter som är baserade på produktattributkoden för Commerce UPC kan du matcha baserat på SKU. Eller mappa ytterligare attribut för att förbättra matchningen.

1. Från **[!UICONTROL Listings]**, markera **[!UICONTROL Settings]**.

1. I formuläret för mappningsattribut ändrar du konfigurationen för mappat attribut efter behov.
