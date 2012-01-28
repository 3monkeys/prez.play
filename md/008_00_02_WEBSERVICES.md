##Envoyer du XML grâce aux templates : la vue

	<?xml version="1.0" encoding="UTF-8"?>
	<bookmarks>
		#{list bookmarks, as:'bookmark'}
	    <bookmark>
	        <label>${bookmark.label}</label>
	        <description>${bookmark.description}</description>
	        <url>${bookmark.url}</url>
	    </bookmark>
	#{/list}
	</bookmarks>