---
title: Amazon-försäljningskanal - [!UICONTROL Listing Rules]
description: Reglerna för hur du använder listor avgör vilka Commerce-katalogprodukter som publiceras som Amazon Marketplace-listor.
feature: Sales Channels, Products
exl-id: b28a625b-64cf-4119-98bb-f1ea33043c8f
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# [!UICONTROL Listing Rules]

Du kan komma åt listreglerna för butik på [butikspanelen](./amazon-store-dashboard.md).

Regler för att ta reda på vilka produkter som Amazon försäljningskanal publicerar till Amazon anges. Dessa regler innehåller många alternativ för att skapa enkla till komplexa regler som inkluderar eller exkluderar produkter som listor. Varje regel består av villkor som ställer in kraven för att få ta med en produktlista.

Dina listregler synkroniseras kontinuerligt med din [!DNL Commerce]-katalog. När du lägger till nya [!DNL Commerce]-produkter som uppfyller behörighetskraven som anges i dina listregler bearbetas produkterna automatiskt för notering på Amazon.

- Om du vill att alla dina produkter ska publiceras i en Amazon-lista ska du inte definiera några villkor för dina listregler.

- Om du vill begränsa vilka katalogprodukter som publiceras till Amazon definierar du villkoren för listreglerna. När du definierar villkoren för dina Amazon-listregler följer du samma logik och process som när du definierar villkoren för [kundvagnsprisreglerna](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

- Om din listregel exkluderar en produkt, ändras produktens kvalificeringsstatus till `Ineligible`. Ej berättigade produkter publiceras inte till Amazon.

- Om en produkt som inte är berättigad redan finns med på Amazon och du matchar Amazon-listan med din [!DNL Commerce]-katalogprodukt, ändras antalet för Amazon-listan till `0` för att förhindra försäljning av produkten. Amazon-listor kan [tas bort manuellt](./end-listings-manually.md).

Ändringar av kvantitet och berättigandestatus påverkar alla listor som delar Amazon Seller SKU på marknadsplatser som finns för butiker som säljer i samma region (som definieras i _[!UICONTROL Amazon Marketplace Country]_under [butiksintegrering](./store-integration.md)). En ändring av en delad [!DNL Amazon Seller SKU] i en region påverkar dock inte produktens Amazon-listor i ett annat land.

![Listregler](assets/ob-listing-rules.png){width="600" zoomable="yes"}

## Konfigurera inställningar för listregler

1. Klicka på **[!UICONTROL Listing Rules]** på butikens kontrollpanel.

1. Ange villkor för vilka produkter som ska listas i Amazon.

Se [Exempel: Definiera ett villkor](./ob-define-condition-example.md).

| Fält | Beskrivning |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Websites] | Vilka alternativ som är tillgängliga beror på vilka [webbplatser](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) du har konfigurerat i din [!DNL Commerce]-konfiguration. Välj webbplats för de produkter som ingår i Amazon. Det går bara att välja en webbplats eftersom varje webbplats kräver en unik Amazon-butik som skapats i Amazon försäljningskanal. |
| [!UICONTROL Conditions] | Används för att definiera attributen [!DNL Commerce] för produktberättigande inom din Amazon-region. Se [Exempel: Definiera ett villkor](./ob-define-condition-example.md). |

## Arbetsytan Villkor

Alla områden i villkoren som är feta kan klickas för att visa de olika alternativen.

- Lägg inte till villkor om alla produkter på de valda webbplatserna är berättigade.
- Det finns en komplex uppsättning back-end-processer för direktkommunikation med Amazon system. Beroende på hur många objekt du försöker lista och hur upptagna Amazon-system kan vara (t.ex. Black Friday) kan det ta tid för dina objekt att listas på Amazon.

Mer information om villkor finns i [Beskriv villkoren](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html).

## Förhandsgranskning av listregel

När du ändrar dina villkorsdefinitioner för dina listregler kan du klicka på **[!UICONTROL Preview Changes]** för att tillämpa dina regeländringar och visa hur dina listor påverkas. Kontrollera dina listor i den här förhandsgranskningsfunktionen innan du sparar ändringarna i listregeln.

Dina Amazon-listor jämförs med dina regler och definierade villkor. Sedan kan du granska:

