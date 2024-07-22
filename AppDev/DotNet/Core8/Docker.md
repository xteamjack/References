Create a docker image for .Net Web Services app

1. Configure Application
   1. 
2. Create docker file
3. Build Image
4. Run Image

Note:

- Careful with docker context
  - Docker files run the context of the directory from where the docker build command runs.
  - COPY or ADD commands in the dockerfile cannot contain ..
  - In case to reference a path from parent directory, better run docker from highest possible directory based on the files to be referenced
  - use -f <dockerfile> to reference the docker file at respective path
  - eg., folders contain /root/docker /root/src
    - so docker/dockerfile cannot reference ../src. Instead run at root and reference the docker as -f docker/dockerfile
- By default, docker expects dockerfile, to place more than one use -f <dockerfile>