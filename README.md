# liquibase

create a project:

```
c:\MyLiquiBaseProject\liquibase init project
```

configure the connection string in liquibase.properties:

```
liquibase.command.url=jdbc:sqlserver://localhost:1433;databaseName=mydatabase;integratedSecurity=false;encrypt=false 

```

create and configure a changelog file to use multiple sql files, and use it in liquibase.properties:

```
<?xml version="1.0" encoding="UTF-8"?> 
<databaseChangeLog
    xmlns="http://www.liquibase.org/xml/ns/dbchangelog"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns:ext="http://www.liquibase.org/xml/ns/dbchangelog-ext"
    xmlns:pro="http://www.liquibase.org/xml/ns/pro"
    xsi:schemaLocation="http://www.liquibase.org/xml/ns/dbchangelog
        http://www.liquibase.org/xml/ns/dbchangelog/dbchangelog-latest.xsd
        http://www.liquibase.org/xml/ns/dbchangelog-ext http://www.liquibase.org/xml/ns/dbchangelog/dbchangelog-ext.xsd
        http://www.liquibase.org/xml/ns/pro http://www.liquibase.org/xml/ns/pro/liquibase-pro-latest.xsd">
    <includeAll  path="changes"/>  
</databaseChangeLog>
```

```
changeLogFile=changelog.xml
```

