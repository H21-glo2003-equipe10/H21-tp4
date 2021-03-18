# TP4 - Énoncé

:calendar: **À remettre pour le 30 avril 2021 à 22h**

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

Faites la même chose qu'au TP3 (incluez les captures d'écran requises). Aucune pondération n'est accordée pour cette partie, mais vous pourrez recevoir **une pénalité allant juqu'à 10%** si la qualité est jugée insuffisante. Cette partie devrait vous être naturelle.

## Partie 2 - Gestion des dépendances (20%)

### 2.1 - Mises à jours des librairies

:warning: Pour cette partie, assurez-vous d'activer les security updates de Dependabot dans `Settings > Security & analysis > Dependabot security updates > Enable`. Cela peut prendre jusqu'à quelques jours avant que les alertes et pull-requests apparaissent. Vous devriez voir apparaître **au moins** les alertes suivantes, accompagnées de leur PR respective :

- `org.eclipse.jetty:jetty-webapp => 9.4.33`
- `junit:junit => 4.13.1` (si vous avez gardé JUnit 4)
- `org.eclipse.jetty:jetty-server => 11.0.1`

Ensuite, pour chaque PR, mergez si possible et :scroll: inclure une capture d'écran de la PR **une fois mergé**.

Si le merge n'est pas possible :

- Analysez les erreurs et tentez de modifiez le code en conséquence et ajouter les librarires manquantes, puis mergez
- S'il y a trop de changements requis, **:scroll: décrivez ces changements et indiquez vos références**
- Si vous ne comprenez ou ne trouvez pas les changements requis, **:scroll: décrivez les erreurs et indiquez vos références**

Afin de connaître les changements requis :

- Faites vos recherches! (les messages/codes d'erreurs sont souvent pratiques)
- Lisez les documentations d'aide à la migration (parfois lourd)

### 2.2 - Mise à jour Java

Mettez à jour Java pour la version **11**. Faites les changements nécessaires dans votre code, et mettez à jour les librairies requises. S'il vous est impossible ou trop difficile de le faire, **:scroll: indiquez pourquoi et justifiez. Incluez vos sources.** Mais sachez qu'avec le code de base, il m'a été très facile de le faire.

## Partie 3 - Open Sourcing (20%)

### 3.1. Lecture préalable

Lisez les chapitres suivants provenant du site Web <https://opensource.guide/>:

- [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
- [Starting an Open Source Project](https://opensource.guide/starting-a-project/)
- [Best Practices for Maintainers](https://opensource.guide/best-practices/)
- [Leadership and Governance](https://opensource.guide/leadership-and-governance/)
- [Your Code of Conduct](https://opensource.guide/code-of-conduct/)
- [The Legal Side of Open Source](https://opensource.guide/legal/)

Ensuite, **discuttez-en en équipe** et répondez aux questions suivantes :

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

## Partie 5 - Publication (20%)

### 5.1 - Documentation d'API

TODO

### 5.2 - Outils d'analyse

Intégrez-vous avez au moins les outils d'analyse de code suivants :

- Couverture des tests
- Qualité du code (ex.: clean code, complexité, sécurité, etc.)

Assurez-vous d'y inclure les badges dans le fichier `README.md`, ou trouvez toute autre manière d'afficher les résultats de façon **dynamique**. Si des badges ne sont pas disponibles, indiquez quel service vous utilisez et fournissez le lien pour y accéder. Si l'accès est restreint au public, communiquez avec votre correcteur.

### 5.3 - README

Mettez à jour votre fichier `README.md`. Il devrait contenir, dans l'ordre :

- Des badges pour:
  - Chaque workflow CI de Github Actions (il devrait y en avoir 2)
  - Chaque outils d'analyse, si possible
  - Tout autre badge vous semblant pertinant
- Les requis (pas besoin de mettre l'IDE)
- Les étapes pour :
  - Préparer/installer le projet
  - Exécuter l'application
  - Exécuter les tests unitaires
  - Exécuter les tests e2e
- Une référence vers votre documentation d'API (ou du moins les étapes pour la générer)
- Des références vers les documents d'Open Sourcing (voir partie [3.2](#32---communauté-opensource))

Assurez-vous de bien séparer le contenu, d'utiliser les bonnes balises Markdown (sous-titres, code, etc.) et d'écrire du contenu clair, concis, pertinant et sans faute.

Aussi, veuillez **supprimer les sections originale suivantes** :

- Technologies
- Structure

## Partie 6 - Rétro (10%)

TODO

- Évaluation du déroulement
  - Bonne répartition? Évolution de vos stratégie?
- Évaluation de l'architecture proposée
  - Trop complexe? Pas assez? Quoi changeriez-vous?
