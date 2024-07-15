---
title: Inställningar för försäljningskanal
description: Uppdatera Commerce-konfigurationen om du vill hantera loggning, referenskälla och synkronisering för Amazon säljkanalsfunktioner.
exl-id: 69f83774-41de-4fde-a357-f100d1bcd9f0
role: Admin, Developer
feature: Sales Channels, Configuration, Logs
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Inställningar för försäljningskanal

När tillägget [!DNL Amazon Sales Channel] är installerat anges standardvärden i Admin for Amazon-försäljningskanalen. De här inställningarna kan ändras i konfigurationsinställningarna för din Amazon Store. De här inställningarna är:

- Intervall för rensning av aktivitetslogghistorik
- Källval för kron
- Alternativ för loggsynkronisering

## Ändra inställningarna för Commerce-kanaler

1. Gå till **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**på sidofältet_ Admin _.

1. Expandera **[!UICONTROL Sales Channels]** i den vänstra panelen och välj **[!UICONTROL Global Settings]**.

1. Välj ett alternativ för **[!UICONTROL Clear Log History]**:

   - `Once Daily` - Välj att rensa din butiksaktivitetshistorik en gång om dagen.

   - `Once Weekly` - Välj att rensa din butiksaktivitetshistorik en gång i veckan.

   - `Once Monthly` - (Standard) Välj att rensa din butiksaktivitetshistorik en gång i månaden.

1. Välj `Magento CRON` för **[!UICONTROL Background Tasks (CRON) Source]**.

   Med det här alternativet kan Amazon-försäljningskanal använda dina [!DNL Commerce] [Cron](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/cron.html) -inställningar för att fastställa kommunikations- och datasynkroniseringsintervall med [!DNL Amazon Seller Central].

1. För **[!UICONTROL Enable Debug Logging]** väljer du `Enabled` om du vill samla in ytterligare synkroniseringsdata när felsökning behövs.

   Loggning av Amazon-försäljningskanal skrivs till filen `{Commerce Root}/var/log/channel_amazon.log` och kan visas i [utvecklarläge](https://experienceleague.adobe.com/docs/commerce-admin/systems/tools/developer-tools.html#operation-modes). Loggning ska endast vara `Enabled` under felsökning och bör vara `Disabled` när felsökningen är slutförd.

1. För **[!UICONTROL Read-Only Mode]** väljer du `Enabled` om du vill blockera alla utgående API-begäranden som ändrar tillståndet.

   Med den här inställningen sparas eventuella ändringar, men skickas inte, förrän [!UICONTROL Read-Only Mode] har inaktiverats. Konfigurationscachen måste rensas för skrivskyddat läge för att aktiveras. Om du vill starta dataöverföringar igen väljer du `Disabled`.

   >[!IMPORTANT]
   >
   >[!UICONTROL Read-Only Mode] är utformat för kopior av produktionsinstansen, till exempel mellanlagring eller QA, och ska inte användas på produktionsinstansen.
   >
   >När en databas migreras till en ny kopia av instansen (identifieras när en butiks URL ändras i konfigurationen) aktiveras [!UICONTROL Read-Only Mode] automatiskt.

1. Klicka på **[!UICONTROL Save Config]**.

![Konfigurationsinställningar för Sales Channel](assets/config-sales-channel-global-settings.png){width="600" zoomable="yes"}
