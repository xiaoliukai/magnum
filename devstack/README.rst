====================
Devstack Integration
====================

This directory contains the files necessary to integrate Magnum with devstack.

Refer the quickstart guide for more information on using devstack and magnum.

Running devstack with magnum for the first time may take a long time as it
needs to download an atomic fedora 21 qcow image. If you already have this image
you can copy it to /opt/stack/devstack/files/fedora-21-atomic.qcow2 to save you
this time.

To install magnum into devstack, Add this repo as an external repository: ::

     > cat local.conf
     [[local|localrc]]
     enable_plugin magnum https://github.com/openstack/magnum

Run devstack as normal: ::

    cd /opt/stack/devstack
    ./stack.sh
