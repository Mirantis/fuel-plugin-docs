# Overview

If you are developing your own plugin for Fuel, you will also need to prepare the documentation set,
which includes Test Plan, Test Report and Plugin Guide.

## How to use

This repo is organized as the doc tree with 2 main folders:
- plugin guide
- testing documentation
  - Test Plan
  - Test Report

To use these doc templates, follow these steps:

1. Clone the repo:

   `git clone https://github.com/irinapovolotskaya/fuel-plugin-docs.git`
  
2. Populate the placeholders of the conf.py files (for Plugin Guide, Test Plan and Report) with plugin-specific information (e.g. document name, plugin release).

3. Populate the content of RST files which make up the document structure.

## How to build documentation

Once you're done with editing the conf.py and sample RST files, you should cd into the corresponding doc dir and
run `make latexpdf`.

For example:
```
cd plugin guide
make latexpdf
```

The PDF will be found in /build subdir.

## Check yourself

Please use the checklists below to make sure you documentation
meets the acceptance criteria.

### Plugin Guide

* The Plugin Guide contains plugin version in <fuel-plugin-name>-XX-XXX-X format.
* The **Overview** section provides information on the following:
  * high-level description of plugin functionality/use case
  * schemes (optional)
* The **Requirements** section provides information on the following:
  * target MOS release (e.g. should be 8.0 not 8.0 and/or higher)
  * required compatible proprietary Partner product version
  * required compatible proprietary hw/software (if applicable)
* The **Prerequisites** section provides information on what should be done prior to the solution installation/configuration, specifically:
  * List of required HW/SW and how to get it (where to order or how to download).
  * Compatible firmware versions (for HW) and software versions (for SW).
  * A link to official documentation and configuration guides of used HW/SH should be provided.
  * How to configure required external hardware/software (e.g. storage devices, switches and so on) so that user could use them via the the application/driver. A simple configuration would be enough.
  * If the solution can use specific HW/SW in several modes, then there should be instructions on how to properly configure the hw/software to use this very mode
* The **Limitations** should outline the issues that might limit the plugin usage. Those can be:
  * specific networking option available for the plugin (e.g. it can only use Neutron VXLAN)
  * known issues that might affect the plugin's operability (e.g. it's impossible to use non-ASCII characters)
* The **Release Notes** section should describe how this plugin version differs from the previous one.
* The **Installing the plugin** section provides commands and estimated output.




