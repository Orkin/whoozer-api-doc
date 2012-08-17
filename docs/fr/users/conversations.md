/api/users/user_id/conversations

# Index (GET /api/users/user_id/conversations)
Retourne la liste des conversations de l'utilisateur user_id
* id
* modification_date
* creation_date
* last_messages (id, message, conversation, sender, creation_date)
* messages (liste des ids des messages de la conversation)