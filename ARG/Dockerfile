## case-1
# ARG version
# FROM almalinux:${version}
# RUN cat /etc/*release
# CMD ["sleep","100"]

# ( cat /etc/os-release )
# only in this case only ARG is first instruction to passing the versions
## ( docker build -t arg:1.0 --build-arg version=8 . ) ---> HERE WE ARE PASSING THE VERSION USING --build-arg


# case-2
# ARG version
# FROM almalinux:${version}
# ARG AUTHOR
# ARG TRAINING
# RUN echo "author is : $AUTHOR ; training is : $TRAINING"
# CMD ["sleep","100"]

# ( docker build -t arg:v1 --build-arg version=9 --build-arg AUTHOR=kithu --build-arg TRAINING=devops . )


# #case-3
# ARG version
# FROM almalinux:${version:-8}
# ARG AUTHOR=Kithu
# ARG TRAINING=Devops
# RUN echo "author is : $AUTHOR ; training is : $TRAINING"
# CMD ["sleep","100"]

## ( FROM almalinux:${version:-8} )---> if user not mention anything printing this default version
# ( docker build -t arg:v1 . ) ---> this command will build with default version 8 and it will print other arguments like Kithu and Devops
# ( docker build -t arg:v1 --build-arg version=9 . ) ---> this will override the version with user recommandation version=9
## ( ARG AUTHOR=Kithu ) --->like this we are passing our default arguments other than version
## (ARG TRAINING=Devops )



#case-4
ARG version
FROM almalinux:${version:-8}
ARG AUTHOR=Kithu
ARG TRAINING=Devops
ARG BOOK=Autobiography
ENV BOOK=${BOOK}
RUN echo "author is : $AUTHOR ; training is : $TRAINING ; book is : ${BOOK}"
CMD ["sleep","100"]


# ARG is accessing in build time only
# ENV is accessing in build time and run time

# ( docker build -t arg:1.0 --build-arg BOOK=LifeLesson . )
# using above command we are passing the arument and accessing in environment variable
# In case-4 ARG BOOK=Autobiography is default value and we are override that value using above command  --build-arg BOOK=LifeLesson then this BOOK=LifeLesson accessing as ENV inside the container
