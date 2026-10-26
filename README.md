# Docker Fundamentals

## Contents:
- Four Task Folders
- Dockerfile present in each folder
- Answers to the resource checklist questions


### Why don’t stopped containers appear with docker ps?
Stopped containers don't appear with docker ps because ps lists running containers only. Every container, in this assignment at least, runs one command and exits immediately, so they’re invisible to ps and only appear under ps -a.

### Why can’t an image be deleted if a container depends on it?
An image can't be deleted if a container depends on it because a container is built on its image’s layers and still references them, so Docker refuses to delete the image and tells you to remove the container first. The general rule of thumb is to always delete the container, then the image.

### What does the --rm flag prevent?
The --rm flag prevents stopped containers from accumulating. It deletes the container the instant it exits, so ps -a stays clean and you don't have to search for random names to remove.