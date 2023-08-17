---
title: Amazon Sales Channel - allmänna inställningar för prisregel
description: Använd de allmänna inställningarna för prisregel för att definiera de primära egenskaperna för en listprisregel.
feature: Sales Channels, Price Rules, Configuration
exl-id: 915b3eed-997e-4f94-a23f-0553a9dfe30c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---

# Allmänna inställningar för prisregel

Definiera regelns namn, beskrivning, aktiva datum och prioritet.

## Fyll i avsnittet Allmänna inställningar för prisregel

1. För **[!UICONTROL Rule Name]** (obligatoriskt) anger du regelns namn.

   Det här namnet är endast till för din interna identifiering. Ju mer beskrivande regelnamnet är, desto bättre.

1. För **[!UICONTROL Description]**, ange en detaljerad beskrivning av regeln.

   Beskrivningen kan innehålla information om produkter som uppfyller kraven, aktiva datum, formeln för beräkning av det justerade priset eller annan information som du tycker är användbar om du vill ändra regeln.

1. För **[!UICONTROL Status]** väljer du ett alternativ:

   - `Active` - Välj det här alternativet om du vill att prisregeln ska gälla för dina produkter och justera ditt listpris innan du publicerar till Amazon.

   - `Inactive` - Välj det här alternativet om du inte vill att prisregeln ska gälla för dina berättigande produkter. Det här alternativet kommer troligtvis att användas när en prisregel ändras eller inaktiveras efter en begränsad kampanj.

1. För **[!UICONTROL From]** och **[!UICONTROL To]** anger du ett start- och slutdatum för prisregeln.

   Du kan också klicka på kalenderikonen för att välja ett datum från den dynamiska kalendern. Det här automatiska start- och stoppalternativet är användbart när du skapar tidsbegränsade eller säsongsinriktade kampanjer med bestämda start- och slutdatum.

1. För **[!UICONTROL Priority]**, anger du ett numeriskt värde för regelprioriteten.

   Prioritetsvärde lika med `1` är högsta prioritet. När du har flera aktiva prisregler kan du använda det här prioritetsvärdet för att avgöra vilken regel som används först. Det här fältet krävs för att använda _[!UICONTROL Discard Subsequent Rules]_-funktion.

1. För **[!UICONTROL Discard Subsequent Rules]** väljer du ett alternativ:

   - `Yes` - Välj det här alternativet om du inte vill att några andra prisregler ska gälla för en produkt. Om flera olika prisregler tillämpas på samma produkt innebär det att endast prisregeln med det högsta prioritetsvärdet tillämpas på produkten. Det här alternativet förhindrar att flera olika prisregler staplas och ger oönskade ytterligare rabatter.

   - `No` - Välj det här alternativet om du vill tillåta att flera prisregler gäller för samma produkt. Det här alternativet kan resultera i en stapling och ge flera rabatter.

>[!NOTE]
>
>Om du vill ignorera efterföljande regler måste en prisregel ha en definierad **Prioritet** värde.

![Allmänna inställningar för prisregel](assets/amazon-pricing-rule-general.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Name] | (Obligatoriskt) Ange ett namn för regeln som används för intern identifiering. Ju mer beskrivande regelnamnet är, desto bättre. Exempel:&quot;25 % rabatt på årsboksförsäljningen.&quot; |
| [!UICONTROL Description] | Ange en detaljerad beskrivning som förklarar regeln (används även för interna syften). Exempel:&quot;Årsslutsförsäljning, 25 % rabatt på alla artiklar i bokkategorin.&quot; |
| [!UICONTROL Status] | Alternativ:<ul><li>**[!UICONTROL Inactive]** - Prisregeln gäller inte för dina listor. Det här alternativet kan användas när du ändrar en prisregel eller inaktiverar den efter en begränsad befordran.</li><li>**[!UICONTROL Active]** - Prisregeln gäller för dina listor och justera dina priser innan du publicerar till Amazon.</li></ul> |
| [!UICONTROL From] | Ange startdatumet när prisregeln börjar. Om du till exempel vill ha en försäljning under årets sista månad anger du `From` datum till 1 december så att prisregeln automatiskt gäller för dina Amazon-listor från 1 december. |
| [!UICONTROL To] | Ange slutdatumet när prisregeln slutar. Om du fortsätter med det föregående exemplet och vill begränsa försäljningen till den sista månaden på året ställer du in `To` den 31 december, så prisregeln upphör den 31 december. |
| [!UICONTROL Priority] | Ange ett värde för prisregelprioriteten. Ett prioritetsvärde som är lika med `1` är högsta prioritet. När du har flera prisregler kan du använda prioritetsvärdet för att avgöra vilken regel som används först. Det här fältet krävs för att använda **Ignorera efterföljande regler** -funktion. |
| [!UICONTROL Discard Subsequent Rules] | Används för att tillåta eller förhindra att flera prissättningsregler staplas och ger ytterligare rabatter. Om du vill ignorera efterföljande regler måste en prisregel ha ett definierat värde för **[!UICONTROL Priority]**. Alternativ:<ul><li>**[!UICONTROL Yes]** - Välj när du inte vill att några andra prisregler ska gälla för en produkt. Om flera olika prisregler tillämpas på samma produkt innebär det att endast prisregeln med det högsta prioritetsvärdet tillämpas.</li><li>**[!UICONTROL No]** - Välj när du vill att flera prisregler ska gälla för samma produkt. Det här alternativet kan resultera i en stapling och flera rabatter på ditt listpris.</li></ul> |
