FROM tensorflow/serving:1.7.1-devel-gpu

COPY pkg /root/
RUN     apt-get clean && \
        apt-get update && \
        apt-get install python -y python-setuptools && \
        easy_install pip && \
        pip install -r /root/pkg && \
        rm -rf /root/.cache/pip/ && \
        find /var/cache/apt/archives/ -type f -delete
