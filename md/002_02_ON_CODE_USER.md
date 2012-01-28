<br>
###User.java

	package models;

	import play.*;
	import play.db.jpa.*;
	import play.data.validation.*;
	import javax.persistence.*;
	import java.util.*;

	@Entity
	public class User extends Model {

		@Required public String username;
	    @Required @Password public String password;
	    @Email @Required public String email;
	    public boolean isAdmin;

		/* === Relations ===
			- une User "peut créer" 0 à n Bookmarks
			- on fait le lien avec l'attribut user de Bookmark
		*/
		@OneToMany(mappedBy="user",cascade=CascadeType.ALL)
		public List<Bookmark> users = new ArrayList();


	    public User(String username, String password, String email) {
	        this.email = email;
	        this.password = password;
	        this.username = username;
	    }

		public String toString() {
			return username + " : " + email;
		}
	}