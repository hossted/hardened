  Wordpress Security Reports
  
  - wordpress_original_scan : is the "docker scan" for the official image
  
  - trivy_wordpress.txt : is the "trivy" output for the official image
  
  - trivy_fixed_wordpress.txt : is the "trivy" output for the hardened image 

Wordpress Download and run :

#Pull the patched wordpress image : 

```$ sudo docker pull iwdiwd/wordpressharden:latest```

#Pull the patched php version

```$ sudo docker pull iwdiwd/newphp:latest```

#Docker run the wordpress patched image

```$ sudo docker run -dit -p 8080:80 iwdiwd/wordpressharden:latest```
