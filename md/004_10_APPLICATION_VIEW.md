##Modifions le contrôleur `Application.java`

	public class Application extends Controller {

	    public static void index() {
			List<Bookmark> bookmarks = Bookmark.findAll();
	        render(bookmarks);
	    }

		public static void bytechno() {
			List<Techno> technos = Techno.findAll();
			render(technos);
		}

	}