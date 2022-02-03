FROM quay.io/pypa/manylinux2010_x86_64:latest
RUN AUDITWHEEL_PATH=$(auditwheel --version | awk 'NR==2{ print $1 }') && \
    sed -i 's/libresolv.so.2"/libresolv.so.2", "libtensorflow_framework.so.2"/g' ${AUDITWHEEL_PATH}/policy/manylinux-policy.json

CMD ["/bin/bash"]

