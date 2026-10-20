# Suivi ON-X — activités Air-Sol et CATIA

Deux interfaces indépendantes, dans le même dépôt.

## Ouvrir l'application

- [Accueil](./index.html) : choix entre les deux suivis.
- [Suivi AS V3R12](./Suivi_AS_V3R12.html) : suivi Air-Sol, thème bleu.
- [Suivi C V1R3](./Suivi_C_V1R3.html) : suivi CATIA, thème orange entreprise.

## Données

**Data-AS** (données Air-Sol conservées) :
- `menouer.json` — Menouer ZAOUI
- `noelle.json` — Noëlle FOUCONNIER
- `vincent.json` — Vincent MONTI
- `armand.json` — Armand JULIEN
- `report-period.json` — période commune au suivi Air-Sol.

**Data_C** (fiches CATIA distinctes, initialement vides) :
- `mathieu.json` — Mathieu Monjardet
- `bachar.json` — Bachar Bahsoun
- `sami.json` — Sami Khiari
- `guillaume.json` — Guillaume Lenoir d'Espinasse
- `report-period.json` — période commune au suivi CATIA.

Le menu des activités CATIA propose : CATIA Bordeaux, Toulouse, Marseille, Nantes, Lille, Lyon, Labo DTI, Téléphonie, Transition, Supervision, Secbox, Réseau et Autre.

### Pourquoi les fiches CATIA sont-elles vides ?

Les données trouvées sous les quatre noms CATIA dans l'ancien dépôt étaient en réalité les activités des collaborateurs Air-Sol (fichiers écrasés/mélangés). Elles n'ont pas été attribuées automatiquement aux utilisateurs CATIA. Les données Air-Sol sont restaurées dans `Data-AS`. Les versions originales restent consultables dans l'historique du dépôt source.

## Sauvegarde et accès

Les deux suivis lisent les JSON de `suivi-onx` et enregistrent automatiquement les modifications. La première fois sur un navigateur, cliquer sur **Configurer l'écriture**, coller le jeton GitHub dans le champ masqué et cliquer **Enregistrer**. L'application vérifie l'accès au dépôt. Le jeton est ensuite mémorisé localement dans ce navigateur et réutilisé automatiquement par Suivi AS et Suivi C ; aucune ressaisie n'est nécessaire tant qu'il reste valable.

Cliquer sur **Écriture automatique** pour remplacer le jeton ou sur **Supprimer l'accès** pour l'effacer du navigateur. Aucun jeton n'est inclus dans les fichiers du dépôt ni dans l'historique de ces versions.

**Sécurité :** le dépôt reste actuellement public, les JSON sont donc accessibles publiquement. L'enregistrement du jeton dans le navigateur (localStorage) n'offre pas une isolation de sécurité par collaborateur. Toute personne ayant accès au profil navigateur ou à des scripts exécutés sur ce même site peut potentiellement accéder au jeton. Ne pas coller un jeton directement dans un fichier HTML publié. Révoquer les anciens jetons exposés dans l'historique GitHub.

## Déploiement

Dans GitHub : Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`.

La page principale du site ouvre le choix entre **Suivi AS** et **Suivi C**.
