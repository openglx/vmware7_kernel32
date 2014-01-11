vmware7_kernel32
================

Patch to have VMware Workstation 7 on kernel 3.2.x

This repository is a compilation from original work by VMware Inc. plus individual patches by
Artem S. Tashkinov and Stefano Angeleri (weltall).

Just pushed to github in order to stop having to scatter around trying to find the right patch, maybe keeping track for
future revisions?


Whilst there are COPYING files with a verbatim of GPL2 license for each of those directories please note you will use
them at your own peril.

NO WARANTY - USE AT YOUR OWN RISK.

Works for me, running VMware Workstation 7.1.6 on Debian 7.2 (kernel 3.2.0-4-amd64).

How to get it running:

git clone git@github.com:openglx/vmware7_kernel32.git
cd vmware7_kernel32
for i in v* ; do tar cf $(echo $i | sed s/-only//g).tar $i ; done
# backup original files at /usr/lib/vmware/modules/source
cp -a /usr/lib/vmware/modules/source /usr/lib/vmware/modules/source_backup
# overwrite
cp -a *tar /usr/lib/vmware/modules/source


Then you should be able to compile the kernel modules correctly.



