# Routes

## Alert Routes

`GET` `/alerts` Returns all alerts.

`GET` `/alerts/{alert_id}` Returns the specified alert by ID

`POST` `/alerts` Creates a new alert with text (string), start time (UTC datetime), and end time (UTC datetime)

`PUT` `/alerts/{alert_id}` Updates the alert by ID with the specified data for text, start time, and end time

`DELETE` `/alerts/{alert_id}` Deletes an alert by ID

## Routes Routes

All routes include Schedule data even though it's a separate model in our database. This is because the schedule should just be sent with the route.

`GET` `/routes` Gets all routes

`POST` `/routes` Parses the uploaded KML file and creates a new routes

`GET` `/routes/{route_id}` Gets a route by the specified ID with its schedule

`PUT` `/routes/{route_id}` Updates a route by ID with the uploaded KML file

`GET` `/routes/{route_id}/stops` Gets all the stops for the specified route by ID

`POST` `/routes/{route_id}/stops` Adds a stop to the specified route by ID

`DELETE` `/routes/{route_id}/stops/{stop_id}` Removes the specified stop by ID from the specified route by ID

## Stops Routes

`GET` `/stops` Gets all stops

`POST` `/stops` Creates a new stop

`GET` `/stops/{stop_id}` Gets the specified stop by ID

`PUT` `/stops/{stop_id}` Updates the specified stop by ID

`DELETE` `/stops/{stop_id}` Deletes the specified stop by ID

## Van Routes

`GET` `/vans` Gets all vans

`GET` `/vans/{van_id}` Gets the specified van by ID

`POST` `/vans` Creates a new van

`PUT` `/vans/{van_id}` Updates the specified van by ID with a new route selection

`DELETE` `/vans/{van_id}` Deletes the specified van by ID

## Analytics Routes

This route structure is designed to be extensible for future types of analytics as they may arise.

`GET` `/stats/ridership` Gets all analytics about ridership

`POST` `/stats/ridership/{van_id}` Updates ridership analytics
