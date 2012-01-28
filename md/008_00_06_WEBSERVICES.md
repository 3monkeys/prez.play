##Utiliser POST pour créer de nouvelles données

	POST    /jsonBookmark		Application.addBookmarkInJson
	
Le contrôleur : 

	public static void addBookmarkInJson() {
		Gson gson = new Gson();
		Bookmark bookmark = gson.fromJson(new InputStreamReader(request.body), Bookmark.class);
		bookmark.save();
	}
	