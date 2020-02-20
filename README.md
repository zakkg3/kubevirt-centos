# kubevirt-images


## usage

cd into the folder of the image and then 

```
make build
```




## Centos 7 kubevirt image

TO-DO: do the 2 stage build on the dockerfile and make the Makefile.


download https://cloud.centos.org/centos/7/images/CentOS-7-x86_64-GenericCloud.qcow2

then 
docker build . -t zakkg3/kubevirt-centos:latest
docker push zakkg3/kubevirt-centos:latest
