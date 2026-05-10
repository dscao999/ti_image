# ti_image
A tool to generate Debian images for TI K3 Jacinto Series SOC

Usage: ./timage. It will prompt for various input to do its job.

1. Select the type of media to generate: A cloned system image or an installation image. The system image can directly boot and run as a Debian 13.4. The installation media can be used to install a Debian 13.4 onto your SOC. The targeted SOC must be able to connect to Internet, without any proxy. DHCP server must be ready as it will try to accquire an IP from DHCP, and to connect to the Debian image server of Tsinghua University, China.

2. If an installation image is to be generated, a target disk on the board to be installed should be given, so that a Debian 13.4 will be installed onto it.

2. Targeted SOC type. Currenty only two types are supported. One for j721e, e.g. J721EXSK/TDA4VM, and the other is j784s4, e.g. J784S4XG01EVM/TDA4VH.

3. It will try to list candidate disks to store the generated image, and will prompt if mutiple disks are usable. It will exit if no candidates exist. Please be noted that this disk is the uSD that is to receive the generated image on the current host. It is not the target disk of the SOC to install, which is specified at step 2 if an installation media is to be generated.

The image generation process will take some time and it depends on the speed of your disk(uSD) to receive the image.
