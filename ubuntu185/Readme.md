## Creating image:

we need:

apt-get install qemu-guest-agent


qemu-img create -f qcow2 /tmp/centos.qcow2 10G


virt-install --virt-type kvm --name ubuntu --ram 1024 \
  --disk ./centos.qcow2,format=qcow2,size=10 \
  --network network=default \
  --graphics vnc,listen=0.0.0.0 --noautoconsole \
  --os-type=linux --os-variant=Ubuntu18 \
  --location=./orig-bionic-server-cloudimg-amd64.qcow2



# another approach

qemu-img convert -f qcow2 orig-bionic-server-cloudimg-amd64.qcow2 -O vdi orig-bionic-server-cloudimg-amd64.vdi
