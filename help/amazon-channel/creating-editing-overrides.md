---
title: Skapa och redigera åsidosättningar
description: Använd åsidosättningar av Amazon Sales Channel för att tillämpa ändringarna på en enstaka Amazon-lista eller på flera listor.
exl-id: 3a254883-b88c-4c94-b4d5-8d7754b9afd2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# Skapa och redigera åsidosättningar

Du kan skapa och åsidosätta en lista eller redigera eller ta bort en åsidosättning som har tillämpats på en lista. Åsidosätter anger ett definierat värde för en viss lista.

## Skapa en åsidosättning för en enstaka lista

Åtgärden _[!UICONTROL Create Override]_är tillgänglig när du visar listor på flikarna_[!UICONTROL Inactive]_, _[!UICONTROL Active]_och_[!UICONTROL Ineligible]_.

1. Visa en lista på en _[!UICONTROL Products Listings]_-sida (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_och_[!UICONTROL Ineligible]_-flik).

1. Klicka på **[!UICONTROL Select]** > **[!UICONTROL Create Override]** i kolumnen _[!UICONTROL Action]_för att öppna sidan Åsidosättningar av produktlistor.

   ![skapa åsidosättning av Amazon-lista](assets/amazon-select-create-override.png)

1. Kontrollera _[!UICONTROL Listing Details]_för att vara säker på att du visar rätt lista.

1. Bestäm vilken typ av åsidosättning du skapar.

   Du kan definiera en enskild åsidosättningstyp eller valfri kombination av typer för listan (Pris, Hanteringstid, Villkor, Seller Notes).

   - **Pris** - Klicka  **[!UICONTROL Change Listing Price]** och ange ett definierat prisvärde för  **[!UICONTROL Price Override]**.
   - **Hantera tid** - Klicka  **[!UICONTROL Change Handling Time]** och ange det definierade tidsvärdet (i dagar) för  **[!UICONTROL Handling Time Override]**.
   - **Villkor** - Klicka  **[!UICONTROL Change Condition]** och välj rätt alternativ för  **[!UICONTROL Condition Override]**.
   - **Seller Notes** - Klicka  **[!UICONTROL Change Seller Notes]** och ange din anteckningstext för  **[!UICONTROL Seller Notes Override]**.

1. Klicka på **[!UICONTROL Save Listing Override]**.

   Sidan _[!UICONTROL Product Listing Overrides]_stängs. Status för listan ändras till `Relist in Progress`. Ändringen kommer att publiceras till Amazon med nästa datasynkronisering (som konfigureras i cron-inställningarna). Listan läggs också till på fliken_[!UICONTROL Overrides]_.

I följande exempel visas en åsidosättning som definierar ett nytt pris på `$55`, en ny hanteringstid på `1 day`, ett nytt villkor på `Used; Like New` och en ny Seller Note-text.

![Exempel på åsidosättning av Amazon-lista](assets/amazon-overrides-edit.png)

## Redigera eller ta bort en åsidosättning för en enstaka lista {#edit-override-single-listing}

Åtgärden _[!UICONTROL Edit Overrides]_är tillgänglig när du visar listor på fliken_[!UICONTROL Overrides]_.

1. Visa en lista på _[!UICONTROL Product Listings]_-sidan (_[!UICONTROL Overrides]_-fliken).

1. Klicka på **[!UICONTROL Select]** > **[!UICONTROL Edit Overrides]** i kolumnen _[!UICONTROL Action]_.

   Sidan _[!UICONTROL Product Listing Overrides]_öppnas.

   ![Markera en åsidosättning av Amazon-lista](assets/amazon-select-edit-overrides.png)

1. Kontrollera _[!UICONTROL Listing Details]_för att vara säker på att du åsidosätter rätt lista.

1. Om du vill redigera dina _[!UICONTROL Override]_-inställningar definierar du avsnitten för den typ som du vill ändra (Pris, Hanteringstid, Villkor, Seller Notes).

   Om du vill behålla samma typ av åsidosättning väljer du `No Change To <override type>` (standard). Med den här inställningen ändras inte det tidigare definierade åsidosättningsvärdet.

   - **Pris** - Klicka  **[!UICONTROL Change Listing Price]** och ange ett definierat prisvärde för  **[!UICONTROL Price Override]**.
   - **Hantera tid** - Klicka  **[!UICONTROL Change Handling Time]** och ange det definierade tidsvärdet (i dagar) för  **[!UICONTROL Handling Time Override]**.
   - **Villkor** - Klicka  **[!UICONTROL Change Condition]** och välj rätt alternativ för  **[!UICONTROL Condition Override]**.
   - **Seller Notes** - Klicka  **[!UICONTROL Change Seller Notes]** och ange din anteckningstext för  **[!UICONTROL Seller Notes Override]**.

1. Om du vill ta bort en åsidosättningstyp klickar du på **Ta bort** för alla typer som du vill ta bort. Om det inte tas bort finns det tidigare definierade värdet kvar i åsidosättningen.

1. Klicka på **[!UICONTROL Save Listing Override]**.

   Sidan _[!UICONTROL Product Listing Overrides]_stängs. Status för listan ändras till `Relist in Progress`. Ändringen kommer att publiceras till Amazon med nästa datasynkronisering (som konfigureras i cron-inställningarna). Om listan inte redan finns läggs även listorna till på fliken_[!UICONTROL Overrides]_.

