**Architecture et isolation**

- Est-il sécurisé de faire tourner tous les services (Apache, MySQL, PHP, WordPress) sur la même machine ? Quels sont les risques ?
- Dans quel cas envisageriez-vous de séparer les services sur des machines distinctes ?
- Connaissez-vous le principe de containerisation ? Dans quel cas l'utiliseriez-vous ici ?
- Si un service est compromis, que se passe-t-il pour les autres services sur la même machine ?
- Quel est l'intérêt d'un reverse proxy devant Apache ? Connaissez-vous des solutions ?

**Système d'exploitation**

- Quels services inutiles sont probablement actifs par défaut sur votre Debian ? Comment les identifier ?
- Quelle est votre politique de mise à jour ? Y a-t-il un moyen d'automatiser les mises à jour de sécurité ?
- Les comptes utilisateurs présents sur le système sont-ils tous nécessaires ? Comment le vérifier ?
- Sous quel utilisateur tourne le service Apache ? Est-ce un problème si cet utilisateur a des droits étendus ?
- Avez-vous activé un pare-feu local sur la machine ? Quels ports doivent être ouverts ?

**Serveur web Apache**

- Apache expose-t-il sa version dans les en-têtes HTTP ? Est-ce un problème ?
- Quels modules Apache sont activés par défaut ? Sont-ils tous nécessaires ?
- La liste des fichiers d'un répertoire est-elle accessible si aucun fichier index n'est présent ? Quel risque cela représente-t-il ?
- Le serveur accepte-t-il toutes les méthodes HTTP (GET, POST, PUT, DELETE, TRACE...) ? Lesquelles sont nécessaires pour WordPress ?
- Comment mettre en place HTTPS ? Quel impact sur le hardening ?

**Base de données MySQL**

- L'utilisateur root MySQL a-t-il un mot de passe ? Est-il accessible depuis l'extérieur ?
- MySQL écoute-t-il sur toutes les interfaces réseau par défaut ? Comment le restreindre ?
- WordPress a-t-il besoin de tous les privilèges sur la base de données, ou uniquement sur sa propre base ?
- Connaissez-vous la commande mysql_secure_installation ? À quoi sert-elle ?
- Les bases de données de test créées par défaut représentent-elles un risque ?

**PHP**

- PHP expose-t-il sa version dans les en-têtes HTTP ? Comment le désactiver ?
- Certaines fonctions PHP dangereuses (exec, system, passthru, shell_exec) sont-elles nécessaires pour WordPress ?
- Quelle est la différence entre display_errors actif en production et en développement ? Quel risque ?
- Le open_basedir permet de restreindre les fichiers accessibles par PHP. Sauriez-vous l'utiliser ici ?

**WordPress**

- L'interface d'administration /wp-admin doit-elle être accessible depuis n'importe quelle IP ?
- WordPress affiche-t-il la version utilisée dans le code source de la page ? Est-ce un problème ?
- Que pensez-vous du fait de garder les thèmes et plugins par défaut non utilisés ?
- Quel est le niveau de risque des plugins tiers ? Comment évalueriez-vous la fiabilité d'un plugin ?
- Les identifiants WordPress sont-ils exposés via l'API REST par défaut (/wp-json/wp/v2/users) ?
- Quel est l'intérêt d'un plugin de sécurité type Wordfence ou WP Cerber ? Est-ce suffisant en soi ?

**Journalisation et supervision**

- Où sont stockés les logs Apache ? Sont-ils suffisants pour détecter une attaque ?
- Centraliseriez-vous les logs ? Pourquoi ?
- Mettez-vous en place une surveillance sur les fichiers WordPress (intégrité) ? Avec quel outil ?

**Sauvegarde et reprise d'activité / résilience**

- Quel est votre plan si WordPress est compromis et défiguré ?
- Les sauvegardes sont-elles stockées sur la même machine ? Quel risque ?
- Testez-vous régulièrement la restauration de vos sauvegardes ?
