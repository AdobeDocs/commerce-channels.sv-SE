---
title: "[!UICONTROL Amazon Stores] vy"
description: Gå till Amazon Stores-vyn och granska enkelt grundläggande statistik för alla Amazon-butiker samt olika alternativ för åtkomsthantering.
feature: Sales Channels, Storefront
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 801d4eee9e84b5c5f8b53397fbe8023ad54281e6
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# [!UICONTROL Amazon Stores]-vy

När du visar startsidan för Amazon-försäljningskanalen öppnas vyn _Amazon Stores_ som standard.

![Vyn Amazon Stores](assets/amazon-sales-channel-home-tabs.png){width="600" zoomable="yes"}

I vyn _[!UICONTROL Amazon Stores]_visas ett butikskort för var och en av dina Amazon-butiker tillsammans med grundläggande statistik och hanteringsalternativ. I sammanfattningsinformationen som visas på varje kort finns information om butiksstatus, skapad den, senaste uppdaterat datum, listor som behöver åtgärdas (exempel: Ofullständiga listor) och den tilldelade webbplatsen [!DNL Commerce].

När du visar vyn _[!UICONTROL Amazon Store]_kan du göra följande med varje butikskort:

- Klicka på **[!UICONTROL View Store]** om du vill öppna en [kontrollpanel](./amazon-store-dashboard.md).

- Om du vill ändra en butiksstatus eller ta bort en butik klickar du på **[!UICONTROL Action]** och väljer:

   - **[!UICONTROL Activate]** / **[!UICONTROL Deactivate]** - Välj att ändra status för butiken till `Active` respektive `Inactive`.

     Om du ändrar ett `Inactive`-arkiv till `Active` aktiveras listor och orderaktivitet för butiken med hjälp av de aktuella butiksinställningarna (till exempel listinställningar, prisregler och åsidosättningar).

     Om du ändrar en butiksstatus från `Active` till `Inactive` pausas listor och orderaktivitet för butiken. En inaktiv butik behåller alla butiksinställningar och listor, men avbryter tillfälligt synkroniseringen av priser, kvantitet och orderhantering tills butiken ändras tillbaka till `Active`-status. Med den här funktionen kan du styra din butiksaktivitet på regional nivå utan att behöva återskapa eller återintegrera din Amazon Store eller förlora historik över order och säljdata.

   - **[!UICONTROL Delete]** - Välj att ta bort en butik som inte längre behövs.

     Välj när du vill ta bort en befintlig Amazon-butik och dess integreringsinställningar med ditt [!DNL Amazon Seller Central]-konto. Om du tar bort kontot tas butiken bort från Amazon försäljningskanal, tillsammans med alla kontoinställningar, listor, loggar och annan information som rör den här butiken. Det går inte att hämta arkivet efter borttagningen. Ett nytt arkiv måste skapas.

>[!NOTE]
>Om du vill ändra webbplatsen som tilldelats butiken under integreringen måste du ta bort butiken och lägga till butiken igen med den andra webbplatsen som definierats under butiksintegreringen.

| Butikskort | Beskrivning |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Övre sektion | Innehåller: <br>Regionikonen för butiken, som definieras under [butiksintegrering](./store-integration.md).<br> Den tilldelade _[!UICONTROL Magento Website]_, som definieras under butiksintegrering.<br>Butikens_[!UICONTROL Status]_. Alternativ: **[!UICONTROL Active]** - Store-integreringen har slutförts och verifierats med Amazon och är tillgänglig för försäljningsaktivitet. **[!UICONTROL Inactive]** - Store-integreringen är klar, men används inte eller är inte tillgänglig för försäljningsaktivitet. När `Inactive` har din Amazon-försäljning pausats. När `Active` sparas försäljningsintäkter och ytterligare inställningar som ska uppdateras innan de aktiveras.<br>Datumet *[!UICONTROL Last Updated]* för den senaste ändringen av Amazon Store-konfigurationen.<br>Datumet *[!UICONTROL Created]* när Amazon Store skapades i Amazon försäljningskanal. |
| Mittsektion | Innehåller ett diagram över butiksaktivitetssammanfattning för de senaste 30 dagarna och innehåller och varnar för alla listor som behöver åtgärdas. |
| Nedre delen | Innehåller alternativen Visa butik och Åtgärd.<br>Klicka på **[!UICONTROL View Store]** om du vill öppna [instrumentpanelen](./amazon-store-dashboard.md) i butiken.<br>Klicka på **[!UICONTROL Actions]** om du vill aktivera, inaktivera eller ta bort en butik. |
