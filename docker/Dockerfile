FROM debian:latest

RUN apt-get update && apt-get upgrade -y
RUN apt-get install git wget bzip2 -y

WORKDIR app/
# RUN git clone https://github.com/llvm-mirror/llvm.git
RUN wget https://ftpmirror.gnu.org/binutils/binutils-2.30.tar.gz
RUN wget https://ftpmirror.gnu.org/gcc/gcc-8.1.0/gcc-8.1.0.tar.gz
RUN wget https://ftpmirror.gnu.org/mpfr/mpfr-4.0.1.tar.gz
RUN wget https://ftpmirror.gnu.org/gmp/gmp-6.1.2.tar.bz2
RUN wget https://ftpmirror.gnu.org/mpc/mpc-1.1.0.tar.gz
RUN wget https://gcc.gnu.org/pub/gcc/infrastructure/isl-0.18.tar.bz2  
RUN wget https://gcc.gnu.org/pub/gcc/infrastructure/cloog-0.18.1.tar.gz
RUN for i in *.tar.gz; do tar -xzf $i; done
RUN for i in *.tar.bz2; do tar -xjf $i; done
RUN rm -f *.tar.*