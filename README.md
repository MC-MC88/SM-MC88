<div align="center">

# 🌐 Subnetting Master — MC88

**Calculer des sous-réseaux, sans jamais se tromper.**

</div>

---

## 👋 Bienvenue

Subnetting Master est un petit atelier pour ceux qui travaillent avec des adresses IP au quotidien.

Vous entrez un réseau, vous indiquez vos besoins, et l'outil vous rend un découpage propre — chaque sous-réseau avec son Network ID, sa plage utilisable, son adresse de broadcast, son masque. VLSM, FLSM, IPv6, tableau CIDR complet, conversion masque ↔ wildcard : tout est là, au même endroit, dans une interface calme et soignée.

Tout fonctionne dans votre navigateur. Pas de serveur, pas d'inscription, pas de données qui partent ailleurs. Vous ouvrez, vous calculez, vous fermez.

---
<!-- 
## 📸 Un aperçu

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/sm-mc88/raw/main/images/Sc1.png" alt="Calculateur VLSM" width="100%" />
</div>

<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/sm-mc88/raw/main/images/Sc2.png" alt="Calculateur FLSM et IPv6" width="100%" />
</div>

<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/sm-mc88/raw/main/images/Sr1.gif" alt="Découper un réseau en VLSM" width="100%" />
</div>

<br />

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/sm-mc88/raw/main/images/Sr2.gif" alt="Consulter la cheat sheet CIDR" width="100%" />
</div>

----->

## ✨ Ce que vous trouverez

**VLSM — découper selon vos besoins réels.**  
Vous indiquez votre réseau de base, son CIDR, et la liste de vos besoins en hôtes (par exemple `100, 50, 25`). L'outil trie les demandes de la plus grande à la plus petite, calcule les bits nécessaires pour chacune, et les place bout à bout sans gaspiller une seule adresse. À la fin, vous avez un plan de sous-réseaux prêt à déployer.

**FLSM — découper en parts égales.**  
Quand vous voulez des sous-réseaux de taille identique, vous entrez simplement le nombre de blocs souhaités. L'outil s'occupe du reste — CIDR ajusté, chaque subnet avec sa plage complète, du premier au dernier.

**IPv6 — générer des sous-réseaux à partir d'un préfixe.**  
Donnez un préfixe IPv6 (par exemple `2001:db8::/32`) et un nouveau préfixe cible. L'outil vous rend jusqu'à huit sous-réseaux prêts à l'emploi.

**Cheat sheet CIDR — la référence toujours sous la main.**  
Un tableau complet, de `/8` à `/32` : masque de sous-réseau, wildcard, nombre d'hôtes utilisables. Plus besoin de retenir — il suffit de regarder.

**Convertisseur CIDR ↔ Masque.**  
Vous entrez l'un, vous obtenez l'autre, instantanément. Dans les deux sens.

**Calculateur de Wildcard Mask.**  
Un masque de sous-réseau entre, un wildcard sort — précieux pour les ACL et les configurations de routeurs.

**Copier d'un seul geste.**  
Chaque valeur affichée a son petit bouton de copie. Un clic, et c'est dans votre presse-papiers, prêt à coller dans votre terminal ou votre documentation.

**Un historique qui se souvient.**  
Vos huit derniers calculs restent dans la barre latérale. Vous pouvez y revenir à tout moment — même après avoir fermé la page.

---

## 🧭 Comment ça marche

Trois étapes, toujours les mêmes.

**1. Choisissez votre calculateur.**  
En haut de la page, quatre onglets : **VLSM**, **IPv4** (FLSM), **IPv6**, et **Cheatsheet**. Selon ce que vous voulez faire, vous basculez d'un onglet à l'autre — chacun garde sa saisie.

**2. Entrez vos paramètres.**  
Adresse réseau, CIDR de base, liste d'hôtes ou nombre de sous-réseaux — les champs sont pré-remplis avec des exemples pour vous guider. Modifiez ce qu'il faut, ou repartez de zéro.

**3. Lancez le calcul.**  
Un clic sur **Calculate**, et le tableau apparaît. Vous pouvez le lire, copier chaque valeur, ou simplement vous en inspirer. Le calcul est enregistré dans l'historique, prêt à être comparé au suivant.

C'est tout. L'outil ne vous demande rien, ne vous impose rien, et ne s'inquiète jamais de ce que vous faites avec les résultats.

---

## 🛠️ Petits coups de main

**L'adresse est refusée ?**  
Vérifiez qu'elle est bien au format `xxx.xxx.xxx.xxx`, chaque octet entre 0 et 255.

**Le CIDR est refusé ?**  
Pour VLSM et FLSM, le préfixe doit être entre `/8` et `/30`. En dessous, on n'est plus dans du sous-réseau. Au-dessus, il ne reste plus assez d'adresses pour deux hôtes.

**« Exceeded base network boundary » ?**  
La somme de vos sous-réseaux dépasse la taille du réseau de base. Réduisez les besoins en hôtes, ou agrandissez le réseau de départ (par exemple, passez de `/24` à `/23`).

**« Cannot fit X hosts in /Y » ?**  
Un de vos sous-réseaux demandés est plus grand que le réseau de base lui-même. Réduisez la demande, ou changez de réseau de base.

**Le bouton Copy ne répond pas ?**  
Autorisez l'accès au presse-papiers dans les réglages du navigateur. En attendant, la sélection manuelle fonctionne très bien.

**L'historique disparaît ?**  
En navigation privée, le stockage local est désactivé — c'est normal. Utilisez une fenêtre normale pour le conserver.

---

<div align="center">

### 📞 Une question, une idée ?

[![Email](https://img.shields.io/badge/Email-mohamed005cheikh@gmail.com-d14836?style=flat-square&logo=gmail&logoColor=white)](mailto:mohamed005cheikh@gmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-+222_30_72_64_75-25D366?style=flat-square&logo=whatsapp&logoColor=white)](https://wa.me/22230726475)

<br />

*Bon calcul.*

<sub>© 2026 Mohamed Cheikh — MC88</sub>

</div>
