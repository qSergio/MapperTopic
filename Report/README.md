To run docker container first build the image:

$ docker build -t some_tag .

and then run the container:

$ docker run -p 8888:8888 -v /Users/username/path_to_this_working_directory:/home/jovyan/work some_tag

* Average: Building 567.0s (11/11) FINISHED