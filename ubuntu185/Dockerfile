FROM alpine as BUILDER
ARG IMG_URL="https://cloud-images.ubuntu.com/bionic/current/bionic-server-cloudimg-amd64.img"

RUN wget $IMG_URL -O ubuntu.qcow2
# ubuntu publish the qcow2 images as .img -.-
FROM scratch
copy  --from=BUILDER /ubuntu.qcow2 /disk/
