---
title: '"Onboarding: Skapa listregel'
description: Skapa de inledande listreglerna för att generera Amazon-listor för dina  [!DNL Commerce] produkter när du slutför processen för registrering av Amazon-försäljningskanal.
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Onboarding: Skapa listregel

Listregler kan definieras under introduktionen, men kan också ändras när som helst. Efter introduktionen kan du komma åt [listreglerna](./listing-rules.md) på butiken [dashboard](./amazon-store-dashboard.md).

## Skapa en listregel under introduktion

1. När du har anslutit butiken klickar du på **[!UICONTROL View Store]** för att hitta den nya butiken.

   Butikens [kontrollpanel](./amazon-store-dashboard.md) visas med meddelandet `No products listed to Amazon`.

1. Klicka på **[!UICONTROL Preview and List Eligible Products]**.

   Sidan _[!UICONTROL Listing Rules]_visas.

1. Ange vilka villkor du vill använda för de produkter som ska listas i Amazon och klicka på **[!UICONTROL Preview changes]** eller klicka på **[!UICONTROL Preview changes]** om du vill hoppa över det här steget.

   Se [Exempel: Definiera ett villkor](./ob-define-condition-example.md).

1. Granska dina listor i Förhandsgranska lista:

   ![Förhandsgranskning av lista](assets/amazon-ob-listing-preview.png)

   - **[!UICONTROL Ineligible Listings]** - Produkter som listas på den här fliken är inte berättigade till Amazon-listning baserat på dina aktuella listregelinställningar.

      Ej berättigade produkter publiceras inte till Amazon. Om en produkt som inte är berättigad redan finns med på Amazon och du matchar Amazon-listan med din [!DNL Commerce]-katalogprodukt, ändras antalet för Amazon-listan till `0` för att förhindra försäljning av produkten. Information om hur du tar bort en lista från Amazon manuellt finns i [Avsluta en Amazon-lista](./end-listings-manually.md). Produkter som inte uppfyller Amazon krav listas inte här. Dessa produkter listas på fliken [[!UICONTROL Inactive Listings]](./inactive-listings.md).

      Om du vill ändra en `Ineligible`-lista till en `Eligible`-lista upprepar du den här processen och ändrar dina listregler.

   - **[!UICONTROL Eligible Listings]** - Produkter som listas på den här fliken är berättigade till Amazon listning baserat på din aktuella listregelinställning och är berättigade enligt Amazon krav. På den här fliken finns dina befintliga Amazon-listor som importeras (om du har **[!UICONTROL Import Third Party Listings]** inställt på `Import Listing` i [listinställningarna](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - De produkter som listas på den här fliken innehåller de  [!DNL Commerce] katalogprodukter som nyligen har tagits med i Amazon enligt din nuvarande listregelinställning och som skapar Amazon-listor.

1. Klicka på **[!UICONTROL Save and Close]** när du är klar.

   Butikens [kontrollpanel](./amazon-store-dashboard.md) öppnas.

När en butik har startats om har informationssynkroniseringen mellan [!DNL Commerce] och Amazon startats. Dina Amazon-listor importeras till [!DNL Commerce] och försöker matcha med produkter i din [!DNL Commerce]-katalog.

Du kan visa din beställningsinformation för Amazon i avsnittet _[!UICONTROL Recent Orders]_på kontrollpanelen för butik. Se [Store Dashboard](./amazon-store-dashboard.md) eller [Hantera order](./managing-orders.md).

>[!IMPORTANT]
>
>Det finns några viktiga butiksinställningar (listor, priser, regler, leveranser med mera) som har standardvärden för en ny butik. Granska dina [butiksinställningar](./default-store-settings.md) för att se till att din butik är konfigurerad för dina specifika behov.

![Nästa ](assets/btn-next.png) [**ikonFortsätt till standardinställningar för lagring**](./default-store-settings.md)
