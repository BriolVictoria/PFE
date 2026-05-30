# My Closet – Cahier des charges

> **Projet de fin d'études (PFE)**
Stack : Laravel · Livewire · Tailwind CSS · MySQL
>

---

## Table des matières

1. Présentation du projet
2. Objectifs
3. Public cible
4. Personas
5. Tâches utilisateurs
6. Fonctionnalités
7. Scénarios d’utilisation
8. Contraintes du projet
9. Critères de réussite
10. Évolutions futures

---

## 1. Présentation du projet

**My Closet** est une application web de gestion de garde-robe personnelle ou familiale. Elle permet à chaque utilisateur de centraliser l'ensemble de ses vêtements dans une interface claire, d'organiser ses tenues à l'avance et de retrouver rapidement un article sans effort.

Le constat de départ est simple : beaucoup de personnes possèdent plus de vêtements qu'elles ne s'en souviennent. Certains articles disparaissent au fond d'une armoire, des achats inutiles s'accumulent, et chaque matin devient une perte de temps. Ce problème touche aussi bien une étudiante pressée qu'un parent qui gère plusieurs garde-robes en même temps.

My Closet répond à ce besoin concret en offrant un outil accessible depuis n'importe quel appareil, conçu pour une utilisation rapide au quotidien — sans courbe d'apprentissage.

---

## 2. Objectifs

### Objectif principal

Permettre à tout utilisateur de gérer sa garde-robe de façon simple, rapide et visuelle, que ce soit pour lui-même ou pour toute sa famille.

### Objectifs secondaires

- Réduire le temps passé à choisir une tenue le matin;
- Faciliter le tri des vêtements inutilisés ou trop petits 
- Permettre la gestion de plusieurs garde-robes (enfants, conjoint·e, etc.);
- Éviter les achats redondants grâce à une meilleure visibilité du stock;
- Préparer ses tenues à l'avance pour gagner du temps;
- Offrir une expérience utilisable sans intérêt particulier pour la mode.

---

## 3. Public cible

My Closet s'adresse à des profils très variés, unis par un besoin commun : mieux s'organiser sans complexité.

- Étudiantes et jeunes actifs pressés le matin;
- Personnes peu intéressées par la mode mais soucieuses de leur organisation;
- Parents gérant les vêtements de plusieurs enfants;
- Personnes cherchant à faire du tri régulièrement;
- Utilisateurs souhaitant une solution légère, sans inscription lourde ni apprentissage.

---

## 4. Personas

### Persona 1 – Ambre, 19 ans · Étudiante

Ambre est étudiante et ses matinées sont courtes. Elle possède beaucoup de vêtements mais son espace de rangement est limité. Elle oublie ce qu'elle a, rachète parfois des pièces en double et se retrouve régulièrement avec des vêtements qu'elle ne porte plus mais qui prennent de la place.

**Ce qu'elle cherche à accomplir :**

- Savoir rapidement ce qu'elle possède sans ouvrir toutes ses armoires;
- Identifier les vêtements qu'elle ne porte plus pour faire du tri facilement;
- Préparer sa tenue la veille pour ne pas perdre de temps le matin;
- Avoir une interface rapide à consulter depuis son téléphone.

**Ce qui la freinerait :**

- Un formulaire trop long pour ajouter un vêtement;
- Une interface qui demande trop d'informations obligatoires;
- Une application lente ou peu adaptée au mobile.

---

### Persona 2 – Lorian, 24 ans · Jeune actif, peu intéressé par la mode

Lorian ne se considère pas comme quelqu'un de fashion. Il s'habille fonctionnellement et n'a aucune envie de passer du temps à réfléchir à ses tenues. Pourtant, il perd du temps chaque matin à chercher ce qui est propre, disponible et acceptable à porter.

**Ce qu'il cherche à accomplir :**

- Savoir en un coup d'œil ce qu'il peut mettre ce matin;
- Connaître le statut de ses vêtements (propre, sale, au lavage);
- Ne pas avoir à réfléchir : juste voir, choisir, partir;
- Utiliser l'appli sans avoir à configurer quoi que ce soit de complexe.

**Ce qui le freinerait :**

- Trop d'options, de catégories, de champs à remplir;
- Une interface trop "mode" ou trop visuelle qui ne correspond pas à son usage;
- Devoir ajouter des photos pour que l'app soit utile.

---

### Persona 3 – Marie, 38 ans · Mère de famille, 2 enfants

Marie gère sa propre garde-robe et celle de ses deux enfants. Le matin, préparer tout le monde en même temps est un défi logistique. Elle cherche à avoir une vue d'ensemble de ce qui est disponible, propre et adapté à la saison pour chaque membre de la famille.

**Ce qu'elle cherche à accomplir :**

