# 🚀 Guide de démarrage rapide

## Bienvenue dans le système de recensement d'église !

Ce guide vous aidera à démarrer rapidement avec l'application.

## 📍 Pages disponibles

### 1. Page d'accueil (`home.html`)
- **URL** : `/home.html`
- **Description** : Landing page avec présentation du système
- **Fonctionnalités** :
  - Statistiques en temps réel
  - Présentation des fonctionnalités
  - Liens rapides vers inscription et carte

### 2. Formulaire d'inscription (`index.html`)
- **URL** : `/index.html`
- **Description** : Formulaire de recensement en 3 étapes
- **Pour qui** : Tous les membres souhaitant s'inscrire

**Étapes du formulaire :**
1. **Informations église** : Lieu de culte, département, baptêmes
2. **Informations personnelles** : Identité, contact, géolocalisation
3. **Informations professionnelles** : Profession, situation

### 3. Carte des membres (`map.html`)
- **URL** : `/map.html`
- **Description** : Carte interactive publique
- **Pour qui** : Tous (consultation publique)
- **Fonctionnalités** :
  - Visualisation géographique des membres
  - Filtres par lieu de culte et département
  - Mode regroupement ou individuel
  - Statistiques en temps réel

### 4. Panneau d'administration (`admin.html`)
- **URL** : `/admin.html`
- **Description** : Interface complète de gestion
- **Pour qui** : Administrateurs de l'église
- **Fonctionnalités** :
  - Tableau de bord avec graphiques
  - Gestion des membres
  - Carte administrative
  - Configuration du système

## 🎯 Premiers pas

### Pour un nouveau membre

1. **Accédez à la page d'accueil** : Ouvrez `home.html`
2. **Cliquez sur "S'inscrire maintenant"**
3. **Complétez le formulaire** en 3 étapes
4. **Autorisez la géolocalisation** (ou cliquez sur la carte)
5. **Soumettez** votre inscription

### Pour un administrateur

1. **Accédez au panneau** : Ouvrez `admin.html`
2. **Explorez les onglets** :
   - Tableau de bord : Vue d'ensemble
   - Membres : Gestion de la liste
   - Carte : Visualisation géographique
   - Configuration : Personnalisation

3. **Personnalisez l'église** :
   - Allez dans "Configuration"
   - Modifiez le nom, logo, couleurs
   - Ajoutez des lieux de culte et départements
   - Enregistrez

## 📊 Données initiales

Le système est pré-configuré avec :

### Lieux de culte
- Temple de la Victoire
- Temple de la Gloire
- Temple de la Grâce
- Salle d'Assemblée Centre-Ville

### Départements de service
- Louange et Adoration
- Accueil
- Jeunesse
- Enfants
- Intercession
- Média et Communication
- Protocole
- Ushers

## ⚙️ Configuration rapide

### Personnaliser l'église

1. Ouvrez `admin.html`
2. Allez dans l'onglet "Configuration"
3. Modifiez :
   - **Nom de l'église** : Votre nom d'église
   - **Description** : Slogan ou description
   - **URL du logo** : Lien vers votre logo
   - **Couleurs** : Choisissez vos couleurs de marque
4. Cliquez sur "Enregistrer la configuration"

### Ajouter un lieu de culte

1. Dans "Configuration" > "Lieux de culte"
2. Tapez le nom du nouveau lieu
3. Cliquez sur le bouton "+"

### Ajouter un département

1. Dans "Configuration" > "Départements de service"
2. Tapez le nom du nouveau département
3. Cliquez sur le bouton "+"

## 📱 Utilisation mobile

Le système est entièrement responsive :
- ✅ Fonctionne sur smartphone
- ✅ Fonctionne sur tablette
- ✅ Fonctionne sur ordinateur

**Note** : La géolocalisation fonctionne mieux sur mobile

## 🗺️ Géolocalisation

### Méthode automatique
1. Cliquez sur "Obtenir ma position"
2. Autorisez votre navigateur
3. La position est détectée automatiquement

### Méthode manuelle
1. Cliquez directement sur la carte
2. Le marqueur se place à l'endroit cliqué
3. Ajustez si nécessaire

**Important** : La géolocalisation nécessite :
- HTTPS en production (ou localhost pour le développement)
- Autorisation du navigateur

