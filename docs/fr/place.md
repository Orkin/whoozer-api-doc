Fields
======
* id : `string`
* name : `string`
* type : `string`
* description : `string`
* is_private : `boolean`
* is_abstract : `boolean`
* user_limit : `integer`

Connections
===========
* questions : array of [questions](#questions) objects containing id, question fields
* members : array of [members](#members) objects containing id, name
* blocks : array of [blocked users](#blocks) objects containing id, name fields
* feeds : array of [feed](#feeds) objects containing the last 25 feeds
* images : array of [image](#images) objects containing the last 25 images
* notifications : array of [notification](#notifications) objects containing the last 25 notifications
* reports : array of [report](#reports) objects containing the last 25 reports

