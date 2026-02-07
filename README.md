# 💰 Argent de Poche - Abbie & Aston

Application web de gestion d'argent de poche pour vos enfants avec synchronisation Firebase en temps réel.

## 🎯 Fonctionnalités

- **Gestion de comptes individuels** pour Abbie et Aston
- **Ajout et retrait de fonds** avec descriptions personnalisées
- **Système d'intérêts mensuels** avec taux personnalisable par enfant
- **Historique complet des transactions** avec possibilité de modification et suppression
- **Synchronisation temps réel** avec Firebase Realtime Database
- **Interface responsive** adaptée mobile et desktop

## 🚀 Démarrage rapide

### Option 1 : Utilisation directe
1. Téléchargez le fichier `argent-poche.html`
2. Ouvrez-le dans votre navigateur web
3. L'application est prête à l'emploi !

### Option 2 : Déploiement sur GitHub Pages
1. Clonez ce repository
2. Renommez `argent-poche.html` en `index.html`
3. Activez GitHub Pages dans les paramètres du repository
4. Accédez à votre application via `https://votre-username.github.io/argent-poche`

## 🔧 Configuration Firebase

L'application utilise Firebase Realtime Database pour stocker les données. La configuration est déjà incluse dans le code :

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyAF0rEY7MfKiaonUNmsRSJ7HLLOiSPK5p8",
  authDomain: "argent-poche-enfant.firebaseapp.com",
  databaseURL: "https://argent-poche-enfant-default-rtdb.europe-west1.firebasedatabase.app/",
  projectId: "argent-poche-enfant",
  storageBucket: "argent-poche-enfant.firebasestorage.app",
  messagingSenderId: "196977028076",
  appId: "1:196977028076:web:94bebbefe24b9b02fd2ec9"
};
```

### Structure de la base de données Firebase

```json
{
  "kids": {
    "abbie": {
      "name": "Abbie",
      "balance": 0,
      "interestRate": 5,
      "history": []
    },
    "aston": {
      "name": "Aston",
      "balance": 0,
      "interestRate": 5,
      "history": []
    }
  }
}
```

## 📱 Utilisation

### Ajouter de l'argent
1. Entrez le montant dans le champ "Montant"
2. Ajoutez une description (optionnel)
3. Cliquez sur "➕ Ajouter"

### Retirer de l'argent
1. Entrez le montant dans le champ "Montant"
2. Ajoutez une description (optionnel)
3. Cliquez sur "➖ Retirer"

### Appliquer les intérêts mensuels
1. Modifiez le taux d'intérêt si nécessaire
2. Cliquez sur "Appliquer les intérêts"
3. Les intérêts sont calculés et ajoutés automatiquement au solde

### Gérer l'historique
- **Modifier** : Cliquez sur ✏️ pour modifier le montant ou la description
- **Supprimer** : Cliquez sur 🗑️ pour supprimer une transaction (le solde sera recalculé)

## 🛠️ Technologies utilisées

- **React 18** - Framework JavaScript
- **Firebase 9** - Base de données temps réel
- **HTML5 / CSS3** - Interface utilisateur
- **Babel Standalone** - Transpilation JSX

## 📊 Fonctionnalités avancées

### Synchronisation multi-appareils
Toutes les modifications sont automatiquement synchronisées entre tous les appareils connectés grâce à Firebase.

### Calcul automatique des intérêts
Le système calcule automatiquement le montant des intérêts en fonction du taux défini et du solde actuel.

### Historique complet
Chaque transaction enregistre :
- Date et heure
- Type (ajout, retrait, intérêts)
- Montant
- Description
- Solde après transaction

## 🔒 Sécurité

⚠️ **Important** : Les clés Firebase sont actuellement publiques dans le code. Pour une utilisation en production, il est recommandé de :
1. Configurer les règles de sécurité Firebase
2. Ajouter une authentification utilisateur
3. Limiter l'accès à la base de données

### Règles de sécurité Firebase recommandées

```json
{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null"
  }
}
```

## 📝 Licence

Ce projet est libre d'utilisation pour un usage personnel et familial.

## 🤝 Contribution

Les suggestions et améliorations sont les bienvenues ! N'hésitez pas à ouvrir une issue ou une pull request.

## 👨‍👩‍👧‍👦 Auteur

Application développée pour la gestion de l'argent de poche d'Abbie et Aston.

---

**Note** : Cette application est conçue pour un usage familial et éducatif. Elle permet d'enseigner aux enfants la gestion financière de manière ludique et interactive.
