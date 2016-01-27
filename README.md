# gradle_with_poi
explore gradle with poi from apache

* gradle init --type groovy-library

* https://spring.io/guides/gs/gradle/

* Markdown basics
	* https://help.github.com/articles/markdown-basics/
	* https://help.github.com/articles/github-flavored-markdown/
	
* example project with poi
* https://github.com/stephanstan/griddle

* showed that poi is part of the dependency tree
gradle -q dependencies

* tutorial
http://www.vogella.com/tutorials/Gradle/article.html


* https://help.github.com/articles/github-flavored-markdown/

| git commands| 
------------------
| git status| 
| git add build.gradle| 
| git commit -a -m "add description to project" | 
| git push| 

```
C:\grails\workspace\gradle_with_poi [master +1 ~1 -0 !]> gradle dependencies
:dependencies

Root project - Stephan Stan - Learning about gradle and incorporating dependencies like poi.  Ultimate goal of converting / upgrading some java projects.  Better standardization.

archives - Configuration for archive artifacts.
No dependencies

compile - Compile classpath for source set 'main'.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
\--- com.oracle:ojdbc6:11.2.0.4

default - Configuration for default artifacts.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
\--- com.oracle:ojdbc6:11.2.0.4

runtime - Runtime classpath for source set 'main'.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
\--- com.oracle:ojdbc6:11.2.0.4

testCompile - Compile classpath for source set 'test'.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
+--- com.oracle:ojdbc6:11.2.0.4
+--- org.spockframework:spock-core:1.0-groovy-2.4
|    +--- org.codehaus.groovy:groovy-all:2.4.1 -> 2.4.5
|    \--- junit:junit:4.12
|         \--- org.hamcrest:hamcrest-core:1.3
\--- junit:junit:4.12 (*)

testRuntime - Runtime classpath for source set 'test'.
+--- org.codehaus.groovy:groovy-all:2.4.5
+--- org.apache.poi:poi:3.14-beta1
|    \--- commons-codec:commons-codec:1.10
+--- org.apache.poi:poi-ooxml:3.14-beta1
|    +--- org.apache.poi:poi:3.14-beta1 (*)
|    +--- org.apache.poi:poi-ooxml-schemas:3.14-beta1
|    |    \--- org.apache.xmlbeans:xmlbeans:2.6.0
|    |         \--- stax:stax-api:1.0.1
|    \--- com.github.virtuald:curvesapi:1.03
+--- com.oracle:ojdbc6:11.2.0.4
+--- org.spockframework:spock-core:1.0-groovy-2.4
|    +--- org.codehaus.groovy:groovy-all:2.4.1 -> 2.4.5
|    \--- junit:junit:4.12
|         \--- org.hamcrest:hamcrest-core:1.3
\--- junit:junit:4.12 (*)

(*) - dependencies omitted (listed previously)

BUILD SUCCESSFUL

Total time: 5.911 secs
C:\grails\workspace\gradle_with_poi [master +1 ~1 -0 !]>
```

```
C:\grails\workspace\gradle_with_poi [master +0 ~1 -0]> gradle test
:compileJava UP-TO-DATE
:compileGroovy UP-TO-DATE
:processResources UP-TO-DATE
:classes UP-TO-DATE
:compileTestJava UP-TO-DATE
:compileTestGroovy UP-TO-DATE
:processTestResources UP-TO-DATE
:testClasses UP-TO-DATE
:test UP-TO-DATE

BUILD SUCCESSFUL

```

```
C:\grails\workspace\gradle_with_poi [master]> gradle tasks
:tasks

------------------------------------------------------------
All tasks runnable from root project - Stephan Stan - Learning about gradle and incorporating dependencies like poi.  Ultimate goal of converting / upgrading some java projects.  Better standardization.
------------------------------------------------------------

Build tasks
-----------
assemble - Assembles the outputs of this project.
build - Assembles and tests this project.
buildDependents - Assembles and tests this project and all projects that depend on it.
buildNeeded - Assembles and tests this project and all projects it depends on.
classes - Assembles main classes.
clean - Deletes the build directory.
jar - Assembles a jar archive containing the main classes.
testClasses - Assembles test classes.

Build Setup tasks
-----------------
init - Initializes a new Gradle build. [incubating]
wrapper - Generates Gradle wrapper files. [incubating]

Documentation tasks
-------------------
groovydoc - Generates Groovydoc API documentation for the main source code.
javadoc - Generates Javadoc API documentation for the main source code.

Help tasks
----------
buildEnvironment - Displays all buildscript dependencies declared in root project 'gradle_with_poi'.
components - Displays the components produced by root project 'gradle_with_poi'. [incubating]
dependencies - Displays all dependencies declared in root project 'gradle_with_poi'.
dependencyInsight - Displays the insight into a specific dependency in root project 'gradle_with_poi'.
help - Displays a help message.
model - Displays the configuration model of root project 'gradle_with_poi'. [incubating]
projects - Displays the sub-projects of root project 'gradle_with_poi'.
properties - Displays the properties of root project 'gradle_with_poi'.
tasks - Displays the tasks runnable from root project 'gradle_with_poi'.

Verification tasks
------------------
check - Runs all checks.
test - Runs the unit tests.

Other tasks
-----------
install - Installs the 'archives' artifacts into the local Maven repository.

Rules
-----
Pattern: clean<TaskName>: Cleans the output files of a task.
Pattern: build<ConfigurationName>: Assembles the artifacts of a configuration.
Pattern: upload<ConfigurationName>: Assembles and uploads the artifacts belonging to a configuration.

To see all tasks and more detail, run gradle tasks --all

To see more detail about a task, run gradle help --task <task>

BUILD SUCCESSFUL

Total time: 4.393 secs
C:\grails\workspace\gradle_with_poi [master]>
```

```
How to run tests

gradle clean
gradle test

see that file Test.xlsx is created

task added to build.gradle to delete the file.
gradle makePretty 
```


















































































































































































































































































































































































































 