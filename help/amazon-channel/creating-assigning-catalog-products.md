---
title: Skapa och tilldela produkter för Amazon försäljningskanal
description: Amazon Sales Channel tillhandahåller [!UICONTROL New Third Party] för att skapa och tilldela matchande Commerce-katalogprodukter med Amazon-listor.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 077d680da3c98ef9a48958eb548a9d5c1612f74e
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# Skapa och tilldela produkter

Vid visning _[!UICONTROL New Third Party]_kan du matcha [!DNL Commerce] katalogprodukter till en befintlig Amazon-lista. Det finns två alternativ för den här matchningen. Du kan tilldela en lista till en befintlig katalogprodukt eller så kan du använda informationen från listan för att skapa katalogprodukter. Dessa alternativ är användbara när dina Amazon-listor inte automatiskt matchar dina [!DNL Commerce] katalog.

Du måste matcha (eller tilldela) dina produkter med dina Amazon-listor för att kunna använda alla funktioner i Amazon försäljningskanal.

När du skapar en katalogprodukt från en Amazon-lista:

- The **ASIN** blir [!DNL Commerce] SKU
- The **Produktlistenamn** blir kataloglistans namn
- The **Pris** och **Kvantitet** importeras från Amazon Listing

Resten av de nödvändiga inställningarna bestäms av [!DNL Commerce] produktinställningar som du väljer när du skapar.

När listor skapas och matchas tas de bort från _[!UICONTROL New Third Party]_och visas på_[!UICONTROL Active]_ -fliken.

## Tilldela en enskild katalogprodukt till en Amazon-lista

1. Visa dina produktlistor på [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) -fliken.

1. Sök efter den lista du vill tilldela i listan genom att klicka på **[!UICONTROL Select]** i _[!UICONTROL Action]_kolumn och klicka på&#x200B;**[!UICONTROL Assign Catalog Product]**.

   Den här åtgärden öppnar _[!UICONTROL Assign Magento Catalog Product]_sida.

1. Bläddra efter eller filtrera listan med [arbetsytekontroller](./workspace-controls.md) och hitta rätt katalogprodukt som matchar listan.

1. När rätt produkt visas i listan klickar du på **[!UICONTROL Assign Catalog Product]** i _[!UICONTROL Action]_kolumn.

Produkten och listan överensstämmer nu. Amazon försäljningskanal kan nu dela produkt- och listdata med Amazon och hantera din lista och information om den, inklusive listpris, fraktpris, aktie/kvantitet, orderinformation och status med mera.

## Skapa en katalogprodukt med Amazon listinformation

1. Visa dina produktlistor på [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) -fliken.

1. Hitta den lista du vill skapa i [!DNL Commerce] katalog, klicka på **[!UICONTROL Select]** i _[!UICONTROL Action]_kolumn och klicka på&#x200B;**[!UICONTROL Create New Catalog Product]**.

   Den här åtgärden öppnar _[!UICONTROL Create Magento Catalog Product]_sida.

1. Slutför produktens kataloginställningar.

   - Ange **[!UICONTROL Enable Product(s)]** växla till `Yes` eller `No` (obligatoriskt).

      |Ja|Välj om du vill att produkten ska vara berättigad till din [!DNL Commerce] butiksförsäljning.| |Nej|Välj att inte göra produkten tillgänglig för din [!DNL Commerce] butiksförsäljning.|

   - För **[!UICONTROL Categories]**, tilldela en kategori för produkten (valfritt).

      Klicka på nedpilen och markera en kategorikryssruta för att välja produktkategori. Klicka **[!UICONTROL Done]** när du är klar.

   - För **[!UICONTROL Website Ids]** väljer du den webbplats (storefront) som produkten ska kopplas till.

      Vilka alternativ som finns i listan beror på [!DNL Commerce] [lagringskonfiguration](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) inställningar.

   - För **[!UICONTROL Attribute Set Id]** (obligatoriskt) väljer du ett alternativ.

      `Default` är standardvalet. Vilka alternativ som finns i listan beror på [!DNL Commerce] [attributuppsättningar](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) du har konfigurerat.

   - För **[!UICONTROL Visibility]** väljer du ett alternativ för den nya produkten.

      |**[!UICONTROL Not Visible Individually]** (standard)|Produkten ingår inte i din butikslista, men den kan finnas som en variant av en annan produkt.| |**[!UICONTROL Catalog]**|Produkten visas i kataloglistorna.| |**[!UICONTROL Search]**|Produkten är tillgänglig för sökåtgärder.| |**[!UICONTROL Catalog and Search]**|Produkten ingår i kataloglistor och är tillgänglig för sökåtgärder.|

   - För **[!UICONTROL Assign Tax Class]** väljer du ett alternativ för produkten.

      Vilka alternativ som visas i den här listan beror på [momsklasser](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) du har konfigurerat.

   - När du är klar klickar du på **[!UICONTROL Create Catalog Products]**.

