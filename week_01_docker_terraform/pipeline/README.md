Useful command used:
docker build -t test:pandas .

Build a container image from a Dockerfile, call the image test with the tag pandas.
Tag is essentially which version of the image you're building, such as latest.
Do not forget the fullstop - the ".", as this tells docker where the files are it needs.
cd into directory with all the files, then use the dot "."