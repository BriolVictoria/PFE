# **Application de gestion de garde-robe**

---

## **📌 Contexte et problématique**

Pour beaucoup de personnes, il n’est pas toujours facile de trouver rapidement une tenue adaptée pour un événement ou une sortie. Certaines possèdent beaucoup de vêtements et oublient parfois ce qu’elles ont déjà, ce qui entraîne des achats inutiles.

L’objectif de ce projet est donc de développer une application web permettant à l’utilisateur de :

- Visualiser l’ensemble de sa garde-robe
- Rester organisé
- Créer et gérer facilement des tenues
- Recevoir des suggestions et alertes pour optimiser l’usage de ses vêtements

---

## **🎯 Objectifs du projet**

### **Objectif général**

Développer une application web permettant à un utilisateur de gérer sa garde-robe personnelle, de créer des tenues, de rechercher des looks adaptés et d’obtenir des suggestions pour ses vêtements.

### **Objectifs spécifiques**

- Ajouter, modifier, consulter et supprimer des vêtements, catégories et tags (CRUD)
- Classer les vêtements par catégorie, couleur, saison et tags
- Créer et gérer des tenues ou looks personnalisés
- Rechercher des vêtements ou tenues selon plusieurs critères
- Fournir une interface fluide, simple, épurée et ergonomique
- Mettre en place des fonctionnalités avancées : alertes, profils multiples, suggestions de tenues en fonction de ce qu’on porte souvent…

---

## **🔒 Périmètre du projet**

### **Inclus dans le projet**

- Gestion des utilisateurs et authentification
- Gestion des vêtements, catégories et tags
- Création et gestion des looks
- Recherche et filtrage dynamique
- Interface responsive
- Profils multiples / partagés
- Alertes pour tri et rangement
- Suggestions automatiques de tenues (basées sur occasion, météo ou historique)
- Intégration météo
- Mode “lookbook” et favoris
- Statistiques d’utilisation des vêtements
- Lien vers des sites de seconde main / marketplaces

### **Exclus du projet**

- Achat de vêtements en ligne directement depuis l’application
- Intelligence artificielle avancée pour la création automatique de tenues

---

## **👥 Acteurs du système**

- **Utilisateur** : doit se connecter pour gérer sa garde-robe.
- **Profil secondaire** : par exemple, un parent peut consulter le dressing de ses enfants.
- Chaque utilisateur possède ses propres tags, catégories et tenues.

---

## **🛠️ Fonctionnalités détaillées (CRUD et avancées)**

### **Authentification**

- Inscription, connexion et déconnexion
- Gestion du profil utilisateur
- Gestion des profils multiples / partagés

### **Gestion des vêtements**

- Ajouter un vêtement : nom, catégorie, couleur, saison, occasion, tags, photo
- Modifier un vêtement
- Supprimer un vêtement
- Consulter la liste des vêtements
- Lien direct vers des sites de seconde main (Vinted, Le Bon Coin…) si un vêtement n’a pas été utilisé depuis longtemps
- Tags dynamiques et auto-suggestion

### **Gestion des catégories et tags**

- Ajouter, modifier, supprimer une catégorie ou un tag
- Associer une catégorie ou plusieurs tags à un vêtement

### **Gestion des looks / tenues**

- Créer un look à partir de plusieurs vêtements
- Nommer et décrire un look
- Modifier / supprimer un look
- Consulter la liste des looks
- Mode “lookbook” pour naviguer par photo
- Favoris

### **Recherche et filtrage avancé**

- Filtrer par catégorie, couleur, saison, occasion, tags
- Résultats dynamiques avec Livewire

### **Suggestions et alertes**

- Suggestions de tenues basées sur : météo, occasion, historique d’utilisation
- Notifications pour vêtements non utilisés depuis longtemps
- Alertes de tri si l’utilisateur possède plus de 200 vêtements
- Statistiques d’utilisation (vêtements les plus ou moins portés)

---

## **👤 Personas et parcours utilisateurs**

**Jackie – Étudiante**

- Veut préparer sa tenue rapidement chaque matin
- Parcours : se connecte → consulte ses vêtements → filtre par occasion et couleur → crée un look → sauvegarde comme favori

**Clotaire – Jeune actif**

- Possède beaucoup de vêtements et oublie ce qu’il a
- Parcours : ajoute un nouveau vêtement → tague “sport” → voit qu’il a beaucoup de vêtement de se tague la → fait un tri en mettant ses vêtements sur Vinted via le lien disponible

**Lou – Passionnée de mode**

- Veut organiser ses tenues par style et créer des looks personnalisés
- Parcours : navigue dans son lookbook → sélectionne des vêtements → compose un look → sauvegarde et ajoute un tag “soirée chic” → consulte les alertes pour optimiser son dressing

**Marie – Maman**

- Veut gérer le dressing de ses enfants
- Parcours : crée un profil enfant → consulte la garde-robe → filtre par taille et saison → propose des tenues → reçoit alertes pour tri

---

## **🎞️ Cas d’utilisation / scénarios**

1. **Ajouter un vêtement** : formulaire + photo + lien vers marketplaces si inactif
2. **Ajouter un tag / catégorie** : formulaire ou déjà existant
3. **Créer un look** : choix de plusieurs vêtements, nom, description, sauvegarde, ajout au favori
4. **Recherche multi-critères** : combinaison de catégorie, couleur, saison, occasion, tags
5. **Suggestions de tenue** : basé sur météo ou historique d’utilisation
6. **Alertes et tri** : notification si dressing > 200 vêtements ou vêtement inactif
7. **Consulter statistiques** : voir vêtements les plus ou moins portés

---

## **🔔 Notifications**

- Quand un vêtement est ajouté, supprimé ou inactif depuis longtemps
- Quand un look est créé ou modifié
- Alertes de tri et suggestions de tenues

---

## **⚙️ Contraintes techniques**

| **Élément** | **Technologie** |
| --- | --- |
| Backend | Laravel  |
| Frontend dynamique | Livewire  |
| UI | Tailwind CSS |
| Base de données | MySQL |
| Authentification | Laravel (Fortify) |
| Stockage | AWS S3 (pour photos) |
| Serveur / Hébergement | Laravel Cloud ou autre |

---

## **⚠️ Contraintes non fonctionnelles**

- Sécurité et confidentialité des données utilisateurs
- Performance acceptable pour recherche et filtrage
- Interface simple, ergonomique et responsive

---


## **🌐 Site public**

- Page d’accueil (connexion / présentation)
- Page d’aide (explications pour ajouter un vêtement ou créer un look)

---

## **✅ Résultats attendus**

- Application CRUD fonctionnelle et ergonomique
- Gestion multi-profil et alertes intelligentes
- Suggestions de tenues basées sur la météo
- Statistiques et lookbook
- Base de données bien structurée
- Interface moderne et responsive
- Projet conforme aux exigences d’un PFE

---