
# Sysinv Devstack summary

## Done

* Code Structure is done
* has run successfully on one devstack vm (centos 7.5)
* si-api(sysinv-api) and si-cond(sysinv-conductor) can run successfully

## Limitation or Issue

* some db migrate code need to adapt. Devstack is using **mysql**, String must have length and String length Max is 255.
* There are several dependence other starlingx python packages need to install, and these python packages do not have setup.cfg files, only support setuptools install, can not use 'pip install -e'.
  * [tsconfig](http://git.openstack.org/cgit/openstack/stx-update/tree/tsconfigstx-update/tsconfig/tsconfig)
  * [configigutilities](https://git.openstack.org/cgit/openstack/stx-config/tree/configutilities)
  * [controllerconfig](https://git.openstack.org/cgit/openstack/stx-config/tree/controllerconfig)
  * [fm_api](https://git.openstack.org/cgit/openstack/stx-fault/tree/fm-api)
  * [platform-util](https://git.openstack.org/cgit/openstack/stx-utils/tree/middleware/util/recipes-common/platform-util/platform-util)
* si-cond process must be trigged in phase test-config , otherwise it will fail.
* sysinv-api port is same as ironic port 6385
* in ubuntu devstack enviroment, si-cond(sysinv-conductor) can not started, the database sysinv is always empty

## ToDo

* fix "Limitation or Issue" and upload official patch
* ubuntu devstack enviroment test
* test-config setup and basic functional test
