##Créer `Security.java` dans `app/controllers/`

	package controllers;

	import models.User;

	public class Security extends Secure.Security{

	    static boolean authenticate(String username, String password) {
		    User user = 
				User
					.find(
						"select u from User u where u.username = '"+
		            	username+"' and u.password = '"+password+"'")
					.first();

		    return user != null;
	    }

	    static boolean check(String profile) {
	        User user = User.find("byUsername", connected()).first();
	        if ("isAdmin".equals(profile)) {
	            return user.isAdmin;
	        }
	        else {
	            return false;
	        }
	    }

		static void onAuthenticated() {
			Application.index();
		}

		static void onDisconnected() {
			Application.index();
		}    
	}