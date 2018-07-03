FROM ubuntu:xenial-20170417.1
# i believe the above is 16.04.2
RUN apt-get update && apt-get install -y \
  tar \
  curl \
  enfuse \
  pfstools \
  jhead \
  libjasper-dev \
  libjasper-runtime \
  libjpeg62-dev \
  libgtk2.0-dev \
  libgimp2.0-dev \
  libjpeg62-dev \
  libexiv2-dev \
  zlib1g-dev \
  libbz2-dev \
  libgtkimageview-dev \
  libpfs-dev \
  gcc \
  autoconf \
  libtool \
  xcftools
RUN curl -O https://carltonathome.com/data-store/pfscalibration-1.5.tar.gz; \
  tar -xvzf pfscalibration-1.5.tar.gz; cd pfscalibration-1.5; \
  ./configure; make; make install
RUN mkdir -p /home/carltonj2000/cj/configsNscripts
RUN mkdir -p /home/carltonj2000/cj/cj_pics
ENV NVM_DIR /usr/local/nvm
RUN mkdir -p $NVM_DIR
ENV NODE_VERSION 10.3.0
RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash \
    && . $NVM_DIR/nvm.sh \
    && nvm install $NODE_VERSION \
    && nvm alias default $NODE_VERSION \
    && nvm use default
ENV PATH="/home/carltonj2000/cj/configsNscripts/linux/cjBin:/home/carltonj2000/cj/configsNscripts/javascript/scripts:/home/carltonj2000/cj/configsNscripts/go/bin:${PATH}"
