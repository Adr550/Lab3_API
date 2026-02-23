


#Export de variables
export BASE_URL="https://api.artic.edu/api/v1"
export RESOURCE="artworks"
export ID="129884"
export QUERY="search?q=dogs"

#Comandos:
1. Listado
http GET $BASE_URL/$RESOURCE
2. Uso de Headers
http GET $BASE_URL/$RESOURCE 
Accept:application/json 
3. Búsqueda por ID
http GET $BASE_URL/$RESOURCE/$ID
4. 
http GET $BASE_URL/$RESOURCE $QUERY
5. Filtros avanzados
http POST $BASE_URL/$RESOURCE/search \
    Content-Type:application/json \
    q="dogs" \
    query:='{"term": {"is_public_domain": true}}'
#La documentación del API indica que se debe utilizar POST para busquedas avanzadas
6. Paginación
http GET $BASE_URL/$RESOURCE page==2 limit==5
7. Segundo recurso
http GET $BASE_URL/artists
8. Error 404
http GET $BASE_URL/$RESOURCE/000000000
9. Error 400
http GET $BASE_URL/$RESOURCE%
#Debido a que no requiere auth key no se puede simular 401 y 403
