---
title: Åsidosättningar
description: På fliken Åsidosättningar i Amazon kan du identifiera och hantera hur du tillämpar åsidosättningar i dina Amazon-listor.
exl-id: e31bbbf9-b20d-42fd-a419-93d596e40be2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---

# Åsidosättningar

The _[!UICONTROL Overrides]_visas de Amazon-listor som du har tillämpat en åsidosättning på. En åsidosättning är en listspecifik inställning som kan användas för att ange ett definierat värde till en lista. En åsidosättning som tillämpas på en lista definierar listans inställning, oavsett andra definierade listinställningar eller regler som listan är tillämplig för. När en åsidosättning tillämpas på en lista visas listan på_[!UICONTROL Overrides]_ -fliken. Värdet som definieras i åsidosättningen visas i rätt kolumn för listan. Det finns fyra typer av åsidosättningar: Price, Handling Time, Condition och Seller Notes.

## Typer av åsidosättningar

| Typ | Beskrivning |
|---|---|
| Pris | En åsidosättning som anger priset på listan och ignorerar alla andra prisinställningar för listan. <br><br>**Exempel**: Du har definierat en regel för 20 % rabatt som gäller för alla produkter i en viss kategori i katalogen. Du har en produkt som är ny på marknaden och efterfrågan är hög, så du vill inte att det rabatterade priset ska tillämpas på listan trots att produkten tillhör den kategorin. Du kan välja listan, [skapa en prisåsidosättning](./creating-editing-overrides.md#edit-override-single-listing)och definiera listpriset i en prisåsidosättning. |
| Hanteringstid | En åsidosättning som anger hanteringstiden för en lista och ignorerar den standardhanteringstid som angetts i listinställningarna.<br><br>**Exempel**: Standardhanteringstiden för dina listor är 2 dagar. Du har en produkt som är bräcklig och som kräver en extra dag för att vara säker på att den är packad för leverans. Du kan visa listan, [skapa en åsidosättning av hanteringstid](./creating-editing-overrides.md#edit-override-single-listing)och definiera hanteringstiden i tre dagar.<br><br>**Obs!** Ej tillgängligt för produkter som är inställda på `Fulfilled by Amazon`. |
| Villkor | En åsidosättning som anger villkorsvärdet för en lista, oavsett vilket villkorsattribut som har tilldelats till listan.<br><br>**Exempel**: De flesta produkterna i din katalog är nya villkor, men du har en produkt som är i Refurbished-läge. Du kan visa listan, [skapa en villkorsåsidosättning](./creating-editing-overrides.md#edit-override-single-listing)och definierar villkoren för återköp för listan.<br><br>**Obs!** Ej tillgängligt för produkter som är inställda på `Fulfilled by Amazon`. |
| Säljaranteckningar | En åsidosättning som definierar _Säljaranteckningar_ i listan. Det här fältet kan användas för att lägga till ytterligare information om produkten eller åsidosättningen, som vanligtvis används för att beskriva villkoret för&quot;icke-nya&quot; produkter. Texten i det här fältet visas med koden för användaren. Det går inte att lägga till säljaranteckningar för en lista med villkorsvärdet `New`. <br><br>**Exempel**: Du har en produkt som `Refurbished` villkor. Vanligtvis innehåller produkterna i det här villkoret inga handböcker eller dokument, men du har en annan leverantör för produkten som innehåller en handbok. Du kan visa listan, [skapa åsidosättning av säljaranteckningar](./creating-editing-overrides.md#edit-override-single-listing)och lägg till en textanteckning som är unik i den här listan om handboken så att kunden vet att den ingår.<br><br>**Anteckning**: Om en produkt har ett definierat villkor för `New`kan du ange åsidosättning av säljarnoteringar, men Amazon visar inte säljaranteckningar för en `New` produkt. |

Du kan skapa, redigera eller ta bort en åsidosättning för en [enda notering](./creating-editing-overrides.md#edit-override-single-listing). På _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ och _[!UICONTROL Ineligible]_-flikar kan du klicka på&#x200B;**[!UICONTROL Select]**i_[!UICONTROL Action]_ kolumn och välj **[!UICONTROL Create Override]**. The _[!UICONTROL Edit Overrides]_åtgärden är bara tillgänglig när en lista har åsidosatts och visas på_[!UICONTROL Overrides]_ -fliken.

Du kan också skapa, redigera eller ta bort en åsidosättning för [flera listor](./creating-editing-overrides.md#edit-override-multiple-listings). På _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ och _[!UICONTROL Ineligible]_-flikar kan du klicka på&#x200B;**[!UICONTROL Select]**i_[!UICONTROL Action]_ kolumn och välj **[!UICONTROL Edit Listing Overrides]**.

Om du tar bort en åsidosättning används de värden som definieras i listinställningarna och reglerna.

När du definierar en åsidosättning kan du även välja att ange en typ av åsidosättning eller en kombination av typerna.

Se [Skapa och redigera åsidosättningar](./creating-editing-overrides.md).

>[!NOTE]
>
>Om du har pågående listor visas antalet listor i ett meddelande ovanför flikarna.

![Fliken Åsidosättningar](assets/amazon-overrides.png)

Amazon hemsidor för försäljningskanaler delar några vanliga sidor [arbetsytekontroller](./workspace-controls.md) som gör att du kan anpassa de data som visas.

## Standardkolumner

| Kolumn | Beskrivning |
|---|---|
| [!UICONTROL Amazon Seller SKU] | SKU (Stock Keeping Unit) som Amazon har tilldelat en produkt för att identifiera produkt, alternativ, pris och tillverkare. |
| [!UICONTROL ASIN] | Ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt.<br><br>ASIN står för Amazon Standard Identification Numbers. Ett ASIN är ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när objektet överförs till deras katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln. |
| [!UICONTROL Condition Override] | Det nya villkoret som definieras i åsidosättningen. Om den åsidosättning som tillämpas på listan inte är en villkorsåsidosättning, `Not Selected` visas i den här kolumnen. |
| [!UICONTROL Product Listing Name] | Produktens namn. |
| [!UICONTROL Seller Notes Override] | De nya säljaranteckningarna som definieras i åsidosättningen. Om den åsidosättning som tillämpas på listan inte är den här typen av åsidosättning är den här kolumnen tom. |
| [!UICONTROL Handling Override] | Den nya hanteringstiden som definieras i åsidosättningen (i dagar). Om den åsidosättning som tillämpas på listan inte är en åsidosättning av hanteringstid, är den här kolumnen tom. |
| [!UICONTROL List Price Override] | Det nya listpris som definieras i åsidosättningen. Om den åsidosättning som tillämpas på noteringen inte är en prisåsidosättning, `N/A` visas i den här kolumnen. |
| [!UICONTROL Action] | Lista över tillgängliga åtgärder som kan tillämpas på en viss lista. Så här använder du en åtgärd i _[!UICONTROL Action]_kolumn, klicka **[!UICONTROL Select]**och välj ett alternativ:<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
