# Suivi des modifications pour l'implémentation des balises Google Ads

## Date: 02/04/2025

### Objectifs initiaux:
- Implémenter correctement les balises HTML fournies par Google Ads dans le code du site
- Configurer le trigger dans Google Tag Manager pour la conversion "time_on_site_2min"
- Améliorer le suivi des conversions

### État actuel du site:
- Google Tag Manager (GTM-WZVSWSDH) est déjà implémenté
- La balise Google Ads (AW-16965181803) est déjà implémentée
- Un tracker de temps passé sur le site est implémenté, mais nécessite des ajustements

### Actions réalisées:
1. Analyse du code existant et identification des points d'amélioration
2. Modification du fichier TimeOnSiteTracker.ts pour:
   - Envoyer correctement l'événement au dataLayer avec le nom exact 'time_on_site_2min'
   - Améliorer les logs pour faciliter le débogage
   - Conserver l'envoi direct via gtag en complément (double sécurité)
3. Création d'un guide détaillé pour configurer le trigger dans Google Tag Manager
4. Application des modifications au projet principal

### Modifications effectuées:
- **TimeOnSiteTracker.ts**: Mise à jour pour garantir que l'événement 'time_on_site_2min' est correctement envoyé au dataLayer
- **guide-configuration-gtm.md**: Guide étape par étape pour configurer le trigger dans Google Tag Manager
- **TimeOnSiteTracker.ts.modified**: Version modifiée du fichier pour référence

### Prochaines étapes:
1. Configurer le trigger dans Google Tag Manager selon le guide
2. Vérifier que l'événement est bien déclenché après le délai configuré
3. Confirmer que la conversion est bien comptabilisée dans Google Ads
4. Envisager d'autres événements de conversion à suivre (formulaires, clics sur téléphone, etc.)
