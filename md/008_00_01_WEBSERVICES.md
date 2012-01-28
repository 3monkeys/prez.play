##Envoyer du XML grâce aux templates : le contrôleur

	public static void bookmarksInXML() {
		List<Bookmark> bookmarks = Bookmark.findAll();		
		render(bookmarks);
	}