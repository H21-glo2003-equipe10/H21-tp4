# Feature 10 - Intégration à une base de donnée réelle

## Description

À l'aide de l'ODM Morphia, intégrez votre code actuel afin qu'il puisse communiquer avec une base de donnée MongoDB.

:warning: Seuls les produits et vendeurs sont demandés, mais vous pouvez toujours en faire plus si vous le désirez.

## Critères de succès

| critère | description                                                                                                         |
| ------- | ------------------------------------------------------------------------------------------------------------------- |
| C1      | Les **produits** ainsi que les **vendeurs** sont hébergés sur une base de donnée externe.                           |
| C2      | L'application communique avec une base de donnée MongoDB de `staging` lorsque dans l'environnement `staging`.       |
| C3      | L'application communique avec une base de donnée MongoDB de `production` lorsque dans l'environnement `production`. |
| C4      | L'application utilise une base de donnée `InMemory` lorsqu'elle n'est pas hébergée sur Heroku.                      |
| C5      | Les bases de données sur MongoDB ne sont jamais effacée une fois finales.                                           |

## Extra

Afin de vous aider à démarrer, voici quelques infos qui pourraient vous être utiles (testées avec Java 11).

**Dépendances**:

```xml
<dependency>
  <!-- Morphia -->
  <groupId>dev.morphia.morphia</groupId>
  <artifactId>morphia-core</artifactId>
  <version>2.1.4</version>
</dependency>
<dependency>
  <!-- Mongo Driver -->
  <groupId>org.mongodb</groupId>
  <artifactId>mongodb-driver-sync</artifactId>
  <version>4.2.2</version>
</dependency>
```

**Création du datastore Morphia**:

```java
MongoClient mongoClient = MongoClients.create(databaseUrl);
Datastore datastore = Morphia.createDatastore(mongoClient, databaseName);
datastore.getMapper().mapPackage(".");
datastore.ensureIndexes();
```

**Suppression de tous les documents**:

```java
datastore.delete(new DeleteOptions().multi(true));
```
