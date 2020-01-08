# Create docker image that gitlab runner will start

docker build -t ubuntu_git --build-arg ssh_prv_key="$(cat .ssh/id_rsa)" --build-arg ssh_pub_key="$(cat .ssh/id_rsa.pub)" .