# 🏛️ Système de Recensement d'Église avec Géolocalisation

Application web complète pour le recensement des membres d'église avec fonctionnalités de géolocalisation, gestion administrative et visualisation cartographique.

## 📋 Fonctionnalités actuellement implémentées

### ✅ Formulaire de recensement multi-étapes
- **Étape 1** : Informations sur l'église
  - Sélection du lieu de culte
  - Choix du département de service
  - Questions sur les baptêmes (eau, Saint-Esprit)
  - Question sur le parler en langues
  
- **Étape 2** : Informations personnelles
  - Nom, prénom, date de naissance
  - Téléphone et email
  - Adresse complète
  - **Géolocalisation interactive** avec carte Leaflet
  - Détection automatique de position GPS
  - Sélection manuelle sur la carte
  
- **Étape 3** : Informations professionnelles
  - Profession
  - Situation professionnelle
  - Récapitulatif avant soumission

### ✅ Géolocalisation des membres
- Intégration de **Leaflet.js** pour les cartes interactives
- Capture automatique de la géolocalisation (avec permission utilisateur)
- Sélection manuelle de position en cliquant sur la carte
- Stockage des coordonnées GPS (latitude/longitude)
- Carte administrative montrant tous les membres géolocalisés
- Marqueurs cliquables avec informations du membre
- Filtres par lieu de culte et département sur la carte

### ✅ Panneau d'administration complet
- **Tableau de bord** avec statistiques en temps réel :
  - Nombre total de membres
  - Statistiques de baptêmes (eau, Saint-Esprit)
  - Nombre de personnes parlant en langues
  - Graphiques circulaires (répartition par lieu de culte)
  - Graphiques en barres (répartition par département)
  
- **Gestion des membres** :
  - Liste complète avec pagination
  - Recherche par nom, prénom, email
  - Filtres par lieu de culte et département
  - Visualisation détaillée de chaque membre
  - Suppression de membres
  - Export CSV de toutes les données
  
- **Carte interactive des membres** :
  - Visualisation géographique de tous les membres
  - Filtres dynamiques
  - Pop-ups avec informations détaillées
  - Ajustement automatique de la vue
  
- **Configuration personnalisable** :
  - Nom de l'église
  - Description
  - Logo personnalisé (URL)
  - Couleurs du thème (primaire et secondaire)
  - Gestion des lieux de culte (ajout/suppression)
  - Gestion des départements de service (ajout/suppression)

### ✅ Design moderne et responsive
- Interface utilisant **Tailwind CSS**
- Compatible mobile, tablette et desktop
- Animations fluides entre les étapes
- Indicateur de progression visuel
- Icons avec **Font Awesome**
- Couleurs personnalisables

### ✅ Stockage de données avec API RESTful
- 4 tables de données :
  - `membres` : informations complètes des membres (17 champs)
  - `lieux_culte` : liste des lieux de culte
  - `departements` : départements de service
  - `configuration` : paramètres de l'église
- API REST complète (GET, POST, PUT, PATCH, DELETE)
- Pagination et recherche intégrées

## 🚀 URIs et Points d'accès

### Pages publiques
- **`/home.html`** - Page d'accueil avec présentation du système
- **`/index.html`** - Formulaire de recensement multi-étapes
- **`/map.html`** - Carte publique des membres géolocalisés avec filtres
- **`/admin.html`** - Panneau d'administration complet

### API REST (endpoints relatifs)

#### Membres
- `GET tables/membres?page=1&limit=10&search=query` - Liste paginée
- `GET tables/membres/{id}` - Détails d'un membre
- `POST tables/membres` - Créer un membre
- `PUT tables/membres/{id}` - Mettre à jour un membre
- `DELETE tables/membres/{id}` - Supprimer un membre

#### Lieux de culte
- `GET tables/lieux_culte?limit=100` - Liste des lieux
- `POST tables/lieux_culte` - Ajouter un lieu
- `DELETE tables/lieux_culte/{id}` - Supprimer un lieu

