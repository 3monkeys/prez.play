##Un modèle

	@Entity 
	public class Post extends Model {

	    @Id
	    public Long id;

	    @Constraints.Required
	    public String message;

	    @Constraints.Required
	    public String author;

	    /**
	     * Generic query helper for entity Post with id Long
	     */
	    public static Finder<Long,Post> find = new Finder(Long.class, Post.class); 

	    public static List<Post> find(String filter) {
	    	return find.where().ilike("author", "%"+filter+"%").findList();
	    }

	}