This is a dockerized version of the EMBL-EBI Ontology Lookup Service that can be found at http://www.ebi.ac.uk/ols/index.

First steps to running are cloning this repository with git and installing docker (https://www.docker.com/).
Edit the obo-config.yaml with your specific ontologies 
Edit ols-config.yaml.sample with your specific ontologies and rename  to ols-config.yaml 
More info on how the configuration file should look, can be found at http://www.ebi.ac.uk/ols/docs/installation-guide under Configurations.

The following commands can be used to build and run the images (Big ontologies can take a lot of time and memory). 
The docker is configured to use 22G of memory. This can be changed in the settings (`MEMORY_USE "-Xmx4g -Xms2g"`). 

  docker build -t ols .
  docker run -d -p 8080:8080 -t ols

The server can than be accessed at {servername}:8080/ols-boot.  







