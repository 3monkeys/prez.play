##Créer un fichier `/app/views/Application/bytechno.html`

	#{extends 'main.html' /}
	#{set title:'JUG-Play!►DEMO' /}

	<ul>
	#{list items:technos, as:'techno'}
		<li><b>${techno.label}</b>
			<ul>
			#{list items:techno.bookmarks, as:'bookmark'}
				<li>
					<a href="${bookmark.url}">${bookmark.label}<a/> 
					by <i>${bookmark.user.username}</i>
				</li>
			#{/list}
			</ul>
		</li>
	#{/list}
	</ul>


