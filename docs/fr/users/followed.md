/api/users/user_id/followed

# Index (GET /api/users/user_id/followed)
Retourne la liste des utilisateurs suivis par user_id:
* id
* login
* first_name
* last_name
* wall

# Post (POST /api/users/user_id/followed)
Fait suivre l'utilisateur passé en paramètre (`followed_user_id`) à user_id
Informations obligatoires:
* followed_user_id

# Delete (DELETE /api/users/user_id/followed/id)
Supprime l'utilisateur id de la liste des utilisateurs suivis par user_id