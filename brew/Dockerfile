FROM ubuntu

RUN apt-get update && apt-get install --yes gcc curl git

RUN /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

RUN echo "eval \$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)" >>~/.bashrc

