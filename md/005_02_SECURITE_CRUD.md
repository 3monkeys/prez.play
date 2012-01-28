##On sécurise les contrôleurs "CRUD" :

	@With(Secure.class)
	@Check("isAdmin")
	public class Bookmarks extends CRUD {}

	@With(Secure.class)
	@Check("isAdmin")
	public class Technos extends CRUD {}

	@With(Secure.class)
	@Check("isAdmin")
	public class Users extends CRUD {}

##`@Check("isAdmin")` ?