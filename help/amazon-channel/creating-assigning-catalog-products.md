---
title: Skapa och tilldela produkter för Amazon försäljningskanal
description: I Amazon Sales Channel finns fliken [!UICONTROL New Third Party] där du kan skapa och tilldela matchande Commerce-katalogprodukter med Amazon-listor.
feature: Sales Channels, Products, Configuration
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---

# Skapa och tilldela produkter

När du visar fliken _[!UICONTROL New Third Party]_kan du matcha dina [!DNL Commerce]-katalogprodukter mot en befintlig Amazon-lista. Det finns två alternativ för den här matchningen. Du kan tilldela en lista till en befintlig katalogprodukt eller så kan du använda informationen från listan för att skapa katalogprodukter. Dessa alternativ är användbara när dina Amazon-listor inte automatiskt matchar din [!DNL Commerce]-katalog.

Du måste matcha (eller tilldela) dina produkter med dina Amazon-listor för att kunna använda alla funktioner i Amazon försäljningskanal.

När du skapar en katalogprodukt från en Amazon-lista:

- **ASIN** blir [!DNL Commerce] SKU
- **Produktlistenamnet** blir kataloglistenamn
- **Price** och **Quantity** importeras från Amazon Listing

Resten av de nödvändiga inställningarna avgörs av de [!DNL Commerce]-produktinställningar som du valde när du skapade.

När listor skapas och matchas tas de bort från fliken _[!UICONTROL New Third Party]_och visas på fliken_[!UICONTROL Active]_.

## Tilldela en enskild katalogprodukt till en Amazon-lista

