# TP4 - Énoncé

:calendar: **À remettre pour le 30 avril 2021 à 22h**

*Les parties indiquées par :scroll: doivent être répondues dans votre fichier `tp4.md`.*

## Objectifs

- Utiliser des outils de planification et de gestion efficacement et de façon organisée
- Analyser et implémenter les mises-à-jour de dépendances
- Intégrer des outils d'analyse de code
- Préparer un projet pour l'Open Source
- Implémenter des récits utilisateurs
- Migrer vers une base de donnée réelle
- Faire une rétrospective d'un processus logiciel
- Faire une évaluation de la qualité logicielle

## Partie 1 - Outils de planification

Faites la même chose qu'au TP3 (incluez les captures d'écran requises). Aucun point n'est accordée pour cette partie, mais vous pourrez recevoir **une pénalité allant jusqu'à 10%** si la qualité est jugée insuffisante. Cette partie devrait vous être naturelle.

## Partie 2 - Gestion des dépendances (20%)

### 2.1 - Mises à jours des librairies

:warning: Pour cette partie, assurez-vous d'activer les security updates de Dependabot dans `Settings > Security & analysis > Dependabot security updates > Enable`. Cela peut prendre jusqu'à quelques heures avant que les alertes et pull-requests apparaissent. Vous devriez voir apparaître **au moins** les alertes suivantes, accompagnées de leur PR respective :

- `org.eclipse.jetty:jetty-webapp => 9.4.33`
- `junit:junit => 4.13.1` (si vous avez gardé JUnit 4)
- `org.eclipse.jetty:jetty-server => 11.0.1`

Ensuite, pour chaque PR, mergez si possible et :scroll: inclure une capture d'écran de la PR **une fois mergé**.

Si le merge n'est pas possible :

- Analysez les erreurs et tentez de modifier le code en conséquence et ajouter les librarires manquantes, puis mergez
- S'il y a trop de changements requis, ne mergez pas et **:scroll: décrivez ces changements en indiquant vos références**
- Si vous ne comprenez ou ne trouvez pas les changements requis, ne mergez pas et **:scroll: décrivez les erreurs en indiquant vos références**

Afin de connaître les changements requis :

