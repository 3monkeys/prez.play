##Les routes

	POST    /news                  	 controllers.Application.save()
	GET     /news                  	 controllers.Application.list()
	GET     /news.json               controllers.Application.listJson()
	GET     /news/search             controllers.Application.filter(filter: String)