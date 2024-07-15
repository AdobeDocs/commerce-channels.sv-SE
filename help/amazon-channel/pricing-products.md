---
title: Hantera Amazon priser
description: Du kan ange priser för dina Amazon-listor som skiljer sig från din Commerce Store genom att använda prisreglerna.
feature: Sales Channels, Price Rules
exl-id: 5c990206-ac72-4ef5-9ed0-ff8d816096eb
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Hantera Amazon priser

Med Amazon försäljningskanal kan du ange prisregler som gör att du kan ange ett annat listpris för Amazon än det definierade **[!UICONTROL Magento Price Source]** i ditt [listpris](./listing-price.md). Du kan också stapla flera regler och till och med använda smarta priser för att justera ditt Amazon-pris baserat på konkurrenternas [[!DNL Buy Box]](./buy-box-competitor-pricing.md)-pris eller det [lägsta konkurrentpriset](./lowest-competitor-pricing.md).

Det finns två typer av prissättningsregler:

- [Standardprisregel](./standard-price-rules.md)
- [Intelligent regel för omprissättning](./intelligent-repricing-rules.md)

  >[!IMPORTANT]
  >
  >Regler för intelligent omprisering fungerar inte korrekt om Amazon-regionen har statusen `Inactive`, som vid introduktionen. Prisberäkningarna beror på fraktkostnaderna och regionen måste ha statusen `Active` för att fraktkostnaderna ska kunna synkroniseras från Amazon.
  >
  >Om du vill uppdatera regionens status i ditt Amazon-konto går du till Inställningar > Kontoinformation > Semesterinställningar. Se [Amazon: Listing Status for Vacations](https://sellercentral.amazon.com/gp/help/help.html?itemID=200135620) (Inloggning till Seller Central krävs).

Med den här funktionen kan du ändra dina Amazon-priser på ett sätt som liknar prisreglerna för [!DNL Commerce] [kataloger](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/pricing/pricing-advanced.html). Du kan skapa komplexa regler som gör att du kan ändra priser för specifika produkter, produkter inom specifika kategorier eller till och med med särskilda attribut.

Du kan lägga till prisregler för dina Amazon-listor. Prisregler kan användas för att automatiskt justera dina listpriser baserat på en uppsättning definierade villkor. Prisreglerna aktiveras och ditt justerade pris beräknas innan din produkt listas på Amazon.

>[!NOTE]
>
>Priskällan för dina Amazon-listor definieras för **[!UICONTROL Magento Price Source]** i inställningarna för [listpris](./listing-price.md). Alla justeringsberäkningar som definieras i prisregeln använder priskällan som startvärde.

Med prisreglerna kan du ange ett annat listpris för Amazon än för din **[!UICONTROL Magento Price Source]** i dina inställningar för [listpris](./listing-price.md). Du kan också stapla flera regler som fungerar tillsammans för att justera priset.

En regel för prissättning/omprissättning kräver tre uppsättningar information under installationen:

- [Allmänna inställningar](./pricing-rule-general-settings.md): Definierar namn, beskrivning, aktiva datum, prioritet för en regel och anger beteendet för efterföljande regler utifrån dess prioritetsinställning.
- [Villkor](./pricing-rule-conditions.md): Bestäm vilka produkter som är berättigade till prisregeln.
- [Åtgärder](./pricing-rule-actions.md): Definiera justeringsberäkningarna som tillämpas på priskällan för att bestämma listpriset.

Du kan skapa [standardprisregler](./standard-price-rules.md) som automatiskt justerar ditt Amazon-pris i förhållande till det valda **[!UICONTROL Magento Price Source]** i dina [listpriser](./listing-price.md) -inställningar. Med den här funktionen kan du ändra dina Amazon-priser på ett sätt som liknar prisreglerna för [!DNL Commerce] [kataloger](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html). Du kan skapa komplexa regler som automatiskt ändrar priser för specifika produkter, produkter i specifika kategorier eller produkter med specifika attribut. Du kan slutföra traditionella inställningar och prissätta dina produkter för att öka eller minska dem baserat på ett fast belopp eller en procentandel.

Ett annat kraftfullt verktyg är funktionen [Intelligent Repricing](./intelligent-repricing-rules.md) som justerar ditt Amazon listpris baserat på konkurrentens [[!DNL Buy Box]](./buy-box-competitor-pricing.md) pris eller [lägsta konkurrentpris](./lowest-competitor-pricing.md). Ungefär som prisreglerna för [!DNL Commerce] [kataloger](https://experienceleague.adobe.com/docs/commerce-admin/marketing/promotions/catalog-rules/price-rules-catalog.html) kan du med den här avancerade funktionen ändra dina Amazon-priser genom att skapa komplexa regler. Regler kan definiera omfattningen av en prisändring för specifika produkter, produkter inom specifika kategorier eller till och med med specifika produktattribut.

Använd smarta ompriser för att justera priserna i Amazon baserat på konkurrentens priser. Amazon försäljningskanal har byggt in säkerhetsfunktioner så att du kan konfigurera för att skydda marginaler eller undvika att matcha en handlares priser med låg feedback. Med hjälp av [smarta omprisregler](./intelligent-repricing-rules.md) kan Amazon listpriser automatiskt ändras som ett fast belopp eller ett procentbelopp (uppåt eller nedåt) eller till och med synkroniseras med [[!DNL Buy Box]](./buy-box-competitor-pricing.md)-priset eller [lägsta konkurrentpriset](./lowest-competitor-pricing.md) per artikel. Regler kan till och med staplas för att ge obegränsad flexibilitet.

Du kan kontrollera viktiga aspekter av regler, som aktiv/inaktiv status, webbplatsens behörighet, valfria datumintervall och valfria prioritetsnivåer (används för regelstackning).

Du kan till exempel definiera och ange villkoren för en prisregel som automatiskt justerar ditt listpris innan det skickas till Amazon när villkoren är uppfyllda.

Ett annat prisalternativ är en [prisåsidosättning](./overrides.md), som ställs in på listnivån. En [prisåsidosättning](./overrides.md) kan anges, och en åsidosättning ignorerar/tar företräde framför alla andra standardvärden, inställningar och regler. Du kan ange en [åsidosättning](./overrides.md) för priser, hanteringstid, villkor och säljaranteckningar (med några få undantag).

![Prisregler](assets/amazon-pricing-rules.png){width="600" zoomable="yes"}

## Standardkolumner

| Kolumn | Beskrivning |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Name] | Namnet på prisregeln, enligt inställningarna i [Allmänna inställningar för prisregel](./pricing-rule-general-settings.md) |
| [!UICONTROL Rule Type] | Regeltypen som anges i [Prisregelåtgärder](./pricing-rule-actions.md) (antingen standardprisregel eller regel för intelligent omprissättning) |
| [!UICONTROL Is Active] | Om regeln är aktiv, enligt inställningen i [Allmänna inställningar för prisregel](./pricing-rule-general-settings.md) |
| [!UICONTROL Priority] | Prioriteten framför andra prisvillkor, enligt inställningen i [Allmänna inställningar för prisregel](./pricing-rule-general-settings.md) |
| [!UICONTROL Stop Further Rules Processing] | Anger om några ytterligare prisregler har bearbetats för produkter som är berättigade till den här regeln, enligt de allmänna inställningarna för [prissättningsregel](./pricing-rule-general-settings.md) |
| [!UICONTROL From Date] | Början av tidsperioden då regeln är aktiv |
| [!UICONTROL To Date] | Slutet på tidsperioden då regeln är aktiv |
| [!UICONTROL Action] | Listar alla åtgärder som kan tillämpas på en viss lista. Om du vill använda en åtgärd klickar du på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_. Alternativ: `Edit Price Rule` / `Delete Price Rule` |
