# Suivi ON-X — activités Air-Sol et CATIA

Deux interfaces indépendantes, dans le même dépôt.

## Ouvrir l'application

- [Accueil](./index.html) : choix entre les deux suivis.
- [Suivi AS V3R17](./Suivi_AS_V3R17.html) : suivi Air-Sol, thème bleu.
- [Suivi Catia V1R11](./Suivi_Catia_V1R11.html) : suivi CATIA, thème orange entreprise.

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

Les deux interfaces lisent les données de `Data-AS` et `Data_C` depuis GitHub et écrivent automatiquement les modifications si un jeton d'écriture est configuré.

**Aucune interface de saisie du jeton.** Dans chaque HTML, modifier directement la constante JavaScript suivante dans une **copie locale non publiée** :

```javascript
const GITHUB_TOKEN = '';
```

Sans jeton, la lecture des fichiers JSON publics fonctionne ; l'écriture est désactivée. Avec un jeton personnel disposant de `Contents: Read and write` sur `suivi-onx`, les modifications sont enregistrées automatiquement.

**Ne pas publier le jeton dans le dépôt GitHub** : il est public, le jeton serait lisible par tout le monde, et GitHub Secret Scanning bloque généralement une telle publication. Le jeton doit rester dans la copie HTML locale. Les versions du dépôt conservent la valeur vide pour éviter d'exposer un secret.

Un jeton GitHub ne limite pas les droits à un collaborateur donné : s'il permet l'écriture sur `suivi-onx`, il peut modifier les huit fiches JSON. Révoquer les anciens jetons éventuellement exposés dans l'historique Git.

## Déploiement

Dans GitHub : Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`.

La page principale du site ouvre le choix entre **Suivi AS** et **Suivi Catia**.