- Gérer plusieurs garde-robes depuis un seul compte (la sienne + celle de chaque enfant);
- Savoir quels vêtements sont propres, sales ou à laver pour chaque personne;
- Identifier les vêtements devenus trop petits pour les enfants;
- Préparer les tenues des enfants la veille pour fluidifier la matinée.

**Ce qui la freinerait :**

- Ne pas pouvoir séparer clairement les garde-robes par personne;
- Devoir se reconnecter ou changer de compte pour accéder aux vêtements de ses enfants;
- Une navigation peu claire qui rend difficile de savoir "dans quelle garde-robe on se trouve".

---

## 5. Tâches utilisateurs

Voici les tâches concrètes que les utilisateurs cherchent à accomplir avec My Closet, indépendamment des fonctionnalités techniques :

| Priorité | Tâche                                                                        |
| --- |------------------------------------------------------------------------------|
| Haute | Ajouter un vêtement rapidement, sans remplir un long formulaire.             |
| Haute | Voir d'un seul coup d'œil tous les vêtements disponibles.                    |
| Haute | Connaître le statut d'un vêtement (propre, sale, à laver…).                  |
| Haute | Préparer une tenue en associant plusieurs vêtements.                         |
| Haute | Passer d'une garde-robe à une autre (ex. : la mienne / celle de mon enfant). |
| Moyenne | Filtrer ses vêtements par catégorie, couleur ou statut.                      |
| Moyenne | Identifier les vêtements peu ou jamais portés pour faire du tri.             |
| Moyenne | Rechercher un vêtement précis par son nom.                                   |
| Basse | Modifier ou supprimer un vêtement existant.                                  |
| Basse | Créer, renommer ou supprimer une garde-robe.                                 |

---

## 6. Fonctionnalités

Toutes les fonctionnalités décrites ci-dessous sont **développées et disponibles** dans la version actuelle de l'application.

---

### 6.1 Gestion du compte utilisateur

L'utilisateur dispose d'un espace personnel sécurisé.

- Inscription avec nom, email et mot de passe;
- Connexion et déconnexion;
- Page de paramètres consultable et modifiable.

L'authentification est gérée via le système natif de Laravel avec sessions sécurisées.

---

### 6.2 Gestion des garde-robes

Un utilisateur peut créer plusieurs garde-robes indépendantes au sein du même compte.

- Créer une nouvelle garde-robe (nom libre);
- Renommer une garde-robe existante;
- Supprimer une garde-robe (et tous ses vêtements);
- Naviguer facilement d'une garde-robe à l'autre.

Cela permet par exemple à un parent de gérer sa propre garde-robe et celle de chacun de ses enfants depuis un compte unique.

---

### 6.3 Gestion des vêtements

Chaque vêtement a une fiche individuelle rattachée à une garde-robe.

Champs disponibles :

| Champ | Obligatoire |
| --- | --- |
| Nom | Oui |
| Catégorie | Non |
| Couleur | Non |
| Marque | Non |
| Statut | Non |
| Photo | Non |
- Ajouter un vêtement depuis un formulaire rapide;
- Modifier les informations d'un vêtement;
- Supprimer un vêtement;
- Associer une photo.

Le nom est le seul champ obligatoire pour permettre un ajout rapide, sans friction.

---

### 6.4 Gestion des statuts

Chaque vêtement peut se voir attribuer un statut pour refléter son état actuel.

Exemples de statuts que l'utilisateur pourra ajouter dans l'application :

- Propre;
- Sale;
- À laver;
- Repassé;
- Peu porté;
- Trop petit/grand.

Le statut est modifiable à tout moment directement depuis la fiche de modification.

---

### 6.5 Recherche et filtres

L'utilisateur peut retrouver rapidement un article parmi tous ses vêtements.

- Recherche par nom (saisie libre);
- Filtre par catégorie;
- Filtre par statut.

Les filtres sont cumulables et s'appliquent en temps réel grâce à Livewire, sans rechargement de page.

---

### 6.6 Création de tenues

L'utilisateur peut assembler plusieurs vêtements pour former une tenue enregistrée.

- Créer une tenue en sélectionnant plusieurs vêtements;
- Nommer la tenue;
- Modifier une tenue existante;
- Supprimer une tenue.

Les tenues sont associées à une garde-robe et peuvent être consultées indépendamment des vêtements.

---

### 6.7 Responsive design

L'application est utilisable sur tous les supports.

- Interface adaptée mobile, tablette et desktop;
- Navigation tactile optimisée sur smartphone.

---

## 7. Scénarios d'utilisation

### Scénario 1 – Ambre prépare sa tenue la veille

Il est 22h. Ambre veut préparer sa tenue pour le lendemain matin depuis son téléphone. Elle ouvre My Closet, accède à sa garde-robe et filtre par statut "Propre". Elle visualise les vêtements disponibles, sélectionne un jean et un pull, crée une tenue qu'elle nomme "Demain matin" et la sauvegarde. Le lendemain, elle n'a qu'à consulter sa tenue enregistrée.

