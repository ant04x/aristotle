# Aristotle
 A simple JavaEE using WAS 9 and DB2 z/OS.

 Generating the IDE image.
  ```
  ./projector.sh build --tag aristotle-idea-u:latest --url https://download.jetbrains.com/idea/ideaIU-2021.3.3.tar.gz
  ```
 
 Run the generated
  ```
  docker run --env DEV_MODE=true --rm -p 8887:8887 -v $PWD/idea.txt:/tmp/idea.key -it aristotle-idea-u:latest
  ```

 Tag and publish image
  ```
  docker tag aristotle:latest ant04x/aristotle-idea-u:latest
  docker push ant04x/aristotle-idea-u:latest
  ```