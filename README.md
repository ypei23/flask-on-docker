This repo set up the docker containers with flask, nginx, guinicorn, postgres, and media files upload and storage featuers. This serves as the back-end of a photo uploading and viewing program like Instagram. 

![Alt text] (s.jpg)  

## Build Instructions  

To build and take up the docker container, run command 

```
$ docker-compose -f docker-compose.prod.yml up -d --build 

$ docker-compose -f docker-compose.prod.yml exec web python manage.py create_db 
```
Then, visit http://localhost:22221/upload to upload your image. 22221 is the port number used in the example. If you want to change the port, please make sure to change the port number through all the files in this repo. 

Finally, you will see the image at http://localhost:22221/media/IMAGE_FILE_NAME.  