#### Départements
- `GET tables/departements?limit=100` - Liste des départements
- `POST tables/departements` - Ajouter un département
- `DELETE tables/departements/{id}` - Supprimer un département

#### Configuration
- `GET tables/configuration?limit=1` - Récupérer la config
- `PUT tables/configuration/main` - Mettre à jour la config

## 📊 Structure des données

### Table `membres`
```javascript
{
  id: "UUID",
  nom: "String",
  prenom: "String",
  dateNaissance: "Timestamp",
  telephone: "String",
  email: "String",
  adresse: "String",
  latitude: "Number",
  longitude: "Number",
  lieuCulte: "String",
  departementService: "String",
  baptiseEau: "Boolean",
  baptiseSaintEsprit: "Boolean",
  parleLangues: "Boolean",
  profession: "String",
  situationProfessionnelle: "String",
  dateInscription: "Timestamp"
}
```

### Table `lieux_culte`
```javascript
{
  id: "UUID",
  nom: "String",
  actif: "Boolean"
}
```

### Table `departements`
```javascript
{
  id: "UUID",
  nom: "String",
  actif: "Boolean"
}
```

### Table `configuration`
```javascript
{
  id: "main",
  nomEglise: "String",
  logoUrl: "String",
  couleurPrimaire: "String (hex)",
  couleurSecondaire: "String (hex)",
  description: "String"
}
```

## 🛠️ Technologies utilisées

- **Frontend** : HTML5, CSS3, JavaScript (Vanilla)
- **Framework CSS** : Tailwind CSS (via CDN)
- **Cartographie** : Leaflet.js 1.9.4
- **Graphiques** : Chart.js
- **Icons** : Font Awesome 6.4.0
- **API** : RESTful Table API intégrée
- **Stockage** : Base de données relationnelle (via API)

## 📦 Structure des fichiers

```
/
├── home.html               # Page d'accueil / Landing page
├── index.html              # Formulaire de recensement
├── map.html                # Carte publique des membres
├── admin.html              # Panneau d'administration
├── css/
│   └── style.css          # Styles personnalisés
├── js/
│   ├── app.js             # Logique du formulaire
│   ├── map.js             # Logique de la carte publique
│   └── admin.js           # Logique administrative
└── README.md              # Cette documentation
```

## 🎯 Guide d'utilisation

### Pour les membres (Inscription)

1. Accédez à **`index.html`**
2. Remplissez les 3 étapes du formulaire :
   - Étape 1 : Informations église
   - Étape 2 : Informations personnelles + géolocalisation
   - Étape 3 : Informations professionnelles
3. Cliquez sur "Obtenir ma position" pour la géolocalisation automatique
4. Ou cliquez sur la carte pour définir manuellement votre position
5. Soumettez le formulaire

### Pour visualiser la communauté

1. Accédez à **`map.html`**
2. Consultez les statistiques en temps réel
3. Utilisez les filtres pour afficher des membres spécifiques :
   - Par lieu de culte
   - Par département de service
   - Mode d'affichage (regroupé ou individuel)
4. Cliquez sur les marqueurs pour voir les informations publiques
5. Actualisez les données avec le bouton "Actualiser"

### Pour les administrateurs

1. Accédez à **`admin.html`**
2. Utilisez les différents onglets :
   - **Tableau de bord** : Vue d'ensemble et statistiques
   - **Membres** : Gestion de la liste des membres
   - **Carte** : Visualisation géographique
   - **Configuration** : Paramètres et personnalisation

#### Exporter les données
1. Allez dans l'onglet "Membres"
2. Appliquez les filtres souhaités
3. Cliquez sur "Exporter CSV"
4. Le fichier sera téléchargé automatiquement

#### Personnaliser l'église
1. Allez dans l'onglet "Configuration"
2. Modifiez le nom, la description, le logo
3. Choisissez les couleurs du thème
4. Ajoutez/supprimez des lieux de culte et départements
5. Enregistrez les modifications

## 🔮 Fonctionnalités non encore implémentées

### À développer dans les prochaines versions

