---
title: Skapa och redigera attribut för Amazon försäljningskanal
description: I Amazon Sales Channel finns attributvyn som du kan använda för att granska aktuella Amazon-attribut och länkade Commerce-attribut.
feature: Sales Channels, Products, Configuration
exl-id: 3cd5fb7e-68a3-45fd-8f50-72d3cc0244b5
source-git-commit: b2e608a633b760672044653a22be757ecffc9540
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Skapa och redigera attribut

Skapa eller uppdatera [!DNL Commerce]-attribut när du säljer via Amazon och uppdatera butikerna. Granska de aktuella Amazon-attributen och de länkade [!DNL Commerce]-attributen via [_[!UICONTROL Attributes]_view ](./attributes-view.md) på startsidan för Amazon-försäljningskanalen. Kolumnen_[!UICONTROL Action]_ visar tillgängliga åtgärder för attributet. Du kan antingen skapa och mappa ett nytt [!DNL Commerce]-attribut för ett olänkat Amazon-attribut, eller så kan du redigera ett befintligt [!DNL Commerce]-attribut och dess mappning till ett Amazon-attribut.

När du skapar och uppdaterar attribut kanske du vill verifiera attributvärdena för [!DNL Commerce] och Amazon-produkter. Dessa värden kan skilja sig om du inte synkroniserar och importerar värden från Amazon. Mer information om hur du granskar Amazon-värden för dessa attribut finns i [Granska Amazon-attributmappning](./amazon-matching-attributes-values.md). Om du vill ändra dessa värden kan du [redigera eller skapa en mappning](./amazon-manually-update-incomplete-listing.md) mellan Amazon och [!DNL Commerce].

## Skapa ett attribut {#create-an-attribute}

De här stegen skapar ett [!DNL Commerce]-attribut och mappar det till ett Amazon-attribut. Beroende på konfigurationer kan värdena börja synkroniseras mellan kataloger.

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Attributes]** på den vänstra menyn, leta upp ett Amazon-attribut och klicka på **[!UICONTROL Create Attribute]** i kolumnen _[!UICONTROL Action]_.

1. Om du vill aktivera synkronisering av Amazon-värden till det länkade [!DNL Commerce]-attributet anger du **[!UICONTROL Is Active]** till `Yes`.

   När värdet är `Yes` synkroniseras värdena enligt din konfiguration.

1. Välj `Create New Magento Attribute` för **[!UICONTROL Select Magento Product Attribute]**.

   Attributet mappas till det valda för **[!UICONTROL Amazon Attribute Name]**.

1. Ange **[!UICONTROL Magento Product Attribute Name]**.

1. Ange **[!UICONTROL Magento Product Attribute Code]**.

   Värdet måste vara i gemener utan blanksteg.

1. För **[!UICONTROL Attribute Set Ids]** väljer du en attributuppsättning att tilldela.

   Normalt är attribut en del av en attributuppsättning, till exempel en uppsättning färger som har attribut för blått, grönt, gult och rött.

1. För **[!UICONTROL Type]** väljer du typ av attributvärde, till exempel text och siffror.

   Det här alternativet påverkar det tillåtna värdet för attributet.

1. För **[!UICONTROL Use for Promo Rule Conditions]** anger du `Yes` så att attributet är tillgängligt för en parameter i dina kampanjvillkor.

1. Ange `Yes` för **[!UICONTROL Used in Search]** om attributet och värdet kan användas i produktsökningar.

1. Ange `Yes` för **[!UICONTROL Comparable on Storefront]** om attributvärdet kan användas i Amazon funktionen Jämför med.

1. Välj [!DNL Commerce] [scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) för attributet och markera sedan en eller flera butiksvyer att importera Amazon-värden till.

   Om omfånget är `Global` kan _[!UICONTROL Store View]_inte ändras efter att attributet har skapats.

   Om du väljer `All Store Views (Global)` synkroniseras och sparas värden i alla dina Amazon Store-vyer. Du kanske bara vill synkronisera värden till specifika butiksvyer.

1. Klicka på **[!UICONTROL Save Attribute Settings]** när du är klar.

När du har sparat kan du redigera attributet för att granska inställningar och matcha Amazon- och [!DNL Commerce]-värden för attributet. Du kan också ange om Amazon-värden ska skriva över [!DNL Commerce]-värden.

