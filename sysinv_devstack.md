
# Sysinv Devstack summary

## Done

* Code Structure is done
* has run successfully on one devstack vm (centos 7.5)
* si-api(sysinv-api) and si-cond(sysinv-conductor) can run successfully

## Limitation or Issue

* some db migrate code need to adapt. Devstack is using **mysql**, String must have length and String length Max is 255.
* There are several dependence python package need to install
  * tsconfig
  * configutilities
  * controllerconfig
  * fm_api
  * stx_utils
* si-cond process must be trigged in phase test-config , otherwise it will fail.
* sysinv-api port is same as ironic port 6385
  
## ToDo

* ubuntu devstack enviroment test
* test-config setup and basic functional test
* fix "Limitation or Issue" and upload official patch
