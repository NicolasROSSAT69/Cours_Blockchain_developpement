
# Blockchain et développement

## Pré-requis

- MetaMask
- Phantom
- RemixIDE

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

- [Documentation](https://docs.soliditylang.org/en/v0.8.17/)
- [CryptoZombies](https://cryptozombies.io/fr/)
- [RemixIDE](https://remix-project.org/)
- [Truffle](https://trufflesuite.com/)

Language pour déployer du code (Comme de la programmation objet).

- Smart contract -> class

EVM (Machine Virtuelle Ethereum) = environnement d'exécution des smarts contracts pour ETH.

- Compte de contrat => Gérer le code executer par EVM.

- Compte externe => Association clé publique, clé privée.

Une adresse Smart contract est déterminée au moment du déploiement/création.

Une transaction s'effectue d'un compte à un autre (d'un "wallet" à un autre).

## Gas Price

c'est le carburant de la transaction qui est payé au moment du déploiement.
Le prix du gaz est le second paramètre à spécifier lors de l'envoi d'une transaction. Comme son nom l'indique, il s'agit du prix en ETH auquel l'utilisateur achète le gaz. L'unité est le wei. 1 ETH = 10^18 wei (1 000 000 000 000 000 000 wei).

## En Groupe

### Questions

- Deployer un smart contract qui cree un token de type ERC20
- Decrivez comment on peut gerer les nombre a virgules flottante avec Solidity
- Pourquoi parle-t-on de nombre de decimales au sein du contrat ERC20.sol ?
- Comment se comporte les blockchains avec le stockage massif de fichiers ? (IPFS.tech et Arweave.org)

### Reponses

- Smart contract token ERC20 :

```
0x5C7cB3991c0625A9B0707dacbEceEc5739fF90F2
```

Les tokens dits « ERC20 » sont issus du processus de proposition / amélioration mis en oeuvre par la Fondation Ethereum

ERC signifie littéralement Ethereum Request for Comments : un processus par lequel une personne demande à la communauté de revoir et de commenter une proposition pour Ethereum. En l’occurence, la 20ème proposition postée sur le Github le 19 novembre 2015 concernait une proposition de standards pour le développement de tokens sur Ethereum – elle s’appela donc ERC20.

ERC20 est un standard : il définit des fonctions et des événements qu’un token doit gérer pour être qualifié d’ERC20. Il ne s’agit pas d’un code précis ou d’un produit. Chacun peut créer son propre code de token ERC20 tant que celui-ci respecte les fonctions standard et leur comportement.

- Solidity et la machine virtuelle Ethereum ne prennent pas en charge les décimales : seuls des nombres entiers peuvent être utilisés. La solution est d'utiliser un token contract qui peut utiliser des valeurs entières plus grandes (l'EVM prend en charge les entiers 256 bits) de sorte qu'un solde de 1000000000000000000 représente 1 ETH avec 18 décimales, donc un transfert de 4000000000000000 correspondra à 0,004ETH envoyé.

## Truffle / Ganache

### Deployer smart contract en local

```
truffle init
```

```
truffle create contract nomducontract
```

Remplir le smart contract.

```
truffle compile
```

```
truffle migrate
```

## Application Web3 React

Pour créer une application React

```
npx create-react-app nomduprojet
```

Pour lancer l'application react

```
npm start
```

Pour créer une application web3 il faut utiliser la librairie [web3.js](https://www.npmjs.com/package/web3).
C'est ce qui nous sert d'API pour communiquer avec la blockchain.
