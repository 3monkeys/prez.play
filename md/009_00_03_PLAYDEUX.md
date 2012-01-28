##Play!► 2, What's next?

###EBean : un petit exemple

	
	// find all the orders shipped since a week ago  
	List<Order> list = Ebean.find(Order.class)  
	    .where()  
	      .eq("status", Order.Status.SHIPPED)  
	      .gt("shipDate", lastWeek)  
	    .findList();