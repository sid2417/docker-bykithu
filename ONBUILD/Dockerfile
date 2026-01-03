## using ONBUILD we are creating our own images, we are author of this image
# in this example, this image is using test folder Dockerfile
# this ONBUILD instruction mainly if anyone using thier image, it must recommand few files
# in this case we recommanded ( index.html )

FROM almalinux:9
RUN dnf install nginx -y
RUN rm -rf /usr/share/nginx/html/index.html
ONBUILD COPY index.html /usr/share/nginx/html/index.html
CMD ["nginx", "-g", "daemon off;"]


# ( docker build -t onbuild:v2 . ) ---> using this command first we will create images using ONBUILD Dockerfile
 
# these below two commands executes in test folder Dockerfile ( onbuild-test:v2  )
# ( docker build -t onbuild-test:v2 . ) --> this will run in test folder 
# ( docker run -d -p 80:80 onbuild-test:v2 )