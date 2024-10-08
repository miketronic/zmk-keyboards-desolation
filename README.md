# Desolation ZMK Module

This repository contains the shield files for [Desolation](https://github.com/miketronic/desolation) to allow users to build firmware. This can be done by adding the module to the west.yml found in your zmk-config's config directory. There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

# Usage

Edit your west.yml file found in your zmk-config's config directory to add the Desolation module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: caksoylar
      url-base: https://github.com/caksoylar
    - name: miketronic
      url-base: https://github.com/miketronic
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-rgbled-widget
      remote: caksoylar
      revision: main
    - name: zmk-keyboards-desolation
      remote: miketronic
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.

# Notes
Big thanks to @grassfedreeve for letting me copy his excellent readme for this, and to @nick-munnich for convincing me that modules are the best way 😃
