# Command Line
```
curt@curt-Blade-Stealth:~$ docker ps -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                          PORTS               NAMES
a0129ea653e6        neo4j:latest        "/sbin/tini -g -- /d…"   3 hours ago         Exited (0) About a minute ago                       testneo4j
8aa28be04587        neo4j               "/sbin/tini -g -- /d…"   5 days ago          Exited (0) 2 days ago                               boring_meninsky
1ae22cc3c6c8        hello-world         "/hello"                 6 days ago          Exited (0) 6 days ago                               vigilant_pasteur
curt@curt-Blade-Stealth:~$ docker start testneo4j 
```

# In Browser
1. Find the actor named Keanu Reeves and return the data
```
MATCH (keanu{name: "Keanu Reeves"}) RETURN keanu
```

2. Find all the movie Laurence Fishburne acted in.
```
MATCH (laurence:Person {name: "Laurence Fishburne"})-[:ACTED_IN]->(laurenceMovies) RETURN laurence,laurenceMovies
```

3. Given a shortest path search, for example

MATCH p=shortestPath( (bacon:Person {name:"Kevin Bacon"})-[*]-(meg:Person {name:"Meg Ryan"}) ) RETURN p

Find out the shortest path between Keanu Reeves and Meg Ryan.

```
MATCH p=shortestPath( (keanu:Person {name:"Keanu Reeves"})-[*]-(meg:Person {name:"Meg Ryan"}) ) RETURN p
```
