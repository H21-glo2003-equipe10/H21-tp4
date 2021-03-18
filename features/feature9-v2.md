# Feature 9 (v2) - Health

## Description

En tant que développeur du service, j'aimerais vérifier que l'ensemble des services de l'application est up-and-running.

## Critères de succès

| critère | description                                                                       |
| ------- | --------------------------------------------------------------------------------- |
| C1      | Chaque service retourne s'il est fonctionnel (`true`) ou non (`false`)            |
| C2      | Si tous les services sont fonctionnels, le statut HTTP retourné est 200           |
| C3      | Si au moins 1 des services n'est pas fonctionnel, le statut HTTP retourné est 500 |

## Requête

`GET /health`

## Réponse

`HTTP 200 OK` ou `HTTP 500 SERVER ERROR`

```ts
{
  services: {
    api: boolean,
    db: boolean
  }
}
```
