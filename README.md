comparators
=====================

Library that bundles the LGPL code for Alphanum Algorithm.

The Alphanum Algorithm is an improved sorting algorithm for strings containing numbers.  
Instead of sorting numbers in ASCII order like standard sort, this algorithm sorts numbers in numeric order.
The Alphanum Algorithm is discussed at http://www.davekoelle.com/alphanum.html

### Using Alphanum Algorithm as a library

This project has been published to a Maven repository so it can be used as a library.

For Gradle, your `build.gradle` file should look like:

~~~
...
repositories {
    mavenCentral()
    maven {
        // CUTR SNAPSHOTs
        url "https://github.com/CUTR-at-USF/cutr-mvn-repo/raw/master/snapshots"
    }
    maven {
        // CUTR Releases
        url "https://github.com/CUTR-at-USF/cutr-mvn-repo/raw/master/releases"
    }
}
...

dependencies {
    ...
    compile 'edu.usf.cutr.util:comparators:0.0.1-SNAPSHOT'
}
~~~

Then, you can use the following in your code to reference the class:

~~~
...
import edu.usf.cutr.util.comparators.AlphanumComparator;
...

private static void sortAlphanumericStrings(List<String> items) {

   Collections.sort(items, new AlphanumComparator());
   
   for (String item : items) {
     // Strings are now sorted!
     System.out.println(item);
   }

}
...
~~~

### CUTR Release Process

We've set up a repository to hold the artifacts from this project as a Gihub project - [cutr-mvn-repo](https://github.com/CUTR-at-USF/cutr-mvn-repo).

At CUTR, we should run the following at the command-line to create a new artifact:
~~~
mvn -DaltDeploymentRepository=cutr-snapshots::default::file:"/Git Projects/cutr-mvn-repo/snapshots" clean deploy
~~~

Then commit using Git and push new artifacts to Github.

Note that the "snapshots" in the command-line should be replaced with "releases" for release versions.
