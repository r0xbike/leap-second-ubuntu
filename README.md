# leap-second-ubuntu
Script to audit Ubuntu servers for leap second issues

### Background
On July 1st, 2015 the global atomic clocks will add a Leap Second to align atomic time to solar time. This process was last performed on July 1st, 2012 and caused issues with many linux servers. Since then, there have been updates to the kernel, ntp, and more that should mitigate most problems. This script will help audit Ubuntu servers to verify that there will be no issues with the 2015 leap second.

This script is heavily based on RedHat's Leap Second Issue Detector script. https://access.redhat.com/labs/leapsecond However, RedHat's script only works on RedHat/CentOS. This script works only on Ubuntu and checks for Ubuntu-specific leap second vulnerabilities and resolutions.

### What the Script Does
The script checks for the following:  
* tzdata version 2015a or greater  
* kernel version 3.4 or greater  
* potential ntp issues with -x or 'slew time'

### Compatibility
This script has been tested on the following versions of Ubuntu:
* 12.04
* 13.10
* 14.04

### Additional reading
* Leap second announcement: https://hpiers.obspm.fr/iers/bul/bulc/bulletinc.dat
* RedHat Leap Second audit script: https://access.redhat.com/labs/leapsecond/
* Linux leap second bug report: https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1020285
* Linux 3.4 kernel patch: https://github.com/torvalds/linux/commit/6b43ae8a619d17c4935c3320d2ef9e92bdeed05d
* NTP 4.2.6 slew time bug: http://bugs.ntp.org/show_bug.cgi?id=2745
* Leap second remediation for RedHat: https://access.redhat.com/articles/15145