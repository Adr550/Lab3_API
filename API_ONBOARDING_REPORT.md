

                                                                -----Institute of Art Chicago API----
Base URL: https://api.artic.edu
Tipo de auth: No requiere autenticación
Rate limit: 100

Endpoints.                  | Método.  | URL                                |   Query params.       | Headers                      | Status esperado | Status obtenido|
https://api.artic.edu/api/v1|  POST    |/artworks                           |    ?page=2&limit=100   |     Accept: application/json|     200         | 200            |
                            |   GET    | /artworks/129884                   | n/a                    |     Accept: application/json|     200         | 200            |
                            |   GET    | /artworks/search                   |.      q=dogs           |    Accept: application/json |     200         | 200            |
                            |   GET    | /artworks%                          |.  n/a                  |    Accept: application/json|     404         | 400            |
                            |   GET    | /artworks/9999999                  |.  n/a                  |  Accept: application/json   |.    404         | 404            |