# Blockchain et développement

## Pré-requis

- MetaMask
- Phantom

## Introduction

Le but de la blockchain est de décentraliser, que tout soit tracé et non effaçable.
Les jetons ne sont pas à confondre avec la Blockchain.

- Clé privé : nous permet de dire que l'on est propriétaire de quelque chose.
- Clé publique : peut seulement valider que l’utilisateur en question est bien le signataire du message reçu.

### Peer to peer

Le peer to peer ou système pair à pair est un modèle d'échange en réseau où chaque entité est à la fois client et serveur. (Tout le monde partage avec tout le monde.) C'est un système décentralisé.

Exemple : Git est un système décentralisé et les torrents aussi.

## Transaction

blabla

## Histoire de la Blockchain

### 1991

- Stuart Haber
- Scott Stornetta

### 1992

- Merkle Tree

### 2005

- Projet Bitgold double spend

### 2009

- La Blockchain est créée.
- Première transaction.

- dApps
- Vitalik Buterin

## Bloc de contenu

### Composition

- Le bloc contient un Id => hash de bloc. (Hexadécimal)
- Le bloc contient le hash du bloc précédent.
- Le bloc contient une ou plusieurs transaction unique.

### Composant Block Chain

#### Les Noeuds légers ou complets

- Réseau d'ordiateurs, de serveurs donc interconnectés
- Contient une copie de la BC si noeud complet
- Se synchronisent (Ordinateur éteint) entre eux (Maj BC)

#### Les Mineurs : acteurs + infrastructure

- Qui mettent à disposition une puissance de calcul (Noeud)
- Sont motivés financièrement
- Sont contrôlé ("proof of stake", "proof of work")
- Outre leur fonction de noeud il crée des blocs

## Solidity

[Documentation](https://docs.soliditylang.org/en/v0.8.17/)
[Documentation](https://cryptozombies.io/fr/)

Language pour déployer du code (Comme de la programmation objet).

- Smart contract -> class
