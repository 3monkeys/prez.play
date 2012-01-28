##Si on va faire un petit tour dans `routes`

Dans `conf/routes`, on trouve :

	# Home page
	GET		/		Application.index

##Cela signifie que :

dès que l'on appelle [http://localhost:9000/](http://localhost:9000/), on déclenche la méthode `index` du contrôleur `Application`