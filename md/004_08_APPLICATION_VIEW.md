##Modifions `app/views/Application/index.html`

	#{extends 'main.html' /}
	#{set title:'JUG-Play!►DEMO' /}

	<ul>
	#{list items:bookmarks, as:'bookmark'}
		<li>
			<a href="${bookmark.url}">${bookmark.label}<a/> 
				in <b>${bookmark.techno.label}</b> 
				by <i>${bookmark.user.username}</i>
		</li>

	#{/list}
	</ul>

###on lance ...

[http://localhost:9000/](http://localhost:9000/)