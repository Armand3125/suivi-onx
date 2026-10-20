# Suivi des activités Air-Sol — ON-X

Interface de suivi d'activités Air-Sol, reprise de la version Suivi_AS_V3R8 et adaptée en V3R9.

## Organisation
- `index.html` : accès au suivi depuis GitHub Pages
- `Suivi_AS_V3R9.html` : interface de suivi
- `data/menouer.json`, `data/noelle.json`, `data/vincent.json`, `data/armand.json` : données des quatre collaborateurs
- `data/report-period.json` : période du rapport partagé

## Restauration
Données récupérées sur `Armand3125/suivi-air-sol` depuis les derniers commits cohérents précédant les modifications suspectes du 16 octobre 2026. Aucun des trois messages de piratage n'a été recopié. Le dépôt source n'a pas été modifié.

## Sécurité
**Aucun jeton GitHub n'est inclus dans l'interface.** La lecture publique n'exige pas de jeton. Pour enregistrer des modifications, utiliser le bouton « Accès GitHub » et saisir un jeton personnel à permissions limitées `Contents: Read and write` sur ce seul dépôt. Le jeton reste en mémoire et disparaît au rechargement. Il faut révoquer les jetons déjà présents dans d'anciennes versions HTML.
**Attention : ce dépôt est public** ; les fichiers JSON sont lisibles par tout le monde. Le code côté navigateur et les jetons personnels ne remplacent pas un backend avec authentification et autorisations par utilisateur.
