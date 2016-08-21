FROM heroku/cedar:14
MAINTAINER ademar

RUN apt-key adv --keyserver pgp.mit.edu --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF

RUN echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/4.0.0 main" > /etc/apt/sources.list.d/mono-xamarin.list \
    && apt-get update \
    && apt-get install -y mono-devel ca-certificates-mono mono-vbnc \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get -q update
RUN apt-get -q -y install curl gcc g++ make wget unzip git autoconf pkg-config libtool automake build-essential mono-devel gettext


COPY build build
CMD ./build
