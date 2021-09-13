---
title: Skapa och tilldela produkter
description: Amazon Sales Channel har fliken [!UICONTROL New Third Party] som du kan använda för att skapa och tilldela matchande Commerce-katalogprodukter med Amazon-listor.
exl-id: de000e80-7546-44d2-905e-28664b24f028
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '1080'
ht-degree: 0%

---

# Skapa och tilldela produkter

När du visar fliken _[!UICONTROL New Third Party]_kan du matcha dina [!DNL Commerce]-katalogprodukter mot en befintlig Amazon-lista. Det finns två alternativ för den här matchningen. Du kan tilldela en lista till en befintlig katalogprodukt eller så kan du använda informationen från listan för att skapa katalogprodukter. Dessa alternativ är användbara när dina Amazon-listor inte automatiskt matchar din [!DNL Commerce]-katalog.

Du måste matcha (eller tilldela) dina produkter med dina Amazon-listor för att kunna använda alla funktioner i Amazon försäljningskanal.

När du skapar en katalogprodukt från en Amazon-lista:

- **ASIN** blir [!DNL Commerce] SKU
- **Produktlistans namn** blir kataloglistans namn
- **Pris** och **Kvantitet** importeras från Amazon Listing

Resten av de nödvändiga inställningarna avgörs av de [!DNL Commerce] produktinställningar du valde när du skapade.

När listor skapas och matchas tas de bort från fliken _[!UICONTROL New Third Party]_och visas på fliken_[!UICONTROL Active]_.

## Tilldela en enskild katalogprodukt till en Amazon-lista

