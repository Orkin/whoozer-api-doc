Fields
======
* id : `string`
* nb_like : `integer`
* can_delete : `boolean`
* is_liked : `string`
* message : `string`
* sender : `integer`
* wall : `integer`

Connections
===========
* comments : array of [questions](#comments) objects containing id, name, message fields
* likes : array of [members](#likes) objects containing id, name