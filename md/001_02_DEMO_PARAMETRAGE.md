##Dépendances :

- dans `conf/dependencies.yml`, ajouter :

		- play -> crud
	    - play -> secure

*Le module crud pour la génération de l'interface d'admin, le module secure pour plus tard pour l'authentification*

- en mode commande (à la racine du répertoire de travail):

		play dependencies bookmarks

Vous devriez obtenir ceci :

	~        _            _ 
	~  _ __ | | __ _ _  _| |
	~ | '_ \| |/ _' | || |_|
	~ |  __/|_|\____|\__ (_)
	~ |_|            |__/   
	~
	~ play! 1.2.3, http://www.playframework.org
	~
	~ Resolving dependencies using /Users/k33g_org/Dropbox/_JUG_/bookmarks/conf/dependencies.yml,
	~
	~
	~ Installing resolved dependencies,
	~
	~ 	modules/crud -> /Users/k33g_org/play/modules/crud
	~ 	modules/secure -> /Users/k33g_org/play/modules/secure
	~
	~ Done!
	~