FROM harbor.vcloud.nii.ac.jp/vcp/tljh:20230327

RUN apt-get update && apt-get install -y gpg-agent

RUN distribution=$(. /etc/os-release;echo $ID$VERSION_ID) \
   && curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | APT_KEY_DONT_WARN_ON_DANGEROUS_USAGE=1 apt-key add - \
   && curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list |  tee /etc/apt/sources.list.d/nvidia-docker.list \
&& apt-get update \
&& apt-get install -y nvidia-container-runtime nvidia-docker2 nvidia-utils-525

#----------
# NVIDIA GPU Prometheus Exporter
ENV GO_VERSION 1.13
RUN curl https://dl.google.com/go/go${GO_VERSION}.linux-amd64.tar.gz > go.tar.gz \
    && tar zxf go.tar.gz -C /usr/local \
    && rm go.tar.gz
RUN /usr/local/go/bin/go get github.com/mindprince/nvidia_gpu_prometheus_exporter
RUN mv "$HOME/go/bin/nvidia_gpu_prometheus_exporter" /usr/local/bin/

#RUN /opt/tljh/hub/bin/python3 /opt/tljh/src/bootstrap/bootstrap.py --admin admin-user01:admin-user01

#RUN /opt/tljh/user/bin/pip3 install torch numpy matplotlib
COPY gpu_exporter.service /etc/systemd/system/
RUN systemctl enable gpu_exporter
#RUN /opt/tljh/user/bin/pip3 install torchvision