## 📤 Export de données

### Exporter en CSV

1. Allez dans `admin.html`
2. Onglet "Membres"
3. Appliquez les filtres souhaités (optionnel)
4. Cliquez sur "Exporter CSV"
5. Le fichier est téléchargé automatiquement

**Format** : Le CSV contient toutes les informations des membres filtrés

## 🔍 Recherche et filtres

### Dans le panneau admin

**Recherche par texte** :
- Tapez un nom, prénom ou email
- Les résultats se filtrent en temps réel

**Filtres** :
- Par lieu de culte
- Par département de service
- Combinaison possible

### Sur la carte publique

**Filtres disponibles** :
- Lieu de culte
- Département
- Mode d'affichage (regroupé/individuel)

## 📈 Statistiques

### Dashboard administrateur

**Cartes statistiques** :
- Total membres
- Baptisés d'eau
- Baptisés Saint-Esprit
- Parlent en langues

**Graphiques** :
- Répartition par lieu (camembert)
- Répartition par département (barres)

## 🎨 Personnalisation avancée

### Modifier les couleurs

Dans `admin.html` > Configuration :
- **Couleur primaire** : Couleur principale (boutons, liens)
- **Couleur secondaire** : Couleur d'accentuation

Les couleurs s'appliquent immédiatement après enregistrement.

### Changer le logo

1. Hébergez votre logo en ligne
2. Copiez l'URL de l'image
3. Collez dans "URL du logo"
4. Enregistrez

**Formats recommandés** : PNG, SVG, JPG (ratio 150x60 px)

## 🆘 Résolution de problèmes

### La géolocalisation ne marche pas
- ✅ Vérifiez que vous êtes en HTTPS
- ✅ Autorisez la géolocalisation dans votre navigateur
- ✅ Utilisez la sélection manuelle sur la carte

### Les données ne se chargent pas
- ✅ Ouvrez la console (F12)
- ✅ Vérifiez les erreurs
- ✅ Rechargez la page

### Export CSV ne fonctionne pas
- ✅ Vérifiez les autorisations de téléchargement
- ✅ Essayez un autre navigateur
- ✅ Désactivez les bloqueurs de pop-up

### La carte ne s'affiche pas
- ✅ Vérifiez votre connexion Internet
- ✅ Actualisez la page
- ✅ Videz le cache du navigateur

## 📞 Support

Pour toute question ou problème :
1. Consultez d'abord le fichier `README.md` complet
2. Vérifiez la console du navigateur (F12)
3. Contactez l'administrateur système

## 🔐 Sécurité

**Bonnes pratiques** :
- Ne partagez pas l'accès admin
- Sauvegardez régulièrement les données (export CSV)
- Vérifiez les inscriptions régulièrement
- Mettez à jour les listes (lieux, départements)

## 🎓 Conseils d'utilisation

### Pour maximiser l'engagement

1. **Communiquez** sur le système auprès des membres
2. **Facilitez** l'inscription avec des postes dédiés
3. **Encouragez** la géolocalisation pour le covoiturage
4. **Utilisez** les données pour mieux organiser les événements
5. **Mettez à jour** régulièrement les informations

### Pour les administrateurs

1. **Vérifiez** régulièrement les nouvelles inscriptions
2. **Nettoyez** les doublons si nécessaire
3. **Exportez** les données mensuellement (backup)
4. **Analysez** les statistiques pour prendre des décisions
5. **Communiquez** avec les membres via leurs coordonnées

## 🚀 Prochaines étapes

Une fois le système en place :

1. ✅ Inscrivez les premiers membres
2. ✅ Personnalisez la configuration
3. ✅ Partagez les liens (home.html, index.html)
4. ✅ Formez les administrateurs
5. ✅ Collectez les feedbacks
6. ✅ Ajoutez de nouvelles fonctionnalités si nécessaire

## 📚 Documentation complète

Pour plus de détails, consultez **README.md** qui contient :
- Liste complète des fonctionnalités
- Structure des données
- API REST documentation
- Fonctionnalités futures
- Guide de maintenance

---

**Version** : 1.0.0  
**Date** : 2026-02-17  
**Status** : ✅ Prêt à l'emploi

Bon recensement ! 🎉
