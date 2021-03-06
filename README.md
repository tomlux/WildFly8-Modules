WildFly8-Modules
================
Modules for JBoss/WildFly 8.x

Modules are deployed under $JBOSS_HOME/modules/system/layers/base/

To use these modules you'll need to copy the correct "jboss-deployment-structure.xml" file under the META-INF on the top directory of the WAR file.

**Current modules:

- PostgreSQL 9.x [700KB]
-------------------------------------------------
> - Modules/org/postgresql/main/*
> - Module Activators/postgres 9.x/*

- PrimeFaces 5.x [4MB]
-------------------------------------------------
> - Modules/org/primefaces/main/*
> - Module Activators/primefaces 5.x/*

- Richfaces 4.5.x [10MB]
-------------------------------------------------
> - Modules/org/richfaces/main/*
> - Module Activators/richfaces 4.5/*

Note: Enable 'Richfaces Resource Servlet' on your web.xml for Richfaces' CSS & JavaScript to work. Add this your web.xml:
```xml
      <servlet>
        <servlet-name>Resource Servlet</servlet-name>
        <servlet-class>org.richfaces.webapp.ResourceServlet</servlet-class>
        <load-on-startup>1</load-on-startup>
      </servlet>
      <servlet-mapping>
        <servlet-name>Resource Servlet</servlet-name>
        <url-pattern>/org.richfaces.resources/*</url-pattern>
      </servlet-mapping>
```
