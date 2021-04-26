WebGIS Api Clients
==================

Um auf die WebGIS API zuzugreifen, ist ein API Client notwendig. Jeder Client bekommt eine eindeutige ID. Wird die WebGIS API in eine Webseite eingebunden, 
muss diese ID angeführt werden.

Zusätzlich zur ID muss für einen API Client noch die Url der Webseite angeben werden, in die die WebGIS API eingebunden wird. 
Dies erfolgt über den HTTP-Referer, der garantieren soll, 
dass ein API Client nicht in einer anderen Seite verwendet werden kann.