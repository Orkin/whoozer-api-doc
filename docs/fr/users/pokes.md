/api/users/user_id/pokes

# Index (GET /api/users/user_id/pokes)
Retourne la liste des pokes reçus par l'utilisateur user_id:

* id
* type (1=poke)
* status (0=unread, 1=read)
* sender
* receiver
* ref_id (null)
* creation_date

# Post (POST /api/users/user_id/pokes)
Crée un poke de l'utilisateur courant (access_token) vers l'utilisateur user_id.