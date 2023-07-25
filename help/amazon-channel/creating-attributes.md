---
title: Skapa och redigera attribut för Amazon försäljningskanal
description: Amazon Sales Channel tillhandahåller vyn Attribut som hjälper dig att granska aktuella Amazon-attribut och länkade Commerce-attribut.
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 0%

---

# Skapa och redigera attribut

Skapa eller uppdatera [!DNL Commerce] attribut när du säljer via Amazon och uppdaterar butikerna. Granska aktuella Amazon-attribut och länkade [!DNL Commerce] attribut via [_[!UICONTROL Attributes]_visa](./attributes-view.md) på startsidan för Amazon försäljningskanal. The_[!UICONTROL Action]_ -kolumnen visar tillgängliga åtgärder för attributet. Du kan antingen skapa och mappa en ny [!DNL Commerce] för ett olänkat Amazon-attribut eller så kan du redigera ett befintligt [!DNL Commerce] och dess mappning till ett Amazon-attribut.

När du skapar och uppdaterar attribut kanske du vill verifiera attributvärdena för [!DNL Commerce] och Amazon. Dessa värden kan skilja sig om du inte synkroniserar och importerar värden från Amazon. Information om hur du granskar Amazon-värden för dessa attribut finns i [Granska Amazon-attributmappning](./amazon-matching-attributes-values.md). Om du vill ändra dessa värden kan du [redigera eller skapa en mappning](./amazon-manually-update-incomplete-listing.md) mellan Amazon och [!DNL Commerce].

## Skapa ett attribut {#create-an-attribute}

De här stegen skapar en [!DNL Commerce] och mappa det till ett Amazon-attribut. Beroende på konfigurationer kan värdena börja synkroniseras mellan kataloger.

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Klicka **[!UICONTROL Attributes]** i den vänstra menyn letar du reda på ett Amazon-attribut och klickar på **[!UICONTROL Create Attribute]** i _[!UICONTROL Action]_kolumn.

1. Aktivera synkronisering av Amazon-värden till den länkade [!DNL Commerce] attribut, ange **[!UICONTROL Is Active]** till `Yes`.

   När inställt på `Yes`synkas värdena enligt din konfiguration.

1. Välj `Create New Magento Attribute` for **[!UICONTROL Select Magento Product Attribute]**.

   Attributet mappas till det valda för **[!UICONTROL Amazon Attribute Name]**.

1. Ange **[!UICONTROL Magento Product Attribute Name]**.

1. Ange **[!UICONTROL Magento Product Attribute Code]**.

   Värdet måste vara i gemener utan blanksteg.

1. För **[!UICONTROL Attribute Set Ids]** väljer du den attributuppsättning som ska tilldelas.

   Normalt är attribut en del av en attributuppsättning, till exempel en uppsättning färger som har attribut för blått, grönt, gult och rött.

1. För **[!UICONTROL Type]** väljer du typ av attributvärde, t.ex. text och siffror.

   Det här alternativet påverkar det tillåtna värdet för attributet.

1. För **[!UICONTROL Use for Promo Rule Conditions]**, ställs in på `Yes` för att attributet ska vara tillgängligt för en parameter inom dina kampanjvillkor.

1. För **[!UICONTROL Used in Search]**, ställs in på `Yes` om attributet och värdet kan användas vid produktsökningar.

1. För **[!UICONTROL Comparable on Storefront]**, ställs in på `Yes` om attributvärdet kan användas i Amazon funktion&quot;Jämför med&quot;.

1. Välj [!DNL Commerce] [omfång](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) för attributet och välj sedan en eller flera butiksvyer att importera Amazon-värden till.

   Om omfånget är inställt på `Global`, _[!UICONTROL Store View]_kan inte ändras efter att attributet har skapats.

   Om du väljer `All Store Views (Global)`synkroniseras och sparar värdena i alla dina Amazon Store-vyer. Du kanske bara vill synkronisera värden till specifika butiksvyer.

1. När du är klar klickar du på **[!UICONTROL Save Attribute Settings]**.

När du har sparat kan du redigera attributet för att granska inställningarna och matcha Amazon och [!DNL Commerce] värden för attributet. Du kan även ange om Amazon-värden ska skrivas över [!DNL Commerce] värden.

