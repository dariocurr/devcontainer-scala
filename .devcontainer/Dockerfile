# for format details, see https://docs.docker.com/engine/reference/builder/

# select image
ARG SCALA_VERSION="8u312_1.5.5_2.12.15"
FROM hseeberger/scala-sbt:${SCALA_VERSION}
LABEL author="dariocurr@gmail.com" maintainer="dariocurr@gmail.com" version="0.0.1"

# create vscode user
RUN groupadd --gid 1000 vscode \
	&& useradd --uid 1000 --gid 1000 -m vscode \
	&& apt update \
	&& apt upgrade -y \
	&& apt install -y sudo \
	&& echo vscode ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/vscode \
	&& chmod 0440 /etc/sudoers.d/vscode

# install zsh
RUN apt install zsh -y

# install ohmyzsh
USER vscode
RUN sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
COPY .devcontainer/.zshrc .
