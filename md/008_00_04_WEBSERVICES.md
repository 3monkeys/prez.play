##Ajouter des paramètres

	GET 	/{techno}/bookmarks.xml            				Application.bookmarksInXML(format:'xml') 

Dans le contrôleur : 
	
	public static void bookmarksInXML(String techno) {
		List<Bookmark> bookmarks = Bookmark.find("where techno.label =", techno);		
		render(bookmarks);
	}
