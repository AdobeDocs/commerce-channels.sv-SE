---
title: Amazon Stores-vy
description: Gå till Amazon Stores-vyn och granska enkelt grundläggande statistik för alla Amazon-butiker samt olika alternativ för åtkomsthantering.
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Amazon Stores-vy

När du tittar på startsidan för Amazon försäljningskanal kan du _Amazon Stores_ visas som standard.

![Amazon Stores-vyn](assets/amazon-sales-channel-home-tabs.png)

The _[!UICONTROL Amazon Stores]_visar ett butikskort för var och en av Amazon butiker tillsammans med grundläggande statistik och hanteringsalternativ. I sammanfattningsinformationen som visas på varje kort finns information om butiksstatus, skapad den, uppdaterat datum och listor som behöver åtgärdas (exempel: Ofullständiga listor) och tilldelade [!DNL Commerce] webbplats.

När du visar _[!UICONTROL Amazon Store]_kan du göra följande med varje butikskort:

- Öppna en butik [kontrollpanel](./amazon-store-dashboard.md), klicka **[!UICONTROL View Store]**.

- Om du vill ändra en butiks status eller ta bort en butik klickar du på **[!UICONTROL Action]** och välj:

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Välj att ändra status för butiken till `Active` eller `Inactive`, respektive.

      Ändra en `Inactive` lagra till `Active` status aktiverar listor och orderaktivitet för butiken med hjälp av butikens aktuella butiksinställningar (till exempel listinställningar, prisregler och åsidosättningar).

      Ändra en butiksstatus från `Active` till `Inactive` status gör att listor och orderaktiviteter för butiken pausas. En inaktiv butik behåller alla butiksinställningar och listor, men avbryter tillfälligt synkroniseringen av priser, kvantitet och orderhantering tills butiken ändras tillbaka till `Active` status. Med den här funktionen kan du styra din butiksaktivitet på regional nivå utan att behöva återskapa eller återintegrera din Amazon Store eller förlora historik över order och säljdata.

   - **[!UICONTROL Delete]** - Välj att ta bort en butik som inte längre behövs.

      Välj när du vill ta bort en befintlig Amazon-butik och dess integreringsinställningar med [!DNL Amazon Seller Central] konto. Om du tar bort kontot tas butiken bort från Amazon försäljningskanal, tillsammans med alla kontoinställningar, listor, loggar och annan information som rör den här butiken. Det går inte att hämta arkivet efter borttagningen. Ett nytt arkiv måste skapas.

>[!NOTE]
>Om du vill ändra webbplatsen som tilldelats butiken under integreringen måste du ta bort butiken och lägga till butiken igen med den andra webbplatsen som definierats under butiksintegreringen.

| Butikskort | Beskrivning |
|--- |--- |
| Övre sektion | Innehåller: <br>Regionikonen för butiken, definierad under [butiksintegrering](./store-integration.md).<br> Den tilldelade _[!UICONTROL Magento Website]_, som definieras under butiksintegrering.<br>The_[!UICONTROL Status]_ i din butik. Alternativ: **[!UICONTROL Active]** - Integreringen i Store är klar och verifierad med Amazon och kan köpas via säljarna. **[!UICONTROL Inactive]** - Butiksintegreringen är klar, men används inte eller är inte tillgänglig för försäljningsaktiviteter. När `Inactive`, din Amazon-försäljning är pausad. När `Active`, försäljningsintäkter och ytterligare inställningar sparas för uppdatering innan aktivering.<br>The *[!UICONTROL Last Updated]* datum för den senaste ändringen av Amazon Store-konfigurationen.<br>The *[!UICONTROL Created]* det datum då Amazon Store skapades i Amazon försäljningskanal. |
| Mitten | Innehåller ett diagram över butiksaktivitetssammanfattning för de senaste 30 dagarna och innehåller och varnar för alla listor som behöver åtgärdas. |
| Nedre delen | Innehåller alternativen Visa butik och Åtgärd.<br>Öppna butiken [kontrollpanel](./amazon-store-dashboard.md), klicka **[!UICONTROL View Store]**.<br>Om du vill aktivera, inaktivera eller ta bort en butik klickar du på **[!UICONTROL Actions]**. |
