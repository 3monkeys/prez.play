##Un contrôleur

    public class Application extends Controller {

        //redirect
        public static Result index() {
            return redirect(routes.Application.list());
        }

        //filter
        public static Result filter(String filter) {
            return ok(list.render(Post.find(filter), form(Post.class)));
        }

        //save
        public static Result save() {
            Form<Post> postForm = form(Post.class).bindFromRequest();
            if (postForm.hasErrors()) {
                flash("error", "Form contains errors");
                return badRequest(list.render(Post.find.all(), form(Post.class)));
            }
            postForm.get().save();
            flash("success", "Post  has been created");
            return index();
        }

        //json
        public static Result listJson() {
            return ok(toJson(Post.find.all()));
        }
    }
