### case-1

# FROM almalinux:9
# RUN mkdir /app
# RUN cd /app
# RUN pwd
# CMD ["sleep","100"]

## in docker entering into the folders using RUN cd /app is not working
## instead of RUN we will use WORKDIR, to enter into the folders


### case-2

FROM almalinux:9
RUN mkdir /app
WORKDIR cd /app
RUN pwd
CMD ["sleep","100"]