FROM ubuntu:16.04

RUN apt-get update && apt-get install -y unzip
RUN apt-get install -y libxt-dev
RUN apt-get install -y curl 

RUN mkdir /working
RUN curl http://ssd.mathworks.com/supportfiles/downloads/R2018b/deployment_files/R2018b/installers/glnxa64/MCR_R2018b_glnxa64_installer.zip > /working/MCR_R2018b_glnxa64_installer.zip

#ADD MCR_R2018b_glnxa64_installer.zip /working/MCR_R2018b_glnxa64_installer.zip
WORKDIR /working
RUN unzip MCR_R2018b_glnxa64_installer.zip
RUN ./install -mode silent -agreeToLicense yes

ENV LD_LIBRARY_PATH /usr/local/MATLAB/MATLAB_Runtime/v95/runtime/glnxa64:/usr/local/MATLAB/MATLAB_Runtime/v95/bin/glnxa64:/usr/local/MATLAB/MATLAB_Runtime/v95/sys/os/glnxa64:/usr/local/MATLAB/MATLAB_Runtime/v95/extern/bin/glnxa64

