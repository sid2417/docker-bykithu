FROM almalinux:9
RUN adduser morrisons
USER morrisons
CMD ["sleep","100"]

# using this USER intruction we will restrict the root access of the containers
# atleast before CMD command we will give the permission to the user
## once you set the normal user you will not get any sudo access, even you are using sudo su -
    
