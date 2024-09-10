# generate a dockerfile with 3 steps. The image used is the alpine image.
# The first step will copy the content of the folder /tree_code to the /app folder in the image.
# The second step will run the command "npm install" in the /app folder.
# The third step will run the command "npm start" in the /app folder.


# The advantage of this approach is that each step is cached, so if the first step is not changed, it will not be executed again.
# Usually this a great idea when you have a lot of dependencies that are not changed frequently.
FROM alpine as tree_root
# set the tree_type and number_of_leaves environment variables equal to the ones received as arguments
ARG tree_type
ARG number_of_leaves
COPY /tree_code/dependencies.txt /app/dependencies.txt

FROM tree_root as tree_trunk
# change to the /app folder in the image and build the dependencies. A cached image will be used if the dependencies.txt file is not changed.
WORKDIR /app
RUN npm install

FROM tree_trunk
# run the application with the tree_type and number_of_leaves environment variables thus passing the arguments to the application
CMD ["npm", "start", "--tree_type", "${tree_type}", "--number_of_leaves", "${number_of_leaves}"]

