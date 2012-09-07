Fields
-------
* id : `string`
* name : `string`
* first_name : `string`
* last_name : `string`
* gender : `string`
* birth_date : `string (Y-m-d)` 
* nickname : `string`
* type : `string`

Connections
------------
* blocks : `array of (client)[client.md] objects containing id, name fields`
* communities : `array of (community)[community.md] objects containing id, name fields`
* conversations : `array of (conversation)[conversation.md] objects containing id field`
* follows : `array of (client)[client.md] objects containing id,name fields`
* feeds : `array of (feed)[feed.md] objects containing the last 25 feeds`
* images : `array of (image)[image.md] objects containing the last 25 images`
* notifications : `array of (notification)[notification.md] objects containing the last 25 notifications`
* poke : `array of (poke)[poke.md] objects containing the last 25 pokes`
* stream : `array of (feed)[feed.md] objects containing the last 25 home feeds`
* report : `array of (report)[report.md] objects containing the last 25 report`
