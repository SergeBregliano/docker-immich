# docker-immich
Docker Compose permettant de lancer une instance du [projet Immich](https://github.com/immich-app/immich). Cette stack suit les [recommandations d'installation](https://immich.app/docs/install/docker-compose) du projet.

Cette stack est prévue pour être utilisée avec [https-portal](https://github.com/SteveLTN/https-portal) en reverse proxy (via le paramètre VIRTUAL_HOST).



## Configuration serveur

Renommer le fichier `sample.env` en `.env`.

Configurer le fichier `.env` avec les valeurs souhaitées.

Préciser notamment :

- VIRTUAL_HOST : nom de domaine de d'Immich.
- UPLOAD_LOCATION : chemin pour le stockage des données.



## Mise à jour des serveurs

Sur des mises à jour mineures, il est possible lancer le script ``updateStack.sh`` en ligne de commande afin de télécharger les dernières images de la stack.

```shell
sh ./updateStack.sh
```

**Attention** : cette commande se contente de télécharger les nouvelles images et de les relancer. Le ``docker-compose`` n'est pas actualisé. Bien penser à vérifier régulièrement sa configuration par rapport aux recommandations.
