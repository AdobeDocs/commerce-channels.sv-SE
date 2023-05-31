---
title: Redigera en tilldelad ASIN
description: Ändra ASIN-värdet för en Commerce-produkt om den inte matchades korrekt med någon av dina Amazon-listor.
exl-id: 2aaeb700-96ac-4a15-9379-f74728d2dcbe
source-git-commit: df26834c81b5e26ad0ea8c94c14292eb7c24bae8
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Redigera en tilldelad ASIN

Du kan redigera Amazon ASIN-värdet som tilldelats en produkt i [!DNL Commerce] katalog. Den här funktionen är användbar om en katalogprodukt inte matchar någon av dina Amazon-listor korrekt. Om du ändrar tilldelat ASIN för listan ändras inte det ASIN som tilldelats en produkt av Amazon. Det ändrar bara den Amazon-lista som katalogprodukten matchas mot.

När ett tilldelat ASIN ändras:

- [!DNL Commerce] avslutar dina Amazon-listor som är kopplade till det gamla ASIN
- Validerar ASIN med Amazon
- Skapar en lista för det uppdaterade ASIN
- Uppdateringar som listar information i Amazon försäljningskanal

**_Så här redigerar du en tilldelad ASIN:_**

1. Visa listan på _[!UICONTROL Product Listings]_sida (_[!UICONTROL Inactive]_, _[!UICONTROL Active]_, eller_[!UICONTROL Ineligible]_ -fliken).

1. Under _[!UICONTROL Actions]_, klicka **[!UICONTROL Edit Assigned ASIN]**.

   Den här åtgärden öppnar _[!UICONTROL Product Listing Update]_sida.

1. För **[!UICONTROL Assign ASIN]** anger du det nya ASIN-värdet.

1. Spara ändringarna genom att klicka på **[!UICONTROL Save Listing Update]**.

![Redigera en tilldelad ASIN](assets/amazon-assigned-asin-edit.png){width="600" zoomable="yes"}
