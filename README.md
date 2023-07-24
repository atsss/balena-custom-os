This is a test purpose directory for a [custom BalenaOS](https://docs.balena.io/reference/OS/customer-board-support/).
This is originally forked from the [template](https://github.com/balena-os/balena-board-template).

## Build information

### Build flags

* Consult layers/meta-balena/README.md for info on various build flags (setting
up serial console support for example) and build prerequisites. Build flags can
be set by using the build script (barys) or by manually modifying `local.conf`.

See below for using the build script.

### Build this repository

* Run the build script:
  `./balena-yocto-scripts/build/barys`

* You can also run barys with the -h switch to inspect the available options

### Custom build using this repository

* Run the build script in dry run mode to setup an empty `build` directory
    `./balena-yocto-scripts/build/barys --remove-build --dry-run`

* Edit the `local.conf` in the `build/conf` directory

* Prepare build's shell environment
    `source layers/poky/oe-init-build-env`

* Run bitbake (see message outputted when you sourced above for examples)

## Family board layer
* Copy [balena-raspberrypi/layers/meta-balena-raspberrypi](https://github.com/balena-os/balena-raspberrypi/tree/master/layers/meta-balena-raspberrypi) layer
