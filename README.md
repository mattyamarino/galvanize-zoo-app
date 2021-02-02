# galvanize-zoo-app

|(URI)|(HTTP Method)|(HTTP Status)| (Description) |(Request) | (Response)
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
|"/animals"  |POST|  201  |Add animal to database | name: lion, type: walking, isHappy: true | {id: 12345,  name: lion, type: walking, isHappy: true}
|"/animals"  |GET|  200  |Returns all animals from database |  | [{id: 12345,  name: lion, type: walking, isHappy: true}, {id: 67890,  name: elephant, type: walking, isHappy: false}]
|"/habitats"  |POST|  201  |Add habitat to database | name: savanah, type: walking | {id: 12345,  name: savanah, type: walking, animal: null}
|"/update-habitat?animalId=12345&habitatId=67890"| PATCH | 200 | Assigns animal to habitat |  | |
|"/animals-by-type-mood?isHappy=true&type=walking" | GET | 200 | Returns animals from database matching mood and type | |[{id: 12345,  name: donkey, type: walking, isHappy: true}, {id: 67890,  name: wolf, type: walking, isHappy: true}]
|"empty-habitats"| GET | 200 | Returns all empty habitats from database | | [{id: 12345,  name: savanah, type: walking, animal: null}, {id: 12345,  name: lake, type: swiming, animal: null}]
|"feed-animal?animalId=12345" | PATCH | 200 | Gives selected animal a treat and makes them happy | | |
            
