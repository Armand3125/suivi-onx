# Suivi ON-X — activités Air-Sol et CATIA

Deux interfaces indépendantes, dans le même dépôt.

## Ouvrir l'application

- [Accueil](./index.html) : choix entre les deux suivis.
- [Suivi AS V3R11](./Suivi_AS_V3R11.html) : suivi Air-Sol, thème bleu.
- [Suivi C V1R2](./Suivi_C_V1R2.html) : suivi CATIA, thème orange entreprise.

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

L'application lit automatiquement les JSON depuis GitHub. La sauvegarde des modifications dans GitHub est **automatique** après une configuration unique sur chaque navigateur : cliquer « Activer l’écriture », coller un **jeton personnel à permissions limitées**, autorisé sur ce seul dépôt et avec `Contents: Read and write`. Le navigateur le conserve localement et le réutilise dans les deux suivis, y compris après rechargement. Le bouton devient « Écriture active » et permet également de remplacer ou supprimer le jeton. Aucun jeton n'est intégré au code HTML ni publié dans le dépôt. Un jeton côté navigateur ne procure **aucune isolation des droits par collaborateur** : toute personne disposant du droit `Contents: write` peut modifier les huit fiches.

**Sécurité :** ce dépôt est actuellement public et les fichiers JSON sont visibles sur Internet. Les jetons intégrés dans de précédentes versions HTML ou historiques Git doivent être révoqués, car retirer le jeton du fichier courant ne suffit pas.

## Déploiement

Dans GitHub : Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`.

La page principale du site ouvre le choix entre **Suivi AS** et **Suivi C**.
