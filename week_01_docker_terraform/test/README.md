Useful commands used during the introduction:
- docker ps -a - view all containers
- mkdir test - Make a file directory called test
- cd test - Navigate into the test directory / folder
- docker run -it     --rm     -v "/$(pwd)/test://app/test"     --entrypoint=bash     python:3.9.16-slim
- ls -la - list all files in directory
- cat file1.txt - preview file1.txt (cat is short for concatenate)