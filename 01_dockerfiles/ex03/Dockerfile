FROM debian:9

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y ca-certificates openssh-server wget postfix

RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && chmod +x script.deb.sh && ./script.deb.sh && apt-get install -y gitlab-ce

RUN apt update && apt install -y tzdata
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 443 80 22

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && tail -f /dev/null

# VBoxManage modifyvm Char --cpus 2
# VBoxManage modifyvm Char --memory 4096

# For this exercise, we made a container that runs some image. I heard people
# saying that this repo is really fat and takes 30mins. So, my colleague helped
# me out of how to "speed it up" and is by setting up the CPU and memory usage
# mentioned above
