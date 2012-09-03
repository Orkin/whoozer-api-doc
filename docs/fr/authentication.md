# Authentification
L'API de Whoozer met en oeuvre le protocole OAUTH2.0

Pour accéder à une donnée de l'API, il est nécessaire de fournir un **access_token**

## Obtenir un access_token à partir d'une connexion
Il vous faut rediriger l'utilisateur vers `http://connect.whoozer.fr/connect/oauth/dialog?scope=*wanted_scopes*&client_id=*your_client_id*&response_type=*code*&redirect_uri=*http://www.whoozer.fr/oauth*`

- your_client_id est à remplacer par la clé de votre application
- response_type peut prendre une de ces valeurs
   - code : un Authcode vous est fourni en paramètre GET (`code`) au retour d'une authentification réussie
   - token : un access_token et `refresh_token` vous sont passé en ancre au retour d'une authentification réussie
   - code-and-token une combinaison des deux précédents
- redirect_uri est l'url de redirection après authentification (réussie ou échec)

## Obtenir un access_token à partir d'un AuthCode
Il faut effectuer une requete POST à http://connect.whoozer.fr/connect/oauth/token avec comme paramètres:

- code=AuthCode
- client_id
- client_secret
- redirect_uri
- grant_type=authorization_code

La réponse contiendra entre autre un access_token et un refresh_token

## Obtenir un access_token à partir d'un refresh_token
Il faut effectuer une requete POST à http://connect.whoozer.fr/connect/oauth/token avec comme paramètres:

- refresh_token
- client_id
- grant_type=refresh_token

La réponse contiendra entre autre un access_token

## Obtenir un access_token à partir du login / mot de passe (demande à faire à whoozer pour en avoir les droits)
Il faut effectuer une requete POST à http://connect.whoozer.fr/connect/oauth/token avec comme paramètres:

- username
- password
- grant_type=password

## Obtenir un access_token à partir d'un access_token et secret_token Twitter (demande à faire à whoozer pour en avoir les droits)
Il faut effectuer une requete POST à http://connect.whoozer.fr/connect/oauth/token avec comme paramètre:

- grant_type=assertion
- assertion_type=twitter_access_token
- assertion= json d'une hashtable contenant key et secret. exemple `{"key":"606351126-rLhhPBwlRU196PI3sWwBQAJ6WURGSYgqT2yd0hOW","secret":"oet5Pba1F8NT6ljUI5QCTas5nDhoUUcoBcfWQwW3k"}`
- client_id
- client_secret
- scope

les clés key et secret de l'assertion doivent être obtenues par l'application officielle whoozer sur twitter

## Obtenir un access_token à partir d'un access_token Facebook (demande à faire à whoozer pour en avoir les droits)
Il faut effectuer une requete POST à http://connect.whoozer.fr/connect/oauth/token avec comme paramètre:

- grant_type=assertion
- assertion_type=facebook_access_token
- assertion= access_token facebook
- client_id
- client_secret
- scope

l'access_token de facebook doit être obtenu par l'application officielle whoozer sur facebook


# API REST
L'API de Whoozer est un webservice REST.

Pour y accéder : http://api.whoozer.fr/api/...
Exemple :
`http://api.whoozer.fr/api/users/1`

Pour accéder à une donnée whoozer il est impératif de spécifier un access_token récupérer précédemment.
## Header Http
Il faut passer l'entête `Authorization` avec pour valeur `OAuth="..."`

## Paramètre POST
Il faut passer le token dans un paramètre POST `oauth_token`

## Paramètre GET
A proscrie mais à dispo au cas où : il faut passer le token dans un paramètre GET `oauth_token`