- Faites vos recherches! (les messages/codes d'erreurs sont souvent pratiques)
- Lisez les documentations d'aide à la migration (parfois lourd)

### 2.2 - Mise à jour Java

Mettez à jour Java pour la version **11**. Faites les changements nécessaires dans votre code, et mettez à jour les librairies requises. S'il vous est impossible ou trop difficile de le faire, **:scroll: indiquez pourquoi et justifiez. Incluez vos sources.** Mais sachez qu'il devrait vous être facile de le faire.

## Partie 3 - Open Sourcing (20%)

### 3.1. Lecture préalable

Lisez les chapitres suivants provenant du site Web <https://opensource.guide>:

- [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
- [Starting an Open Source Project](https://opensource.guide/starting-a-project/)
- [Best Practices for Maintainers](https://opensource.guide/best-practices/)
- [Leadership and Governance](https://opensource.guide/leadership-and-governance/)
- [Your Code of Conduct](https://opensource.guide/code-of-conduct/)
- [The Legal Side of Open Source](https://opensource.guide/legal/)

Ensuite, **discutez-en en équipe** et répondez aux questions suivantes :

- :scroll: Qu'avez vous appris? / Qu'est-ce qui vous à le plus étonné? / Qu'est-ce qui va à l'encontre de votre pensée initiale sur l'Open Source?
- :scroll: Quels sont, selon vous, les 3 principaux bénéfices de l'Open Sourcing?
- :scroll: Quel est le principal danger de l'Open Source? Comment réduire ce risque?

### 3.2 - Communauté OpenSource

Assurez-vous de créer les fichiers suivants à la racine de votre projet à partir des lectures précédentes :

- `CODE_OF_CONDUCT.md`
- `CONTRIBUTING.md`
- `LICENSE.md`

:warning: Si vous utilisez des templates, assurez-vous de bien **lire et comprendre** leur contenu et :scroll: **citez vos sources**!

## Partie 4 - Code (30%)

### 4.1 - Implémentation de récits utilisateurs

Parmis les récits que vous avez écrits au TP3, choisissez-en **2 parmis ceux acceptés par le correcteur** et implémentez-les. Assurez-vous de créer les issues et PRs nécessaires (**mettre vos screenshots dans la partie 1**).

Vous pouvez également choisir des récits parmis les suivants :

- [US 1](./user-stories/us1.md)
- [US 2](./user-stories/us2.md)
- [US 3](./user-stories/us3.md)
- [US 4](./user-stories/us4.md)
- [US 5](./user-stories/us5.md)
- [US 6](./user-stories/us6.md)

### 4.2 - Features

Vous devez également implémenter les features suivantes :

- [Feature 10](./features/feature10.md)
- [Feature 9 (v2)](./features/feature9-v2.md)

Rappellez-vous que des tests doivent également être ajoutés.

## Partie 5 - Publication (20%)

### 5.1 - Documentation d'API

Vous devez documenter votre API à l'aide de la<!--🐰🥚--> spécification [OpenAPI version 3.0.3](https://swagger.io/specification/), en format YAML. Il vous est fortement recommandé d'utiliser le [SwaggerEditor](https://editor.swagger.io/#) afin de visualiser et valider votre documentation.

Afin de vous aider, un fichier de démarrage vous est fourni [ici](./openapi.yaml). 

On vous demande de documenter au moins les routes suivantes :

- `POST /seller`
- `GET /seller/{sellerId}`
- `POST /inventory`
- `GET /inventory`
- `GET /inventory/{productId}`
- `POST /buyer`
- `POST /buyer/offer`
- `GET /buyer`

:warning: Assurez-vous de remplir **tous** les champs de descriptions, de validation de valeurs, etc. et n'oubliez-pas d'indiquer les headers lorsque nécessaires. Soyez précis dans les descriptions lorsque nécessaire. **Remettez le fichier YAML exporté dans le dossier `/docs`**.

### 5.2 - Outils d'analyse

Intégrez au moins 1 outils pour **chacune** des catégories d'analyse de code suivantes :

- Couverture des tests
- Qualité du code (clean code et/ou complexité et/ou sécurité, etc.)

Assurez-vous d'y inclure les badges dans le fichier `README.md`, ou trouvez toute autre manière d'afficher les résultats de façon **dynamique**. :scroll: Si des badges ne sont pas disponibles, indiquez quel service vous utilisez et fournissez le lien pour y accéder. Si l'accès est restreint au public, communiquez avec votre correcteur.

### 5.3 - README

Mettez à jour votre fichier `README.md`. Il devrait contenir, dans l'ordre :

- Des badges pour:
  - Chaque workflow CI de Github Actions (il devrait y en avoir 2)
  - Chaque outils d'analyse, si possible
  - Tout autre badge vous semblant pertinent
- Les requis (pas besoin de mettre l'IDE)
- Les étapes pour :
  - Préparer/installer le projet
  - Exécuter l'application
  - Exécuter les tests unitaires
  - Exécuter les tests e2e
- Une référence vers votre documentation d'API (ou du moins les étapes pour la générer)
- Des références vers les documents d'Open Sourcing (voir partie [3.2](#32---communauté-opensource))

Assurez-vous de bien séparer le contenu, d'utiliser les bonnes balises Markdown (sous-titres, code, etc.) et d'écrire du contenu clair, concis, pertinent et sans faute.

Aussi, veuillez **supprimer les sections originale suivantes** :

- Technologies
- Structure

## Partie 6 - Rétro (10%)

Pour cette partie, veuillez discutter, **en équipe**, des points suivants et répondez dans le fichier `tp4.md`.

1. :scroll: **Processus**
   1. Décrivez le processus que vous avez mis en place. Pensez à parler de la séparation du travail, la communication entre les membres, l'utilisation des outils, la gestion des changements, etc.
   2. Était-il efficace? Donnez 2 points positifs et 2 points négatifs.
   3. Que pourriez-vous améliorer? Donnez au moins 3 suggestions.
2. :scroll: **Outils**
   1. Quels outils avez-vous finalement utilisés au quotidien?
   2. Parmis ceux-ci, lesquels avez-vous préférés? Choisissez-en 1 et dites pourquoi.
   3. Quels autres outils auriez-vous également aimer travailler avec? Pensez à des outils que vous avez vu, entendu parler, travaillé avec dans un stage ou un emploi, dans un autre cours, etc.
3. :scroll: **Architecture**
   1. L'architecture du projet était-elle trop complexe? Pourquoi? Si oui, donnez des suggestions afin de la simplifier. Si non, justifiez.
   2. Avez-vous déjà utilisé ou entendu parler d'une autre architecture? Si non, faites des recherches et trouvez-en une. Ensuite, décrivez-la brièvement. Citez vos sources.
   3. Cette autre architecture aurait-elle bien fonctionnée pour le projet? Pourquoi? Citez vos sources.
