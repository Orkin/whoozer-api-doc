/api/users/user_id/feeds

# Index (GET /api/users/user_id/feeds)
Retourne une liste de feeds de l'utilisateur user_id
* id
* message
* sender (user_id, name)
* wall_owner (wall_id, name)

# Get (GET /api/users/user_id/feeds/feed_id)
Retourne les informations de l'utilisateur `user_id` avec:
* id
* message
* sender (user_id, name)
* wall_owner (wall_id, name)

# Post (POST /api/users/user_id/feeds)
Crée un nouveau feed, ayant pour auteur user_id.

Informations obligatoires
* wall
* message

# Delete (DELETE /api/users/user_id/feeds/feed_id)
Supprime le feed feed_id