![skapa attributinställningar](assets/amazon-attribute-settings-create.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Anger om det här attributet är live och synkroniseras aktivt mellan Amazon och [!DNL Commerce]. Ange som `Yes` för att säkerställa att attributvärdena från Amazon och [!DNL Commerce] är synkroniserade för det valda attributet. |
| Välj produktattribut för Magento | Anger det markerade attribut som du vill länka till det angivna Amazon-attributnamnet. Välj `Create New Magento Attribute` när du skapar ett attribut. |
| [!UICONTROL Amazon Attribute Name] | Visar namnet på det Amazon-attribut som du har valt. Det markerade attributet länkar till det här Amazon-attributet. Du kan inte redigera det här värdet via [!DNL Commerce]. |
| [!UICONTROL Magento Product Attribute Name] | Anger attributnamnet eller etiketten. |
| [!UICONTROL Magento Product Attribute Code] | Anger attributkoden, alla med gemener utan blanksteg. |
| [!UICONTROL Attribute Set Ids] | Anger den attributuppsättning som attributet ska tilldelas till. Attribut är ofta en del av en attributuppsättning, till exempel en uppsättning för färger som har attribut för blått, grönt, gult och rött. |
| [!UICONTROL Type] | Anger värdetypen för attributvärdet, t.ex. text och siffror. Markeringen påverkar det tillåtna värdet för attributet. |
| [!UICONTROL Use for Promo Rule Conditions] | Växla till `Yes` om du vill tillåta att attributet är tillgängligt för en parameter inom dina kampanjvillkor. |
| [!UICONTROL Used in Search] | Anger om attributet och värdet kan användas vid produktsökningar. |
| [!UICONTROL Comparable on Storefront] | Anger om attributvärdet kan användas i Amazon&quot;Jämför med&quot;-funktionen. |
| [!UICONTROL Magento Product Attribute Scope] | Anger attributets [scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings). Alternativ: Global/Store-vy<br>Om värdet är `Global` kan Store-vyn inte redigeras efter att attributet har skapats. |
| [!UICONTROL Store Views (to import values into to)] | Visas bara när omfånget är inställt på `Store View`. Välj den [butiksvy](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) som Amazon-attributvärdena ska synkroniseras med. Om du väljer `All Store Views (Global)` uppdateras värdet i alla [!DNL Commerce]-butiksvyer. |

## Redigera ett attribut {#edit-an-attribute}

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL Attributes]** på den vänstra menyn, leta upp ett Amazon-attribut och klicka på **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Om du vill aktivera eller inaktivera synkronisering av Amazon-värden till det länkade [!DNL Commerce]-attributet anger du **Är aktiv** till `Yes` eller `No`.

   När värdet är `Yes` synkroniseras värdena enligt din konfiguration.

1. Verifiera eller uppdatera attributet för **[!UICONTROL Select Magento Product Attribute]** för att mappa till vald **[!UICONTROL Amazon Attribute Name]**.

1. Ange om du vill att det inkommande Amazon-attributvärdet ska skriva över det befintliga attributvärdet.

   Du kanske inte vill skriva över priserna från Amazon till [!DNL Commerce].

   - **[!UICONTROL Do Not Overwrite Existing Magento Values]** - Behåller värdet och behåller olika värden för dina [!DNL Commerce]- och Amazon-butiker.

   - **[!UICONTROL Overwrite Existing Magento Values]** - Skriver över värdet i produktkatalogen [!DNL Commerce] med det inkommande Amazon-värdet.

1. Om det är tillgängligt för redigering väljer du en eller flera **[!UICONTROL Store Views (to import Amazon values into)]**.

   Om attributet har skapats med ett `Global`-omfång kan _Store-vyn_ inte ändras efter att attributet har skapats.

   Om du väljer `All Store Views (Global)` synkroniseras och sparas värdena i alla butiksvyer. Du kanske bara vill synkronisera värden till specifika butiksvyer.

1. Klicka på **[!UICONTROL Save Attribute Settings]** när du är klar.

![redigera attributinställningar](assets/amazon-attribute-settings-edit.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Is Active] | Anger om det här attributet är live och synkroniseras aktivt mellan Amazon och [!DNL Commerce]. Ange som `Yes` för att säkerställa att attributvärdena från Amazon och [!DNL Commerce] är synkroniserade för det valda attributet. |
| [!UICONTROL Select Magento Product Attribute] | Anger det markerade [!DNL Commerce]-attributet som du vill länka till det angivna Amazon-attributnamnet. Om du vill ändra det länkade [!DNL Commerce]-attributet väljer du ett annat attribut i listrutan. Värden synkroniseras enligt konfigurationer. |
| [!UICONTROL Amazon Attribute Name] | Visar namnet på Amazon-attributet enligt definitionen i [!DNL Amazon Seller Central]. Det markerade [!DNL Commerce]-attributet länkar till det här Amazon-attributet. Du kan inte redigera det här värdet via [!DNL Commerce]. |
| [!UICONTROL Overwrite Existing Value] | Anger om Amazon-attributvärdena skriver över befintliga [!DNL Commerce]-värden, vilket påverkar alla produkter med det här [!DNL Commerce]-attributet.<ul><li>**Skriv inte över befintliga Magento-värden** - (Standard) Behåller [!DNL Commerce]-värdet och behåller olika värden för [!DNL Commerce]- och Amazon-butiker.</li><li>**Skriv över befintliga Magento-värden** - Sparar Amazon-värdet över [!DNL Commerce]-värdet i produktkatalogen [!DNL Commerce].</li></ul> |
| [!UICONTROL Magento Product Attribute Scope] | Visas inte när du redigerar ett attribut om attributet har skapats med omfånget `Global`. Anger att [!DNL Commerce] [scope](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings) skapades och angavs till `Store View`. |
| [!UICONTROL Store Views (to import values into to)] | Välj den [!DNL Commerce] [butiksvy](https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html) som du vill synkronisera Amazon-attributvärden till. Om du väljer `All Store Views (Global)` uppdateras värdet i alla butiksvyer. |
