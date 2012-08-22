Sous Propriétés
-----------------

 1. [feeds](happenings/feeds.md)


API
---

# Index (GET /api/happenings)
Retourne une liste d'happening avec:
* id
* title
* description
* checking_area
* creation_date
* starting_date
* ending_date
* owner(id,name)
* status
* category(id,name)

# Get (GET /api/happenings/happening_id)
Retourne les informations de l'happening `happening_id` avec:
* id
* title
* description
* checking_area
* creation_date
* starting_date
* ending_date
* owner(id,name)
* status
* category(id,name)

# Post (POST /api/happenings)
Crée un nouvel happening. Informations obligatoires:
* title
* description
* checking_area
* starting_date
* ending_date
* status
* happening_category
