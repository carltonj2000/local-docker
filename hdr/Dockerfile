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
ENV PATH="/home/carltonj2000/cj/configsNscripts/linux/cjBin:/home/carltonj2000/cj/configsNscripts/go/bin:${PATH}"
