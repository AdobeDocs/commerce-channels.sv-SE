---
title: Konfigurera produktmatchning
description: Mappa attribut för matchning av Commerce-produkter med befintliga Walmart Marketplace-listor
exl-id: 98c8d3f6-f129-43c6-920c-d9c36b0e4a40
source-git-commit: e6368d30e16ccffcb1dfc64bdd56561116934b54
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Konfigurera produktmatchning

Innan du publicerar en lista på Walmart Marketplace måste du mappa minst en unik identifierare från produktkatalogattributen till en av de produktidentifierare som krävs för Walmart Marketplace. Det här steget krävs för att matcha produkter på Walmart Marketplace.

För produktmatchning måste Commerce-produkten ha minst ett av följande produkt-ID (Product Identifiers) i katalogattributen.

**Nödvändiga Walmart-produkt-ID:n**

| **Godkänd typ** | **Namn** | **Syfte** | **Godtagbara siffror** |
|-------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| GTIN | Global handelspost | Allmänt ändamål, används världen över | 14 siffror |
| ISBN | Internationellt standardboknummer | Papperskopiering, maskinvaruservice och elektroniska böcker | 10 eller 13 siffror |
| ISSN | Internationellt standardserienummer | 8-siffrigt serienummer som används för att identifiera tidskrifter, tidningar, tidningar och tidskrifter av alla slag som levereras i alla slags medier och elektroniska | 8 siffror |
| ISBN | Internationellt standardboknummer | Återrapportering, maskinvaruservice och elektronisk | 12 siffror |

Om du har en annan typ av produkt-ID-attribut i katalogen konverterar du den till en av de obligatoriska typerna. Mappa det sedan till motsvarande Walmart Marketplace-attribut i listkonfigurationen för Channel Manager-butiken.

## Konfigurera inställningar för produktattribut

1. På [!UICONTROL Listings] sidan för den anslutna försäljningskanalen, välj en eller flera produkter i *Utkast* status.

1. Välj **[!UICONTROL Settings]**.

   - Hitta det Walmart Marketplace-attribut du vill mappa.

   - Välj motsvarande attribut i butikskatalogen.

      I följande exempel mappas UPC-attributet Walmart Marketplace till UPC-attributet i produktkatalogen.
   ![Mappningsattribut för produktmatchningsvillkor](assets/products-map-attributes-for--match.png)

   - Välj **[!UICONTROL Save]**.


## Uppdatera konfiguration för mappat attribut

Ändra identifieraren för Commerce-produkt för matchande produkter genom att uppdatera inställningarna för mappat attribut.

I stället för att matcha produkter som är baserade på produktattributkoden för Commerce UPC kan du matcha baserat på SKU. Eller mappa ytterligare attribut för att förbättra matchningen.

1. Från **[!UICONTROL Listings]**, markera **[!UICONTROL Settings]**.

1. I formuläret för mappningsattribut ändrar du konfigurationen för mappat attribut efter behov.
