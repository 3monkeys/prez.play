<br>
###Techno.java

	package models;

	import play.*;
	import play.db.jpa.*;
	import play.data.validation.*;
	import javax.persistence.*;
	import java.util.*;

	@Entity
	public class Techno extends Model {
		@Required public String label = "???";

		/* === Relations ===
			- une Techno "comprend" 0 à n Bookmarks
			- on fait le lien avec l'attribut techno de Bookmark
		*/
		@OneToMany(mappedBy="techno",cascade=CascadeType.ALL)
		public List<Bookmark> bookmarks = new ArrayList();

		public Techno(String label) {
		    this.label = label;
		}

		public String toString() {
			return label;
		}
	}