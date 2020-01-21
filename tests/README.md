# Testing examples

Examples are tested using tool [htrun](https://github.com/ARMmbed/mbed-os-tools/tree/master/packages/mbed-host-tests) and templated print log. 

To run the test, use the following command after you build the example:
```bash
$ mbedhtrun -d <MOUNT_POINT> -p <SERIAL_PORT> -m <TARGET> -f ./BUILD/<TARGET>/<TOOLCHAIN>/mbed-os-example-sys-info.bin --compare-log tests/sys-info.log
```
For example:
```bash
$ mbedhtrun -d /media/user01/DAPLINK -p /dev/ttyACM0 -m K64F -f ./BUILD/K64F/GCC_ARM/mbed-os-example-sys-info.bin --compare-log tests/sys-info.log
```

More details about `htrun` are [here](https://github.com/ARMmbed/htrun#testing-mbed-os-examples).