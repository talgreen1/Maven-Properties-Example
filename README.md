# Maven-Properties-Example
Example project on how to use Maven properties from Java code

The properties file contains a placeholder:
name=${name}

This placeholder can be replaced from a POM file propertis or from command line.
Add this to the pom file in order to enable this feature:

<build>
.
.
.
        <resources>
            <resource>
                <directory>src/main/resources</directory>
                <filtering>true</filtering>
            </resource>
        </resources>
.
.
.
</build>


Run: 

`mvn clean install exec:java -Dexec.mainClass="com.talgreen.App"`

You can override this parameter from command line by adding -D:

`mvn clean install exec:java -Dexec.mainClass="com.talgreen.App" -Dname=fromCMD`
