---
title: Skapa en listregel för Amazon
description: Skapa de inledande listreglerna för att generera Amazon-listor för dina [!DNL Commerce] produkter när du slutför Amazon introduktionskanalsintroduktionsprocess.
role: Admin
feature: Sales Channels, Products, Merchandising, Configuration
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Skapa en listregel för Amazon

Listregler kan definieras under introduktionen, men kan också ändras när som helst. Efter introduktionen kan du komma åt [listreglerna](./listing-rules.md) på butikens [kontrollpanel](./amazon-store-dashboard.md).

## Skapa en listregel under introduktion

1. När din butik är ansluten klickar du på **[!UICONTROL View Store]** för att få information om den nya butiken.

   Butikens [kontrollpanel](./amazon-store-dashboard.md) visas med meddelandet `No products listed to Amazon`.

1. Klicka på **[!UICONTROL Preview and List Eligible Products]**.

   Sidan _[!UICONTROL Listing Rules]_visas.

1. Ange önskade villkor för berättigande av produkter som ska listas i Amazon och klicka på **[!UICONTROL Preview changes]**, eller klicka på **[!UICONTROL Preview changes]** om du vill hoppa över det här steget.

   Se [Exempel: Definiera ett villkor](./ob-define-condition-example.md).

1. Granska dina listor i Förhandsgranska lista:

   ![Listförhandsgranskning](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]** - Produkter som visas på den här fliken är inte berättigade till Amazon-listning baserat på dina aktuella listregelinställningar.

     Ej berättigade produkter publiceras inte till Amazon. Om en produkt som inte är berättigad redan finns med på Amazon och du matchar Amazon-listan med din [!DNL Commerce]-katalogprodukt, ändras antalet för Amazon-listan till `0` för att förhindra försäljning av produkten. Mer information om hur du tar bort en lista från Amazon manuellt finns i [Avsluta en Amazon-lista](./end-listings-manually.md). Produkter som inte uppfyller Amazon krav listas inte här. Dessa produkter listas på fliken [[!UICONTROL Inactive Listings]](./inactive-listings.md).

     Om du vill ändra en `Ineligible`-lista till en `Eligible`-lista upprepar du den här processen och ändrar dina listregler.

   - **[!UICONTROL Eligible Listings]** - Produkter som listas på den här fliken är berättigade till Amazon-listning baserat på din aktuella listregelinställning och är berättigade enligt Amazon krav. På den här fliken finns befintliga Amazon-listor som importeras (om du har **[!UICONTROL Import Third Party Listings]** inställt på `Import Listing` i [listinställningarna](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Produkterna som listas på den här fliken innehåller dina [!DNL Commerce]-katalogprodukter som nyligen har tagits med i Amazon-listan baserat på din aktuella listregelinställning och som skapar Amazon-listor.

1. Klicka på **[!UICONTROL Save and Close]** när du är klar.

   Butikens [instrumentpanel](./amazon-store-dashboard.md) öppnas.

När en butik har introducerats har informationssynkroniseringen mellan [!DNL Commerce] och Amazon initierats. Dina Amazon-listor importeras till [!DNL Commerce] och försöker matcha med produkter i [!DNL Commerce]-katalogen.

Du kan visa din beställningsinformation för Amazon i avsnittet _[!UICONTROL Recent Orders]_på kontrollpanelen för butik. Se [Lagra instrumentpanel](./amazon-store-dashboard.md) eller [Hantera beställningar](./managing-orders.md).

>[!IMPORTANT]
>
>Det finns några viktiga butiksinställningar (listor, priser, regler, leveranser med mera) som har standardvärden för en ny butik. Granska dina [butiksinställningar](./default-store-settings.md) för att se till att din butik är konfigurerad för dina specifika behov.

![Nästa ikon](assets/btn-next.png) [**Fortsätt till standardinställningar för lagring**](./default-store-settings.md)
