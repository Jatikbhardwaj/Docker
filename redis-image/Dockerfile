# Use an existing docker image  as a base
FROM alpine

# Download and install a dependency
RUN apk add --update redis

# Tell the image what to do when it starts as a container
CMD ["redis-server"]


# "FROM alpine" :- That told the Docker server or Docker daemon to go and download the Alpine image. And we use the
# Alpine image as a base because it comes pre-installed with some really handy programs that are useful for us creating our image.

# "RUN ":-  the run instruction was executed by the Docker server.
# The first thing that occurred there was it looked for the image from the previous step,
# and so it went back to the previous step and got the Alpine image that had just been downloaded.
# That image was then used to create a brand new very temporary container.
# and then the command that we had specified,so apk add --update redis
# was executed inside of that temporary container.
# The APK program was executed.
# It downloaded and installed Redis inside the file system of that container.
# So the result is a container with a modified file system.
# It now has Redis added onto it.We then took a snapshot of that container's new file system 
# and the result was a file system snapshot.We then shut down the temporary container,

# "CMD ":- We again get the image from the previous step. We again create a temporary container out of it,
# but this time around, rather than executing a command inside there,which is the purpose of the run instruction,
# we instead use the CMD instruction, So we told the temporary container that we just created
# that whenever it gets started in the future,it should try to execute the command redis-server.
# And the result was a container that has a modified primary command.
# We then shut down that temporary container and we got it ready, where you took an image out of it,
# and got it ready for the next instruction.