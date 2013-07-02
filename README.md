# FreshRSS
FreshRSS est un simple agrégateur de flux RSS.

* Site officiel : http://marienfressinaud.github.io/FreshRSS/
* Démo : http://marienfressinaud.fr/projets/freshrss/
* Développeur : Marien Fressinaud <dev@marienfressinaud.fr>
* Version actuelle : 0.3.0
* Date de publication 2013-05-05
* License AGPL3

# Disclaimer
Cette application a été développée pour s'adapter à mes besoins personnels.
Je ne garantis en aucun cas la sécurité de celle-ci, ni son bon fonctionnement
sur un autre serveur que le mien. Je m'engage néanmoins à répondre dans la
mesure du possible aux demandes d'évolution si celles-ci me semblent justifiées.
Privilégiez pour cela des demandes sur GitHub
(https://github.com/marienfressinaud/FreshRSS/issues) ou par mail (dev@marienfressinaud.fr)

# Pré-requis
* Serveur Apache ou Nginx (non testé sur les autres)
* PHP 5.3 (il me faudrait des retours sur d'autres versions antérieures)
* libxml pour PHP
* cURL
* PDO et MySQL

# Installation
1. Récupérez l'application FreshRSS via la commande git ou en téléchargeant l'archive
2. Déplacez l'application où vous voulez sur votre serveur (attention, la partie accessible se trouve dans le répertoire `./public`)
3. Accédez à FreshRSS à travers votre navigateur web et suivez les instructions d'installation
4. Tout devrait fonctionner :) En cas de problème, n'hésitez pas à me contacter.

# Sécurité et conseils
1. Si possible, faites pointer un sous-domaine sur le répertoire `./public`
2. Le fichier de log peut être utile à lire si vous avez des soucis
3. Le fichier `./public/index.php` défini les chemins d'accès aux répertoires clés de l'application. Si vous les bougez, tout se passe ici.
4. Vous pouvez ajouter une tâche CRON sur le script d'actualisation des flux. Il s'agit d'un script PHP à exécuter avec la commande `php`. Par exemple, pour exécuter le script toutes les heures :
```
0 * * * * php /chemin/vers/freshrss/actualize_script.php >/dev/null 2>&1
```

# Changelog
2013-05-05 changes with FreshRSS 0.3.0

* Fallback pour les icônes SVG (utilisation de PNG à la place)
* Fallback pour les propriétés CSS3 (utilisation de préfixes)
* Affichage des tags associés aux articles
* Internationalisation de l'application (gestion des langues anglaise et française)
* Gestion des flux protégés par authentification HTTP
* Mise en cache des favicons
* Création d'un logo *temporaire*
* Affichage des vidéos dans les articles
* Gestion de la recherche et filtre par tags pleinement fonctionnels
* Création d'un vrai script CRON permettant de mettre tous les flux à jour
* Correction bugs divers

2013-04-17 changes with FreshRSS 0.2.0

* Création d'un installateur
* Actualisation des flux en Ajax
* Partage par mail et Shaarli ajouté
* Export par flux RSS
* Possibilité de vider une catégorie
* Possibilité de sélectionner les catégories en vue mobile
* Les flux peuvent être sortis du flux principal (système de priorité)
* Amélioration ajout / import / export des flux
* Amélioration actualisation (meilleure gestion des erreurs)
* Améliorations CSS
* Changements dans la base de données
* Màj de la librairie SimplePie
* Flux sans auteurs gérés normalement
* Correction bugs divers

2013-04-08 changes with FreshRSS 0.1.0

* "Première" version