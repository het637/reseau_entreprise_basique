# Projet Réseau d'Entreprise sous Filius

## Description du Projet
Ce projet simule l'infrastructure réseau d'une entreprise à l'aide du logiciel Filius. Il comprend plusieurs segments réseau correspondant aux différentes équipes de l'entreprise ainsi qu'aux services essentiels (DNS, messagerie, et web).

## Architecture du Réseau
Le réseau est structuré en plusieurs sous-réseaux connectés via un routeur central :

- **Direction** (192.168.9.0/24) : Deux postes clients connectés via un switch.
- **Équipe 1** (192.168.1.0/24) : Quatre postes connectés via un switch.
- **Équipe 2** (Plages IP variées : 192.168.2.0/24, 192.168.3.0/24, 192.168.4.0/24) : Trois postes connectés via un switch.
- **Serveurs de l'entreprise** (192.168.0.0/24) : Hébergent les services DNS, messagerie et web.

Chaque segment est relié au routeur central qui assure la communication entre eux.

## Configuration des Serveurs

### 1. Serveur DNS
- Adresse IP : **192.168.0.10**
- Enregistrement A :
  - `www.mentreprise.fr` → **192.168.0.12** (Serveur web)

### 2. Serveur de Messagerie
- Adresse IP : **192.168.0.11**
- Domaine : `entreprise.fr`
- Comptes configurés :
  - **Direction** :
    - `mr.directeur@entreprise.fr`
    - `mme.manager@entreprise.fr`
  - **Équipe 1** :
    - `employe1@entreprise.fr` à `employe4@entreprise.fr`
  - **Équipe 2** :
    - `employe5@entreprise.fr` à `employe8@entreprise.fr`

### 3. Serveur Web
- Adresse IP : **192.168.0.12**
- Contenu hébergé : Un site web basique accessible via `www.mentreprise.fr`

## Fonctionnalités et Tests

- **Résolution DNS** : Les clients peuvent résoudre `www.mentreprise.fr` vers l'IP du serveur web.
- **Messagerie** : Les utilisateurs peuvent envoyer et recevoir des emails sous le domaine `entreprise.fr`.
- **Accès Web** : Toute machine du réseau peut accéder au site web de l'entreprise via le navigateur.
- **Communication Inter-Équipe** : Toutes les machines peuvent communiquer entre elles grâce au routeur central.

## Conclusion
Ce projet Filius modélise un réseau d'entreprise fonctionnel avec les services essentiels. Il permet de tester la connectivité, la résolution DNS, la messagerie et l'accès web dans un environnement simulé.

