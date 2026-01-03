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


#case-3
ARG version
FROM almalinux:${version:-8}
ARG AUTHOR
ARG TRAINING
RUN echo "author is : $AUTHOR ; training is : $TRAINING"
CMD ["sleep","100"]

## ( FROM almalinux:${version:-8} )---> if user not mention anything printing this default version
