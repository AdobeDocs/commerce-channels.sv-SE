---
title: 'Intelligent Repricing Rule: Select Rule Type'
description: Bestäm Amazon listpris enligt konkurrentpriser genom att skapa en intelligent regel för omprissättning.
feature: Sales Channels, Products, Price Rules
exl-id: 2690323a-a076-484b-a437-adadb08094f5
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# Intelligent regel för omprissättning: Välj regeltyp

>[!IMPORTANT]
>
>Regler för intelligent omprisering fungerar inte korrekt om Amazon-regionen har statusen `Inactive`, som vid introduktionen. Prisberäkningarna beror på fraktkostnaderna och regionen måste ha statusen `Active` för att fraktkostnaderna ska kunna synkroniseras från Amazon.<br><br>
>
>Om du vill uppdatera regionens status i ditt Amazon-konto går du till Inställningar > Kontoinformation > Semesterinställningar. Se [Amazon: Liststatus för semester](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620/&quot;target=&quot;_blank)

En intelligent regel för omprissättning använder Amazon konkurrenters priser för att fastställa ert pris. Konkurrenterna är andra säljare som listar samma produkter som dina på Amazon.

Avsnitt i en intelligent regel för återprissättning omfattar:

- Välj regeltyp
- [Villkorsavvikelser för konkurrenter](./competitor-conditional-variances.md)
- [Prisjustering](./price-adjustment.md)
- [Baspris](./floor-price.md)
- [Valfritt takpris](./optional-ceiling-price.md)

## Konfigurera regeltypen

Definiera regeltypen i avsnittet _[!UICONTROL Select Rule Type]_.

1. Välj `Intelligent repricing rule` för **[!UICONTROL Rule Type]**.

   Den här inställningen aktiverar fältet _[!UICONTROL Competitor Price Source]_och avsnitten [_[!UICONTROL Competitor Conditional Variances]_](./competitor-conditional-variances.md), [_[!UICONTROL Floor Price]_](./floor-price.md) och [_[!UICONTROL Optional Ceiling Price]_](./optional-ceiling-price.md).

1. Välj ett alternativ för **[!UICONTROL Competitor Price Source]**:

   - **[!UICONTROL Use "Buy Box" Price]** - Välj när du vill justera ditt Amazon-pris baserat på Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) -försäljningspris. Ett pris på [!DNL Buy Box] gäller när flera säljare på Amazon erbjuder samma produkt. Amazon definierar säljaren för [!DNL Buy Box] baserat på prestandakrav. Marknadsförare försöker vinna säljarstatusen för [!DNL Buy Box] och erbjuder maximal synlighet för sina produktlistor.

   - **[!UICONTROL Use Lowest Competitor Price]** - Välj när du vill jämföra och justera ditt listpris till konkurrentpriser för samma produkt. När du väljer det här alternativet aktiveras fälten _[!UICONTROL Minimum Positive Feedback]_och_[!UICONTROL Minimum Feedback Count]_.

1. Om den är aktiverad väljer du ett alternativ för **[!UICONTROL Minimum Positive Feedback]**.

   - **[!UICONTROL All Competitor's Prices]** - Välj när du vill jämföra och justera dina priser baserat på alla konkurrentpriser för samma produkt.

   - **[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Välj när du vill begränsa vilka konkurrenter som priset jämförs med för samma produkt. Denna inställning begränsar konkurrenterna ytterligare genom att kräva att deras notering ska ha minst den valda procentandelen positiv återkoppling innan regeln om lägsta pris tillämpas.

1. Om den är aktiverad anger du ett numeriskt värde för **[!UICONTROL Minimum Feedback Count]**.

   Detta valfria numeriska värde minskar det konkurrenskraftiga priset ytterligare. Om en handlare till exempel har en 95-procentig positiv feedback-klassificering, men bara har ett antal feedback-kommentarer på `20`, kanske det inte är en konkurrent som du vill ändra dina priser mot. Om du anger värdet `1000` måste handlaren dock ha 95 % positiv feedback och minst 1 000 handlarrecensioner.

>[!NOTE]
>
>Du kan använda dessa konkurrentpriser och alternativ för feedback för att undvika att basera dina priser på en konkurrent som har dålig feedback och säljer en produkt av lägre kvalitet.

![Intelligent ompriseringsregel - välj regeltyp](assets/ob-intelligent-price-rule-type.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Rule Type] | Välj en regeltyp. Alternativ:<ul><li>**[!UICONTROL Standard price rule]** - Med den här regeltypen kan du öka eller minska Amazon listpris med en viss procentandel eller ett fast belopp i förhållande till _[!UICONTROL Magento Price Source]_. </li><li>**[!UICONTROL Intelligent repricing rule]** - Med den här regeltypen kan du justera ditt listpris för Amazon baserat på konkurrentens priser. När du väljer det här alternativet aktiveras fälten _[!UICONTROL Minimum Positive Feedback]_och_[!UICONTROL Minimum Feedback Count]_.</li></ul> |
| [!UICONTROL Competitor Price Source] | Välj önskad priskälla. Alternativ:<ul><li>**[!UICONTROL Use "Buy Box" Price]** - Välj det här alternativet om du vill justera ditt Amazon-pris baserat på Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md) -försäljningspris. Ett pris på [!DNL Buy Box] gäller när flera säljare på Amazon erbjuder samma produkt. Amazon definierar säljaren för [!DNL Buy Box] baserat på prestandakrav. Marknadsförare försöker vinna säljarstatusen för [!DNL Buy Box] och erbjuder maximal synlighet för sina produktlistor.</li><li>**[!UICONTROL Use Lowest Competitor Price]** - Välj det här alternativet när du vill jämföra och justera ditt listpris till det [lägsta konkurrentpriset](./lowest-competitor-pricing.md) för samma produkt. När du väljer det här alternativet aktiveras fälten _[!UICONTROL Minimum Positive Feedback]_och_[!UICONTROL Minimum Feedback Count]_.</li></ul> |
| [!UICONTROL Minimum Positive Feedback] | Endast aktiv om `Use Lowest Competitor Price` har valts. Alternativ:<ul><li>**[!UICONTROL All Competitor's Prices]** - Välj när du vill jämföra och justera dina priser baserat på alla konkurrentpriser för samma produkt.</li><li>**[!UICONTROL Minimum 80/90/95/98% positive feedback]** - Välj när du vill begränsa vilka konkurrenter du jämför med och justera dina priser. Denna inställning begränsar dina konkurrenter ytterligare genom att kräva att deras notering ska ha minst den valda procentandelen positiv feedback och sedan använda det lägsta priset för den delmängden av konkurrenter.</li></ul> |
| [!UICONTROL Minimum Feedback Count] | Endast aktiv om `Use Lowest Competitor Price` har valts. Detta valfria numeriska värde ger ytterligare en konkurrensjämförelse. Om en handlare till exempel har en 95-procentig positiv feedback men bara har ett antal feedback-kommentarer på `20`, kanske det inte är en konkurrent som du vill ändra dina priser mot. Om du anger värdet `1000` måste handlaren dock ha 95 % positiv feedback och minst 1 000 handlarrecensioner. |
