<br>
###Bookmark.java

	package models;

	import play.*;
	import play.db.jpa.*;
	import play.data.validation.*;
	import javax.persistence.*;
	import java.util.*;

	@Entity
	public class Bookmark extends Model {
		@Required public String label;
		@Lob
		@MaxSize(200) 
		public String description;
		public String url;

		/* === Relations ===
			- un Bookmark "a" une techno 
				- une techno + sieurs bookmarks
			- un Bookmark est créé par un utilisateur
				- un user + sieurs bookmarks
		*/
		@ManyToOne
		public Techno techno;
		@ManyToOne
		public User user;

		public Bookmark(String label, String description, String url) {
		    this.label = label;
			this.description = description;
			this.url = url;
		}

		public String toString() {
			return label;
		}	
	}