![skapa attributinställningar](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Anger om attributet är live och synkroniseras aktivt mellan Amazon och [!DNL Commerce]. Ange till `Yes` för att säkerställa attributvärdena från Amazon och [!DNL Commerce] Håll dig synkad för det valda attributet. |
| Välj produktattribut för Magento | Anger det markerade attribut som du vill länka till det angivna Amazon-attributnamnet. När du skapar ett attribut väljer du `Create New Magento Attribute`. |
| [!UICONTROL Amazon Attribute Name] | Visar namnet på det Amazon-attribut som du har valt. Det markerade attributet länkar till det här Amazon-attributet. Du kan inte redigera det här värdet via [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Anger attributnamnet eller etiketten. |
| [!UICONTROL Magento Product Attribute Code] | Anger attributkoden, alla med gemener utan blanksteg. |
| [!UICONTROL Attribute Set Ids] | Anger den attributuppsättning som attributet ska tilldelas till. Attribut är ofta en del av en attributuppsättning, till exempel en uppsättning för färger som har attribut för blått, grönt, gult och rött. |
| [!UICONTROL Type] | Anger värdetypen för attributvärdet, t.ex. text och siffror. Markeringen påverkar det tillåtna värdet för attributet. |
| [!UICONTROL Use for Promo Rule Conditions] | Växla till `Yes` för att attributet ska vara tillgängligt för en parameter inom dina kampanjvillkor. |
| [!UICONTROL Used in Search] | Anger om attributet och värdet kan användas vid produktsökningar. |
| [!UICONTROL Comparable on Storefront] | Anger om attributvärdet kan användas i Amazon&quot;Jämför med&quot;-funktionen. |
| [!UICONTROL Magento Product Attribute Scope] | Anger [omfång](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) för attributet. Alternativ: Global/butiksvy<br>När inställt på `Global`kan inte butiksvyn redigeras efter att attributet har skapats. |
| [!UICONTROL Store Views (to import values into to)] | Visas bara när omfånget är inställt på `Store View`. Välj [butiksvy](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) som Amazon-attributvärdena synkroniseras till. Välja `All Store Views (Global)` uppdaterar värdet för alla [!DNL Commerce] butiksvyer. |

## Redigera ett attribut {#edit-an-attribute}

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Klicka **[!UICONTROL Attributes]** i den vänstra menyn letar du reda på ett Amazon-attribut och klickar på **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Aktivera eller inaktivera synkronisering av Amazon-värden till den länkade [!DNL Commerce] attribut, ange **Är aktiv** till `Yes` eller `No`.

   När inställt på `Yes`synkas värdena enligt din konfiguration.

1. För **[!UICONTROL Select Magento Product Attribute]**, verifiera eller uppdatera attributet så att det matchar det valda **[!UICONTROL Amazon Attribute Name]**.

1. Ange om du vill att det inkommande Amazon-attributvärdet ska skriva över det befintliga attributvärdet.

   Du kanske inte vill skriva över priserna från Amazon till [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Behåller värdet och behåller olika värden för [!DNL Commerce] och Amazon butiker.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Skriver över värdet i [!DNL Commerce] produktkatalog med det inkommande Amazon-värdet.

1. Om det är tillgängligt för redigering väljer du en eller flera **[!UICONTROL Store Views (to import Amazon values into)]**.

   Om attributet skapades med en `Global` omfång, _Butiksvy_ kan inte ändras efter att attributet har skapats.

   Om du väljer `All Store Views (Global)`synkroniseras och sparar värden till alla butiksvyer. Du kanske bara vill synkronisera värden till specifika butiksvyer.

1. När du är klar klickar du på **[!UICONTROL Save Attribute Settings]**.

![redigera attributinställningar](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Anger om attributet är live och synkroniseras aktivt mellan Amazon och [!DNL Commerce]. Ange till `Yes` för att säkerställa attributvärdena från Amazon och [!DNL Commerce] Håll dig synkad för det valda attributet. |
| [!UICONTROL Select Magento Product Attribute] | Anger det markerade [!DNL Commerce] som du vill länka till det angivna Amazon-attributnamnet. Om du vill ändra den länkade [!DNL Commerce] väljer du ett annat attribut i listrutan. Värden synkroniseras enligt konfigurationer. |
| [!UICONTROL Amazon Attribute Name] | Visar namnet på Amazon-attributet enligt definitionen i [!DNL Amazon Seller Central]. Den markerade [!DNL Commerce] attributlänkar till det här Amazon-attributet. Du kan inte redigera det här värdet via [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Anger om Amazon-attributvärdena skriver över befintliga [!DNL Commerce] värden, som påverkar alla produkter med detta [!DNL Commerce] -attribut.<ul><li>**Skriv inte över befintliga Magento-värden** - (Standard) Behåller [!DNL Commerce] värde, behålla olika värden för [!DNL Commerce] och Amazon butiker.</li><li>**Skriv över befintliga Magento-värden** - Sparar Amazon-värdet över [!DNL Commerce] värdet i [!DNL Commerce] produktkatalog.</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | Visas inte när ett attribut redigeras om attributet har skapats med `Global` omfång. Anger att [!DNL Commerce] [omfång](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) skapades och angavs till `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Välj [!DNL Commerce] [butiksvy](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) som Amazon-attributvärdena ska synkroniseras med. Välja `All Store Views (Global)` uppdaterar värdet i alla butiksvyer. |
