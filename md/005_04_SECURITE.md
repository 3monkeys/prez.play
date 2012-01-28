##Modifions `app/views/Application/index.html`

	#{extends 'main.html' /}
	#{set title:'JUG-Play!►DEMO' /}

	<!-- authentication -->
	<a href="@{Secure.login()}">Login</a>
	#{if session.get("username")}      
		<b>${user.username} / ${user.email}</b>
		<a href="@{Secure.logout()}">Logout</a>
		#{if user.isAdmin}
			<a href="admin">Admin</a>
		#{/if}
	#{/if}
	<hr>

	<ul>
	#{list items:bookmarks, as:'bookmark'}
		<li>
			<a href="${bookmark.url}">${bookmark.label}<a/> 
				in <b>${bookmark.techno.label}</b> 
				by <i>${bookmark.user.username}</i>
		</li>
	#{/list}
	</ul>
