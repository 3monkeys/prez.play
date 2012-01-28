##Une vue

	<a href="/news"> <h1>What's up?</h1> </a>    
    @form(routes.Application.save()) {
        <fieldset>
	        <div class="input">        
        	    @inputText(postForm("author"), 'label -> "Your name : ")
	            @inputText(postForm("message"), 'label -> "Your message : ")
        	</div>
        </fieldset>

        <div class="actions">
            <input type="submit" value="Go!" class="btn primary"> or 
            <a href="/" class="btn">Cancel</a> 
        </div>        
    }

	<h1>Messages</h1>
    @for(post <- posts){
    	<div class="post"> 
    		<span class="author">@post.author : </span> 
    		<a href="/news/edit/@post.id"><p>@post.message</p></a>
    	</div>
    }

	<form action="/news/search">    	        
	 	<label for=search>Search : </label> <input type="text" id="search" name="filter">        	
     	<input type="submit" value="Go!" class="btn primary">
    </form>
 