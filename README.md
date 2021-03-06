# gmaps-initiation-project

### Exercise 1

1. The starter code provided already loads a map and places a marker at at arbitrary location.

2. Add an event listener to detect mouse clicks on the map
	a) as the user clicks on the map, update the position of the marker to that of the event's latLng:

	b) preview your map to make sure the marker moves as you click around the map

3. Modify the listener event handler function to reverse geocode the latLng to get a textual address
 	a) add a Geocoder object in the initialize function and  modify the event handler function in 2a,
     to use the geocode method to reverse geocode the event.latLng

### Exercise 2

1) First, in the initialize function, create a Directions service object using the constructor class: google.maps.DirectionsService();

2) The DirectionsResult contains the result of the directions query, which you may either handle yourself, or pass to a DirectionsRenderer object, which can automatically handle displaying the result on a map. To display a DirectionsResult using a DirectionsRenderer, you simply need to do the following:

	a) Create a DirectionsRenderer object.
	b) Use setMap() on the renderer to bind it to the map.
	c) Use setPanel() on the renderer to indicate where to print the step by step directions.
	
3) Use the route method of the directions service to calculate directions, passing the response in callback function to the setDirections() method of the renderer to handle to display of steps and polyline.


### Exercise 3

1. The starter code already displays a map and has input elements (origin1, origin2, destinationA, destinationB) where users can enter the origins and destinations

2. To use the Distance Matrix service in JS v3 API,
	a) First, in the initialize function, create a Distance Matrix service object using the constructor class: google.maps.DistanceMatrixService()

	b) Next, use the getDistanceMatrix() method to initiate a request to the Distance Matrix service, passing it an object literal containing the origins, destinations, and travel mode, as well as a callback method to execute upon receipt of the response.

	c) Accessing the Distance Matrix service is asynchronous, since the Google Maps API needs to make a call to an external server. For that reason, you need to pass a callback method (like you did in previous step) to process the results.
