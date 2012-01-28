##Petites modifications de `Application.java`

	public class Application extends Controller {

		public static void bookmarksInJSON() {
			List<Object> bookmarks = 
				Bookmark
					.find("select b.label, b.url, b.user.username, b.techno.label from Bookmark b")
					.fetch();
		
			AsyncController.liveStream.publish("Application.bookmarksInJSON has been called");
		
			renderJSON(bookmarks);
		}

	    public static void index() {
	
			String username = session.get("username");
			User user = User.find("select u from User u where u.username = '"+
		                            username+"'").first();
			if(user != null) {
				session.put("username",user.username);
			}
	
			List<Bookmark> bookmarks = Bookmark.findAll();
		
			AsyncController.liveStream.publish("Application.index has been called");
		
	        render(bookmarks, user);
	    }

		public static void bytechno() {
			List<Techno> technos = Techno.findAll();
		
			AsyncController.liveStream.publish("Application.bytechno has been called");
		
			render(technos);
		}
	}