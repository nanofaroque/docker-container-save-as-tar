# docker-container-save-as-tar
Locally, build docker image and save as tar and distribute


Saving docker images and load

1. List all the images

  `docker images`

2. save the image as tar file

  `docker save demo > demo_save.tar` # demo is the image name which i build by running docker build -t demo .

You can also export the image as a tar file, export will save the changes you made inside the container as well. Look at here: https://sh-tsang.medium.com/docker-tutorial-4-exporting-container-and-saving-image-c3a7d792cfb6

3. Remove the demo images to see the effect

  `docker rmi demo` # rmi means remove images

4. Load the image from tar file

  `sudo docker load < demo_save.tar`

5. Run the image

`docker run -d -p 3000:3000 --name demo demo`


