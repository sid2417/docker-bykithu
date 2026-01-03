## using ONBUILD we are creating our own images, we are author of this image
# in this example, this image is using test folder Dockerfile
# this ONBUILD instruction mainly if anyone using thier image, it must recommand few files
# in this case we recommanded ( index.html )

FROM almalinux:9
RUN dnf install nginx -y
RUN rm -rf /usr/share/nginx/html/index.html
ONBUILD COPY index.html /usr/share/nginx/html/index.html
CMD ["nginx", "-g", "daemon off;"]


# ( docker build -t onbuild:v2 . ) 