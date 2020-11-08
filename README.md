# templates
templates in openshift

Commands to create templates 

1) vim gogstmp.yml : create gogstmp.yml using the code given in the file
2) We are using two images in which one is postgresql and another is gogs
3) find DockerImage in that the gogs path is mention in it we have to check if this docker image is available in that path or we have to change the path
4) search for docker gogs image using following command and search for openshift image which is (docker.io/openshiftdemos/gogs)
5) docker search gogs
6) Now change the path of the Gogs in gogstmp.yml
7) Now another postgresql image we are using this imahe from image Stream 
8) check in Image stream using following commands
9)oc get is -n openshift : you will get list of different images from this we are using postgresql image
10) Now check the version using #oc edit is postgresql -n openshift
11) oc create a file
12) oc create -f gogstmp.yml -n openshift : check if the image is find in console or not
13) Now create a Project in console (for example : mypro)
14) Now in command line type  #oc create -f gogstmp.yml -n mypro
15) now to goto console and goto mypro (console login and password is admin)
16) Now search in catlog for gogs
17) Now create it adn check the status as running pods.
18) check the pods are running or not
19) #oc get pods -n mypro
20) now using route get  a link
21) oc get route -n mypro
22) now paste link in address bar 
23) and now get the svc of postgresql
24) #oc get svc :: copy the svc and port in the given field (postgresql ip and port for example 142.25.1.2:5432)
25) now describe the deployment config 
26) oc describe dc postgresql -n mypro
27) put user , password and link in it
28 ) paste the link which we are getting using route.





