---
title: Standardinställningar för lagring
description: Ändra standardinställningarna för Commerce för att anpassa Amazon Sales Channel för din butik.
exl-id: 368e5e8e-2bf9-4f9c-86c6-6d375f8a8720
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Standardinställningar för lagring

När din butik är ansluten och du har konfigurerat din första listregel synkroniseras data mellan Amazon och [!DNL Commerce] börjar. Det finns flera typer av butiksinställningar som gör att du kan anpassa din butik efter dina behov. Butiksinställningarna är tillgängliga i butiken [kontrollpanel](./amazon-store-dashboard.md).

Lagringsinställningarna inkluderar:

- [**[!UICONTROL Listing settings]**](./listing-settings.md) - Styr hur produktkatalogen interagerar med [!DNL Amazon Marketplace].

- [**[!UICONTROL Order settings]**](./order-settings.md) - Styr hur Amazon beställningar hanteras.

- [**[!UICONTROL Listing rules]**](./listing-rules.md) - Definiera vilka katalogprodukter som kan listas i Amazon.

- [**[!UICONTROL Pricing rules]**](./pricing-products.md) - Ange hur listpriset för Amazon ändras för kvalificerade listor.

- **[!UICONTROL Store reports]** - [Konkurrenskraftiga prisanalyser](./competitive-price-analysis.md) och [förbättringar av listor](./listing-improvements.md).

- **[!UICONTROL Logs]** - [Ändringar i listan](./listing-changes-log.md) och [kommunikationsfel](./communication-errors-log.md).

- [**[!UICONTROL Store integration settings]**](./store-integration-settings.md) - Granska inställningarna för e-post och Amazon-butiksnamn i [!DNL Commerce] Admin.

## Vissa viktiga standardinställningar

| Inställning | Standard | Beskrivning | Plats |
|--- |--- |--- |--- |
| [!UICONTROL Import Amazon Orders] | `Enabled` | Skapar motsvarande [!DNL Commerce] beställningar när nya beställningar tas emot från Amazon, vilket gör att beställningar kan hanteras i [[!DNL Commerce] Beställningar](https://docs.magento.com/user-guide/sales/orders.html){target="_blank"} arbetsflöde. När `Disabled`beställer Amazon importorderinformation för granskning, men beställningarna måste hanteras i [!DNL Amazon Seller Central] konto. | [Orderinställningar](./order-settings.md) |
| [!UICONTROL Customer Creation] | `No Customer Creation (guest)` | Kunddata från Amazon beställningar importeras inte till [!DNL Commerce] databas. Importerade Amazon-beställningar behandlas som en gästutcheckning. Om du vill skapa [!DNL Commerce] kunddatabas bör du ändra den här inställningen till `Build New Customer Account`. | [Orderinställningar](./order-settings.md) |
| [!UICONTROL Automatic List Action] | `Automatically List Eligible Products` | [!DNL Commerce] katalogprodukter (som uppfyller Amazon behörighetskrav) för att automatiskt publicera till Amazon och skapa Amazon-listor. Om du vill granska och publicera dina produkter manuellt bör du ändra den här inställningen till `Do Not Automatically List Eligible Products`. Produkter som väntar på manuell publicering visas på [_Klar för lista_](./ready-to-list.md) -fliken. | [Produktlistningsåtgärder](./product-listing-actions.md) |
| [!UICONTROL Magento Price Source] | `Price` | Definierar priskällattributet som används som bas för dina Amazon-listor. Om du inte vill använda [!DNL Commerce] `Price` som baspriset som prisreglerna baseras på bör du ändra inställningen till ett annat attribut. | [Listpris](./listing-price.md) |
| [!UICONTROL Product Fulfilled By] | `Fulfilled by Merchant` | Handlaren uppfyller alla order. Om du använder Fulfillment by Amazon eller en blandning av leveransmetoder bör du ändra den här inställningen. | [Fullgjord av](./listing-price.md) |
| [!UICONTROL Listing Product Condition] | `New` | Om alla dina produkter uppfyller samma villkor kan du välja ett av Amazon villkorsalternativ för alla dina produkter. Om katalogen innehåller produkter med olika villkor (till exempel Ny, Används och Återanvänd) måste du ändra inställningen till `Assign Condition Using Product Attribute` och kartlägga [!DNL Commerce] villkorsattribut till villkoren i Amazon. | [Villkor för produktlista](./product-listing-condition.md) |
| [!UICONTROL Listing Rules] | ingen | Definiera de regler som används för att avgöra vilka produkter Amazon försäljningskanal publicerar till Amazon. Dessa regler innehåller många alternativ för att skapa enkla till komplexa regler som inkluderar eller exkluderar produkter som listor. | [Listregler](./listing-rules.md) |
| Prisregler | ingen | Definiera Amazon prisattribut som skiljer sig från det definierade _[!UICONTROL Magento Price Source]_i [Listpris](./listing-price.md). Justera ert listpris (uppåt eller nedåt) mot ert_[!UICONTROL Magento Price Source]_ ange, skapa regler. | [Prisregler](./pricing-products.md) |

Mer information finns i [Lagringsinställningar](./ob-store-review.md).
