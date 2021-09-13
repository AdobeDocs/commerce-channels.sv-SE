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

På fliken _[!UICONTROL Overrides]_visas de Amazon-listor som du har tillämpat en åsidosättning på. En åsidosättning är en listspecifik inställning som kan användas för att ange ett definierat värde till en lista. En åsidosättning som tillämpas på en lista definierar listans inställning, oavsett andra definierade listinställningar eller regler som listan är tillämplig för. När en åsidosättning tillämpas på en lista visas listan på fliken_[!UICONTROL Overrides]_. Värdet som definieras i åsidosättningen visas i rätt kolumn för listan. Det finns fyra typer av åsidosättningar: Price, Handling Time, Condition och Seller Notes.

## Typer av åsidosättningar

| Typ | Beskrivning |
|---|---|
| Pris | En åsidosättning som anger priset på listan och ignorerar alla andra prisinställningar för listan. <br><br>**Exempel**: Du har definierat en regel för 20 % rabatt som gäller för alla produkter i en viss kategori i katalogen. Du har en produkt som är ny på marknaden och efterfrågan är hög, så du vill inte att det rabatterade priset ska tillämpas på listan trots att produkten tillhör den kategorin. Du kan välja listan, [skapa en prisåsidosättning](./creating-editing-overrides.md#edit-override-single-listing) och definiera priset i en prisåsidosättning. |
| Hanteringstid | En åsidosättning som anger hanteringstiden för en lista och ignorerar den standardhanteringstid som angetts i listinställningarna.<br><br>**Exempel**: Standardhanteringstiden för dina listor är 2 dagar. Du har en produkt som är bräcklig och som kräver en extra dag för att vara säker på att den är packad för leverans. Du kan visa listan, [skapa en åsidosättning av hanteringstid](./creating-editing-overrides.md#edit-override-single-listing) och definiera hanteringstiden i tre dagar.<br><br>**Obs!** Inte tillgängligt för produkter som är inställda på  `Fulfilled by Amazon`. |
| Villkor | En åsidosättning som anger villkorsvärdet för en lista, oavsett vilket villkorsattribut som har tilldelats till listan.<br><br>**Exempel**: De flesta produkterna i din katalog är nya villkor, men du har en produkt som är i Refurbished-läge. Du kan visa listan, [skapa en villkorsåsidosättning](./creating-editing-overrides.md#edit-override-single-listing) och definiera det återfyllda villkoret för listan.<br><br>**Obs!** Inte tillgängligt för produkter som är inställda på  `Fulfilled by Amazon`. |
| Säljaranteckningar | En åsidosättning som definierar avsnittet _Seller Notes_ i listan. Det här fältet kan användas för att lägga till ytterligare information om produkten eller åsidosättningen, som vanligtvis används för att beskriva villkoret för&quot;icke-nya&quot; produkter. Texten i det här fältet visas med koden för användaren. Det går inte att lägga till säljaranteckningar för en lista med villkorsvärdet `New`. <br><br>**Exempel**: Du har en produkt som är i  `Refurbished` skick. Vanligtvis innehåller produkterna i det här villkoret inga handböcker eller dokument, men du har en annan leverantör för produkten som innehåller en handbok. Du kan visa listan, [skapa en åsidosättning av en säljaranteckning](./creating-editing-overrides.md#edit-override-single-listing) och lägga till din textanteckning som är unik för den här listan om handboken så att användaren vet att den ingår.<br><br>**Obs**: Om en produkt har ett definierat villkor  `New`kan du ange åsidosättning av en säljaranteckning, men Amazon visar inte säljaranteckningar för en  `New` produkt. |

Du kan skapa, redigera eller ta bort en åsidosättning för en [enstaka lista](./creating-editing-overrides.md#edit-override-single-listing). På flikarna _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ och _[!UICONTROL Ineligible]_kan du klicka på&#x200B;**[!UICONTROL Select]**i kolumnen_[!UICONTROL Action]_ och välja **[!UICONTROL Create Override]**. Åtgärden _[!UICONTROL Edit Overrides]_är bara tillgänglig när en lista har åsidosatts och visas på fliken_[!UICONTROL Overrides]_.

Du kan också skapa, redigera eller ta bort en åsidosättning till [flera listor](./creating-editing-overrides.md#edit-override-multiple-listings). På flikarna _[!UICONTROL Inactive]_,_[!UICONTROL Active]_ och _[!UICONTROL Ineligible]_kan du klicka på&#x200B;**[!UICONTROL Select]**i kolumnen_[!UICONTROL Action]_ och välja **[!UICONTROL Edit Listing Overrides]**.

Om du tar bort en åsidosättning används de värden som definieras i listinställningarna och reglerna.

När du definierar en åsidosättning kan du även välja att ange en typ av åsidosättning eller en kombination av typerna.

Se [Skapa och redigera åsidosättningar](./creating-editing-overrides.md).

>[!NOTE]
>
>Om du har pågående listor visas antalet listor i ett meddelande ovanför flikarna.

![Fliken Åsidosättningar](assets/amazon-overrides.png)

Amazon hemsidor för försäljningskanaler har gemensamma [kontroller för arbetsytan](./workspace-controls.md) som gör att du kan anpassa de data som visas.

## Standardkolumner

| Kolumn | Beskrivning |
|---|---|
| [!UICONTROL Amazon Seller SKU] | SKU (Stock Keeping Unit) som Amazon har tilldelat en produkt för att identifiera produkt, alternativ, pris och tillverkare. |
| [!UICONTROL ASIN] | Ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt.<br><br>ASIN står för Amazon Standard Identification Numbers. Ett ASIN är ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när objektet överförs till deras katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln. |
| [!UICONTROL Condition Override] | Det nya villkoret som definieras i åsidosättningen. Om den åsidosättning som används för listan inte är en villkorsåsidosättning visas `Not Selected` i den här kolumnen. |
| [!UICONTROL Product Listing Name] | Produktens namn. |
| [!UICONTROL Seller Notes Override] | De nya säljaranteckningarna som definieras i åsidosättningen. Om den åsidosättning som tillämpas på listan inte är den här typen av åsidosättning är den här kolumnen tom. |
| [!UICONTROL Handling Override] | Den nya hanteringstiden som definieras i åsidosättningen (i dagar). Om den åsidosättning som tillämpas på listan inte är en åsidosättning av hanteringstid, är den här kolumnen tom. |
| [!UICONTROL List Price Override] | Det nya listpris som definieras i åsidosättningen. Om den åsidosättning som tillämpas på listan inte är en prisåsidosättning visas `N/A` i den här kolumnen. |
| [!UICONTROL Action] | Lista över tillgängliga åtgärder som kan tillämpas på en viss lista. Om du vill använda en åtgärd klickar du på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_och väljer ett alternativ:<ul><li>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md#edit-override-single-listing)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
