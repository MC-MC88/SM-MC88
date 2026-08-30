# 🌐 Subnetting Master — MC88 | Suite d'Ingénierie Réseau

**Subnetting Master** est une suite professionnelle de calcul de sous-réseaux IP (IPv4 & IPv6) avec une interface luxueuse de style "cyber-obsidienne" et des accents néon améthyste. L'outil fonctionne entièrement dans votre navigateur, sans aucun serveur.

---

## 📋 Prérequis

1. Un navigateur web moderne (Chrome, Firefox, Edge, Safari, Brave, Opera)
2. Aucune connexion Internet requise après le chargement initial
3. Aucune installation de logiciel nécessaire

---

## 🚀 Guide d'installation

### Étape 1 : Télécharger le fichier
1. Téléchargez le fichier `subnetting-master.html` sur votre ordinateur
2. Placez-le dans un dossier de votre choix (ex : `C:\SubnettingMaster\`)

### Étape 2 : Lancer l'application
- **Méthode simple** : Double-cliquez sur le fichier
- **Méthode alternative** : Faites un clic droit → « Ouvrir avec » → choisissez votre navigateur

---

## 🎯 Fonctionnalités principales

### 📊 1. Calculateur VLSM (Variable Length Subnet Masking)

Le calculateur VLSM permet de découper un réseau en sous-réseaux de tailles variables selon les besoins en hôtes.

**Paramètres d'entrée :**
- **Adresse réseau** : ex. `192.168.1.0`
- **CIDR de base** : ex. `24`
- **Liste d'hôtes** : ex. `50, 20, 10` (séparés par des virgules)

**Résultats affichés :**
| Colonne | Description |
|---------|-------------|
| **Subnet** | Nom du sous-réseau (Subnet 1, Subnet 2…) |
| **Hosts** | Nombre d'hôtes demandés |
| **Network ID** | Adresse réseau du sous-réseau |
| **Usable Range** | Plage d'adresses utilisables |
| **Broadcast** | Adresse de diffusion |
| **CIDR** | Nouveau préfixe CIDR |

**Méthode de calcul :**
1. Trie les demandes d'hôtes par ordre décroissant
2. Calcule les bits nécessaires pour chaque demande : `bits = ceil(log2(hôtes + 2))`
3. Assigne séquentiellement les sous-réseaux sans gaspillage d'adresses

---

### 📐 2. Calculateur FLSM (Fixed Length Subnet Masking)

Le calculateur FLSM divise un réseau en sous-réseaux de **taille égale**.

**Paramètres d'entrée :**
- **Adresse réseau** : ex. `10.0.0.0`
- **CIDR de base** : ex. `16`
- **Nombre de sous-réseaux** : ex. `4`

**Résultats affichés :**
| Colonne | Description |
|---------|-------------|
| **#** | Numéro du sous-réseau |
| **Subnet ID** | Adresse du sous-réseau |
| **Usable Range** | Plage utilisable |
| **Broadcast** | Adresse de diffusion |

**Méthode de calcul :**
1. Calcule les bits supplémentaires : `bits = ceil(log2(nombre_sous_réseaux))`
2. Nouveau CIDR : `nouveau_cidr = cidr_base + bits`
3. Taille du sous-réseau : `2^(32 - nouveau_cidr)` adresses

---

### 🌍 3. Calculateur IPv6

Génère des sous-réseaux IPv6 à partir d'un préfixe donné.

**Paramètres d'entrée :**
- **Préfixe IPv6** : ex. `2001:db8::/32`
- **Nouveau préfixe** : ex. `48` (entre 32 et 64)

**Résultats :**
- Génère jusqu'à 8 sous-réseaux avec leurs adresses réseau

---

### 📚 4. Cheat Sheet CIDR

Tableau de référence complet des préfixes CIDR de `/8` à `/32` :

| Colonne | Description |
|---------|-------------|
| **CIDR** | Préfixe (ex. /24) |
| **Subnet Mask** | Masque de sous-réseau (ex. 255.255.255.0) |
| **Wildcard Mask** | Masque inversé (ex. 0.0.0.255) |
| **Usable Hosts** | Nombre d'hôtes utilisables |

---

### 🔄 5. Convertisseur CIDR ↔ Masque

Convertit automatiquement entre les deux formats :
- **Entrée** : `/24` → **Sortie** : `255.255.255.0`
- **Entrée** : `255.255.255.0` → **Sortie** : `/24`

---

### 🎭 6. Calculateur de Wildcard Mask

Calcule le masque inversé à partir d'un masque de sous-réseau :
- **Entrée** : `255.255.255.0` → **Sortie** : `0.0.0.255`
- **Entrée** : `255.255.0.0` → **Sortie** : `0.0.255.255`

---

## 📖 Guide d'utilisation détaillé

### 🔹 Étape 1 : Choisir un outil

Utilisez la **barre de navigation** en haut pour basculer entre :
- **VLSM** : Sous-réseaux de taille variable
- **IPv4** : Sous-réseaux de taille fixe
- **IPv6** : Sous-réseaux IPv6
- **Cheatsheet** : Tableau de référence

### 🔹 Étape 2 : Saisir les paramètres

1. Remplissez les champs d'entrée avec vos valeurs
2. Les champs ont des valeurs par défaut pour vous aider à démarrer
3. Les formats acceptés sont indiqués dans les placeholders

### 🔹 Étape 3 : Lancer le calcul

Cliquez sur le bouton **« Calculate »** (ou **« Generate »** pour IPv6) :
- Les résultats s'affichent dans un tableau
- Un bouton **📋 Copy** permet de copier chaque valeur
- L'historique est mis à jour automatiquement

### 🔹 Étape 4 : Utiliser les résultats

- **Copier** : Cliquez sur le chip de copie à côté de chaque valeur
- **Historique** : Les 8 derniers calculs sont sauvegardés dans la barre latérale
- **Persistance** : L'historique survit au rechargement de la page

---

## 🛠️ Guide de dépannage

### Problème 1 : Erreur "Invalid network address"

**Cause** : L'adresse IP saisie n'est pas valide.

**Solution** :
- Vérifiez que l'adresse est au format `xxx.xxx.xxx.xxx`
- Chaque octet doit être entre 0 et 255
- Exemple valide : `192.168.1.0`

---

### Problème 2 : Erreur "CIDR must be between 8 and 30"

**Cause** : Le préfixe CIDR est hors limites.

**Solution** :
- Pour VLSM : utilisez un CIDR entre 8 et 30
- Pour FLSM : utilisez un CIDR entre 8 et 30
- `/8` = 16 777 214 hôtes maximum
- `/30` = 2 hôtes utilisables (liaison point-à-point)

---

### Problème 3 : Erreur "Exceeded base network boundary"

**Cause** : La somme des sous-réseaux dépasse la taille du réseau de base.

**Solution** :
- Réduisez le nombre d'hôtes demandés
- Ou augmentez le CIDR de base (ex. passez de /24 à /23)
- Vérifiez que la somme des hôtes + 2 par sous-réseau ≤ hôtes disponibles

---

### Problème 4 : Erreur "Cannot fit X hosts in /Y"

**Cause** : Un sous-réseau demandé est plus grand que le réseau de base.

**Solution** :
- Réduisez la demande d'hôtes
- Ou augmentez le CIDR de base
- Exemple : impossible de mettre 500 hôtes dans un /24

---

### Problème 5 : Le tableau ne s'affiche pas

**Cause** : Le panneau est masqué ou le navigateur est ancien.

**Solution** :
- Vérifiez que vous êtes sur le bon onglet (VLSM, IPv4, etc.)
- Rechargez la page (F5)
- Utilisez un navigateur moderne (Chrome, Firefox, Edge)

---

### Problème 6 : L'historique ne se sauvegarde pas

**Cause** : Le stockage local est désactivé ou en navigation privée.

**Solution** :
- Vérifiez que le stockage local est activé
- En navigation privée, l'historique sera réinitialisé
- C'est un comportement normal

---

### Problème 7 : Les boutons Copy ne fonctionnent pas

**Cause** : L'API presse-papiers est bloquée.

**Solution** :
- Autorisez l'accès au presse-papiers dans les paramètres du navigateur
- Utilisez la sélection manuelle du texte comme alternative
- Essayez Chrome ou Edge (meilleur support)

---

## 📊 Exemples de calcul

### Exemple 1 : VLSM

**Entrée :**
- Réseau : `192.168.1.0/24`
- Hôtes demandés : `100, 50, 25`

**Résultat :**
| Subnet | Hosts | Network ID | Usable Range | Broadcast | CIDR |
|--------|-------|------------|--------------|-----------|------|
| Subnet 1 | 100 | 192.168.1.0 | 192.168.1.1 - 192.168.1.126 | 192.168.1.127 | /25 |
| Subnet 2 | 50 | 192.168.1.128 | 192.168.1.129 - 192.168.1.190 | 192.168.1.191 | /26 |
| Subnet 3 | 25 | 192.168.1.192 | 192.168.1.193 - 192.168.1.222 | 192.168.1.223 | /27 |

---

### Exemple 2 : FLSM

**Entrée :**
- Réseau : `10.0.0.0/16`
- Sous-réseaux : `4`

**Résultat :**
| # | Subnet ID | Usable Range | Broadcast |
|---|-----------|--------------|-----------|
| 1 | 10.0.0.0 | 10.0.0.1 - 10.0.63.254 | 10.0.63.255 |
| 2 | 10.0.64.0 | 10.0.64.1 - 10.0.127.254 | 10.0.127.255 |
| 3 | 10.0.128.0 | 10.0.128.1 - 10.0.191.254 | 10.0.191.255 |
| 4 | 10.0.192.0 | 10.0.192.1 - 10.0.255.254 | 10.0.255.255 |

---

### Exemple 3 : IPv6

**Entrée :**
- Préfixe : `2001:db8::/32`
- Nouveau préfixe : `/48`

**Résultat :**
| Subnet # | Network Address |
|----------|----------------|
| 0 | 2001:db8:0:0::/48 |
| 1 | 2001:db8:0:1::/48 |
| 2 | 2001:db8:0:2::/48 |
| ... | ... |

---

## 📄 Copyright

**© 2026**  
📧 mohamed005cheikh@gmail.com  
**Créé par MC88**  
**Tous droits réservés**

---

## 🔗 Ressources techniques

### Formules utilisées

| Formule | Description |
|---------|-------------|
| `bits = ceil(log2(hôtes + 2))` | Bits nécessaires pour un sous-réseau |
| `nouveau_cidr = 32 - bits` | Nouveau préfixe CIDR |
| `masque = ~(0xFFFFFFFF >>> cidr)` | Conversion CIDR → masque |
| `wildcard = ~masque` | Calcul du wildcard mask |
| `hôtes_utilisables = 2^(32-cidr) - 2` | Hôtes disponibles |

---

## ✅ Fonctionnalités techniques

- **Calcul VLSM** avec tri automatique des demandes
- **Calcul FLSM** avec sous-réseaux égaux
- **Génération IPv6** jusqu'à 8 sous-réseaux
- **Cheat sheet CIDR** complet (/8 à /32)
- **Convertisseur CIDR ↔ Masque** bidirectionnel
- **Calculateur Wildcard** instantané
- **Boutons Copy** pour chaque valeur
- **Historique persistant** (8 derniers calculs)
- **SPA Router** avec support back/forward
- **Particles animées** en arrière-plan
- **Design responsive** mobile-first
- **Glassmorphism** avec effets de flou
- **Animations fluides** avec courbes d'accélération

---

**Bon calcul de sous-réseaux ! 🌐✨**
