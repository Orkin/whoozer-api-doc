Sous Propriétés
-----------------

 1. [applications](users/applications.md)
 2. [blocked](users/blocked.md)
 3. [conversations](users/conversations.md)
 4. [feeds](users/feeds.md)
 5. [followed](users/followed.md)
 6. [notifications](users/notifications.md)
 7. [pokes](users/pokes.md)


API
---

# Index (GET /api/users)
Retourne une liste d'utilisateurs avec:
* id
* login
* first_name
* last_name
* wall
* unread_notifications_count

# Get (GET /api/users/user_id)
Retourne les informations de l'utilisateur `user_id` avec:
* id
* login
* first_name
* last_name
* wall
* unread_notifications_count

# Post (POST /api/users)
Crée un nouvel utilisateur. Informations obligatoires:
* type : `client`, `place` ou `community`

Si client, informations obligatoires:
* first_name
* last_name
* birth_date
* gender
* login
* password
* pseudo

Facultatif:
* job

# Put (PUT /api/users/user_id)
Modifie l'utilisateur user_id. Informations obligatoires:

Si client, informations obligatoires:
* first_name
* last_name
* birth_date
* gender
* login
* password
* pseudo

Facultatif:
* job
* unread_notifications_count (paramètre exclusif, si présent, aucune autre modification ne sera faite)