- Vilka produkter som flyttas till en icke-berättigad status baserat på ditt aktuella [!DNL Amazon Seller Central]-konto
- Vilka produkter som går från ett icke-stödberättigande läge till en berättigande status
- Vilka produkter är nya Amazon-listor och läggs till i din Amazon-lista från dina [!DNL Commerce]-produkter som omfattas

Med Förhandsgranska lista kan du förhandsgranska dina potentiella Amazon-listor och göra nödvändiga justeringar i dina listregler.

De potentiella Amazon-listorna visas på sidan _[!UICONTROL Listing Preview]_på en av tre flikar:

- **[!UICONTROL Ineligible Listings]** - De listade produkterna är inte berättigade till Amazon-listning baserat på dina nuvarande regler och villkor.

  Ej berättigade produkter publiceras inte till Amazon. Om en produkt som inte är berättigad redan finns med på Amazon och du matchar Amazon-listan med din [!DNL Commerce]-katalogprodukt, ändras antalet för Amazon-listan till `0` för att förhindra försäljning av produkten. Mer information om hur du tar bort en lista manuellt finns i [Avsluta en Amazon-lista](./end-listings-manually.md). Produkter som inte uppfyller Amazon krav listas inte här. Dessa produkter listas på fliken [Inaktiva listor](./inactive-listings.md).

- **[!UICONTROL Eligible Listings]** - De listade produkterna är berättigade till Amazon-listning baserat på dina nuvarande regler och villkor och är även berättigade enligt Amazon krav. Den här listan innehåller dina befintliga Amazon-listor som importeras (om du har **Importera tredjepartslistor** inställda på `Import Listing` i [Listinställningar](./third-party-listing-settings.md)).

- **[!UICONTROL New Listings]** - Produkter i listan innehåller dina [!DNL Commerce]-katalogprodukter som nyligen har tagits med i Amazon enligt dina nuvarande regler och villkor och som skapar och publicerar nya Amazon-listor.

### Visa förhandsgranskning av din lista

1. Klicka på **[!UICONTROL Listing Rules]** på butikens kontrollpanel.

1. Visa eller lägg till dina [listregler](./listing-rules.md).

1. Ändra [listregelvillkoren](./ob-define-condition-example.md).

1. Klicka på **[!UICONTROL Preview Changes]**.

1. Granska och bekräfta dina listor på flikarna _[!UICONTROL Ineligible Listings]_,_[!UICONTROL Eligible Listings]_ och _[!UICONTROL New Listings]_.

1. Om dina listor matchar dina förväntningar klickar du på **[!UICONTROL Save and close]**.

   Om dina listor inte visas som förväntat klickar du på **[!UICONTROL Back]** och ändrar dina regler och villkor tills dina listor matchar dina förväntningar.

![Förhandsgranskning av listregel](assets/amazon-listing-rule-preview.png){width="600" zoomable="yes"}

### Visar poster för förhandsgranskning

| Fält | Beskrivning |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Product ID] | Det unika sekventiella nummer som tilldelas en [!DNL Commerce]-katalogprodukt när den läggs till. |
| [!UICONTROL Thumbnail] | Visar en miniatyrbild av huvudproduktbilden. |
| [!UICONTROL Name] | Namnet på produkten, som hanteras i [!DNL Commerce] [produktrutnätet](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html). |
| [!UICONTROL Type] | Typen av produkt som hanteras i produktrutnätet för [!DNL Commerce]. |
| [!UICONTROL Attribute Set] | Namnet på den attributuppsättning som används som mall för produkten, som hanteras i produktrutnätet för [!DNL Commerce]. |
| [!UICONTROL SKU] | Den unika Stock Keeping-enheten som är tilldelad produkten, hanteras i produktrutnätet för [!DNL Commerce]. |
| [!UICONTROL Visibility] | Anger var produkten är synlig och hanteras i produktrutnätet [!DNL Commerce]. Alternativ:<ul><li>`Not visible individually`</li><li>`Catalog`</li><li>`Search`</li><li>`Catalog, Search`</li></ul> |
| Status | Anger statusen för produkten, som hanteras i produktrutnätet [!DNL Commerce]. Alternativ: `Enabled` / `Disabled` |

![Listar förhandsgranskningsarbetsflöde](assets/listing-preview-flowchart.png){width="500" zoomable="yes"}
