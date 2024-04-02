# SAP Cloud SDK calls RFC

## Local Execution

Setup SAP JCo as described in the install documenation. In the JCo folder run:

```bash
mvn install:install-file -Dfile=sapjco3.jar -DgroupId=com.sap.conn.jco -DartifactId=com.sap.conn.jco.sapjco3 -Dversion=3.1.9 -Dpackaging=jar
```

Set the destination:

```bash
export destinations='[{"name": "SAP_ABAP_BACKEND_RFC", "type": "RFC"}]'
```

Switch to the application folder and start the app:

```
cd application/
mvn spring-boot:run -D"spring-boot.run.profiles"=local
```
