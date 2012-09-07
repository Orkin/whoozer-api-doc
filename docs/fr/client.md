Fields
===========
* id : `string`
* name : `string`
* first_name : `string`
* last_name : `string`
* gender : `string`
* birth_date : `string (Y-m-d)` 
* nickname : `string`
* type : `string`

Connections
============
* blocks : array of [blocked users](#blocks) objects containing id, name fields
* communities : array of [community](#communities) objects containing id, name fields
* conversations : array of [conversation](#conversations) objects containing id field
* follows : array of [follow](#follows) objects containing id,name fields
* feeds : array of [feed](feed.md) objects containing the last 25 feeds
* images : array of [image](image.md) objects containing the last 25 images
* notifications : array of [notification](notification.md) objects containing the last 25 notifications
* poke : array of [poke](poke.md) objects containing the last 25 pokes
* stream : array of [feed](feed.md) objects containing the last 25 home feeds
* report : array of [report](report.md) objects containing the last 25 report

Blocks
------
### Read block (GET)
Vous pouvez récuperer la liste des utilisateurs bloquer en envoyant une requete GET sur /users/PROFILE_ID/blocks

### Appartenance (GET)
Vous pouvez vérifier si un utilisateur est bloquer en envoyant une requete GET sur /users/PROFILE_ID/blocks    
Vous devez passer en parametre de la requete :   
* `id` de l'utilisateur dont vous voulez vérifier si il est bloqué.   

### Block user (POST)
Vous pouvez blocker un utilisateur en envoyant une requete POST sur /users/PROFILE_ID/blocks  
Vous devez passer en parametre de la requete :  
* `id` de l'utilisateur à bloquer    

### Unblock User (DELETE)
Vous pouvez débloquer un utilisateur en envoyant une requete DELETE sur /users/PROFILE_ID/blocks   
Vous devez passer en parametre de la requete :   
* `id` de l'utilisateur à débloquer   

Communities
-----------

### Read communities (GET)
Vous pouvez récupérer la liste des communautés d'un utilisateur en envoyant une requete GET sur /users/PROFILE_ID/communities

### Appartenance (GET)
Vous pouvez vérifier si un utilisateur à rejoint une communauté en envoyant une requete GET sur /users/PROFILE_ID/communities   
Vous devez passer en parametre de la requete :    
* `id` de la communauté que vous voulez vérifier    

### Join (POST)
Vous pouvez rejoindre une communauté en envoyant une requete POST sur /users/PROFILE_ID/communities   
Vous devez passer en parametre de la requete :   
* `id` de la communauté que vous voulez rejoindre

### Leave (DELETE)
Vous pouvez quitter une communauté en envoyant une requete DELTE sur /users/PROFILE_ID/communities   
vous devez passer en parametre de la requetes :
* `id` de la communauté que vous voulez quitter

Conversations
-------------

### Read conversations (GET)
Vous pouvez récupérer la liste des conversation d'un utilisateur en envoyant une requete GET sur /users/PROFILE_ID/conversations

### Read conversation (GET)
Vous pouvez récupérer la liste des messages d'une conversation en envoyant une requete GET sur /users/PROFILE_ID/conversations   
Vous devez passer en parametre de la requete :    
* `id` de la conversation à récuperer 

### UPDATE conversation (PUT)
Vous pouvez mettre à jour la conversation en envoyant une requete POST sur /users/PROFILE_ID/conversations   
Vous devez passer en parametre de la requete :   
* `id` de la conversation à mettre a jour  

### DELETE conversation (DELETE)
Vous pouvez quitter une conversation en envoyant une requete DELETE sur /users/PROFILE_ID/converations   
Vous devez passer en parametre de la requete :   
* `id` de la conversation à quitter

Follows
-------

### Read follows (GET)
Vous pouvez récuperer la liste des utilisateur suivis en envoyant une requete GET sur /users/PROFILE_ID/followed

### Appartenance (GET)
Vous pouvez vérifier si un utilisateur en suit un autre en envoyant une requete GET sur /users/PROFILE_ID/followed  
Vous devez passer en parametre de la requete :
* `id` de l'utilisateur à vérifier  

### Follow (POST)
Vous pouvez faire suivre un utilisateur en envoyant une requete POST sur /users/PROFILE_ID/followed   
Vous devez passer en parametre de la requete :   
* `id` de l'utisateur à suivre

### Unfollow (DELETE)
Vous pouvez faire désuivre un utilisateur en envoyant une requete DELETE sur /users/PROFILE_ID/followed  
Vous devez passer en parametre de la requete :  
* `id` de l'utilisateur à unfollow

Feed
====
