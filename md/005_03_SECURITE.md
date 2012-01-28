##Modifions `index()` dans `Application.java`

	public class Application extends Controller {

	    public static void index() {

			String username = session.get("username");
			User user = User.find("select u from User u where u.username = '"+
		                            username+"'").first();
			if(user != null) {
				session.put("username",user.username);
			}

			List<Bookmark> bookmarks = Bookmark.findAll();
	        render(bookmarks, user);
	    }
		/* ... */
	}

