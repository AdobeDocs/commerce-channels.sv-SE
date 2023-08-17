---
title: Amazon försäljningskanal - Prisregelvillkor
description: Använd prisregelvillkoren för att avgöra vilka produkter som är berättigade till listprisregeln.
feature: Sales Channels, Price Rules
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Prisregelvillkor

Villkoren avgör vilka produkter som omfattas av prisregeln. När du definierar villkoren för dina Amazon-prisregler följer du samma logik och process som när du definierar villkoren för [Kundprisregler](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart.html) in [!DNL Commerce].

>[!IMPORTANT]
>
>Om prisregeln gäller för alla produkter i [!DNL Commerce] och lämna sedan avsnittet tomt.

Alla områden i villkoren som är feta kan klickas för att visa de olika alternativen.

## Exempel: skapa ett prisregelvillkor

Den här processen kan vara enkel eller detaljerad, beroende på katalogkonfigurationen. Du kan definiera villkor så att när `ALL` eller `ANY` av villkoren antingen `TRUE` eller `FALSE` för en produkt är produkten berättigad till prissättningsregeln.

Villkoren baseras på dina [produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html). Om du vill tillämpa regeln på alla produkter lämnar du villkorsavsnittet tomt.

>[!NOTE]
>
>Om du vill definiera ett villkor baserat på ett visst produktattribut, **Använd för villkor för kampanjregel** för attributet måste anges till `Yes` i [Egenskaper för Storefront](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html) för attributet.

![Prisregelvillkor - rad 1](assets/ob-price-rules-condition-1.png){width="600" zoomable="yes"}

I det här exemplet definieras en regel som tillämpar en rabatt på 25 % på alla produkter som definieras i `Books` kategori.

Programsatsen rule har två feta länkar som, när de klickas, visar alternativen för den delen av villkorssatsen. Om du sparar villkoret utan att ändra ett fetstil, gäller regeln alla dina produkter.

- Klicka **[!UICONTROL ALL]** och välj antingen `ALL` eller `ANY`.
- Klicka **[!UICONTROL TRUE]** och väljer antingen `TRUE` eller `FALSE`.
- Om du vill tillämpa regeln på alla produkter låter du villkoret vara oförändrat.

Du kan skapa olika villkor genom att ändra kombinationen av dessa värden. I det här exemplet används följande villkor:

`If ALL of these conditions are TRUE:`

1. Om du vill visa tillgängliga attribut som villkoret gäller för klickar du på Lägg till (![Ikonen Lägg till](assets/btn-add-grn.png)) i början av villkorslinjen och väljer ett attribut som villkoret ska baseras på.

   **[!UICONTROL Conditions Combination]** - Välj om du vill skapa en annan uppsättning `All/Any` och `True/False` villkor inuti det befintliga villkoret.

   ![Kombination av prisregelvillkor](assets/ob-conditions-combinations.png){width="500"}

   **[!UICONTROL Product Attribute]** - Vilka produktattribut som är tillgängliga beror på [inställning av attributet](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/create/attribute-product-create.html). För ett attribut som ska visas i listan *[!UICONTROL Use for Promo Rule Conditions]* för attributet måste anges till `Yes` i butiksegenskaperna.

   - För **[!UICONTROL Product Attribute]** väljer du det attribut som du vill definiera som bas för villkoret. I det här exemplet är det markerade villkoret `Category`.

     ![Prisregelvillkor - rad 2, del 2](assets/ob-price-rule-condition-2.png){width="500"}

     Det markerade villkoret visas i programsatsen, följt av ytterligare två feta länkar. Alternativen varierar beroende på vilket produktattribut du väljer.

     När du har angett attributet kan det inte redigeras. Om du vill ändra attributet måste du ta bort raden och lägga till det nya attributet. Du kan ta bort en villkorslinje genom att klicka på Ta bort (![Ikonen Ta bort](assets/btn-del-red.png) ikonen i slutet av raden.

   - Klicka **[!UICONTROL is]** och välj den jämförelseoperator som beskriver villkoren för produkterna att uppfylla.

     I detta exempel är jämförelseoperatorn `is`. Vilka alternativ som är tillgängliga beror på vilket attribut du valde i föregående steg och kan innehålla olika jämförelsealternativ. Alternativen kan innehålla matchande värden, som inte inkluderar eller innehåller minst ett av värdena, och större än, lika med och mindre än ett numeriskt värde. I det här exemplet är alternativen `is` och `is not`.

   - Klicka **[!UICONTROL ...]** och välj det attributvärde som villkoret baseras på. Alternativen beror på attributets inställning.

     Du kan uppmanas att välja ett alternativ eller ange ett värde för villkoret. I det här exemplet visas fältet tomt. Om du vill välja kategori(er) för regeln klickar du på väljarikonen (![Väljarikon](assets/btn-chooser.png)) för att visa dina markeringsalternativ. Den här regeln gäller för _Böcker_ väljer du **[!UICONTROL Books]** kryssrutan. Kategorinumret fylls i. Klicka på den gröna bockmarkeringsikonen (![Kryssmarkeringsikon](assets/btn-check-mark-green.png)).

     ![Prisregelvillkor - rad 2, del 3](assets/ob-price-rule-condition-3.png){width="500"}

     Det markerade objektet visas i satsen för att slutföra villkoret.

     ![Prisregelvillkor - rad 2, del 4](assets/ob-price-rule-condition-4.png){width="500"}

     Detta exempelvillkor är klart. Detta innebär, som sagt, att alla produkter i [!DNL Commerce] katalog som har en definierad kategori med böcker (`4`) omfattas av denna prisregel. Du kan lägga till fler villkorslinjer för att ytterligare begränsa vilka produkter som omfattas.

1. Om du vill lägga till ytterligare en villkorslinje till satsen går du tillbaka till steg 1 och upprepar processen tills alla önskade villkor är klara.

   Du kan när som helst ta bort en rad i villkorssatsen genom att klicka på Ta bort (![Ikonen Ta bort](assets/btn-del-red.png)) i slutet av raden.
