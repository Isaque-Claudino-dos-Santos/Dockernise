# Dockerfile Java 24

## Contents

- ubuntu 24.04
- java 24
- maven

## Docker-compose.yml Recomendations

### Add Volumen to maven file `pom.xml` 

```yml

app:
  - "./pom.xml:/usr/src/app/pom.xml"

```
