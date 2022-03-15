 Mediawiki Security Reports
  
  - mediawiki_original_scan : is the "docker scan" for the official image
  
  - trivy_mediawiki.txt : is the "trivy" output for the official image
  
  - trivy_fixed_mediawiki.txt : is the "trivy" output for the hardened image
  
  - mediawiki-docker : Mediawiki directory containing Dockerfile
  
  - php.zip : the hardened image of php 

How to run Dockerfile : 

#go into Edited Dockerfile directory

```$ mediawiki-docker/1.37/apache/```

#build the Docker image

```$ sudo docker build -t imagename:latest . ```

#PS: make sure to run the PHP Dockerfile.

#########################################################################

Mediawiki Download and run :

#Pull the patched mediawiki image : 

```$ sudo docker pull iwdiwd/mediawikipatched:latest```

#Pull the patched php version

```$ sudo docker pull iwdiwd/newphp:latest```

#Docker run the mediawiki patched image

```$ sudo docker run -dit -p 8080:80 iwdiwd/mediawikipatched:latest```