---

### Scénario 2 – Ambre fait du tri

Ambre manque de place. Elle ouvre l'application et filtre ses vêtements par statut "Peu porté". Elle identifie en quelques secondes une dizaine de pièces qu'elle n'a pas mises depuis longtemps. Elle peut alors décider de les donner ou les vendre, et les supprime de sa garde-robe.

---

### Scénario 3 – Lorian vérifie ce qu'il peut mettre

Lorian se lève et veut s'habiller vite. Il ouvre My Closet, filtre ses vêtements par statut "Propre" et voit immédiatement ce qui est disponible. Il choisit ce qu'il va mettre, ferme l'app et part. Il n'a pas eu à chercher physiquement dans son armoire ni à réfléchir.

---

### Scénario 4 – Lorian met à jour un statut après la lessive

Lorian vient de faire sa lessive. Il ouvre My Closet et passe le statut de plusieurs vêtements de "Sale" à "Propre" directement depuis la modification de la fiche. L'opération lui prend moins d'une minute.

---

### Scénario 5 – Marie prépare les enfants le soir

Marie veut préparer les affaires de ses deux enfants pour le lendemain. Elle se connecte à My Closet, navigue vers la garde-robe de son fils, filtre par "Propre" et prépare une tenue. Elle fait de même pour sa fille. Elle revient ensuite sur sa propre garde-robe pour choisir sa tenue du lendemain. Tout se fait depuis la même session, sans changer de compte.

---

### Scénario 6 – Marie identifie les vêtements trop petits

Marie remarque que son fils a grandi. Elle ouvre sa garde-robe et filtre par statut "Trop petit". Elle retrouve toutes les pièces concernées, les trie et les supprime de l'application une fois données ou rangées. Sa garde-robe reste à jour.

---

### Scénario 7 – Nouvel utilisateur, premier ajout

Un nouvel utilisateur crée son compte et veut ajouter son premier vêtement. Il clique sur "Ajouter un vêtement", entre uniquement le nom ("Veste noire") et valide. Le vêtement apparaît immédiatement dans sa garde-robe. Il peut ensuite enrichir la fiche en ajoutant une photo, une catégorie ou un statut selon ses envies.

---

## 8. Contraintes du projet

### Temps

Le projet a été réalisé dans le cadre du PFE, avec une durée limitée à la période définie par l'établissement. Les choix de développement ont donc privilégié la stabilité et la cohérence d'une version complète plutôt que la multiplication des fonctionnalités.

### Techniques

Les technologies utilisées sont celles que je maîtrise le mieux, à savoir :

| Technologie | Rôle                                                     |
| --- |----------------------------------------------------------|
| Laravel | Framework back-end (routes, auth, modèles, contrôleurs); |
| Livewire | Composants réactifs sans JavaScript custom ;             |
| Tailwind CSS | Styles utilitaires, responsive design;                   |
| MySQL | Base de données relationnelle.                           |

### Périmètre

La priorité a été de livrer une application stable, utilisable et cohérente de bout en bout. Les fonctionnalités secondaires (notifications, calendrier, recommandations) ont été volontairement repoussées aux évolutions futures.

---

## 9. Critères de réussite

Le projet est considéré comme réussi si :

- Un nouvel utilisateur comprend l'interface sans explication;
- L'ajout d'un vêtement prend moins de 30 secondes;
- Il est possible de consulter sa garde-robe entièrement depuis un smartphone;
- La recherche et les filtres permettent de retrouver un article en moins de 10 secondes;
- Un utilisateur peut gérer plusieurs garde-robes depuis un seul compte sans confusion;
- La création d'une tenue est intuitive sans documentation.

---

## 10. Évolutions futures

### Conception et choix de développement

Toutes les fonctionnalités décrites ont été **entièrement conçues et donc intégrées sur Figma**. Les maquettes couvrent l'ensemble des écrans, interactions et flux utilisateurs associés à chacune d'elles.

Durant le développement, l'objectif a été d'intégrer un maximum de fonctionnalités en code. Cependant, une décision a été prise délibérément : **ne pas intégrer une fonctionnalité à moitié**. Plutôt que de livrer des écrans incomplets ou des parcours cassés, j’ai préféré maintenir une application stable, cohérente et pleinement utilisable de bout en bout. Certaines fonctionnalités ont donc été conservées au niveau Figma uniquement, prêtes à être développées.

Ce projet est **vivant et évolutif**. Il peut être évalué dans son état actuel, mais aussi dans sa capacité à évoluer — les bases techniques posées (Laravel, Livewire, architecture modulaire) permettent d'intégrer ces fonctionnalités. Dans deux ans, l'application pourrai-t être différente tout en restant fidèle à sa vision initiale.

---

*Cahier des charges rédigé dans le cadre du Projet de Fin d'Études – My Closet.*