# KVM development envierment
In this repository, prepared a development envierment 

## Setup KVM
```sh
sudo apt install \
    bridge-utils \
    cpu-checker \
    libvirt-clients \
    libvirt-daemon \
    libvirt-daemon-system \
    libguestfs-tools \
    qemu-system-x86 \
    libxslt-dev \
    libxml2-dev \
    libvirt-dev \
    zlib1g-dev \
    ruby-dev \
    ruby-libvirt \
    ebtables \
    dnsmasq-base \
    uvtool \
    virtiofsd


sudo usermod -aG {USER} libvirt-qemu
sudo usermod -aG libvirt-qemu {USER}

sudo usermod -aG {USER} libvirt
sudo usermod -aG libvirt {USER}
```

## Setup envierment

Before starting the installation, you need to specify the source of the workspace in the template.xml file 
```xml
<source dir="/home/{WORKSPACE}"/>
```

```sh
ansible-playbook environment.yml --extra-vars "envietment_name={development-envietment-name}"
```

## CLI
```sh
uvt-kvm ssh {development-envietment-name}
uvt-kvm ip {development-envietment-name}
```