1. **Authentification administrateur**
   - Système de connexion sécurisé
   - Gestion des rôles et permissions
   - Protection des pages admin

2. **Notifications**
   - Notifications email après inscription
   - Rappels pour mise à jour des informations
   - Alertes pour les administrateurs

3. **Rapports avancés**
   - Génération de rapports PDF
   - Statistiques par période
   - Graphiques d'évolution temporelle

4. **Module de communication**
   - Envoi de messages groupés par SMS
   - Newsletter par email
   - Filtrage avancé des destinataires

5. **Gestion d'événements**
   - Création d'événements
   - Inscription des membres
   - Suivi de présence

6. **Photos de profil**
   - Upload de photos
   - Galerie de photos
   - Affichage sur la carte

7. **Import/Export avancé**
   - Import depuis Excel
   - Export en PDF
   - Synchronisation avec d'autres systèmes

8. **Mode hors ligne**
   - Progressive Web App (PWA)
   - Formulaire disponible hors ligne
   - Synchronisation automatique

9. **Géolocalisation avancée**
   - Calcul de distances
   - Regroupement géographique
   - Itinéraires vers l'église

10. **Dashboard personnalisable**
    - Widgets déplaçables
    - Choix des graphiques affichés
    - Thèmes personnalisés

## 🔧 Prochaines étapes recommandées

### Priorité haute
1. **Sécurité** : Ajouter un système d'authentification pour l'administration
2. **Validation** : Améliorer la validation côté serveur
3. **Performance** : Optimiser le chargement des grandes listes de membres

### Priorité moyenne
4. **UX** : Ajouter des animations et transitions plus fluides
5. **Accessibilité** : Améliorer le support ARIA et navigation clavier
6. **Internationalisation** : Support multi-langues

### Priorité basse
7. **Tests** : Ajouter des tests unitaires et d'intégration
8. **Documentation** : Guide utilisateur illustré
9. **Analytics** : Intégrer des statistiques d'utilisation

## 📝 Notes importantes

- **Géolocalisation** : Nécessite HTTPS en production (sauf localhost)
- **Permissions** : Le navigateur demande l'autorisation pour la géolocalisation
- **Données** : Les données sont stockées via l'API RESTful Table
- **Responsive** : Testé sur mobile, tablette et desktop
- **Navigateurs** : Compatible avec tous les navigateurs modernes

## 🆘 Support et maintenance

### Problèmes courants

**La géolocalisation ne fonctionne pas**
- Vérifiez que le site est en HTTPS (ou localhost)
- Autorisez la géolocalisation dans votre navigateur
- Utilisez la sélection manuelle sur la carte

**Les données ne se chargent pas**
- Vérifiez la console du navigateur (F12)
- Assurez-vous que l'API REST est accessible
- Rechargez la page

**Export CSV ne fonctionne pas**
- Vérifiez les autorisations de téléchargement
- Testez sur un autre navigateur

## 📄 Licence

Ce projet est développé pour une utilisation dans le cadre d'activités religieuses et communautaires.

## 🤝 Contribution

Pour toute suggestion d'amélioration ou rapport de bug, veuillez contacter l'administrateur système.

## 🎬 Démarrage rapide

**Pour commencer immédiatement** : Consultez le fichier **[QUICKSTART.md](QUICKSTART.md)** qui contient :
- Guide pas à pas pour les nouveaux utilisateurs
- Instructions pour les administrateurs
- Résolution des problèmes courants
- Conseils d'utilisation optimale

**Points d'entrée recommandés** :
- 🏠 **Visiteurs** → Ouvrez `home.html` pour découvrir le système
- ✍️ **Membres** → Ouvrez `index.html` pour vous inscrire
- 🗺️ **Consultation** → Ouvrez `map.html` pour voir la carte
- ⚙️ **Admin** → Ouvrez `admin.html` pour gérer

---

**Version** : 1.0.0  
**Date de création** : 2026-02-17  
**Dernière mise à jour** : 2026-02-17  
**Statut** : ✅ Opérationnel et prêt à l'emploi
