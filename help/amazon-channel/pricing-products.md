---
title: Hantera Amazon-priser
description: Du kan ange priser för dina Amazon-listor som skiljer sig från din mmerce-butik genom att använda prisreglerna.
redirect_from: /sales-channels/asc/ob-pricing-rules.html
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 15b9468d090b6ee79fd91c729f2481296e98c93a
workflow-type: tm+mt
source-wordcount: '865'
ht-degree: 0%

---

# Hantera Amazon priser

Med Amazon försäljningskanal kan du ange prisregler som gör att du kan ange ett annat listpris för Amazon än det definierade **[!UICONTROL Magento Price Source]** i [pris](./listing-price.md). Du kan också stapla flera regler och till och med använda smarta priser för att justera priset på Amazon baserat på konkurrenternas [[!DNL Buy Box]](./buy-box-competitor-pricing.md) priset eller [lägsta konkurrentpris](./lowest-competitor-pricing.md).

Det finns två typer av prissättningsregler:

- [Standardprisregel](./standard-price-rules.md)
- [Intelligent regel för omprissättning](./intelligent-repricing-rules.md)

   >[!IMPORTANT]
   >
   >Regler för intelligent omprisering fungerar inte korrekt om Amazon är inställt på `Inactive` som vid introduktionen. Prisberäkningarna beror på fraktkostnaderna och regionen måste vara `Active` status för dina fraktpriser att synkronisera från Amazon.
   >
   >Om du vill uppdatera regionens status i ditt Amazon-konto går du till Inställningar > Kontoinformation > Semesterinställningar. Se [Amazon: Liststatus för semester](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620){target=&quot;_blank&quot;} (Inloggning till Seller Central krävs).

Med den här funktionen kan du ändra dina Amazon-priser på ett sätt som liknar [!DNL Commerce] [katalogprisregler](https://docs.magento.com/user-guide/catalog/pricing.html){target=&quot;_blank&quot;}. Du kan skapa komplexa regler som gör att du kan ändra priser för specifika produkter, produkter i specifika kategorier eller till och med med specifika attribut.

Du kan lägga till prisregler för dina Amazon-listor. Prisregler kan användas för att automatiskt justera dina listpriser baserat på en uppsättning definierade villkor. Prisreglerna aktiveras och ditt justerade pris beräknas innan din produkt listas på Amazon.

>[!NOTE]
>
>Priskällan för dina Amazon-listor definieras för **[!UICONTROL Magento Price Source]** i [pris](./listing-price.md) inställningar. Alla justeringsberäkningar som definieras i prisregeln använder priskällan som startvärde.

Med prisreglerna kan du ange ett annat listpris för Amazon än ditt **[!UICONTROL Magento Price Source]** i [pris](./listing-price.md) inställningar. Du kan också stapla flera regler som fungerar tillsammans för att justera priset.

En regel för prissättning/omprissättning kräver tre uppsättningar information under installationen:

- [Allmänna inställningar](./pricing-rule-general-settings.md): Definierar namn, beskrivning, aktiva datum, prioritet för en regel och ställer in beteendet för efterföljande regler baserat på dess prioritetsinställning.
- [Villkor](./pricing-rule-conditions.md): Bestäm vilka produkter som är berättigade till prisregeln.
- [Åtgärder](./pricing-rule-actions.md): Definiera justeringsberäkningarna som tillämpas på priskällan för att bestämma listpriset.

Du kan skapa [standardprisregler](./standard-price-rules.md) som automatiskt justerar ditt Amazon-pris i förhållande till det valda **[!UICONTROL Magento Price Source]** i [pris](./listing-price.md) inställningar. Med den här funktionen kan du ändra dina Amazon-priser på ett sätt som liknar [!DNL Commerce] [katalogprisregler](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;}. Du kan skapa komplexa regler som automatiskt ändrar priser för specifika produkter, produkter i specifika kategorier eller produkter med specifika attribut. Du kan slutföra traditionella inställningar och prissätta dina produkter för att öka eller minska dem baserat på ett fast belopp eller en procentandel.

Ett annat kraftfullt verktyg är [Intelligent omprisering](./intelligent-repricing-rules.md) funktioner som justerar ditt Amazon-pris baserat på konkurrent [[!DNL Buy Box]](./buy-box-competitor-pricing.md) pris eller [Lägsta konkurrentpris](./lowest-competitor-pricing.md). Liknar [!DNL Commerce] [katalogprisregler](https://docs.magento.com/user-guide/marketing/price-rules-catalog.html){target=&quot;_blank&quot;} kan du med den här avancerade funktionen ändra dina Amazon-priser genom att skapa komplexa regler. Regler kan definiera omfattningen av en prisändring för specifika produkter, produkter inom specifika kategorier eller till och med med specifika produktattribut.

Använd smarta ompriser för att justera priserna i Amazon baserat på konkurrentens priser. Amazon försäljningskanal har byggt in säkerhetsfunktioner så att du kan konfigurera för att skydda marginaler eller undvika att matcha en handlares priser med låg feedback. Använda [regler för intelligent reprisering](./intelligent-repricing-rules.md)kan Amazon listpriser automatiskt ändras som ett fast eller procentuellt belopp (uppåt eller nedåt) eller till och med synkroniseras med [[!DNL Buy Box]](./buy-box-competitor-pricing.md) pris eller [Lägsta konkurrentpris](./lowest-competitor-pricing.md) per artikel. Regler kan till och med staplas för att ge obegränsad flexibilitet.

Du kan kontrollera viktiga aspekter av regler, som aktiv/inaktiv status, webbplatsens behörighet, valfria datumintervall och valfria prioritetsnivåer (används för regelstackning).

Du kan till exempel definiera och ange villkoren för en prisregel som automatiskt justerar ditt listpris innan det skickas till Amazon när villkoren är uppfyllda.

Ett annat prisalternativ är [prisåsidosättning](./overrides.md), som anges på listnivå för sig. A [prisåsidosättning](./overrides.md) kan ställas in och en åsidosättning åsidosätter/får företräde framför alla andra standardinställningar, inställningar och regler. An [åsidosätta](./overrides.md) kan anges för pris, hanteringstid, villkor och säljaranteckningar (med några få undantag).

![Prisregler](assets/amazon-pricing-rules.png)

## Standardkolumner

| Kolumn | Beskrivning |
|---|---|
| [!UICONTROL Name] | Namnet på prisregeln enligt [Allmänna inställningar för prisregel](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | Regeltypen enligt [Prisregelåtgärder](./pricing-rule-actions.md) (antingen Standard price rule eller Intelligent repricing rule) |
| [!UICONTROL Is Active] | Om regeln är aktiv, enligt inställningen i [Allmänna inställningar för prisregel](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | Prioriteten framför andra prisvillkor, enligt [Allmänna inställningar för prisregel](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Anger om några ytterligare prisregler bearbetas för produkter som omfattas av denna regel, enligt inställningen i [allmänna inställningar för prisregel](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Början av tidsperioden då regeln är aktiv |
| [!UICONTROL To Date] | Slutet på tidsperioden då regeln är aktiv |
| [!UICONTROL Action] | Visar alla åtgärder som kan tillämpas på en viss lista. Om du vill använda en åtgärd klickar du på **[!UICONTROL Select]** i _[!UICONTROL Action]_kolumn. Alternativ: `Edit Price Rule` / `Delete Price Rule` |
