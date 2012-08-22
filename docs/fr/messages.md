/api/messages

# Get (GET /api/messages/message_id)
Retourne les informations du message `message_id` avec:
* id
* message
* conversation
* sender
* creation_date

# Post (POST /api/messages)
Crée un nouveau message. Informations obligatoires:
* conversation (pour ajouter un message à la conversation donnée)

ou 
* recipients (pour créer une nouvelle conversation avec tous les recipients comme destinataires)

Egalement : 
* message