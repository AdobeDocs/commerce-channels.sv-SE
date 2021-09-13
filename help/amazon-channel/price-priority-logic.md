---
title: Prioritetslogik
description: Amazon försäljningskanal prioriterar när det gäller att fastställa det publicerade priset för en Amazon-lista.
exl-id: 3aa5ce5e-bb8b-4f9e-ae95-d961565474bd
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 4%

---

# Prioritetslogik

I följande exempel, hur avgör systemet om du ska publicera $31.99, $24.99 eller $27.99?

![Handelspris](assets/amazon-price-scope.png)

Om du vill ta reda på vilket pris som används om en produkt finns på två webbplatser och har ett varierande pris per webbplats använder du prisprioritetslogik (som bestäms av värdet [Sorteringsordning](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).

Om du vill visa sorteringsordningen för dina butiker går du till **[!UICONTROL Stores]** > **[!UICONTROL All Stores]** i sidofältet _Admin_. Klicka på webbplatsnamnet i kolumnen _[!UICONTROL Web Site]_. På sidan_[!UICONTROL Web Site Information]_ visas inställningen _[!UICONTROL Sort Order]_för webbplatsen, vilket avgör webbplatsens prioritet. Värdet `1` anger den högsta prioriteten.

Om produktpriset är `Use Default`, återgår det till standardpriset i stället för webbplatsens prisvärde.

## Exempel 1

|  | Webbplatsprioritet | Pris (webbplats) | Använd standard |
|---|---|---|---|
| Standard | 0 | 31,99 USD | — |
| Butik 1 | 3 | 24,99 USD | Nej |
| Butik 2 | 2 | 27,99 USD | Ja |

- **[!UICONTROL Magento Price Source]** (definieras i [listpriset](./listing-price.md) är inställt på attributet `Price`.
- Titta på webbplatsen med den högsta webbplatsprioriteten, som är Store 1 (definieras med värdet [Sorteringsordning](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).
- Eftersom Store 1 är inställd på att använda webbplatspriset (Använd standard = Nej) är det publicerade priset $24,99.

## Exempel 2

|  | Webbplatsprioritet | Priswebbplats | Använd standard |
|---|---|---|---|
| Standard | 0 | 31,99 USD | — |
| Butik 1 | 3 | 24,99 USD | Ja |
| Butik 2 | 2 | 27,99 USD | Nej |

- **[!UICONTROL Magento Price Source]** (definieras i [listpriset](./listing-price.md) är inställt på attributet `Price`.
- Titta på webbplatsen med den högsta webbplatsprioriteten, som är Store 1 (definieras av [sorteringsordningen](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;} värde).
- Eftersom Store 1 **inte är inställd på att använda webbplatspriset (Använd standard = Ja) kan du titta på nästa webbplats i sorteringsordningen.**
- Eftersom Store 2 **är** inställd på att använda webbplatspriset (Använd standard = Nej) är det publicerade priset $27,99.

## Exempel 3

|  | Webbplatsprioritet | Priswebbplats | Använd standard |
|---|---|---|---|
| Standard | 0 | 31,99 USD | 30,00 USD |
| Butik 1 | 3 | 24,99 USD | — |
| Butik 2 | 2 | 27,99 USD | $20.00 |

I det här exemplet läggs det icke-prisvärde som används om du väljer ett annat värde för _[!UICONTROL Magento Price Source_] (som definieras i inställningarna för [listpris](./listing-price.md)). Icke-prisvärdet använder alltid pris som reservpris.

- **[!UICONTROL Magento Price Source]** (som definieras i dina [[!UICONTROL Listing Price]](./listing-price.md)-inställningar) är inställt på `Non-Price`.
- Titta på webbplatsen med den högsta webbplatsprioriteten, som är `Store 1`(definierad av värdet [Sorteringsordning](https://docs.magento.com/user-guide/stores/stores-all-create-view.html){:target=&quot;_blank&quot;}).
- Eftersom Store 1 **inte är** inställd på att använda attributet `Non-Price` bör du titta på nästa webbplats i sorteringsordningen.
- Eftersom Store 2 **är** inställd på att använda attributet `Non-Price` (Non-Price [Website] = $20.00) är det publicerade priset $20.00.
