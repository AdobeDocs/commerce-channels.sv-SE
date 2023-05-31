---
title: Skapa en listregel för Amazon
description: Skapa de inledande listreglerna för hur du genererar Amazon-listor när du slutför processen för registrering av Amazon-försäljningskanal [!DNL Commerce] produkter.
exl-id: b318823e-a726-4a59-b117-9838562c7d8b
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Skapa en listregel för Amazon

Listregler kan definieras under introduktionen, men kan också ändras när som helst. Efter introduktionen har du tillgång till [listregler](./listing-rules.md) i butiken [kontrollpanel](./amazon-store-dashboard.md).

## Skapa en listregel under introduktion

1. När butiken är ansluten klickar du på **[!UICONTROL View Store]** för det nya arkivet.

   Butiken [kontrollpanel](./amazon-store-dashboard.md) visas med `No products listed to Amazon` meddelande.

1. Klicka **[!UICONTROL Preview and List Eligible Products]**.

   The _[!UICONTROL Listing Rules]_visas.

1. Ange villkor för att få köpa de produkter som ska listas i Amazon och klicka på **[!UICONTROL Preview changes]** eller klicka **[!UICONTROL Preview changes]** om du vill hoppa över det här steget.

   Se [Exempel: Definiera ett villkor](./ob-define-condition-example.md).

1. Granska dina listor i Förhandsgranska lista:

   ![Förhandsgranskning av lista](assets/amazon-ob-listing-preview.png){width="600" zoomable="yes"}

   - **[!UICONTROL Ineligible Listings]** - Produkter som listas på den här fliken är inte berättigade till Amazon-listning baserat på dina aktuella listregelinställningar.

      Ej berättigade produkter publiceras inte till Amazon. Om en produkt som inte uppfyller kraven redan finns i Amazon och du matchar Amazon lista med [!DNL Commerce] katalogprodukt, kvantiteten för Amazon-listan ändras till `0` för att förhindra försäljning av produkten. Information om hur du tar bort en lista från Amazon manuellt finns i [Avslutar en Amazon-lista](./end-listings-manually.md). Produkter som inte uppfyller Amazon krav listas inte här. Dessa produkter är listade på [[!UICONTROL Inactive Listings] tab](./inactive-listings.md).

      Ändra en `Ineligible` lista till en `Eligible` visa, upprepa den här processen och ändra dina listregler.

   - **[!UICONTROL Eligible Listings]** - Produkter som listas på den här fliken är berättigade till Amazon listning baserat på din aktuella listregelinställning och är berättigade enligt Amazon krav. På den här fliken finns befintliga Amazon-listor som importeras (om du har **[!UICONTROL Import Third Party Listings]** ange till `Import Listing` i [Listinställningar](./listing-settings.md)).

   - **[!UICONTROL New Listings]** - Produkter som listas på den här fliken innehåller [!DNL Commerce] katalogprodukter som nyligen har tagits med i Amazon och som baseras på din nuvarande listregelinställning och som skapar Amazon-listor.

1. När du är klar klickar du på **[!UICONTROL Save and Close]**.

   Butiken [kontrollpanel](./amazon-store-dashboard.md) öppnas.

När en butik har introducerats synkroniseras informationen mellan [!DNL Commerce] och Amazon startas. Dina Amazon-listor importeras till [!DNL Commerce] och försöker matcha med produkterna i [!DNL Commerce] Katalog.

Du kan se din beställningsinformation för Amazon på _[!UICONTROL Recent Orders]_-avsnittet på butikspanelen. Se [Instrumentpanel för butik](./amazon-store-dashboard.md) eller [Hantera order](./managing-orders.md).

>[!IMPORTANT]
>
>Det finns några viktiga butiksinställningar (listor, priser, regler, leveranser med mera) som har standardvärden för en ny butik. Kontrollera att din butik är konfigurerad för dina specifika behov genom att granska [lagringsinställningar](./default-store-settings.md) .

![Nästa ikon](assets/btn-next.png) [**Fortsätt till standardinställningar för lagring**](./default-store-settings.md)
