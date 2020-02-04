FROM debian

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install build-essential libncurses5-dev libncursesw5-dev -y

COPY ft_shooter/ ./ft_shooter
WORKDIR ./ft_shooter

RUN make
ENTRYPOINT ./ft_retro

# Thank you Kevin :)
