/api/users/user_id/blocked

# Index (GET /api/users/user_id/blocked)
Retourne la liste des utilisateurs bloqués par user_id:
* id
* login
* first_name
* last_name
* wall

# Post (POST /api/users/user_id/blocked)
ajoute l'utilisateur blocked_user_id à la liste des utilisateurs bloqués de user_id

Informations obligatoires:
* blocked_user_id

# Delete (DELETE /api/users/user_id/blocked/blocked_user_id)
Supprime l'utilisateur blocked_user_id de la liste des utilisateurs bloqués de user_id