1. Visa dina produktlistor på fliken [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Leta upp listan som du vill tilldela i listan, klicka på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_och klicka på&#x200B;**[!UICONTROL Assign Catalog Product]**.

   Åtgärden öppnar sidan _[!UICONTROL Assign Magento Catalog Product]_.

1. Bläddra efter eller filtrera listan med hjälp av [arbetsytekontrollerna](./workspace-controls.md) och leta reda på rätt katalogprodukt som matchar listan.

1. När rätt produkt visas i listan klickar du på **[!UICONTROL Assign Catalog Product]** i kolumnen _[!UICONTROL Action]_.

Produkten och listan överensstämmer nu. Amazon försäljningskanal kan nu dela produkt- och listdata med Amazon och hantera din lista och information om den, inklusive listpris, fraktpris, aktie/kvantitet, orderinformation och status med mera.

## Skapa en katalogprodukt med Amazon listinformation

1. Visa dina produktlistor på fliken [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Leta reda på den lista du vill skapa i din [!DNL Commerce]-katalog, klicka på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_och klicka på&#x200B;**[!UICONTROL Create New Catalog Product]**.

   Åtgärden öppnar sidan _[!UICONTROL Create Magento Catalog Product]_.

1. Slutför produktens kataloginställningar.

   - Ställ in växlingen **[!UICONTROL Enable Product(s)]** till `Yes` eller `No` (krävs).

     |Ja|Välj om du vill att produkten ska vara berättigad till din [!DNL Commerce]-butiksförsäljning.|
|Nej|Välj att inte göra produkten berättigad till försäljning i [!DNL Commerce]-butiken.|

   - För **[!UICONTROL Categories]** tilldelar du en kategori för produkten (valfritt).

     Om du vill välja produktkategori klickar du på nedpilen och markerar en kategorikryssruta. Klicka på **[!UICONTROL Done]** när du är klar.

   - För **[!UICONTROL Website Ids]** väljer du den webbplats (storefront) som produkten ska kopplas till.

     Alternativen i den här listan beror på inställningarna för din [!DNL Commerce] [butikskonfiguration](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html).

   - Välj ett alternativ för **[!UICONTROL Attribute Set Id]** (obligatoriskt).

     `Default` är standardvalet. Alternativen i den här listan beror på de [!DNL Commerce] [attributuppsättningar](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) du har konfigurerat.

   - För **[!UICONTROL Visibility]** väljer du ett alternativ för den nya produkten.

     |**[!UICONTROL Not Visible Individually]** (standard)|Produkten ingår inte i din butikslista, men den kan finnas som en variant av en annan produkt.|
|**[!UICONTROL Catalog]**|Produkten visas i kataloglistorna.|
|**[!UICONTROL Search]**|Produkten är tillgänglig för sökåtgärder.|
|**[!UICONTROL Catalog and Search]**|Produkten ingår i kataloglistor och är tillgänglig för sökåtgärder.|

   - För **[!UICONTROL Assign Tax Class]** väljer du ett alternativ för produkten.

     Vilka alternativ som visas i den här listan beror på de [momsklasser](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) som du har konfigurerat.

   - Klicka på **[!UICONTROL Create Catalog Products]** när du är klar.

Katalogprodukten skapas i din [!DNL Commerce]-katalog och tilldelas till den Amazon-lista som den skapades från. När listan nu matchar en befintlig Amazon-lista tas listan bort från fliken _[!UICONTROL New Third Party]_och visas på fliken_[!UICONTROL Active]_.

## Skapa flera katalogprodukter med hjälp av deras Amazon listinformation

1. Visa dina produktlistor på fliken [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Välj de listor som katalogprodukterna ska skapas för.

   Du kan markera enskilda kryssrutor i den vänstra kolumnen eller klicka på nedpilen i den övre vänstra kolumnen och välja **[!UICONTROL Select All]** eller **[!UICONTROL Select All on this Page]**.

1. Klicka på **[!UICONTROL Create New Catalog Product(s)]** under _[!UICONTROL Actions]_.

1. Om du vill godkänna bekräftelsemeddelandet och öppna sidan _[!UICONTROL Create Magento Catalog Product]_klickar du på&#x200B;**[!UICONTROL OK]**.

1. Slutför kataloginställningarna för produkterna.

   >[!NOTE]
   >När du skapar katalogprodukter för flera valda listor används de angivna produktinställningarna för alla listor.

   - Ställ in växlingen **[!UICONTROL Enable Product(s)]** till `Yes` eller `No` (krävs).

     |Ja|Välj om du vill att produkten ska vara berättigad till din [!DNL Commerce]-butiksförsäljning.|
|Nej|Välj att inte göra produkten berättigad till försäljning i [!DNL Commerce]-butiken.|

   - För **[!UICONTROL Categories]** tilldelar du en kategori för produkten (valfritt).

     Om du vill välja produktkategori klickar du på nedpilen och markerar en kategorikryssruta. Klicka på **Klar** när du är klar.

   - För **[!UICONTROL Website Ids]** väljer du den webbplats (storefront) som produkten ska kopplas till.

     Alternativen i den här listan beror på inställningarna för din [!DNL Commerce] [butikskonfiguration](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html).

   - Välj ett alternativ för **[!UICONTROL Attribute Set Id]** (obligatoriskt).

     `Default` är standardvalet. Alternativen i den här listan beror på de [!DNL Commerce] [attributuppsättningar](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) du har konfigurerat.

   - För **[!UICONTROL Visibility]** väljer du ett alternativ för den nya produkten.

     |**[!UICONTROL Not Visible Individually]** (standard)|Produkten ingår inte i din butikslista, men den kan finnas som en variant av en annan produkt.|
|**[!UICONTROL Catalog]**|Produkten visas i kataloglistorna.|
|**[!UICONTROL Search]**|Produkten är tillgänglig för sökåtgärder.|
|**[!UICONTROL Catalog and Search]**|Produkten ingår i kataloglistor och är tillgänglig för sökåtgärder.|

   - För **[!UICONTROL Assign Tax Class]** väljer du ett alternativ för produkten.

     Vilka alternativ som visas i den här listan beror på de [momsklasser](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) som du har konfigurerat.

   - Klicka på **[!UICONTROL Create Catalog Products]** när du är klar.

Katalogprodukterna skapas i din [!DNL Commerce]-katalog och tilldelas till den Amazon-lista som den skapades från. När listorna nu matchar deras respektive Amazon-lista tas de bort från fliken [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) och visas på fliken [_[!UICONTROL Active]_](./active-listings.md).

![Skapa Commerce-katalogprodukt](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Product(s)] | (Obligatoriskt) Om den är aktiverad visas produkten i [!DNL Commerce]-butiken. Om den är inaktiverad visas inte produkten i din [!DNL Commerce]-butik. |
| [!UICONTROL Categories] | Du kan ange namnet på kategorin för den nya produkten eller välja en kategori genom att klicka på nedpilen för att visa dina alternativ. Alternativen beror på din [kategorikonfiguration](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html). |
| [!UICONTROL Website Ids] | (Obligatoriskt) Välj den webbplats (storefront) som produkten ska kopplas till. Alternativen beror på inställningarna för din [!DNL Commerce] [butikskonfiguration](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) |
| Attributuppsättnings-ID | Välj en attributuppsättning. Alternativen beror på dina konfigurerade [!DNL Commerce] [attributuppsättningar](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html). |
| [!UICONTROL Visibility] | Alternativ:<ul><li>**[!UICONTROL Not Visible Individually]** - Produkten är inte synlig i [!DNL Commerce]-butiken (vanligaste för variantprodukter).</li><li>**[!UICONTROL Catalog]** - Gör att produkten kan nås via den kategori som den är kopplad till på webbplatsen.</li><li>**Sök** - Tillåter att produkten bara hittas via sökverktyget.</li><li>**[!UICONTROL Catalog and Search]** - Tillåter att produkterna kan nås via kategoristrukturen och genom att använda sökverktyget.</li></ul> |
| [!UICONTROL Assign Tax Class] | Tilldela en momsklass till den nya produkten. Alternativen beror på dina konfigurerade [momsklasser](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html). |
