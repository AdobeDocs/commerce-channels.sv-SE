---
title: Redigera en tilldelad ASIN
description: Ändra ASIN-värdet för en Commerce-produkt om den inte matchades korrekt med någon av dina Amazon-listor.
feature: Sales Channels, Products, Configuration
exl-id: 2aaeb700-96ac-4a15-9379-f74728d2dcbe
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Redigera en tilldelad ASIN

Du kan redigera det Amazon ASIN-värde som tilldelats en produkt i din [!DNL Commerce]-katalog. Den här funktionen är användbar om en katalogprodukt inte matchar någon av dina Amazon-listor korrekt. Om du ändrar tilldelat ASIN för listan ändras inte det ASIN som tilldelats en produkt av Amazon. Det ändrar bara den Amazon-lista som katalogprodukten matchas mot.

När ett tilldelat ASIN ändras:

- [!DNL Commerce] avslutar dina Amazon-listor som är kopplade till det gamla ASIN
- Validerar ASIN med Amazon
- Skapar en lista för det uppdaterade ASIN
- Uppdateringar som listar information i Amazon försäljningskanal

**_Så här redigerar du ett tilldelat ASIN:_**

1. Visa listan på sidan _[!UICONTROL Product Listings]_(_[!UICONTROL Inactive]_, _[!UICONTROL Active]_eller fliken_[!UICONTROL Ineligible]_).

1. Klicka på **[!UICONTROL Edit Assigned ASIN]** under _[!UICONTROL Actions]_.

   Åtgärden öppnar sidan _[!UICONTROL Product Listing Update]_.

1. Ange det nya ASIN-värdet för **[!UICONTROL Assign ASIN]**.

1. Klicka på **[!UICONTROL Save Listing Update]** om du vill spara ändringarna.

![Redigera ett tilldelat ASIN](assets/amazon-assigned-asin-edit.png){width="600" zoomable="yes"}
