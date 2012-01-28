##Avec jQuery

	<div></div>

	<script>
		$(document).ready(function() {
			$.get('/bookmarks.json',function(data){
				data.forEach(function(item){
					$('div').append(item.join('<br>'));
					$('div').append('<hr>');
				})
			});
		});
	</script>

##On appelle : [http://localhost:9000/public/testjson.html](http://localhost:9000/public/testjson.html)