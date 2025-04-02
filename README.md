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

### Actions à réaliser:
1. Modifier le fichier TimeOnSiteTracker.ts pour améliorer le déclenchement de l'événement
2. S'assurer que l'ID de conversion correct est utilisé
3. Configurer un déclencheur dans Google Tag Manager qui réagit au dataLayer
4. Vérifier que tout fonctionne correctement

### Modifications effectuées:
- [En cours]