1. Visa dina produktlistor på fliken [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Leta reda på den lista du vill tilldela i listan, klicka på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_och klicka på&#x200B;**[!UICONTROL Assign Catalog Product]**.

   Den här åtgärden öppnar sidan _[!UICONTROL Assign Magento Catalog Product]_.

1. Bläddra efter eller filtrera listan med hjälp av [arbetsytekontrollerna](./workspace-controls.md) och leta reda på rätt katalogprodukt som matchar listan.

1. När rätt produkt visas i listan klickar du på **[!UICONTROL Assign Catalog Product]** i kolumnen _[!UICONTROL Action]_.

Produkten och listan överensstämmer nu. Amazon försäljningskanal kan nu dela produkt- och listdata med Amazon och hantera din lista och information om den, inklusive listpris, fraktpris, aktie/kvantitet, orderinformation och status med mera.

## Skapa en katalogprodukt med Amazon listinformation

1. Visa dina produktlistor på fliken [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Leta reda på den lista du vill skapa i din [!DNL Commerce]-katalog, klicka på **[!UICONTROL Select]** i _[!UICONTROL Action]_-kolumnen och klicka på&#x200B;**[!UICONTROL Create New Catalog Product]**.

   Den här åtgärden öppnar sidan _[!UICONTROL Create Magento Catalog Product]_.

1. Slutför produktens kataloginställningar.

   - Ställ in växlingen **[!UICONTROL Enable Product(s)]** till `Yes` eller `No` (obligatoriskt).

      |Ja|Välj om du vill att produkten ska vara berättigad till din försäljning i [!DNL Commerce] butiken.|
|Nej|Välj om du vill att produkten inte ska vara berättigad till din försäljning i [!DNL Commerce]-butiken.|

   - För **[!UICONTROL Categories]** tilldelar du en kategori för produkten (valfritt).

      Klicka på nedpilen och markera en kategorikryssruta för att välja produktkategori. Klicka på **[!UICONTROL Done]** när du är klar.

   - För **[!UICONTROL Website Ids]** väljer du den webbplats (storefront) som produkten ska kopplas till.

      Alternativen i den här listan beror på dina [!DNL Commerce] [lagringskonfigurationer](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}-inställningar.

   - Välj ett alternativ för **[!UICONTROL Attribute Set Id]** (obligatoriskt).

      `Default` är standardvalet. Alternativen i den här listan beror på [!DNL Commerce] [attributuppsättningar](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} som du har konfigurerat.

   - För **[!UICONTROL Visibility]** väljer du ett alternativ för den nya produkten.

      |**[!UICONTROL Not Visible Individually]** (standard)|Produkten ingår inte i din butikslista, men den kan finnas som en variant av en annan produkt.|
|**[!UICONTROL Catalog]**|Produkten visas i kataloglistorna.|
|**[!UICONTROL Search]**|Produkten är tillgänglig för sökåtgärder.|
|**[!UICONTROL Catalog and Search]**|Produkten ingår i kataloglistor och är tillgänglig för sökåtgärder.|

   - Välj ett alternativ för **[!UICONTROL Assign Tax Class]**.

      Vilka alternativ som visas i den här listan beror på de [momsklasser](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} som du har konfigurerat.

   - Klicka på **[!UICONTROL Create Catalog Products]** när du är klar.

Katalogprodukten skapas i din [!DNL Commerce]-katalog och tilldelas den Amazon-lista som den skapades från. När listan nu matchar en befintlig Amazon-lista tas den bort från fliken _[!UICONTROL New Third Party]_och visas på fliken_[!UICONTROL Active]_.

## Skapa flera katalogprodukter med hjälp av deras Amazon listinformation

1. Visa dina produktlistor på fliken [_[!UICONTROL New Third Party]_](./new-third-party-listings.md).

1. Välj de listor som katalogprodukterna ska skapas för.

   Du kan markera enskilda kryssrutor i den vänstra kolumnen eller klicka på nedpilen i den övre vänstra kolumnen och välja **[!UICONTROL Select All]** eller **[!UICONTROL Select All on this Page]**.

1. Klicka på **[!UICONTROL Create New Catalog Product(s)]** under _[!UICONTROL Actions]_.

1. Om du vill godkänna bekräftelsemeddelandet och öppna sidan _[!UICONTROL Create Magento Catalog Product]_klickar du på&#x200B;**[!UICONTROL OK]**.

1. Slutför kataloginställningarna för produkterna.

   >[!NOTE]
   >När du skapar katalogprodukter för flera valda listor används de angivna produktinställningarna för alla listor.

   - Ställ in växlingen **[!UICONTROL Enable Product(s)]** till `Yes` eller `No` (obligatoriskt).

      |Ja|Välj om du vill att produkten ska vara berättigad till din försäljning i [!DNL Commerce] butiken.|
|Nej|Välj om du vill att produkten inte ska vara berättigad till din försäljning i [!DNL Commerce]-butiken.|

   - För **[!UICONTROL Categories]** tilldelar du en kategori för produkten (valfritt).

      Klicka på nedpilen och markera en kategorikryssruta för att välja produktkategori. Klicka på **Klar** när du är klar.

   - För **[!UICONTROL Website Ids]** väljer du den webbplats (storefront) som produkten ska kopplas till.

      Alternativen i den här listan beror på dina [!DNL Commerce] [lagringskonfigurationer](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}-inställningar.

   - Välj ett alternativ för **[!UICONTROL Attribute Set Id]** (obligatoriskt).

      `Default` är standardvalet. Alternativen i den här listan beror på [!DNL Commerce] [attributuppsättningar](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;} som du har konfigurerat.

   - För **[!UICONTROL Visibility]** väljer du ett alternativ för den nya produkten.

      |**[!UICONTROL Not Visible Individually]** (standard)|Produkten ingår inte i din butikslista, men den kan finnas som en variant av en annan produkt.|
|**[!UICONTROL Catalog]**|Produkten visas i kataloglistorna.|
|**[!UICONTROL Search]**|Produkten är tillgänglig för sökåtgärder.|
|**[!UICONTROL Catalog and Search]**|Produkten ingår i kataloglistor och är tillgänglig för sökåtgärder.|

   - Välj ett alternativ för **[!UICONTROL Assign Tax Class]**.

      Vilka alternativ som visas i den här listan beror på de [momsklasser](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;} som du har konfigurerat.

   - Klicka på **[!UICONTROL Create Catalog Products]** när du är klar.

Katalogprodukterna skapas i din [!DNL Commerce]-katalog och tilldelas till den Amazon-lista som den skapades från. När listorna nu matchar deras respektive Amazon-lista tas de bort från fliken [_[!UICONTROL New Third Party]_](./new-third-party-listings.md) och visas på fliken [_[!UICONTROL Active]_](./active-listings.md).

![Skapa Commerce Catalog-produkt](assets/amazon-magento-catalog-product.png)

| Fält | Beskrivning |
|--- |--- |
| [!UICONTROL Enable Product(s)] | (Obligatoriskt) Om den är aktiverad visas produkten i [!DNL Commerce]-butiken. Om den är inaktiverad visas inte produkten i [!DNL Commerce]-butiken. |
| [!UICONTROL Categories] | Du kan ange namnet på kategorin för den nya produkten eller välja en kategori genom att klicka på nedpilen för att visa dina alternativ. Alternativen beror på din [konfiguration](https://docs.magento.com/user-guide/catalog/category-create.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Website Ids] | (Obligatoriskt) Välj den webbplats (storefront) som produkten ska kopplas till. Alternativen är beroende av dina [!DNL Commerce] [butikskonfiguration](https://docs.magento.com/user-guide/stores/websites-stores-views.html){target=&quot;_blank&quot;}-inställningar |
| Attributuppsättnings-ID | Välj en attributuppsättning. Alternativen beror på din konfigurerade [!DNL Commerce] [attributuppsättning](https://docs.magento.com/user-guide/stores/attribute-sets.html){target=&quot;_blank&quot;}. |
| [!UICONTROL Visibility] | Alternativ:<ul><li>**[!UICONTROL Not Visible Individually]** - Produkten syns inte i  [!DNL Commerce] butiken (vanligaste för variantprodukter).</li><li>**[!UICONTROL Catalog]** - Tillåter att produkten kan nås via den kategori den är kopplad till på webbplatsen.</li><li>**Sök**  - Tillåter att produkten bara hittas via sökverktyget.</li><li>**[!UICONTROL Catalog and Search]** - Tillåter att produkterna kan nås via kategoristrukturen och sökverktyget.</li></ul> |
| [!UICONTROL Assign Tax Class] | Tilldela en momsklass till den nya produkten. Alternativen beror på din konfigurerade [momsklass](https://docs.magento.com/user-guide/tax/tax-class.html){target=&quot;_blank&quot;}. |
