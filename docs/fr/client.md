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
* picture : `object(url, width, height, type)`
* cover : `object(url, width, height, type)`
* distance : `integer`
* position : `object(lat, long, alt, vacc, hacc)`
* controls : object('distance_privacy', 'age_privacy', 'presentation_privacy', 'relationship_privacy', 'phone_privacy', 'job_privacy')

Connections
============
* applications :  array of [applications](#applications) objects containing (id,name,description)
* blocks : array of [blocked users](#blocks) objects containing `(id, name)` fields
* communities : array of [community](#communities) objects containing `(id, name)` fields
* conversations : array of [conversation](#conversations) objects containing id field
* follows : array of [follow](#follows) objects containing id,name fields
* feeds : array of [feed](#feeds) objects containing the last 25 feeds
* images : array of [image](#images) objects containing the last 25 images
* notifications : array of [notification](#notifications) objects containing the last 25 notifications
* pokes : array of [poke](#pokes) objects containing the last 25 pokes
* stream : array of [feed](#stream) objects containing the last 25 home feeds
* reports : array of [report](#reports) objects containing the last 25 report


Blocks
------
### Read block (GET)
Vous pouvez récuperer la liste des utilisateurs bloquer en envoyant une requete GET sur /USER_ID/blocked

### Appartenance (GET)
Vous pouvez vérifier si un utilisateur est bloquer en envoyant une requete GET sur /USER_ID/blocked    
Vous devez passer en parametre de la requete :   
* `id` de l'utilisateur dont vous voulez vérifier si il est bloqué.   

### Block user (POST)
Vous pouvez blocker un utilisateur en envoyant une requete POST sur /USER_ID/blocked  
Vous devez passer en parametre de la requete :  
* `id` de l'utilisateur à bloquer    

### Unblock User (DELETE)
Vous pouvez débloquer un utilisateur en envoyant une requete DELETE sur /USER_ID/blocked   
Vous devez passer en parametre de la requete :   
* `id` de l'utilisateur à débloquer   

Communities
-----------

### Read communities (GET)
Vous pouvez récupérer la liste des communautés d'un utilisateur en envoyant une requete GET sur /USER_ID/communities

### Appartenance (GET)
Vous pouvez vérifier si un utilisateur à rejoint une communauté en envoyant une requete GET sur /USER_ID/communities   
Vous devez passer en parametre de la requete :    
* `id` de la communauté que vous voulez vérifier    

### Join (POST)
Vous pouvez rejoindre une communauté en envoyant une requete POST sur /USER_ID/communities   
Vous devez passer en parametre de la requete :   
* `id` de la communauté que vous voulez rejoindre

### Leave (DELETE)
Vous pouvez quitter une communauté en envoyant une requete DELTE sur /USER_ID/communities   
vous devez passer en parametre de la requetes :
* `id` de la communauté que vous voulez quitter

Conversations
-------------

### Lire conversations (GET)
Vous pouvez récupérer la liste des conversation d'un utilisateur en envoyant une requete GET sur /USER_ID/conversations

### Lire conversation (GET)
Vous pouvez récupérer la liste des messages d'une conversation en envoyant une requete GET sur /CONVERSATION_ID   
Vous devez passer en parametre de la requete :    
* `id` de la conversation à récuperer 

### Mettre a jour conversation (PUT)
Vous pouvez mettre à jour la conversation en envoyant une requete POST sur /CONVERSATION_ID   
Vous devez passer en parametre de la requete :   
* `id` de la conversation à mettre a jour  

### Quitter conversation (DELETE)
Vous pouvez quitter une conversation en envoyant une requete DELETE sur /CONVERSATION_ID   
Vous devez passer en parametre de la requete :   
* `id` de la conversation à quitter

Follows
-------

### Lire follows (GET)
Vous pouvez récuperer la liste des utilisateur suivis en envoyant une requete GET sur /USER_ID/followed

### Appartenance (GET)
Vous pouvez vérifier si un utilisateur en suit un autre en envoyant une requete GET sur /USER_ID/followed  
Vous devez passer en parametre de la requete :
* `id` de l'utilisateur à vérifier  

### Suivre (POST)
Vous pouvez faire suivre un utilisateur en envoyant une requete POST sur /USER_ID/followed   
Vous devez passer en parametre de la requete :   
* `id` de l'utisateur à suivre

### Désuivre (DELETE)
Vous pouvez faire désuivre un utilisateur en envoyant une requete DELETE sur /USER_ID/followed  
Vous devez passer en parametre de la requete :  
* `id` de l'utilisateur à unfollow

Feeds
-----

### Lire feeds (GET)
Vous pouvez récupérer la liste des feed d'un utilisateur en envoyant une requete GET sur /USER_ID/feeds

### Poster un feed (POST)
Vous pouvez post un feed en envoyant une requete POST sur /USER_ID/feeds  
Vous devez passer en parametre de la requete :   
* `message : string`
* `wall : int` (optional)

### Supprimer un feed (DELETE)
Vous pouvez supprimer un feed en envayant une requete DELETE sur /FEED_ID 
Vous devez passer en parametre de la requete :   
* `id' du feed a supprimer

Images
------

### Lire images (GET)
Vous pouvez récupérer la liste des images d'un utilisateur en envoyant une requete GET sur /USER_ID/images

### Poster une image (POST)
Vous pouvez post un feed en envoyant une requete POST sur /USER_ID/images  
Vous devez dans le body de la requete le contenu du fichier  


### Supprimer une image (DELETE)
Vous pouvez supprimer un feed en envayant une requete DELETE sur /IMAGE_ID  
Vous devez passer en parametre de la requete :   
* `id' de l'image a supprimer

Notifications
-------------

### Lire notifications (GET)
Vous pouvez récupérer la liste des notifications d'un utilisateur en envoyant une requete GET sur /USER_ID/notifications

### Lire une notification (GET)
Vous pouvez récupérer une notification en envoyant une requete GET sur /NOTIFICATION_ID/   
Vous devez passer en parametre de la requete :   
* `id` de la notification à récupérer

### Supprimer une notification (DELETE)
Vous pouvez supprimer une notification en envoyant une requete DELETE sur /NOTIFICATION_ID   
Vous devez passer en aprametre de la requete :   
* `id` de la notification à supprimer

Pokes
-----

### Lire Poke (GET)
Vous pouvez récupérer la liste des pokes d'un utilisateur en envoyant une requete GET sur /USER_ID/pokes

### Appartenance (GET)
Vous pouvez récupérer un poke d'un utilisateur et tester son existance en envoyant une requete GET sur /USER_ID/pokes   
Vous devez passer en parametre de la requete :   
* `id` du poke

### Creation d'un poke (POST)
Vous pouvez poker un utilisateur en envoyant une requete POST sur /USER_ID/pokes   
Vous devez passer en parametre de la requete :   
* `id`de l'utilisateur à bloquer

### Supprimer un poke (DELETE)
Vous pouvez supprimer un poke en envoyant une requete DELETE sur /POKE_ID  
Vous devez passer en parametre de la requete :   
* `id` du poke à supprimer


Stream
------

### Lire Stream (GET)
Vous pouvez récupérer votre stream en envoyant une requete GET sur /USER_ID/stream

Report
------

### Lire Reports (GET)
Vous pouvez récupérer la liste des report d'un utilisateur en envoyant une requete GET sur /USER_ID/reports

### Info reports (GET)
Vous pouvez récuperer un report en envoyant une requete GET sur /REPORT_ID

### Creation d'un report (POST)
Vous pouvez créer un report en envoyant une requete POST sur /USER_ID/reports   
Vous devez passer en parametre de la requete :   







