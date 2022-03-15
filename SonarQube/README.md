  SonarQube Security Reports
  
  - sonarqube_original_scan : is the "docker scan" for the official image
  
  - trivy_sonarqube.txt : is the "trivy" output for the official image
  
  - trivy_fixed_sonarqube.txt : is the "trivy" output for the hardened image 
  
  - Dockerfile : it's the edited dockerfile to run the hardened image 

SonarQube Download and run :

#Run the Hardened SonarQube image :

```$ sudo docker run docker.io/iwdiwd/harden```
