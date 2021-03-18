# Feature 10 - Intégration à une base de donnée réelle

## Description

À l'aide de l'ODM Morphia, intégrez votre code actuel afin qu'il puisse communiquer avec une base de donnée MongoDB.

## Critères de succès

| critère | description                                                                                                         |
| ------- | ------------------------------------------------------------------------------------------------------------------- |
| C1      | L'application communique avec une base de donnée MongoDB de `test` lorsque dans l'environnement `staging`.          |
| C2      | L'application communique avec une base de donnée MongoDB de `production` lorsque dans l'environnement. `production` |
| C3      | L'application utilise une base de donnée `InMemory` lorsqu'elle n'est pas hébergée sur Heroku.                      |
| C4      | Les bases de données sur MongoDB ne sont jamais effacée une fois finales                                            |
