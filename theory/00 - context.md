# Définitions

## Pourquoi en parler ?

- [cyber.gouv.fr/reglementation/cybersecurite-des-produits/cyber-resilience-act/](cyber.gouv.fr/reglementation/cybersecurite-des-produits/cyber-resilience-act/)
- [www.watchguard.com/fr/wgrd-news/blog/comprendre-les-differences-entre-le-reglement-dora-et-la-directive-nis-2](www.watchguard.com/fr/wgrd-news/blog/comprendre-les-differences-entre-le-reglement-dora-et-la-directive-nis-2)

## Hardening - *Durcissement*

[Wikipedia says](https://en.wikipedia.org/wiki/Hardening_(computing))

>In [computer security](https://en.wikipedia.org/wiki/Computer_security "Computer security"), **hardening** is usually the process of securing a system by reducing its [attack surface](https://en.wikipedia.org/wiki/Attack_surface "Attack surface"), which is larger when a system performs more functions; in principle a single-function system is more secure than a multipurpose one. Reducing available ways of attack typically includes changing default passwords, the removal of unnecessary software, unnecessary [usernames](https://en.wikipedia.org/wiki/User_\(computing\) "User (computing)") or [logins](https://en.wikipedia.org/wiki/Login "Login"), and the disabling or removal of unnecessary [services](https://en.wikipedia.org/wiki/Daemon_\(computing\) "Daemon (computing)"). 
>
>Hardening measures can include setting up [intrusion prevention systems](https://en.wikipedia.org/wiki/Intrusion_detection_system "Intrusion detection system"), disabling accounts, reducing [file system permissions](https://en.wikipedia.org/wiki/File-system_permissions "File-system permissions") and using encrypted network connections.

En français

> En sécurité informatique, le durcissement est généralement le processus de sécurisation d'un système par la réduction de sa **surface d'attaque**, qui est plus grande lorsqu'un système exécute plus de fonctions ; en principe, un système à fonction unique est plus sûr qu'un système polyvalent. La réduction des moyens d'attaque disponibles comprend généralement la **modification des mots de passe par défaut**, la **suppression des logiciels inutiles**, des **noms d'utilisateur** ou des **identifiants de connexion inutiles**, ainsi que la **désactivation** ou la **suppression des services inutiles**. 
> 
> Les mesures de renforcement peuvent inclure la mise en place de systèmes de prévention d'intrusions, **la désactivation des comptes**, la **réduction des autorisations du système de fichiers** et **l'utilisation de connexions réseau chiffrées**. 

## Attack Surface - *Surface d'attaque* 

[Wikipedia says](https://en.wikipedia.org/wiki/Attack_surface)

> The **attack surface** of a [software](https://en.wikipedia.org/wiki/Software "Software") environment is the sum of the different points (for "[attack vectors](https://en.wikipedia.org/wiki/Attack_vector "Attack vector")") where an unauthorized user (the "attacker") can try to enter data to, extract data, [control a device or critical software in an environment](https://cheatsheetseries.owasp.org/cheatsheets/Attack_Surface_Analysis_Cheat_Sheet.html). Keeping the attack surface as small as possible is a basic security measure.

En français

> La **surface d'attaque** d'un environnement logiciel est **la somme des différents points** (ou « vecteurs d'attaque ») où un **utilisateur non autorisé** (l'« attaquant ») peut essayer d'**entrer des données, d'extraire des données, de contrôler un dispositif ou un logiciel critique dans un environnement**. Maintenir la surface d'attaque aussi réduite que possible est une mesure de sécurité de base.

## Attack Vector - *Vecteur d'attaque*

[Wikipedia says](https://en.wikipedia.org/wiki/Attack_vector)

> In [computer security](https://en.wikipedia.org/wiki/Computer_security "Computer security"), an **attack vector** is a specific path, method, or scenario that can be exploited to break into an IT system, thus compromising its security. The term was derived from the corresponding notion of [vector in biology](https://en.wikipedia.org/wiki/Vector_\(epidemiology\) "Vector (epidemiology)"). An attack vector may be exploited manually, automatically, or through a combination of manual and automatic activity.

En français

> En sécurité informatique, un **vecteur d'attaque** est **un chemin**, une méthode ou **un scénario spécifique** qui peut être exploité pour **pénétrer dans un système informatique et compromettre ainsi sa sécurité**. Le terme est dérivé de la notion correspondante de vecteur en biologie. Un vecteur d'attaque peut être **exploité manuellement, automatiquement ou par une combinaison d'activités manuelles et automatiques**.

# Synthèse

Le hardening repose sur plusieurs principes fondamentaux :

- Principe du moindre privilège : chaque utilisateur, service ou processus ne dispose que des droits strictement nécessaires à son fonctionnement
- Réduction de la surface d'attaque : moins il y a de composants exposés, moins il y a d'opportunités pour un attaquant
- Défense en profondeur : les mesures de sécurité sont superposées, aucune couche n'est suffisante à elle seule
- Sécurité par défaut : tout ce qui n'est pas explicitement autorisé est interdit

Le hardening consiste à augmenter le niveau de sécurité d'un système en réduisant sa surface d'attaque. La surface d'attaque d'un système est la somme de ses vecteurs d'attaques.

| Ce que le hardening N'est PAS | Et pourquoi c'est important de le préciser ! |
|---|---|
| Une solution miracle | Le hardening réduit le risque, il ne l'élimine pas |
| Un antivirus ou un EDR | Ce sont des outils de détection/protection, complémentaires mais distincts |
| Un audit de sécurité ou un pentest | Ces démarches évaluent la sécurité, le hardening l'améliore |
| Un acte ponctuel | Le hardening est un processus continu, pas une case à cocher |
| De la conformité | Être conforme à un référentiel n'implique pas forcément d'être sécurisé, et inversement |
| Un substitut à la mise à jour des systèmes | Le patch management est un prérequis, pas une composante du hardening à proprement parler |

