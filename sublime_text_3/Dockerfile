FROM debian:jessie

ENV DEBIAN_FRONTEND noninteractive


RUN apt-get update && apt-get install -y \
    curl \
    libglib2.0 \
    libx11-6 \
    libgtk2.0 \
    --no-install-recommends

RUN curl http://c758482.r82.cf2.rackcdn.com/sublime-text_build-3065_amd64.deb  > /usr/src/subl3.deb

RUN dpkg -i /usr/src/subl3.deb || true
RUN apt-get install -fy

ENTRYPOINT ["/opt/sublime_text/sublime_text"]
#ENTRYPOINT ["/bin/bash"]
