# CS1660FinalProj
Mapreduce. Inverted Index

Link to Demo & Code walk-through: 
https://pitt-my.sharepoint.com/:v:/g/personal/awn10_pitt_edu/EcTZ-_rz_ZVNpYvwa9ZpPkkB-7hJ6obJ3mSiv6EjmVY0Hg

(this is a public link that anyone with a Pitt account can view. I have also added Dr. Farag individually to the permissions)

Docker Image:
https://hub.docker.com/r/awn3/projimage4/tags

Branches:
    1. GUI files in main branch
    2. TopN files in TopN branch
    3. Term Search is in Term Search branch


Steps to run on a different computer:

1. Download docker image. 
    - Docker image is Debian based and includes java 8 (which was the version used in all of my java applications
    - I had issues with the display working correctly. I would try following the medium guide from the first HW. For some reason it was not working on my Macbook
    - The GUI jar contained in the image includes the Google Authentication json file that is used to connect to my cluster. I have turned off the cluster for now because I do not have enough credits to leave it running for a couple weeks. If you email me, I can turn on the cluster for a couple days. 
    - The jar within the image will prompt the user for file inputs and should be in the format of "/textFiles/<book name>.txt"
    -Once the input files are specified, the user selects an action, then enters a search term or N value. 
    - Hit the search button. A log file will pop up that will show the progress of the job and ends with the final results from the request. 
    - There are two sh files (one for wordSearch and one for topN) that take the input from the gui and form commands for the hadoop cluster. These two sh files are the middle-man between the GUI and the GCP cluster. 


Sources:

https://github.com/GoogleCloudPlatform/java-docs-samples/blob/master/compute/cmdline/src/main/java/ComputeEngineSample.java

https://blog.alexellis.io/linux-desktop-on-mac/

https://hadoop.apache.org/docs/current/hadoop-mapreduce-client/hadoop-mapreduce-client-core/MapReduceTutorial.html

http://www-scf.usc.edu/~shin630/Youngmin/files/HadoopInvertedIndexV5.pdf

https://acadgild.com/blog/building-inverted-index-mapreduce

https://medium.com/@mreichelt/how-to-show-x11-windows-within-docker-on-mac-50759f4b65cb
