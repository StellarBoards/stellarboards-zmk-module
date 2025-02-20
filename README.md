# StellarBoards ZMK Module

This repository contains the board files for the [Kasasagi](https://github.com/StellarBoards/Kasasagi/) to allow users to build firmware. 
This can be done by adding the module to the west.yml found in your zmk-config's config directory. 
There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the StellarBoards module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: stellarboards
      url-base: https://github.com/stellarboards
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: stellarboards
      remote: stellarboards-zmk-module
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.

## More Info

For more info on modules, you can read through  through the [Zephyr modules page](https://docs.zephyrproject.org/3.5.0/develop/modules.html). [Zephyr's west manifest page](https://docs.zephyrproject.org/3.5.0/develop/west/manifest.html#west-manifests) may also be of use.
