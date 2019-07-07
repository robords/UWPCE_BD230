1. Go to DockerHub (Links to an external site.) and find an interesting docker project and start it up. Run the hello world of that technology and write about what you thought.

2. Volume map a docker container and write some code against it.  You could, for example, spin up a multi-note Kafka Cluster (Links to an external site.) and add docker exec into it and put messages into  a Topic.  Or you could spin up Kafka and connect it to the Wiki stream and use some KSQL to write data back to put data back to a topic (see tutorial below).  Submit your code and dockerfile for full credit.

***

1. Found: https://hub.docker.com/r/rocker/shiny

   I was particularly interested in seeing if I could run R Shiny Server from Docker, and came across this in Docker Hub.  Getting it to run took just two commands, whereas previously (at work) it took a lot longer for me to get to the basic "hello world" version of this running (essentially getting to the "Welcome to Shiny Server" page).  
   
   I can see the utility in building it this way, but I'd be concerned about using this at work since we have some stringent application security policies regarding using third party tools -> they would much prefer I build something like this from scratch.  I don't think it would be too difficult, however, to create a Dockerfile myself based on what we've gone over in class so far and my experience creating apps from scratch at work.
   
   Even given how easy it may be to do, I'd like to dig further into building apps with docker using different technologies..
