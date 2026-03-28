# Secure-Webmail-Deployment-Roundcube
Déploiement d'une solution de messagerie collaborative Roundcube sous Ubuntu. Intégration complète d'une stack LAMP, sécurisation des flux via SSL/TLS, et interconnexion avec les services Postfix (SMTP) et Dovecot (IMAP).

# Déploiement d'un Webmail Sécurisé (Roundcube) sur Ubuntu
**Projet Académique - Administration Système & Sécurité**
**Établissement : ISM Dakar (Licence 3 ETSE)**

## Présentation du projet
Ce projet consiste en la mise en place d'une solution de messagerie web (Webmail) complète et sécurisée. L'objectif était d'intégrer Roundcube au sein d'une infrastructure **LAMP** préexistante tout en assurant une liaison robuste avec les services de transport et de réception de courrier pour le domaine `dylan.com`.

## Architecture Technique
L'infrastructure repose sur les composants suivants :
* **Webmail :** Roundcube (installation manuelle et configuration VirtualHost Apache).
* **Moteur de base de données :** MySQL pour la gestion des comptes et des préférences.
* **Services de messagerie (Backend) :** Postfix (SMTP) pour l'envoi et Dovecot (IMAP) pour la réception.
* **Environnement :** VMware / Ubuntu Server 22.04.

---

## Réalisations Principales

### 1. Déploiement et Configuration LAMP
* Création d'une base de données dédiée `roundcubemail` avec des privilèges restreints pour l'utilisateur 'roundcube'.
* Configuration d'Apache avec un VirtualHost dédié pour assurer l'accès via une URL propre.

### 2. Sécurisation et Durcissement (Hardening)
La sécurité a été au centre de l'implémentation :
* **Chiffrement :** Activation des modules SSL/TLS pour sécuriser les flux de données.
* **Pare-feu (UFW) :** Restriction stricte des accès aux seuls ports nécessaires (HTTP/S, IMAPS, SMTP).
* **Protection Brute Force :** Intégration de Fail2Ban pour prévenir les tentatives d'intrusion.

### 3. Personnalisation et Optimisation
* Intégration d'un branding personnalisé et optimisation des ressources graphiques via ImageMagick pour améliorer la fluidité de l'interface.

---

## Conclusion
Ce projet valide la mise en œuvre d'un service critique en entreprise. Il démontre une maîtrise de l'interconnexion entre les services système et les protocoles réseau sécurisés. Vous pouvez **[consulter ici le rapport complet du Projet Webmail (PDF)](https://github.com/cruz456-debug/Secure-Webmail-Deployment-Roundcube/blob/main/Rapport_Webmail_Securise_Dylan.pdf.pdf)** pour voir les détails techniques de l'implémentation.

**Responsable du projet :** Dylan Bassinga
