/api/users/user_id/applications

# Index (GET /api/users/user_id/applications)
Retourne la liste des applications installées par l'utilisateur:
* id
* name
* description

# Delete (DELETE /api/users/user_id/applications/id)
Supprime les droits d'accès de l'application `id` pour l'utilisateur `user_id`. Il pourra toujours rajouter cette application par la suite.

Les access_token, refresh_token, et auth_code sont également invalidés.