Piggybacking i _Create an Override_ example. I följande exempel visas en redigering av den tidigare skapade åsidosättningen som definierar det nya priset `$50`, tar bort åsidosättningen av hanteringstid och behåller de föregående åsidosättningarna av villkor och säljaranteckningar.

![Redigera eller ta bort en åsidosättning](assets/amazon-overrides-edit-2.png)
__

## Redigera eller ta bort en åsidosättning för flera listor {#edit-override-multiple-listings}

Åtgärden _[!UICONTROL Edit Listing Overrides]_är tillgänglig på flikarna_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ och _[!UICONTROL Ineligible]_.

>[!NOTE]
>
>Eftersom du ändrar åsidosättningar för flera listor visas inte _[!UICONTROL Listing Details]_-avsnittet på samma sätt som när du ändrar en enskild lista.

1. Visa listan på en _[!UICONTROL Products Listings]_-sida (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_,_[!UICONTROL Overrides]_ och _[!UICONTROL Ineligible]_-flik).

1. Markera kryssrutan i den vänstra kolumnen för varje lista som du vill ändra.

1. Klicka på **[!UICONTROL Edit Listing Overrides]** under _[!UICONTROL Actions]_.

   Sidan _[!UICONTROL Product Listing Overrides]_öppnas.

   ![Markera en åsidosättning av Amazon-lista](assets/amazon-actions-edit-listing-overrides.png)

1. Om du vill redigera dina _[!UICONTROL Override]_-inställningar definierar du avsnitten för den typ som du vill ändra (Pris, Hanteringstid, Villkor, Seller Notes).

   Om du vill behålla en åsidosättning väljer du `No Change To <override type>` (standard). Med den här inställningen ändras inte det tidigare definierade åsidosättningsvärdet.

   - **Pris** - Klicka  **[!UICONTROL Change Listing Price]** och ange ett definierat prisvärde för  **[!UICONTROL Price Override]**.
   - **Hantera tid** - Klicka  **[!UICONTROL Change Handling Time]** och ange det definierade tidsvärdet (i dagar) för  **[!UICONTROL Handling Time Override]**.
   - **Villkor** - Klicka  **[!UICONTROL Change Condition]** och välj rätt alternativ för  **[!UICONTROL Condition Override]**.
   - **Seller Notes** - Klicka  **[!UICONTROL Change Seller Notes]** och ange din anteckningstext för  **[!UICONTROL Seller Notes Override]**.

1. Om du vill ta bort en åsidosättningstyp klickar du på **[!UICONTROL Remove]** för varje typ som du vill ta bort. Om det inte tas bort finns det tidigare definierade värdet kvar i åsidosättningen.

1. Klicka på **[!UICONTROL Save Listing Override]**.

   Sidan _[!UICONTROL Product Listing Overrides]_stängs. Status för listorna ändras till `Relist in Progress`. Ändringen kommer att publiceras till Amazon med nästa datasynkronisering (som konfigureras i cron-inställningarna). Om listan inte redan finns läggs även listorna till på fliken_[!UICONTROL Overrides]_.

### Åsidosättningstyper

| Åsidosätt | Beskrivning |
|--- |--- |
| [!UICONTROL Price Override] | En prisåsidosättning definierar priset för listorna. Åsidosättningen har högre prioritet än alla automatiska inställningar tills åsidosättningen tas bort.<br><br>Om du vill åsidosätta priset på din produkt väljer du  **[!UICONTROL Change Listing Price]** och anger det nya priset för  **[!UICONTROL Price Override]**. |
| [!UICONTROL Handling Time Override] | En åsidosättning av hanteringstid definierar den tid det tar (i dagar) att bearbeta och leverera produkter. Åsidosättning av hanteringstid har högre prioritet än alla automatiska inställningar och standardinställningar för hanteringstid tills åsidosättningen tas bort.<br><br>Värdet som finns i  _[!UICONTROL Handling Time Override]_rutan är antingen den standardhanteringstid som definieras i  [listinställningarna ](./listing-settings.md) eller den standardhanteringstid som definieras för åsidosättning. Om du tar bort en åsidosättning av hanteringstid används som standard den hanteringstid som definieras i listinställningarna.<br><br>Om du vill definiera en åsidosättning av hanteringstid väljer du **[!UICONTROL Change Handling Time]**och anger den nya hanteringstiden (i dagar) för **[!UICONTROL Handling Time Override]**. |
| [!UICONTROL Condition Override] | Om du vill åsidosätta listvillkoret väljer du **[!UICONTROL Change Condition]** och väljer det nya villkoret från **Villkorsåsidosättning**. |
| [!UICONTROL Seller Notes Override] | För produkter i din katalog som har definierats med ett annat villkor än `New`, kan en säljaranteckning läggas till för att ytterligare beskriva produkten och dess tillstånd för potentiella köpare. Du kan ange åsidosättning av en säljaranteckning för en `New`-villkorsprodukt, men Amazon visar inte anteckningen.<br><br>Om du vill åsidosätta Seller Notes väljer du  **[!UICONTROL Change Seller Notes]** och anger den nya anteckningen för  **[!UICONTROL Seller Notes Override]**. |
