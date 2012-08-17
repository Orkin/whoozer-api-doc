/api/users/user_id/notifications

# Index (GET /api/users/user_id/notifications)
Retourne la liste des notifications reçues par l'utilisateur user_id:

* id
* type (1=poke)
* status (0=unread, 1=read)
* sender
* receiver
* ref_id (null)
* creation_date