Katalogprodukten skapas i [!DNL Commerce] och tilldelas till den Amazon-lista som den skapades från. När listan nu matchar en befintlig Amazon-lista tas den bort från _[!UICONTROL New Third Party]_och visas i_[!UICONTROL Active]_ -fliken.

## Skapa flera katalogprodukter med hjälp av deras Amazon listinformation

1. Visa dina produktlistor på [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) -fliken.

1. Välj de listor som katalogprodukterna ska skapas för.

   Du kan markera enskilda kryssrutor i den vänstra kolumnen eller klicka på nedpilen i den övre vänstra kolumnen och välja **[!UICONTROL Select All]** eller **[!UICONTROL Select All on this Page]**.

1. Under _[!UICONTROL Actions]_, klicka **[!UICONTROL Create New Catalog Product(s)]**.

1. Om du vill godkänna bekräftelsemeddelandet och öppna _[!UICONTROL Create Magento Catalog Product]_sida, klicka **[!UICONTROL OK]**.

1. Slutför kataloginställningarna för produkterna.

   >[!NOTE]
   >När du skapar katalogprodukter för flera valda listor används de angivna produktinställningarna för alla listor.

   - Ange **[!UICONTROL Enable Product(s)]** växla till `Yes` eller `No` (obligatoriskt).

      |Ja|Välj om du vill att produkten ska vara berättigad till din [!DNL Commerce] butiksförsäljning.| |Nej|Välj att inte göra produkten tillgänglig för din [!DNL Commerce] butiksförsäljning.|

   - För **[!UICONTROL Categories]**, tilldela en kategori för produkten (valfritt).

      Klicka på nedpilen och markera en kategorikryssruta för att välja produktkategori. Klicka **Klar** när du är klar.

   - För **[!UICONTROL Website Ids]** väljer du den webbplats (storefront) som produkten ska kopplas till.

      Vilka alternativ som finns i listan beror på [!DNL Commerce] [lagringskonfiguration](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) inställningar.

   - För **[!UICONTROL Attribute Set Id]** (obligatoriskt) väljer du ett alternativ.

      `Default` är standardvalet. Vilka alternativ som finns i listan beror på [!DNL Commerce] [attributuppsättningar](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html) du har konfigurerat.

   - För **[!UICONTROL Visibility]** väljer du ett alternativ för den nya produkten.

      |**[!UICONTROL Not Visible Individually]** (standard)|Produkten ingår inte i din butikslista, men den kan finnas som en variant av en annan produkt.| |**[!UICONTROL Catalog]**|Produkten visas i kataloglistorna.| |**[!UICONTROL Search]**|Produkten är tillgänglig för sökåtgärder.| |**[!UICONTROL Catalog and Search]**|Produkten ingår i kataloglistor och är tillgänglig för sökåtgärder.|

   - För **[!UICONTROL Assign Tax Class]** väljer du ett alternativ för produkten.

      Vilka alternativ som visas i den här listan beror på [momsklasser](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html) du har konfigurerat.

   - När du är klar klickar du på **[!UICONTROL Create Catalog Products]**.

Katalogprodukterna skapas i [!DNL Commerce] och tilldelas till den Amazon-lista som den skapades från. När listorna nu matchar deras respektive Amazon-lista tas de bort från [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) och visas i [_[!UICONTROL Active]_](./active-listings.md) -fliken.

![Skapa Commerce Catalog-produkt](assets/amazon-magento-catalog-product.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obligatoriskt) Om det här alternativet är aktiverat visas produkten i [!DNL Commerce] storefront. Om den är inaktiverad visas inte produkten i [!DNL Commerce] storefront. |
| [!UICONTROL Categories] | Du kan ange namnet på kategorin för den nya produkten eller välja en kategori genom att klicka på nedpilen för att visa dina alternativ. Alternativen beror på [kategorier](https://experienceleague.adobe.com/docs/commerce-admin/catalog/categories/create/category-create.html) konfiguration. |
| [!UICONTROL Website Ids] | (Obligatoriskt) Välj den webbplats (storefront) som produkten ska kopplas till. Alternativen beror på [!DNL Commerce] [lagringskonfiguration](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) inställningar |
| Attributuppsättnings-ID | Välj en attributuppsättning. Alternativen beror på din konfiguration [!DNL Commerce] [attributuppsättningar](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-sets.html). |
| [!UICONTROL Visibility] | Alternativ:<ul><li>**[!UICONTROL Not Visible Individually]** - produkten inte syns i [!DNL Commerce] storefront (vanligaste för variantprodukter).</li><li>**[!UICONTROL Catalog]** - Tillåter att produkten kan nås via den kategori den är kopplad till på webbplatsen.</li><li>**Sök** - Tillåter att produkten bara hittas via sökverktyget.</li><li>**[!UICONTROL Catalog and Search]** - Tillåter att produkterna kan nås via kategoristrukturen och sökverktyget.</li></ul> |
| [!UICONTROL Assign Tax Class] | Tilldela en momsklass till den nya produkten. Alternativen beror på din konfiguration [momsklasser](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/taxes/tax-class.html). |
