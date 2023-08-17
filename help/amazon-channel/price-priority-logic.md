---
title: Amazon försäljningskanal - Prioritetslogik
description: Amazon försäljningskanal prioriterar när det gäller att fastställa det publicerade priset för en Amazon-lista.
feature: Sales Channels, Price Rules
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 4%

---

# Prioritetslogik

I följande exempel, hur avgör systemet om du ska publicera $31.99, $24.99 eller $27.99?

![Handelspris](assets/amazon-price-scope.png){width="400"}

Använd prisprioritetslogik (som bestäms av [Sorteringsordning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) värde).

Om du vill visa butikernas sorteringsordning går du till **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** i _Administratör_ sidofält. I _[!UICONTROL Web Site]_klickar du på webbplatsens namn. The_[!UICONTROL Web Site Information]_ sidan visar _[!UICONTROL Sort Order]_för webbplatsen, vilket avgör webbplatsens prioritet. Värdet för `1` anger högsta prioritet.

Om produktpriset är inställt på `Use Default`, används standardpriset istället för webbplatsens prisvärde.

## Exempel 1

|         | Webbplatsprioritet | Pris (webbplats) | Använd standard |
|---------|------------------|-----------------|-------------|
| Standard | 0 | $31.99 | — |
| Butik 1 | 1 | $24.99 | Nej |
| Butik 2 | 2 | $27.99 | Ja |

- The **[!UICONTROL Magento Price Source]** (definieras i [Listpris](./listing-price.md) är inställt på `Price` -attribut.
- Titta på webbplatsen med högsta webbplatsprioritet, som är Store 1 (definieras av [Sorteringsordning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) värde).
- Eftersom Store 1 är inställd på att använda webbplatspriset (Använd standard = Nej) är det publicerade priset $24,99.

## Exempel 2

|         | Webbplatsprioritet | Priswebbplats | Använd standard |
|---------|------------------|---------------|-------------|
| Standard | 0 | $31.99 | -- |
| Butik 1 | 1 | $24.99 | Ja |
| Butik 2 | 2 | $27.99 | Nej |

- The **[!UICONTROL Magento Price Source]** (definieras i [Listpris](./listing-price.md) är inställt på `Price` -attribut.
- Titta på webbplatsen med högsta webbplatsprioritet, som är Store 1 (definieras av [sorteringsordning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) värde).
- Sedan butik 1 **är inte** ange att webbplatspriset ska användas (Använd standard = Ja), se nästa webbplats i sorteringsordningen.
- Sedan butik 2 **är** om du vill använda webbplatspriset (Använd standard = Nej) är det publicerade priset $27,99.

## Exempel 3

|         | Webbplatsprioritet | Priswebbplats | Använd standard |
|---------|------------------|---------------|-------------|
| Standard | 0 | $31.99 | $30.00 |
| Butik 1 | 1 | $24.99 | -- |
| Butik 2 | 2 | $27.99 | $20.00 |

I det här exemplet läggs det icke-prisvärde som används om du väljer ett annat värde för _[!UICONTROL Magento Price Source_] (definieras i [Listpris](./listing-price.md) inställningar). Icke-prisvärdet använder alltid pris som reservpris.

- The **[!UICONTROL Magento Price Source]** (definieras i [[!UICONTROL Listing Price]](./listing-price.md) inställningar) är inställda på `Non-Price`.
- Webbplatsen har högsta webbplatsprioritet, vilket är `Store 1`(definieras av [Sorteringsordning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/site-store/store-views.html) värde).
- Sedan butik 1 **är inte** ange att `Non-Price` -attribut, se nästa webbplats i sorteringsordningen.
- Sedan butik 2 **är** ange att `Non-Price` attribute (Non-Price [Webbplats] = 20,00 USD) är det publicerade priset 20,00 USD.
