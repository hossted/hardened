 Mediawiki Security Reports
  
  - mediawiki_original_scan : is the "docker scan" for the official image
  
  - trivy_mediawiki.txt : is the "trivy" output for the official image
  
  - trivy_fixed_mediawiki.txt : is the "trivy" output for the hardened image **in progress**

Mediawiki Download and run :

$ sudo docker pull iwdiwd/mediawikipatched:latest
```$ sudo docker pull iwdiwd/newphp:latest```
$ sudo docker run -dit -p 8080:80 iwdiwd/mediawikipatched:latest
