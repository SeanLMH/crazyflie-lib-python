# cflib: Crazyflie python library [![CI](https://github.com/bitcraze/crazyflie-lib-python/workflows/CI/badge.svg)](https://github.com/bitcraze/crazyflie-lib-python/actions)

cflib is an API written in Python that is used to communicate with the Crazyflie
and Crazyflie 2.0 quadcopters. It is intended to be used by client software to
communicate with and control a Crazyflie quadcopter. For instance the [Crazyflie PC client](https://www.github.com/bitcraze/crazyflie-clients-python)  uses the cflib.

See [below](#platform-notes) for platform specific instruction.
For more info see our [documentation](https://www.bitcraze.io/documentation/repository/crazyflie-lib-python/master/).

## Installation
See the [installation instructions](docs/installation/install.md) in the github docs folder.

## Official Documentation

Check out the [Bitcraze crazyflie-lib-python documentation](https://www.bitcraze.io/documentation/repository/crazyflie-lib-python/master/) on our website.

## Contribute

Everyone is encouraged to contribute to the CrazyFlie library by forking the Github repository and making a pull request or opening an issue.

## Changes from Upstream
This fork introduces a custom CRTP packet which allows users to directly control motor PWMs. Although similar to the param.set_value function, this custom function allows for all 4 motors to be set in one go instead of through 4 separate calls to param.set_value which in turn reduces latency. This will only work if the custom firmware <insert link to forked firmware repo> is used.
