comparators
=====================

Library that bundles the LGPL code for Alphanum Algorithm.

The Alphanum Algorithm is an improved sorting algorithm for strings containing numbers.  
Instead of sorting numbers in ASCII order like standard sort, this algorithm sorts numbers in numeric order.
The Alphanum Algorithm is discussed at http://www.davekoelle.com/alphanum.html

### CUTR Release Process

We've set up a repository to hold the artifacts from this project as a Gihub project - [cutr-mvn-repo](https://github.com/CUTR-at-USF/cutr-mvn-repo).

At CUTR, we should run the following at the command-line to create a new artifact:
~~~
mvn -DaltDeploymentRepository=cutr-snapshots::default::file:"/Git Projects/cutr-mvn-repo/snapshots" clean deploy
~~~

Then commit using Git and push new artifacts to Github.

Note that the "snapshots" in the command-line should be replaced with "releases" for release versions.
