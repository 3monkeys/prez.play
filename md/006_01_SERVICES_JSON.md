##On ajoute une méthode à `Application.java`

	public static void bookmarksInJSON() {
		List<Object> bookmarks = 
			Bookmark
				.find("select b.label, b.url, b.user.username, b.techno.label from Bookmark b")
				.fetch();
				
		renderJSON(bookmarks);
	}

##On ajoute une "route"

	GET 	/bookmarks.json		Application.bookmarksInJSON

##On appelle : [http://localhost:9000/bookmarks.json](http://localhost:9000/bookmarks.json)

`ps : pour la demo lancer : play run bookmarks04 (si cela ne fonctionne pas faire un play dependencies bookmarks04)`