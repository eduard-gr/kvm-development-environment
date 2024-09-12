# KVM development envierment
In this repository, prepared a development envierment 



## Setup

Before starting the installation, you need to specify the source of the workspace in the template.xml file <source dir="/home/{WORKSPACE}"/>

ansible-playbook environment.yml --extra-vars "envietment_name={development-envietment-name}"

## CLI
uvt-kvm ssh {development-envietment-name}
uvt-kvm ip {development-envietment-name}
