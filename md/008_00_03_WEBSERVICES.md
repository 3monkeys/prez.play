##Envoyer du XML grâce aux templates : le fichier routes

	GET 	/bookmarks.xml            				Application.bookmarksInXML(format:'xml') 
	
Le paramètre `format` permet d'utiliser la méthode render avec le template XML

[http://localhost:9000/bookmarks.xml](http://localhost:9000/bookmarks.xml)

`ps : pour la demo lancer : play run bookmarks05 (si cela ne fonctionne pas faire un play dependencies bookmarks05)`