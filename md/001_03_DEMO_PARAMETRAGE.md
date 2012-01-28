##Routes

- dans `conf/routes`, ajouter :

		#Admin
		GET /admin  module:crud

		#Import CRUD routes
		*	/admin module:crud

###Base de données

- dans `conf/application.conf`, ajouter (dans la section `Database configuration`) :

		db=fs