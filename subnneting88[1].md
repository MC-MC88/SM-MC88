<h2 id="français">🇫🇷 Version française</h2>

<div align="center">

# 🎯 Subnetting Master — MC88

**Calculateur VLSM, IPv4 et IPv6 en ligne.**

</div>

🌍 **Langues :** [Français](#français) · [English](#english)

---

> **En bref** — Un outil web pour calculer des sous-réseaux VLSM, FLSM et IPv6, avec table de référence CIDR.
> 
> **VLSM · FLSM · IPv6 · Cheatsheet**

<!-- 
## 📸 Aperçu

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/[REPO]/raw/main/images/Sc1.png" alt="[Description]" width="100%" />
</div>

---

🔗 **Démo en ligne :** [https://...](https://...)
📦 **Code source :** [https://github.com/mohamed005cheikh-rgb/[REPO]](https://github.com/mohamed005cheikh-rgb/[REPO])
-->

## 👋 Bienvenue

Subnetting Master est un outil web pour ingénieurs réseau et étudiants. Il calcule des sous-réseaux VLSM, FLSM et IPv6, affiche les plages utilisables, les adresses de broadcast, et propose une table de référence CIDR complète. Tout fonctionne dans le navigateur. Aucune donnée n'est envoyée.

---

## ✨ Ce que vous trouverez

**Calculateur VLSM.**  
Entrez un réseau, un CIDR, et une liste de besoins en hôtes. L'outil trie les besoins du plus grand au plus petit, alloue les sous-réseaux dans l'ordre, et affiche l'ID réseau, la plage utilisable, le broadcast et le CIDR final.

**Calculateur FLSM.**  
Entrez un réseau, un CIDR et un nombre de sous-réseaux. L'outil calcule la taille de chaque sous-réseau et affiche la liste complète avec ID, plage et broadcast.

**Générateur IPv6.**  
Entrez un préfixe IPv6 et un nouveau préfixe. L'outil génère jusqu'à huit sous-réseaux avec les adresses réseau correspondantes.

**Table de référence CIDR.**  
Du /8 au /32, avec masque de sous-réseau, masque wildcard et nombre d'hôtes utilisables. Utile pour vérifier rapidement une valeur.

**Outils rapides.**  
Convertisseur CIDR ↔ masque, et calculateur de masque wildcard. Les deux se mettent à jour en direct pendant la saisie.

**Historique local.**  
Vos huit dernières conversions restent dans la barre latérale. Elles sont conservées dans votre navigateur.

---

## 🧭 Comment ça marche

**1. Choisissez un onglet.**  
VLSM pour l'allocation optimisée, IPv4 pour le découpage égal, IPv6 pour les préfixes, Cheatsheet pour la table de référence.

**2. Entrez vos paramètres.**  
Le réseau de base, le CIDR, et selon l'outil : les besoins en hôtes, le nombre de sous-réseaux, ou le nouveau préfixe.

**3. Cliquez sur Calculer.**  
Les résultats s'affichent dans un tableau. Chaque valeur peut être copiée d'un clic.

**4. Consultez l'historique.**  
Les dernières opérations sont listées dans la barre latérale. Cliquez pour les rejouer.

C'est tout. Pas d'inscription, pas de serveur, pas de tracking.

---

## 🛠️ Petits coups de main

**Le calcul VLSM refuse mes valeurs ?**  
Vérifiez que le CIDR est entre 8 et 30, et que la somme des hôtes demandés tient dans le réseau de base. L'outil affiche un message si l'allocation dépasse la frontière.

**Le calcul FLSM échoue ?**  
Vérifiez que le nombre de sous-réseaux est une puissance de 2 compatible avec le CIDR de base. L'outil refuse au-delà de /30.

**Le générateur IPv6 ne renvoie rien ?**  
Le nouveau préfixe doit être strictement supérieur à l'ancien. Par exemple, /32 → /48 fonctionne, mais /48 → /32 non.

**L'historique disparaît ?**  
En navigation privée, le stockage local est désactivé. En fenêtre normale, l'historique reste tant que vous ne videz pas le cache.

---

<br /><br /><br />

<h2 id="english">🇬🇧 English version</h2>

<div align="center">

# 🎯 Subnetting Master — MC88

**VLSM, IPv4 and IPv6 calculator online.**

</div>

🌍 **Languages:** [Français](#français) · [English](#english)

---

> **In short** — A web tool to compute VLSM, FLSM and IPv6 subnets, with a CIDR reference table.
> 
> **VLSM · FLSM · IPv6 · Cheatsheet**

<!-- 
## 📸 Preview

<div align="center">
  <img src="https://github.com/mohamed005cheikh-rgb/[REPO]/raw/main/images/Sc1.png" alt="[Description]" width="100%" />
</div>

---

🔗 **Live demo:** [https://...](https://...)
📦 **Source code:** [https://github.com/mohamed005cheikh-rgb/[REPO]](https://github.com/mohamed005cheikh-rgb/[REPO])
-->

## 👋 Welcome

Subnetting Master is a web tool for network engineers and students. It computes VLSM, FLSM and IPv6 subnets, shows usable ranges, broadcast addresses, and offers a full CIDR reference table. Everything runs in the browser. No data is sent.

---

## ✨ What you'll find

**VLSM calculator.**  
Enter a network, a CIDR, and a list of host requirements. The tool sorts requirements from largest to smallest, allocates subnets in order, and shows the network ID, usable range, broadcast and final CIDR.

**FLSM calculator.**  
Enter a network, a CIDR and a number of subnets. The tool computes each subnet size and shows the full list with ID, range and broadcast.

**IPv6 generator.**  
Enter an IPv6 prefix and a new prefix. The tool generates up to eight subnets with their network addresses.

**CIDR reference table.**  
From /8 to /32, with subnet mask, wildcard mask and usable host count. Useful to quickly check a value.

**Quick tools.**  
CIDR ↔ mask converter, and wildcard mask calculator. Both update live as you type.

**Local history.**  
Your last eight conversions stay in the sidebar. They are kept in your browser.

---

## 🧭 How it works

**1. Pick a tab.**  
VLSM for optimized allocation, IPv4 for equal splitting, IPv6 for prefixes, Cheatsheet for the reference table.

**2. Enter your parameters.**  
The base network, the CIDR, and depending on the tool: host requirements, subnet count, or the new prefix.

**3. Click Compute.**  
Results appear in a table. Each value can be copied with one click.

**4. Check the history.**  
The last operations are listed in the sidebar. Click to replay them.

That's it. No signup, no server, no tracking.

---

## 🛠️ A little help

**The VLSM computation rejects my values?**  
Check that the CIDR is between 8 and 30, and that the sum of requested hosts fits in the base network. The tool shows a message if the allocation exceeds the boundary.

**The FLSM computation fails?**  
Check that the subnet count is a power of 2 compatible with the base CIDR. The tool refuses beyond /30.

**The IPv6 generator returns nothing?**  
The new prefix must be strictly greater than the old one. For example, /32 → /48 works, but /48 → /32 does not.

**The history disappears?**  
In private browsing, local storage is disabled. In a normal window, history stays until you clear the cache.

---

<div align="center">

### 📞 Une question, une idée ? / A question, an idea?

[![Email](https://img.shields.io/badge/Email-mohamed005cheikh@gmail.com-d14836?style=flat-square&logo=gmail&logoColor=white)](mailto:mohamed005cheikh@gmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-+222_30_72_64_75-25D366?style=flat-square&logo=whatsapp&logoColor=white)](https://wa.me/22230726475)
[![GitHub](https://img.shields.io/badge/GitHub-mohamed005cheikh--rgb-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/mohamed005cheikh-rgb)

<br />

*Calculez. / Compute.*

<sub>MIT License · © 2026 Mohamed Cheikh — MC88</sub>

</div>