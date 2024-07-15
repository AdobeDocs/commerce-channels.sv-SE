---
title: Standardinställningar för Amazon-listor
description: Ändra standardinställningarna för Commerce för att anpassa Amazon-Sales Channelen för din butik.
role: Admin
feature: Sales Channels, Integration, Configuration
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Standardinställningar för Amazon-listor

När din butik är ansluten och du har konfigurerat din första listregel startas synkroniseringen av data mellan Amazon och [!DNL Commerce]. Det finns flera typer av butiksinställningar som gör att du kan anpassa din butik efter dina behov. Lagringsinställningarna är tillgängliga på butikens [instrumentpanel](./amazon-store-dashboard.md).

Lagringsinställningarna inkluderar:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Kontrollera hur din produktkatalog interagerar med [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Kontrollera hur Amazon-beställningar hanteras.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Ange vilka katalogprodukter som kan listas i Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Definiera hur listpriset för Amazon ändras för kvalificerade listor.

- **[!UICONTROL Store reports]** - [Konkurrenskraftiga prisanalyser](./competitive-price-analysis.md) och [listförbättringar](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Visar ändringar](./listing-changes-log.md) och [kommunikationsfel](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Granska inställningarna för e-postmarknadsföring och Amazon-butiksnamn i [!DNL Commerce]-administratören.

## Vissa viktiga standardinställningar

| Inställning | Standard | Beskrivning | Plats |
|----------------------------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [!UICONTROL Import Amazon Orders] | `Enabled` | Skapar motsvarande [!DNL Commerce] order när nya order tas emot från Amazon, vilket gör att order kan hanteras i arbetsflödet [[!DNL Commerce] Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html). När det är `Disabled` beställer Amazon importorderinformation för granskning, men beställningarna måste hanteras i ditt [!DNL Amazon Seller Central]-konto. | [Beställningsinställningar](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Kunddata från Amazon-beställningar importeras inte till din [!DNL Commerce]-databas. Importerade Amazon-beställningar behandlas som en gästutcheckning. Om du vill skapa din [!DNL Commerce]-kunddatabas bör du ändra den här inställningen till `Build New Customer Account`. | [Beställningsinställningar](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] katalogprodukter (som uppfyller Amazon behörighetskrav) som automatiskt publiceras till Amazon och skapar Amazon-listor. Om du vill granska och publicera dina produkter manuellt bör du ändra inställningen till `Do Not Automatically List Eligible Products`. Produkter som väntar på manuell publicering visas på fliken [_Klar att lista_](./ready-to-list.md). | [Produktlistningsåtgärder](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Definierar priskällattributet som används som bas för dina Amazon-listor. Om du inte vill använda attributet [!DNL Commerce] `Price` som baspris som dina prisregler baseras på bör du ändra den här inställningen till ett annat attribut. | [Listpris](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | Handlaren uppfyller alla order. Om du använder Fulfillment by Amazon eller en blandning av leveransmetoder bör du ändra den här inställningen. | [Fullgjord av](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Om alla dina produkter uppfyller samma villkor kan du välja ett av Amazon villkorsalternativ för alla dina produkter. Om din katalog innehåller produkter med olika villkor (till exempel Nytt, Används och Renoverat) måste du ändra den här inställningen till `Assign Condition Using Product Attribute` och mappa dina [!DNL Commerce]-villkorsattribut till villkoren i din Amazon-lista. | [Villkor för produktlista](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | ingen | Definiera de regler som används för att avgöra vilka produkter Amazon försäljningskanal publicerar till Amazon. Dessa regler innehåller många alternativ för att skapa enkla till komplexa regler som inkluderar eller exkluderar produkter som listor. | [Listregler](./listing-rules.md) |
| Prisregler | ingen | Definiera ditt Amazon-attribut för listpris som skiljer sig från det definierade _[!UICONTROL Magento Price Source]_i ditt [listpris](./listing-price.md). Om du vill justera listpriset (uppåt eller nedåt) mot_[!UICONTROL Magento Price Source]_-inställningen skapar du regler. | [Prisregler](./pricing-products.md) |

Mer information finns i [Lagringsinställningar](./ob-store-review.md).
