# Guide de configuration du trigger Google Tag Manager pour time_on_site_2min

Ce guide détaille les étapes pour configurer correctement le déclencheur (trigger) dans Google Tag Manager afin qu'il fonctionne avec l'événement time_on_site_2min.

## Étape 1: Créer un nouveau déclencheur dans GTM

1. Connectez-vous à Google Tag Manager (https://tagmanager.google.com/)
2. Sélectionnez votre conteneur (GTM-WZVSWSDH)
3. Dans le menu de gauche, cliquez sur "Déclencheurs"
4. Cliquez sur "Nouveau" pour créer un nouveau déclencheur

## Étape 2: Configurer le déclencheur

1. Nommez le déclencheur "Time on Site - 2min"
2. Choisissez le type de déclencheur "Événement personnalisé"
3. Dans le champ "Nom de l'événement", saisissez exactement `time_on_site_2min`
   - C'est crucial que ce nom corresponde exactement à celui utilisé dans le dataLayer.push() de votre code
4. Conservez les options par défaut:
   - Ce déclencheur est déclenché sur: "Tous les événements personnalisés"
5. Cliquez sur "Enregistrer"

## Étape 3: Associer le déclencheur à la balise Google Ads

1. Dans le menu de gauche, cliquez sur "Balises"
2. Trouvez la balise "Google Ads Conversion Tracking - time_on_site_2min" et cliquez dessus
3. Dans la section "Déclenchement", cliquez sur le crayon pour modifier
4. Sélectionnez le déclencheur "Time on Site - 2min" que vous venez de créer
5. Cliquez sur "Enregistrer"
6. N'oubliez pas d'enregistrer la balise également

## Étape 4: Publier les modifications

1. Cliquez sur le bouton "Soumettre" en haut à droite
2. Ajoutez une description comme "Configuration du trigger pour time_on_site_2min"
3. Cliquez sur "Publier"

## Vérification du fonctionnement

Pour vérifier que tout fonctionne correctement:

1. Ouvrez votre site web dans un navigateur
2. Ouvrez les outils de développement (F12 ou Ctrl+Shift+I)
3. Allez dans l'onglet "Console"
4. Attendez que le délai configuré soit écoulé (2 minutes en production, 10 secondes en test)
5. Vous devriez voir des messages de log indiquant que l'événement a été envoyé
6. Dans Google Tag Manager, vous pouvez utiliser le mode "Aperçu" pour vérifier en temps réel si les événements sont déclenchés correctement

## Points importants à retenir

- Le nom de l'événement dans le code (`'event': 'time_on_site_2min'`) doit correspondre exactement au nom configuré dans le déclencheur GTM
- Le code JavaScript envoie l'événement au dataLayer, pas directement à Google Ads
- Google Tag Manager intercepte cet événement et déclenche la balise Google Ads configurée
- Si vous modifiez le nom de l'événement dans le code, vous devrez également mettre à jour le déclencheur dans GTM
