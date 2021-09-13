---
title: Villkor för prisregel
description: Använd prisregelvillkoren för att avgöra vilka produkter som är berättigade till listprisregeln.
redirect_from: /sales-channels/asc/ob-pricing-rules-conditions.html
exl-id: 39b03a2e-15c6-4c56-b0e0-7c6823e95fa8
source-git-commit: ac190d88711f07c0b255a8cb50b12b62945f625e
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Prisregelvillkor

Villkoren avgör vilka produkter som omfattas av prisregeln. När du definierar villkoren för dina Amazon-prisregler följer du samma logik och process som när du definierar villkoren för [kundprisregler](https://docs.magento.com/user-guide/marketing/price-rules-cart.html){:target=&quot;_blank&quot;} i [!DNL Commerce].

>[!IMPORTANT]
>
>Om prisregeln gäller för alla produkter i din [!DNL Commerce]-katalog lämnar du det här avsnittet tomt.

Alla områden i villkoren som är feta kan klickas för att visa de olika alternativen.

## Exempel: skapa ett prisregelvillkor

Den här processen kan vara enkel eller detaljerad, beroende på katalogkonfigurationen. Du kan definiera villkoren så att när `ALL` eller `ANY` av villkoren är `TRUE` eller `FALSE` för en produkt är produkten berättigad till att tillämpa prisregeln.

Villkoren baseras på dina [produktattribut](https://docs.magento.com/user-guide/catalog/product-attributes.html){:target=&quot;_blank&quot;}. Om du vill tillämpa regeln på alla produkter lämnar du villkorsavsnittet tomt.

>[!NOTE]
>
>Om du vill definiera ett villkor baserat på ett specifikt produktattribut måste **Use for Promo Rule Conditions** for the attribute anges som `Yes` i [Store Properties](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;} för attributet.

![Prisregelvillkor - rad 1](assets/ob-price-rules-condition-1.png)

I det här exemplet definieras en regel som tillämpar en rabatt på 25 % på alla produkter som definieras i kategorin `Books`.

Programsatsen rule har två feta länkar som, när de klickas, visar alternativen för den delen av villkorssatsen. Om du sparar villkoret utan att ändra ett fetstil, gäller regeln alla dina produkter.

- Klicka på **[!UICONTROL ALL]** och välj antingen `ALL` eller `ANY`.
- Klicka på **[!UICONTROL TRUE]** och välj antingen `TRUE` eller `FALSE`.
- Om du vill tillämpa regeln på alla produkter låter du villkoret vara oförändrat.

Du kan skapa olika villkor genom att ändra kombinationen av dessa värden. I det här exemplet används följande villkor:

`If ALL of these conditions are TRUE:`

1. Om du vill visa tillgängliga attribut som villkoret gäller för klickar du på ikonen Lägg till (![Lägg till](assets/btn-add-grn.png)) i början av villkorslinjen och väljer ett attribut som villkoret ska baseras på.

   **[!UICONTROL Conditions Combination]** - Välj att skapa en annan uppsättning  `All/Any` och  `True/False` villkor inuti det befintliga villkoret.

   ![Kombination av prisregelvillkor](assets/ob-conditions-combinations.png)

   **[!UICONTROL Product Attribute]** - Vilka produktattribut som är tillgängliga beror på  [inställningen av attributet](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}. För att ett attribut ska kunna visas i listan måste *[!UICONTROL Use for Promo Rule Conditions]* för attributet anges till `Yes` i [butiksegenskaperna](https://docs.magento.com/user-guide/stores/attribute-product-create.html){:target=&quot;_blank&quot;}.

   - För **[!UICONTROL Product Attribute]** väljer du det attribut som du vill definiera som bas för villkoret. I det här exemplet är det markerade villkoret `Category`.

      ![Prisregelvillkor - rad 2, del 2](assets/ob-price-rule-condition-2.png)

      Det markerade villkoret visas i programsatsen, följt av ytterligare två feta länkar. Alternativen varierar beroende på vilket produktattribut du väljer.

      När du har angett attributet kan det inte redigeras. Om du vill ändra attributet måste du ta bort raden och lägga till det nya attributet. Du kan ta bort en villkorslinje genom att klicka på ikonen Ta bort (![Ta bort](assets/btn-del-red.png)) i slutet av raden.

   - Klicka på **[!UICONTROL is]** och välj den jämförelseoperator som beskriver villkoren för att produkterna ska uppfylla.

      I det här exemplet är jämförelseoperatorn `is`. Vilka alternativ som är tillgängliga beror på vilket attribut du valde i föregående steg och kan innehålla olika jämförelsealternativ. Alternativen kan innehålla matchande värden, som inte inkluderar eller innehåller minst ett av värdena, och större än, lika med och mindre än ett numeriskt värde. I det här exemplet är alternativen `is` och `is not`.

   - Klicka på **[!UICONTROL ...]** och välj det attributvärde som villkoret baseras på. Alternativen beror på attributets inställning.

      Du kan uppmanas att välja ett alternativ eller ange ett värde för villkoret. I det här exemplet visas fältet tomt. Om du vill välja kategori(er) för regeln klickar du på väljarikonen (![Väljarikon](assets/btn-chooser.png)) för att visa dina markeringsalternativ. Den här regeln gäller _Böcker_ och markera kryssrutan **[!UICONTROL Books]**. Kategorinumret fylls i. Klicka på den gröna bockmarkeringsikonen (![bockmarkeringsikonen](assets/btn-check-mark-green.png)) för att godkänna dina kategorival.

      ![Prisregelvillkor - rad 2, del 3](assets/ob-price-rule-condition-3.png)

      Det markerade objektet visas i satsen för att slutföra villkoret.

      ![Prisregelvillkor - rad 2, del 4](assets/ob-price-rule-condition-4.png)

      Detta exempelvillkor är klart. Detta villkor innebär, som sagt, att alla produkter i din [!DNL Commerce]-katalog som har en definierad kategori böcker (`4`) är berättigade till den här prissättningsregeln. Du kan lägga till fler villkorslinjer för att ytterligare begränsa vilka produkter som omfattas.

1. Om du vill lägga till ytterligare en villkorslinje till satsen går du tillbaka till steg 1 och upprepar processen tills alla önskade villkor är klara.

   Du kan när som helst ta bort en rad i villkorssatsen genom att klicka på ikonen Ta bort (![Ta bort](assets/btn-del-red.png)) i slutet av raden.
