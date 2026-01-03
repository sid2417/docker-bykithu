## case:1
#FROM almalinux:9
#CMD ["ping","-c5","google.com"]

# ( docker run entrypoint:1.0 ping -c5 yahoo.com )
# using this above command the CMD command is override


## case:2
FROM almalinux:9
ENTRYPOINT ["ping","-c5","google.com"]
# ( docker run entrypoint:1.0 ping -c5 yahoo.com )
# using this above command the ENTRYPOINT command is NOT override, you will get error

## case:3
FROM almalinux:9
CMD ["google.com"]  
ENTRYPOINT ["ping","-c5"]

# for better results we mix CMD and ENTRYPOINT 
# here CMD is passing default arguments
# and ENTRYPOINT is act as a command
#  
