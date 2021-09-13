---
title: Amazon Stores-vy
description: Gå till Amazon Stores-vyn och granska enkelt grundläggande statistik för alla Amazon-butiker samt olika alternativ för åtkomsthantering.
exl-id: 1376cd84-da81-4d3b-a5be-218aa802eed6
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Amazon Stores-vyn

När du visar startsidan för Amazon-försäljningskanalen öppnas vyn _Amazon Stores_ som standard.

![Amazon Stores-vyn](assets/amazon-sales-channel-home-tabs.png)

I vyn _[!UICONTROL Amazon Stores]_visas ett butikskort för var och en av dina Amazon-butiker tillsammans med grundläggande statistik och hanteringsalternativ. I sammanfattningsinformationen som visas på varje kort finns information om butiksstatus, skapad den, uppdaterat datum och listor som behöver åtgärdas (exempel: Ofullständiga listor) och den tilldelade [!DNL Commerce]-webbplatsen.

När du visar vyn _[!UICONTROL Amazon Store]_kan du med varje butikskort:

- Om du vill öppna en butik [instrumentpanel](./amazon-store-dashboard.md) klickar du på **[!UICONTROL View Store]**.

- Om du vill ändra en butiksstatus eller ta bort en butik klickar du på **[!UICONTROL Action]** och väljer:

   - **[!UICONTROL Activate]** /  **[!UICONTROL Deactivate]** - Välj om du vill ändra butikens status till  `Active` respektive  `Inactive`.

      Om du ändrar en `Inactive`-butik till `Active`-status aktiveras listor och orderaktivitet för butiken med hjälp av de aktuella butiksinställningarna (som listinställningar, prisregler och åsidosättningar).

      Om du ändrar en butiksstatus från `Active` till `Inactive` avbryts listor och orderaktivitet för butiken. En inaktiv butik behåller alla butiksinställningar och listor, men avbryter tillfälligt synkroniseringen av priser, kvantitet och orderhantering tills butiken ändras tillbaka till `Active`-status. Med den här funktionen kan du styra din butiksaktivitet på regional nivå utan att behöva återskapa eller återintegrera din Amazon Store eller förlora historik över order och säljdata.

   - **[!UICONTROL Delete]** - Välj att ta bort en butik som inte längre behövs.

      Välj när du vill ta bort en befintlig Amazon-butik och dess integreringsinställningar med ditt [!DNL Amazon Seller Central]-konto. Om du tar bort kontot tas butiken bort från Amazon försäljningskanal, tillsammans med alla kontoinställningar, listor, loggar och annan information som rör den här butiken. Det går inte att hämta arkivet efter borttagningen. Ett nytt arkiv måste skapas.

>[!NOTE]
>Om du vill ändra webbplatsen som tilldelats butiken under integreringen måste du ta bort butiken och lägga till butiken igen med den andra webbplatsen som definierats under butiksintegreringen.

| Butikskort | Beskrivning |
|--- |--- |
| Övre sektion | Innehåller: <br>Regionikonen för butiken, som definieras under [butiksintegrering](./store-integration.md).<br> Den tilldelade  _[!UICONTROL Magento Website]_, som definieras under butiksintegrering.<br>Butikens_[!UICONTROL Status]_ namn. Alternativ: **[!UICONTROL Active]** - Integreringen i Store är klar och verifierad med Amazon och är tillgänglig för försäljningsaktivitet. **[!UICONTROL Inactive]** - Butiksintegreringen är klar, men används inte eller är inte tillgänglig för försäljningsaktiviteter. När `Inactive` är din Amazon-försäljning pausad. När `Active` sparas försäljningsintäkter och ytterligare inställningar som ska uppdateras innan aktivering.<br>Datum  *[!UICONTROL Last Updated]* för den senaste ändringen av Amazon Store-konfigurationen.<br>Det  *[!UICONTROL Created]* datum då Amazon Store skapades i Amazon försäljningskanal. |
| Mitten | Innehåller ett diagram över butiksaktivitetssammanfattning för de senaste 30 dagarna och innehåller och varnar för alla listor som behöver åtgärdas. |
| Nedre delen | Innehåller alternativen Visa butik och Åtgärd.<br>Om du vill öppna  [kontrollpanelen](./amazon-store-dashboard.md) för arkivet klickar du på  **[!UICONTROL View Store]**.<br>Om du vill aktivera, inaktivera eller ta bort en butik klickar du på  **[!UICONTROL Actions]**. |
