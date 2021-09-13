---
title: Logg för kommunikationsfel
description: I loggen för kommunikationsfel visas alla kommunikationsfel mellan Amazon och [!DNL Commerce].
exl-id: 0d9f54ba-0fb7-4cd8-a18e-3335f37097a4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# Logg för kommunikationsfel

I loggen för kommunikationsfel visas alla rapporterade kommunikationsfel med Amazon. Informationen innehåller information om Amazon säljkanalsbutik, felkod och kortfattad beskrivning samt datum och tid för felet.

Inga åtgärder är tillgängliga för loggen. Det är en funktion som bara är till för granskning.

Amazon hemsidor för försäljningskanaler har gemensamma [kontroller för arbetsytan](./workspace-controls.md) som gör att du kan anpassa de data som visas.

![Logg för kommunikationsfel](assets/amazon-comm-errors-log.png)

## Standardkolumner

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Amazon Store Name] | Namnet på butiken som definierades när Amazon Store konfigurerades. Se [Store-integrering](./store-integration.md). |
| [!UICONTROL Error Code] | Koden som togs emot från Amazon för att identifiera feltypen. |
| [!UICONTROL Message] | Meddelandet som beskriver felet som är associerat med felkoden. |
| [!UICONTROL Created On] | Datum och tid då felet inträffade. |
