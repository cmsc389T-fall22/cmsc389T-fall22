# Project 6 Base Image

The files included in this directory allow you to create a docker image with python and twilio preinstalled. You should put this in the root of your repository and rebuild the image if you edit your hooks file. 

You can create an image by running

```
docker build -t project6 .
```

When you want to run this image and connect to its container, just run

```
docker run -it project6 bash
```

Once you are inside the container, you can test your hook by doing a quick test commit. An example is provided below:

```
touch test.txt
git add test.txt
git commit -m "test hook"
```
