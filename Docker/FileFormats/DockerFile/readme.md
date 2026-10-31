# Instruction/commands supported by Dockerfile:-
- ADD = Add local or remote files or directories
- ARG = Use build-time variables
- CMD = Specify default commands
- Copy = copy files or directories 
- Entrypoint = specify default executable
- ENV = set environment variables
- EXPOSE = Describe which ports your application is listening on
- FROM = create a new build stage from a base image
- HEALTHCARE = check a container's health on startup
- LABEL = Add metadate to an image
- MAINTAINER = specify the author of an image
- ONBUILD = specify instructions for when the image is used in a build
- RUN = Execute build commands
- SHELL = set the default shell of an image
- STOPSIGNAL = specify the system call signal for exiting a container
- USER = set user and group ID
- VOLUME = create volume mounts
- WORKDIR = change working directory

# Format
A DockerFile must begin with a From instruction.IT specifies the base image from which yoy are building.

**Base image:-**
A base image is an image you designate in a FROM directive in a Dockerfile. It defines the starting point for your build. 
**ARG:-**
specify build time variables
The ARG declares a variable that Docker can use in the FROM instruction.
    **example**
    ARG IMAGE=ubuntu
    ARG VERSION=22.04
    FROM ${IMAGE}:${VERSION}

Buildkit treats line that begin with # as a comment unless the line is valid in parser directive,otherwise it will be treated as an argument in a line.

## Parser Directives
- They are special comments written at the start of Dockerfile.They tell docker how to process dockerfile
syntax:-- # directive=value
       **example**
       # syntax=docker/dockerfile:1
            FROM ubuntu:22.04
            RUN echo "Hello World"

            {Syntax=docker/dockerfile:1 tells Docker which Dockerfile syntax/frontend version to use.
            FROM selects the base image.
            RUN executes a command.}

- They are optional,and affect the way in which subsequent lines in a Dockerfile are handled.
- They dont add layers to the build,and dont show up as build steps

### Types of Parser Directives:-
1. Syntax 
Specifies which Dockerfile frontend (syntax implementation) should be used to interpret the Dockerfile.
{
    # syntax=docker/dockerfile:1
    FROM ubuntu:22.04
    RUN echo "Hello"
}
Here, this is telling which version of dockerfile instruction language to use

2. Escape
Changes the escape character used in the Dockerfile.
By default, Docker uses a backslash (\).
{
    # escape=`
    FROM microsoft/nanoserver
    COPY test.txt C:\
    RUN dir C:\
}
Here backtick(`) is used instead of backslash as the escape character.This is particularly useful when writng dockerfiles for windows because windows path commonly contain backslash.

3. Check
Use to configure dockerfile build check
{
    # check=skip=JSONArgsRecommended
    FROM ubuntu:22.04
    RUN echo "Hello"
}
This tells Docker to skip the JSONArgsRecommended build check.
Build checks help identify potential issues and bad practices in Dockerfiles.

## Comment Vs ParserDirectives
1. ordinary comment
        # This Dockerfile uses Ubuntu
        FROM ubuntu:22.04

2. ParserDirectives
        # check=skip=JSONArgsRecommended
        FROM ubuntu:22.04
        RUN echo "Hello"

# Envirnoment Replacement
- It means using variable inside dockerfile instruction and replacing those variable with their assigned values.
- Declared using ENV statement
- They are notated in the Dockerfile either with  $variable_name or ${variable_name}


{
    FROM ubuntu:22.04
    ENV NAME=Yash
    RUN echo $NAME || RUN echo ${name}

    1. FROM ubuntu:22.04 selects Ubuntu as the base image.
    2.ENV NAME=Yash creates an environment variable called NAME.
    3.RUN echo $NAME uses that variable.
    4.Docker replaces $NAME with Yash.

    **output = YASH***
}
