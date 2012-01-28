##Choisir le format de données

	GET 	/bookmarks.{<json|xml>format}          				Application.bookmarks

Dans le contrôleur : 
	
	if (request.format.equals("json"))
		renderJSON(bookmarks); // <-- serialization JSON
	else render("@bookmarksInXML", bookmarks); // sérialisation XMl également dispo avec XStream
