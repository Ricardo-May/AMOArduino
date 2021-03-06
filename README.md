# Arduino libraries

The following libraries have been split off into unique repositories, owned by @JQIamo. As such, this repository will no longer be maintained/updated. All new code development should take place in the library's individual repository.

## Renaming convention

Each library is split into a new repo, with the name `<LIBRARY>-arduino`. For example, the `AD9954` is now its own repository, `AD9954-arduino`.

Newly developed libraries should be created as their own repository, with the same naming convention. When you clone them to your local machine, you should place them in your `Arduino/libraries` folder, with just the name of the library. Ie, the github repository `AD9954-arduino` should be cloned into the directory `Arduino/libraries/AD9954`.

## Doxygen documentation

Each repository will now host its own Doxygen documentation/project pages.

# OLD INFO

**SEE NEW LIBRARIES FOR LATEST DOCUMENTATION!** The following is kept for historic purposes only.

These are a few arduino libraries we are using at the JQI. Hopefully they are useful to others, too! The idea is
to make it easy to interface with various instruments in the lab (frequency sythesizers, DACs/ADCs, etc).

Some of these libraries are in flux, so your mileage may vary! If you see a bug or would like to contribute, open an
issue or send us a pull request.

For library-specific documentation information, check out the [Doxygen Documentation](http://jqiamo.github.io/AMOArduino). 
There is also lots of good info in the README files for each library.

Send questions to [npisenti] at [umd].

## AD9954

This one is a class to handle SPI/serial communication with an AD9954 DDS chip.
Still in development, but currently supports single-frequency setpoints and bi-directional 
linear ramps, controlled by pin PS0.

## LockFreq

This class handles a voltage input from a frequency lock signal, and updates the corresponding
DDS frequency to track the lock.

## ADF4350

Class to handle SPI/serial communication with the ADF4350 PLL chips (slash eval boards...)

## MyEEPROM

Class to interface with an external EEPROM chip (specifically, 24LC16B). The Arduino Due should be able to utilize part of 
its onboard Flash memory through in-application programming on the SAM3X, but I wasn't able to get that to work. Ultimately, it
seemed easier to just use an external EEPROM chip.

## SimpleLCD

Wrapper class for writing to SparkFun's Serial LCD display: [https://www.sparkfun.com/products/9066](https://www.sparkfun.com/products/9066). NOTE: you want the 3.3V version for the Arduino Due!

## AD536x

Library for working with Analog devices' AD536x family DACs. Should work with { AD5360, AD5361 }  (16 channels, 16/14 bit DAC) and { AD5362, AD5363 } (8 channels, 14/16 bit DAC).
