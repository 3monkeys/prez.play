##Maintenant

Dans `app/controllers/Application.java` :

	public class Application extends Controller {

	    public static void index() {
			List<Bookmark> bookmarks = Bookmark.findAll();
	        render(bookmarks);
	    }
	}