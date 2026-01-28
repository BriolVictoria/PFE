# Cahier des charges — Application de gestion de garde-robe

---

## **📌 Contexte et problématique**

Pour beaucoup de personnes, le matin ou à tout moment de la journée, il n’est pas toujours facile de trouver rapidement une tenue adaptée pour un événement ou une sortie.

Certaines personnes possèdent également beaucoup de vêtements et oublient parfois ce qu’elles ont déjà, ce qui entraîne des achats inutiles.

L’objectif de ce projet est donc de développer une application web permettant à l’utilisateur de :

- Visualiser l’ensemble de sa garde-robe
- Rester organisé
- Créer et gérer facilement des tenues
- Réduire la surconsommation, en évitant d'acheter des vêtements qu'on posséde dèjà

---

## **🎯 Objectifs du projet**

### **Objectif général**

Développer une application web permettant à un utilisateur de gérer sa garde-robe personnelle, de créer des tenues et de rechercher des looks adaptés à ses besoins.

### **Objectifs spécifiques**

- Ajouter, modifier, consulter et supprimer des vêtements et des tags (CRUD)
- Classer les vêtements par catégories et tags
- Créer des tenues à partir des vêtements existants
- Rechercher des vêtements ou tenues selon différents critères
- Fournir une interface fluide, simple, épurée et ergonomique

---

## **🔒 Périmètre du projet**

### **Inclus dans le projet**

- Gestion des utilisateurs (authentification)
- Gestion des vêtements
- Gestion des catégories et des tags
- Création et gestion des looks
- Recherche et filtrage dynamique
- Interface responsive

### **Exclus du projet**

- Achat de vêtements en ligne
- Intelligence artificielle pour créer automatiquement des tenues

---

## **👥 Acteurs du système**

- **Utilisateur** : doit se connecter pour accéder à l’application et gérer sa garde-robe.
- Chaque utilisateur a ses propres tags et catégories.
- Aucune interface client/public pour le moment (optionnelle ultérieurement).

---

## **🛠️ Fonctionnalités détaillées (CRUD)**

### **Authentification**

- Inscription
- Connexion / Déconnexion
- Gestion du profil utilisateur

### **Gestion des vêtements**

- Ajouter un vêtement : nom, catégorie, couleur, saison, occasion, tags, photo
- Modifier un vêtement
- Supprimer un vêtement
- Consulter la liste des vêtements

### **Gestion des catégories**

- Ajouter / modifier / supprimer une catégorie
- Associer une catégorie à un vêtement

### **Gestion des tags**

- Ajouter / modifier / supprimer un tag
- Associer un ou plusieurs tags à un vêtement

### **Gestion des looks (tenues)**

- Créer un look à partir de plusieurs vêtements
- Nommer et décrire un look
- Modifier / supprimer un look
- Consulter la liste des looks

### **Recherche et filtrage**

- Filtrer par catégorie, couleur, saison ou tags
- Résultats dynamiques avec Livewire

---

## **👤 Personas et parcours utilisateurs**

**Jackie – Étudiante**

- Veut préparer sa tenue rapidement chaque matin.
- Parcours : se connecte → consulte ses vêtements → filtre par occasion et couleur → crée un look pour la journée.

**Clotaire – Jeune actif**

- Possède beaucoup de vêtements et oublie ce qu’il a.
- Parcours : ajoute un nouveau vêtement → tague avec “sport” → recherche des tenues pour le week-end.

**Lou – Passionnée de mode**

- Veut organiser ses tenues par style et créer des looks personnalisés.
- Parcours : navigue dans ses catégories → sélectionne des vêtements → compose un look → sauvegarde et ajoute un tag “soirée chic”.

---

## **🎞️ Cas d’utilisation / scénarios**

**Scénario 1 – Ajouter un vêtement**

1. L’utilisateur clique sur “Ajouter un vêtement”
2. Remplit le formulaire (nom, catégorie, couleur, occasion, tags)
3. Téléverse une photo
4. Clique sur “Enregistrer”
5. Le vêtement apparaît dans sa garde-robe

**Scénario 2 – Ajouter un tag**

1. L’utilisateur clique sur “Ajouter un tag”
2. Remplit le formulaire (nom du tag)
3. Clique sur “Enregistrer”
4. Le tag devient disponible lors de la création de vêtements

**Scénario 3 – Ajouter une catégorie**

1. L’utilisateur clique sur “Ajouter une catégorie”
2. Remplit le formulaire (nom)
3. Clique sur “Enregistrer”
4. La catégorie devient disponible lors de la création de vêtements

**Scénario 4 – Créer un look**

1. L’utilisateur sélectionne plusieurs vêtements
2. Donne un nom et éventuellement une description au look
3. Sauvegarde le look
4. Il peut retrouver ce look rapidement pour une occasion spécifique

**Scénario 5 – Rechercher des vêtements**

1. L’utilisateur filtre les vêtements par tags, couleur, occasion
2. Les résultats s’affichent immédiatement (Livewire)
3. L’utilisateur peut ajouter directement ces vêtements dans un look

---

## **🔔 Notifications**

- Notifications dans l’application :
    - Quand un vêtement est ajouté ou supprimé
    - Quand un look est créé ou modifié

---

## **⚙️ Contraintes techniques**

| **Élément** | **Technologie** |
| --- | --- |
| Backend | Laravel 12 |
| Frontend dynamique | Livewire 4 |
| UI | Tailwind CSS |
| Base de données | MySQL |
| Authentification | Laravel (Fortify) |
| Stockage | AWS S3 (pour photos) |
| Serveur / Hébergement | Laravel Cloud  |

---

## **⚠️ Contraintes non fonctionnelles**

- Sécurité des données utilisateurs
- Performance acceptable pour la recherche
- Interface simple et ergonomique
- Responsive (mobile / tablette / desktop)

---

## **🌐 Site public**

- Page d’accueil (connexion / présentation)
- Page “Aide” pour expliquer comment ajouter un vêtement ou créer un look

---

## **✅ Résultats attendus**

- Application CRUD fonctionnelle
- Base de données bien structurée
- Interface moderne et responsive
- Projet conforme aux exigences d’un PFE