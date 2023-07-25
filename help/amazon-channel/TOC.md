---
user-guide-title: Användarhandbok för Amazon Sales Channel
user-guide-description: Generera säljmaterial genom Amazon genom att integrera Adobe Commerce eller Magento Open Source med [!DNL Amazon Seller Central] konto.
breadcrumb-title: Amazon försäljningskanal
role: Admin, User
feature: Sales Channels
recommendations: noDisplay
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---


# Amazon försäljningskanal - [!DNL channel manager] för Adobe Commerce {#amazon}

- [Användarhandbok för Amazon Sales Channel](guide-overview.md)
- [Introduktion till Amazon försäljningskanal](overview.md)
- Komma igång {#getting-started}
   - [Om Amazon Marketplace](about-amazon-marketplace.md)
   - [Amazon och Commerce-katalogen](about-listings-and-catalog.md)
   - [God praxis och begränsningar](amazon-best-practices.md)
   - [Installera tillägget](install.md)
- Onboarding {#onboarding}
   - [Införliva Amazon försäljningskanal](amazon-onboarding-home.md)
   - [Åtgärder före installation](amazon-pre-setup-tasks.md)
   - [Skapa [!DNL Commerce] attribut för Amazon](ob-creating-magento-attributes.md)
   - [Verifiera Amazon API-nyckeln](amazon-verify-api-key.md)
   - [Integrering med Store](store-integration.md)
   - [Skapa listregel](ob-create-listing-rule.md)
   - [Standardinställningar för lagring](default-store-settings.md)
- Hantera försäljningskanalen {#manage}
   - [Startsida](amazon-sales-channel-home.md)
   - [Amazon butiker](managing-stores.md)
   - [Arbetsytekontroller](workspace-controls.md)
   - [Utbildning och förberedelse](learning-preparation.md)
   - Attribut {#attributes}
      - [Visa attribut](attributes-view.md)
      - [Hantera attribut](managing-attributes.md)
      - [Skapa och redigera attribut](creating-attributes.md)
      - [Visa attributmappning](amazon-matching-attributes-values.md)
   - [Administrationsinställningar för försäljningskanal](sales-channel-settings.md)
   - [Amazon Store-instrumentpanel](amazon-store-dashboard.md)
   - [Lagringsinställningar](ob-store-review.md)
- Listinställningar {#listing-settings}
   - [Visa listinställningar](listing-settings.md)
   - [Produktlistningsåtgärder](product-listing-actions.md)
   - [Tredjepartslistor](third-party-listing-settings.md)
   - [Listpris](listing-price.md)
   - [(B2B) företagspriser](business-pricing.md)
   - [Lager/kvantitet](stock-quantity.md)
   - [Fullgjord av](fulfilled-by.md)
   - [Katalogsökning](catalog-search.md)
   - [Villkor för produktlista](product-listing-condition.md)
   - [Förnyade produkter](renewed-products.md)
- [Orderinställningar](order-settings.md)
- [Inställningar för butiksintegrering](store-integration-settings.md)
- Listregler och prissättningsregler {#rules}
   - [Listregler](listing-rules.md)
   - Prisregler {#pricing-rules}
      - [Hantera priser](pricing-products.md)
      - [Lägg till ny prisregel](add-pricing-rule.md)
      - [Allmänna inställningar för prisregel](pricing-rule-general-settings.md)
      - [Prisregelvillkor](pricing-rule-conditions.md)
      - [Prisregelåtgärder](pricing-rule-actions.md)
      - [Standardprisregel](standard-price-rules.md)
      - [Intelligent regel för omprissättning](intelligent-repricing-rules.md)
      - [Villkorsavvikelser för konkurrenter](competitor-conditional-variances.md)
      - [Prisjustering](price-adjustment.md)
      - [Golvpris](floor-price.md)
      - [Optimalt pris](optional-ceiling-price.md)
      - [Prisområde](price-scope.md)
      - [Prioritetslogik](price-priority-logic.md)
      - [Buy Boxens konkurrentpriser](buy-box-competitor-pricing.md)
      - [Lägsta konkurrentpris](lowest-competitor-pricing.md)
   - Exempel {#rules-examples}
      - [Definiera ett villkor](ob-define-condition-example.md)
      - [Exempel på prisregler](price-rule-examples.md)
- Rapporter och loggar {#reports-logs}
   - [Loggar och butiksrapporter](amazon-logs-reports.md)
   - Lagra rapporter {#store-reports}
      - [Konkurrenskraftiga prisanalyser](competitive-price-analysis.md)
      - [Förbättrad lista](listing-improvements.md)
   - Loggar {#logs}
      - [Logg för liständringar](listing-changes-log.md)
      - [Logg för kommunikationsfel](communication-errors-log.md)
- Hantera listor {#admin-listings}
   - [Hantera Amazon-listor](managing-product-listings.md)
   - Efter status/flik {#status-tab}
      - [Hantera efter status/flik](managing-listings-by-tab.md)
      - [Ofullständiga listor](incomplete-listings.md)
      - [Nya tredjepartslistor](new-third-party-listings.md)
      - [Klar att visas](ready-to-list.md)
      - [Inaktiva listor](inactive-listings.md)
      - [Aktiva listor](active-listings.md)
      - [Åsidosättningar](overrides.md)
      - [Ej berättigade listor](ineligible-listings.md)
      - [Avslutade listor](ended-listings.md)
   - Efter åtgärder {#actions}
      - [Hantera efter åtgärder](managing-listings-by-action.md)
      - [Skapa och tilldela katalogprodukter](creating-assigning-catalog-products.md)
      - [Skapa och redigera åsidosättningar](creating-editing-overrides.md)
      - [Skapa en SKU för Aliasförsäljare](create-alias-seller-sku.md)
      - [Redigera en tilldelad ASIN](edit-assigned-asin.md)
      - [Avsluta en Amazon-lista](end-listings-manually.md)
      - [Publicera en Amazon-lista](publish-listings-manually.md)
      - [Uppdatera nödvändig information](amazon-manually-update-incomplete-listing.md)
      - [Visa detaljer](product-listing-details.md)
- Hantera order {#admin-orders}
   - [Hantera order](managing-orders.md)
   - [Visa Amazon-order](amazon-orders-all.md)
   - [Visa beställningsinformation för Amazon](amazon-order-details.md)
   - [Vanliga åtgärder för orderbehandling](common-order-processing.md)
   - [Arbetsflöden för uppfyllelse](fulfillment-workflows.md)
   - [Avbryt ej levererade order](cancel-unshipped-order.md)
- [Versionsinformation](release-notes.md)
