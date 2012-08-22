# Authentification
L'API de Whoozer met en oeuvre le protocole OAUTH2.0

Pour accéder à une donnée de l'API, il est nécessaire de fournir un **access_token**

## Obtenir un access_token à partir d'une connexion
Il vous faut rediriger l'utilisateur vers `http://api.whoozer.fr/oauth/dialog?scope=full_access&client_id=*your_client_id*&response_type=*code*&redirect_uri=*http://www.whoozer.fr/oauth*`
* your_client_id est à remplacer par la clé de votre application
* response_type peut prendre une de ces valeurs
code : un Authcode vous est fourni en paramètre GET (`code`) au retour d'une authentification réussie
token : un access_token et `refresh_token` vous sont passé en ancre au retour d'une authentification réussie
code-and-token une combinaison des deux précédents
* redirect_uri est l'url de redirection après authentification (réussie ou échec)

## Obtenir un access_token à partir d'un AuthCode
Il faut effectuer une requete POST à http://api.whoozer.fr/oauth/token avec comme paramètres:
* code=AuthCode
* client_id
* client_secret
* redirect_uri
* grant_type=authorization_code

La réponse contiendra entre autre un access_token et un refresh_token

## Obtenir un access_token à partir d'un refresh_token
Il faut effectuer une requete POST à http://api.whoozer.fr/oauth/token avec comme paramètres:
* refresh_token
* client_id
* grant_type=refresh_token

La réponse contiendra entre autre un access_token

## Obtenir un access_token à partir du login / mot de passe (possible uniquement à partir du site web de Whoozer.fr)
Il faut effectuer une requete POST à http://api.whoozer.fr/oauth/token avec comme paramètres:
* username
* password

## Obtenir un access_token à partir d'une signed_request Facebook (possible uniquement à partir du site web de Whoozer.fr)
Il faut effectuer une requete POST à http://api.whoozer.fr/oauth/login-facebook avec comme paramètre:
* signed_request
Le signed request doit être celui de l'application officielle whoozer


# API REST
L'API de Whoozer est un webservice REST.

Pour y accéder : http://api.whoozer.fr/api/...
Exemple :
`http://api.whoozer.fr/api/users`

Pour accéder à une donnée whoozer il est impératif de spécifier un acce_token récupérer précédemment.
## Header Http
Il faut passer l'entête `Authorization` avec pour valeur `OAuth="..."`

## Paramètre GET
Il faut passer le token dans un paramètre GET `oauth_token`

## Paramètre POST
Il faut passer le token dans un paramètre POST `oauth_token`