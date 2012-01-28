##Création d'une page de test `testsocket.html` :

	<script src="javascripts/jquery-1.5.2.min.js" charset="utf-8"></script>
	<H1>TEST SOCKET</H1>

	<div></div>

	<script>
		$(document).ready(function() {

			var socket = new WebSocket('ws://localhost:9000/asyncTest');

			socket.onmessage = function(event) {

			    $('div').html(event.data);
			}
		});
	</script>