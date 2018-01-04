# Licences Nomis Mocks

Mocks of Nomis APIs used by the Licences project

Push to master for auto-deploy via Heroku, see https://dashboard.heroku.com/apps/licences-nomis-mocks

# To build and run the fat JAR
```
./gradlew clean shadowJar
java -jar build/libs/licences-nomis-mocks-all.jar --root-dir src/main/resources --port 9090
```

# To run via Gradle
```
./gradlew clean run
```

# To view available mappings
```
curl http://localhost:9090/__admin/
```

# Example request
```
curl -H "Authorization: token" http://localhost:9090/api/v2/prisoners?firstName=john&lastName=smith
```

# To reload mappings after making changes

Do a POST to

http://localhost:9090/__admin/mappings/reset

