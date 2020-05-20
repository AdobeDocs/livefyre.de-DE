---
product: livefyre
audience: end-user
user-guide-title: Livefyre-Implementierungshandbuch
translation-type: tm+mt
source-git-commit: 3664bc1c51d2b372c358385127a1ca9c2f0cfef8
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 4%

---


# Livefyre-Implementierungshandbuch {#implementation}

+ [Livefyre-Implementierungshandbuch](home.md)
+ Erste Schritte {#getting-started}
   + [Erste Schritte mit der Livefyre-Integration](c-getting-started/c-getting-started.md)
   + Implementierungsverfahren {#implementation-process}
      + [Implementierungsverfahren](c-getting-started/c-implementation-process/c-implementation-process.md)
      + [App-Integrationstypen](c-getting-started/c-implementation-process/c-app-integration-types.md)
      + [App-Implementierung](c-getting-started/designer-app-implementation.md)
      + [Implementieren von Livefyre mit Integration von Drittanbietern](c-app-integrations/implement-livefyre-3rd-party.md)
      + [Architektur](c-getting-started/c-implementation-process/c-architecture.md)
      + [Eine App einbetten](c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)
      + [Hinzufügen einer App mithilfe von Livefyre.js](c-getting-started/c-implementation-process/c-add-authetication-to-an-app-using-livefyre.js.md)
      + [Serverseitige Tokens erstellen](c-getting-started/c-implementation-process/c-build-server-side-tokens.md)
      + [CollectionMeta-Token](c-getting-started/c-implementation-process/c-collectionmeta-tokent.md)
      + [Auth-Token des Benutzers](c-getting-started/c-implementation-process/c-user-auth-token.md)
      + [Erstellen einer Sammlung mit dem CollectionMeta-Token](t-create-a-collectionmeta-token.md)
      + [Erstellen einer Prüfsumme](c-creating-a-checksum.md)
+ Identitätsintegration {#identity-integration}
   + [Identitätsintegration](t-about-identity-integration/t-about-identity-integration.md)
   + [Authentifizierungspaket](t-about-identity-integration/c-authorization-package.md)
   + [AuthDelegate-Objekt](t-about-identity-integration/c-building-an-auth-delegate.md)
   + [Veröffentlichen von Benutzerberechtigungen auf externen Systemen (optional)](t-about-identity-integration/c-posting-user-permissions-to-external-systems.md)
   + Einführung der einmaligen Anmeldung {#implementing-sso}
      + [Implementierung der SSO](t-about-identity-integration/c-implementing-sso/c-implementing-sso.md)
      + [Debuggen des Auth-Delegates](t-about-identity-integration/c-implementing-sso/c-debugging-auth.md)
   + Synchronisieren mit Livefyre {#sync-ping-for-pull}
      + [Synchronisieren mit Livefyre mit Ping für Pull](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)
      + [Pull-Endpunkt erstellen](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-pull-endpoint.md)
      + [Endpunkt mit Studio registrieren](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-register-the-endpoint-with-studio.md)
      + [Ping erstellen](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-build-the-ping.md)
      + [Anforderungsstruktur abrufen](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-pull-request-structure.md)
      + [Ping für vollständige Antwort erstellen](t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/c-build-the-ping-for-pull-response.md)
+ Livefyre-Identität {#livefyre-identity}
   + [Livefyre-Identität](c-livefyre-identity-comp/c-livefyre-identity-comp.md)
   + [Livefyre-Identität aktivieren](c-livefyre-identity-comp/t-enable-livefyre-identity.md)
   + Social-Apps mit Livefyre-Identität verwenden {#use-social-apps-with-livefyre-identity}
      + [Social-Apps erstellen](c-livefyre-identity-comp/t-create-your-social-apps.md)
      + [Facebook-App zur Verwendung mit Livefyre-Identität erstellen](c-livefyre-identity-comp/t-create-a-facebook-app-for-use-with-livefyre-identity.md)
      + [Erstellen einer Twitter-App zur Verwendung mit einer Livefyre-Identität](c-livefyre-identity-comp/t-create-a-twitter-app-for-use-with-livefyre-identity.md)
      + [Erstellen Sie ein Yahoo! App für die Verwendung mit Livefyre-Identität](c-livefyre-identity-comp/t-create-a-yahoo-app-for-use-with-livefyre-identity.md)
      + [Erstellen einer Microsoft Live-Identitäts-App zur Verwendung mit Livefyre-Identität](c-livefyre-identity-comp/t-create-a-microsoft-live-id-app-for-use-with-livefyre-identity.md)
      + [Erstellen einer LinkedIn-App zur Verwendung mit Livefyre-Identität](c-livefyre-identity-comp/t-create-a-linkedin-app-for-use-with-livefyre-identity.md)
      + [Erstellen einer GitHub-Identitätsanwendung zur Verwendung mit Livefyre-Identität](c-livefyre-identity-comp/c-create-a-github-identity.md)
      + [Verwenden von Studio zum Verbinden Ihrer Social-Apps mit Ihrer Livefyre-Implementierung](c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)
   + [Hinzufügen von Livefyre.js zur Seite](c-livefyre-identity-comp/t-add-livefyre.js-to-the-page.md)
   + [Livefyre-Identität initialisieren](c-livefyre-identity-comp/t-initialize-livefyre-identity.md)
   + [E-Mails für Livefyre-Identität](c-livefyre-identity-comp/c-emails-for-livefyre-identity.md)
   + [Janrain Capture/Backplane](c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)
   + Installation {#installation}
      + [Installieren von Bibliotheken](c-installing-libraries/c-installing-libraries.md)
      + [Klassen und Methoden](c-installing-libraries/c-methods-livefyre.md)
      + [Netzwerkmethoden](c-installing-libraries/c-network-methods.md)
      + [setSSL-Netzwerkmethode](c-installing-libraries/r-setssl-method.md)
      + [buildLivefyreToken-Netzwerkmethode](c-installing-libraries/r-buildlivefyretoken-method.md)
      + [buildUserAuthToken-Netzwerkmethode](c-installing-libraries/r-builduserauthtoken-method.md)
      + [validateLivefyreToken-Netzwerkmethode](c-installing-libraries/c-validatelivefyretoken-network-method.md)
      + [setUserSyncUrl-Netzwerkmethode](c-installing-libraries/r-setusersyncurl-method.md)
      + [syncUser-Netzwerkmethode](c-installing-libraries/r-syncuser-method.md)
      + [getUrn-Netzwerkmethode](c-installing-libraries/r-geturn-method.md)
      + [getUrnForUser-Netzwerkmethode](c-installing-libraries/r-geturnforuser-method.md)
      + [getNetworkName-Netzwerkmethode](c-installing-libraries/r-getnetworkname-method.md)
      + [getSite-Netzwerkmethode](c-installing-libraries/r-getsite-method.md)
      + [Methoden der Netzwerkklasse](c-installing-libraries/c-network-class-methods.md)
      + [Methoden der Sammlungsklasse](c-installing-libraries/c-collection-methods.md)
      + [createOrUpdate-Erfassungsmethode](c-installing-libraries/r-createorupdate-collection-method.md)
      + [buildCollectionMetaToken-Erfassungsmethode](c-installing-libraries/r-buildcollectionmetatoken-collection-method.md)
      + [buildChecksum-Erfassungsmethode](c-installing-libraries/r-buildchecksum-collection-method.md)
      + [getCollectionContent Collection-Methode](c-installing-libraries/t-getcollectioncontent-collection-method.md)
      + [getUrn-Erfassungsmethode](c-installing-libraries/r-geturn-collection-method.md)
      + [Site-Klassenmethoden](c-installing-libraries/c-site-methods.md)
      + [buildBlogCollection-Site-Methode](c-installing-libraries/r-buildblogcollection-site-method.md)
      + [buildChatCollection-Site-Methode](c-installing-libraries/r-buildchatcollection-site-method.md)
      + [buildCommentsCollection-Site-Methode](c-installing-libraries/r-buildcommentscollection-site-method.md)
      + [buildCountingCollection-Site-Methode](c-installing-libraries/r-buildcountingcollection-site-method.md)
      + [buildRatingsCollection-Site-Methode](c-installing-libraries/r-buildratingscollection-site-method.md)
      + [buildReviewsCollection-Site-Methode](c-installing-libraries/r-buildreviewscollection-site-method.md)
      + [buildSitenotesCollection-Site-Methode](c-installing-libraries/r-buildsitenotescollection-site-method.md)
      + [buildCollection-Site-Methode](c-installing-libraries/r-buildcollection-site-method.md)
      + [getUrn-Site-Methode](c-installing-libraries/r-geturn-site-method.md)
      + [Beispiele](c-installing-libraries/c-libraries-examples.md)
   + Mobile SDKs {#mobile-sdks}
      + [Mobile SDKs](c-mobile-sdks/c-mobile-sdks.md)
      + [Livefyre iOS SDK](c-mobile-sdks/c-livefyre-ios-sdk.md)
      + [Android SDK](c-mobile-sdks/c-android-sdk.md)
+ [Livefyre.js](c-livefyre.js.md)
+ [Erstellen von Livefyre-Token C#](c-creating-livefyre-tokens-c-.md)
+ App-Integrationen {#app-integrations}
   + [Chat](c-app-integrations/c-app-integratios-chat.md)
   + Kommentare {#comments}
      + [Kommentare](c-app-integrations/c-comments-integration/c-comments-integration.md)
   + [Live-Blog](c-app-integrations/c-live-blog-integration.md)
   + [Reviews](c-app-integrations/c-reviews-integration.md)
   + Sir {#sidenotes}
      + [Integration von Sizilien](c-app-integrations/c-sidenotes-integration/r-sidenotes-integration.md)
      + [Hinzufügen von Sidemarken zu einer Seite](c-app-integrations/c-sidenotes-integration/r-adding-sidenotes-to-a-page.md)
      + [Sizilien-App-Ereignis](c-app-integrations/c-sidenotes-integration/r-app-events.md)
      + [Sidebar-Konfigurationsoptionen](c-app-integrations/c-sidenotes-integration/r-configuration-options.md)
      + [Benutzerdefinierte Stile](c-app-integrations/c-sidenotes-integration/r-custom-styles.md)
      + [Benutzerdefinierte Zeichenfolgen für Sidebar](c-app-integrations/c-sidenotes-integration/r-custom-strings.md)
      + [Implementierung von Sizilien](c-app-integrations/c-sidenotes-integration/r-sidenotes-implementation.md)
      + [updateAnchors-Methode](c-app-integrations/c-sidenotes-integration/update-anchors-method.md)
   + [Landkarte](c-app-integrations/c-map-integration.md)
   + [Medienwall](c-app-integrations/c-media-wall-integration.md)
   + [Trends](c-app-integrations/c-trending-integration.md)
+ App-Anpassungen {#app-customizations}
   + [App-Anpassungen](c-app-customizations/c-app-customizations.md)
   + [Anzeigeoptionen ändern](c-app-customizations/c-change-display-options.md)
   + [CSS-Klassen](c-app-customizations/c-css-classes.md)
   + [CSS-Klassen formatieren](c-app-customizations/c-storify-css-classes.md)
   + [Übersetzungssätze](c-app-customizations/c-translation-sets.md)
   + [Das Livefyre-Logo verschieben](c-app-customizations/c-move-the-livefyre-logo.md)
   + [Medien beschränken](c-app-customizations/c-restrict-media.md)
   + [App-Elemente ausblenden](c-app-customizations/c-hide-app-elements.md)
   + [Symbol @mention ändern](c-app-customizations/c-change-mention-icon.md)
   + [Inhalt hervorheben](c-app-customizations/c-highlight-content.md)
   + [Anpassen des Datums- und Uhrzeitstempels](c-app-customizations/c-date-time-stamp.md)
   + Funktionsinhalt {#feature-content}
      + [Funktionsinhalt](c-app-customizations/t-feature-content.md)
      + [Aktivieren von Inhalten in Studio](c-app-customizations/t-enable-featuring-content-in-studio.md)
      + [Wählen Sie Inhalte für Funktionen aus einer App](c-app-customizations/t-select-content-to-feature.md)
      + [Wählen Sie Inhalt aus Studio](c-app-customizations/t-select-content-to-feature-from-studio.md)
      + [CSS zum Formatieren von speziellen Inhalten verwenden](c-app-customizations/c-use-css-to-style-featured-content.md)
      + [Feature APIs](c-app-customizations/c-feature-apis.md)
   + [Verbinden von Janrain mit Livefyre mithilfe von AuthDelegate](c-app-customizations/c-connecting-janrain-to-livefyre-using-authdelegate.md)
   + [Aggregierte spezielle Inhalte mit den speziellen APIs](c-app-customizations/c-aggregated-featured-content-using-the-featured-apis.md)
   + Inhalt formatieren {#style-content}
      + [Inhalt der Benutzergruppe formatieren](c-app-customizations/c-style-user-group-content.md)
      + [Hinzufügen von Benutzern zu Gruppen](c-app-customizations/c-adding-users-to-groups.md)
   + Benutzerdefinierte Stile anwenden {#apply-custom-styles}
      + [Anwenden benutzerdefinierter Stile](c-app-customizations/c-applying-custom-styles-.md)
      + [Hinzufügen benutzerdefinierter Schaltflächen](c-app-customizations/t-add-custom-buttons.md)
   + JavaScript-Ereignisse {#javascript-events}
      + [JavaScript-Ereignisse - Definitionen und Beispiele](c-app-customizations/c-javascript-events.md)
      + [JavaScript-Ereignisse für Visualisierungs-Apps](c-app-customizations/c-javascript-events-for-visualization-apps.md)
      + [JavaScript-Ereignisse für Media Wall](c-app-customizations/c-javascript-events-media-wall.md)
      + [JavaScript-Ereignis für Konvertierungs-Apps](c-app-customizations/c-javascript-events-for-conversation-apps.md)
   + [Kommentaranwendung einbetten](c-app-customizations/c-embed-a-comments-app.md)
   + [Verweisverfolgung](c-app-customizations/c-referral-tracking.md)
   + [Geräte- und Browserunterstützung](c-app-customizations/c-device-and-browser-support.md)
   + [Twitter-Anzeigeanforderungen](c-app-customizations/c-twitter-display-requirements.md)
+ [Stresstest-Richtlinie](c-stress-test-policy.md)
+ Analytics {#analytics}
   + [Analytics](livefyre-analytics/livefyre-analytics.md)
   + [Verwenden von Livefyre mit Adobe Analytics und dem dynamischen Tag-Manager (DTM)](livefyre-analytics/c-use-livefyre-with-adobe-analytics.md)
   + [Verwenden von Livefyre mit anderen Analysetools](livefyre-analytics/c-livefyre-analytics.md)
   + [Livefyre Analytics-Ereignis](livefyre-analytics/c-livefyre-analytics-events.md)
+ [Integration von Livefyre mit AEM](c-livefyre-aem-integration.md)
+ Erweiterte Themen {#advanced-topics}
   + [Anzahl angezeigter Kommentare](c-advanced-topics/t-display-comment-count.md)
   + [Social Sharing aktivieren](c-advanced-topics/c-enabling-social-sharing.md)
   + [Aktivitäten-Stream](c-advanced-topics/c-activity-stream.md)
   + [Bootstrap-HTML](c-advanced-topics/c-bootstrap-html.md)
   + [Sammlung ändern](c-advanced-topics/c-change-collection.md)
   + [Mehrere Sammlungen](c-advanced-topics/c-multiple-collections.md)
   + [Core-App-Typen wechseln](c-advanced-topics/c-switch-core-app-types.md)
   + [Social-Zähler](c-advanced-topics/c-social-counter.md)
   + [Bootsrap- und Stream-API mit Livefyre-Apps verwenden](c-advanced-topics/bootstrap-stream-api.md)
