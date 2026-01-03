## case-1
# ARG version
# FROM almalinux:${version}
# RUN cat /etc/*release
# CMD ["sleep","100"]

# ( cat /etc/os-release )
# only in this case only ARG is first instruction to passing the versions
## ( docker build -t arg:1.0 --build-arg version=8 . ) ---> HERE WE ARE PASSING THE VERSION USING --build-arg


# case-2
ARG version
FROM almalinux:${version}
ARG AUTHOR
ARG TRAINING
CMD ["sleep","100"]