---
title: 'Exempel: Definiera ett villkor för Amazon listregler'
description: När du skapar dina listregler definierar du villkor för att identifiera de Commerce-katalogprodukter som ska listas på Amazon Marketplace.
feature: Sales Channels, Products, Configuration
exl-id: 8a48acfc-d31b-4919-bef7-8c300f0f9d94
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Exempel: Definiera ett villkor

## Villkor

Alla områden i villkoren som är feta kan klickas för att visa de olika alternativen.

**Lägg inte till villkor om alla produkter på den valda webbplatsen är berättigade.**

>[!NOTE]
>
>Det finns en komplex uppsättning back-end-processer för direktkommunikation med Amazon system. Beroende på hur många objekt du försöker lista och hur upptagna Amazon-system kan vara (t.ex. Black Friday) kan det ta tid för dina objekt att listas på Amazon.

Se avsnittet Villkor i [Skapa en kundprisregel](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog-create.html).

## Definiera ett villkor

Den här processen kan vara enkel eller detaljerad, beroende på vilken katalogkonfiguration du har. Du kan konfigurera dina villkor så att produkten kan listas på Amazon när `ALL` eller `ANY` av de definierade villkoren är antingen `TRUE` eller `FALSE` för en produkt.

Villkoren baseras på befintliga produktattributvärden. Om du vill tillämpa regeln på alla produkter lämnar du villkorsavsnittet tomt.

>[!NOTE]
>
>Om du vill definiera ett villkor baserat på ett specifikt produktattribut anger du **[!UICONTROL Use for Promo Rule Conditions]**-inställningen för attributet till `Yes`. Du kan komma åt den här inställningen på sidan [Egenskaper för Storefront](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes-add.html) för attributet.

![Villkor - rad 1](assets/ob-listing-rule-conditions-start.png){width="500"}

Regeln i det här exemplet definierar en regel som ställer in Amazon-berättigande för alla katalogprodukter som har attributet _Amazon FBA_ inställt på `Yes`.

Programsatsen rule har två feta länkar som, när de klickas, visar alternativen för den delen av programsatsen. Om du sparar villkoret utan att ändra ett fetstil, gäller regeln alla dina produkter.

- Klicka på **[!UICONTROL ALL]** och välj antingen `ALL` eller `ANY`.
- Klicka på **[!UICONTROL TRUE]** och välj antingen `TRUE` eller `FALSE`.
- Om du vill tillämpa regeln på alla produkter låter du villkoret vara oförändrat.

Du kan skapa olika villkor genom att ändra kombinationen av dessa värden. I det här exemplet används följande villkor:

`If ALL of these conditions are TRUE:`

1. Klicka på ikonen Lägg till (![Lägg till ikon](assets/btn-add-grn.png)) i början av villkorslinjen och välj ett attribut som villkoret ska baseras på, till exempel en villkorskombination eller ett produktattribut.

   - **[!UICONTROL Conditions Combination]** - Välj om du vill tillåta att du skapar ytterligare en uppsättning med `All/Any`- och `True/False`-villkor inuti den befintliga uppsättningen.

     ![Villkorskombination](assets/ob-conditions-combinations.png){width="500"}

   - **[!UICONTROL Product Attribute]** - Produktattributen beror på attributets inställning. För att ett attribut ska visas i listan måste det konfigureras för användning i kampanjregelvillkor. Se _Använd för villkor för kampanjregel_ i [Produktattribut](https://experienceleague.adobe.com/docs/commerce-admin/catalog/product-attributes/product-attributes.html).

     I listan under **[!UICONTROL Product Attribute]** väljer du det attribut som du vill använda som grund för villkoret. I det här exemplet är det markerade villkoret `Amazon FBA`.

     ![Villkorslinje 2, del 2](assets/ob-condition-attribute-dropdown.png){width="350"}

     Det markerade villkoret visas i programsatsen, följt av ytterligare två feta länkar. Alternativen varierar beroende på vilket produktattribut du väljer.

     När du har angett attributet kan det inte ändras. Om du vill ändra attributet måste du ta bort raden och lägga till det nya attributet. Du kan ta bort en villkorslinje genom att klicka på ikonen Ta bort (![Ta bort](assets/btn-del-red.png)) i slutet av raden.

      1. Klicka på **[!UICONTROL is]** och välj den jämförelseoperator som beskriver villkoren för produkter att uppfylla.

         I det här exemplet är jämförelseoperatorn `is`. Vilka alternativ som är tillgängliga beror på vilket attribut du valde i föregående steg. Alternativ kan innehålla olika jämförelsealternativ, t.ex. matchningsvärden, som inte inkluderar eller inkluderar minst ett av värdena, och större än, lika med och mindre än ett numeriskt värde. I det här exemplet är alternativen `is` och `is not`.

      1. Klicka på **[!UICONTROL ...]** och välj det attributvärde som villkoret baseras på.

         Alternativen beror på attributets inställning. Du kan uppmanas att välja ett alternativ eller att ange text eller numeriska värden för villkoret. I detta exempel är markeringen `Yes`.

         Det markerade objektet visas i satsen för att slutföra villkoret.

         ![Villkorslinje 2, del 3](assets/ob-listing-rule-condition-is.png){width="500"}

   Detta villkor är klart. Som du anger innebär det här villkoret att alla produkter i din [!DNL Commerce]-katalog som har Amazon FBA-attributet inställt på värdet `Yes` kan tas upp i Amazon för regionen och butiken. Du kan lägga till fler villkorslinjer för att ytterligare begränsa vilka produkter som omfattas.

1. Om du vill lägga till ytterligare en villkorslinje i satsen, går du tillbaka till steg 1 och upprepar processen tills alla önskade villkor är klara.

Du kan ta bort en rad i villkorssatsen när som helst genom att klicka på ikonen Ta bort (![Ta bort](assets/btn-del-red.png)) i slutet av raden.
