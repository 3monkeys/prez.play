##Création d'un contrôleur `AsyncController.java`

	package controllers;

	import org.apache.commons.lang.exception.ExceptionUtils;
	import play.Logger;
	import play.libs.F.EventStream;
	import play.mvc.WebSocketController;

	public class AsyncController extends WebSocketController {

	    public static EventStream<String> liveStream = new EventStream<String>();

	    public static void asyncMessage() {
	        while (inbound.isOpen()) {
	            String message = await(liveStream.nextEvent());
	            if (message != null) {
	                outbound.send(message);
	            }
	        }
	    }
	}