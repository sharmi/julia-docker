FROM stackbrew/ubuntu

MAINTAINER Sharmila Gopirajan Sivakumar

RUN sudo apt-get update
RUN sudo apt-get install --yes --force-yes git vim make
RUN sudo apt-get install --yes --force-yes g++ cfortran m4 libncurses5-dev
RUN git clone https://github.com/JuliaLang/julia.git
RUN sudo apt-get install --yes --force-yes curl
RUN cd julia && echo "BUILD_LLVM_CLANG=1" >> Make.user && make -j 4 debug && ln -s usr/bin/julia-readline /usr/bin/julia

ENTRYPOINT ["julia"]



