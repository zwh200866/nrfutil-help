# nrfutil-help
nrfutil pkg generate --help
Usage: nrfutil pkg generate [OPTIONS] ZIPFILE

  Generate a zip package for distribution to apps that support Nordic DFU
  OTA. The application, bootloader, and SoftDevice files are converted to
  .bin if supplied as .hex files. For more information on the generated
  package, see: http://developer.nordicsemi.com/nRF5_SDK/doc/

  The following combinations are supported by this command:

  * BL only: Supported.

  * SD only: Supported (SD of same Major Version).

  * APP only: Supported.

  * BL + SD: Supported.

  * BL + APP: Not supported (use two packages instead).

  * BL + SD + APP: Supported.

  * SD + APP: Supported (SD of same Major Version).

Options:
  --debug-mode                    Debug mode switch, enables version check
                                  skipping.
  --application TEXT              The application firmware file.
  --application-version INTEGER   The application version.
  --application-version-string TEXT
                                  The application version string, e.g
                                  "2.7.31".
  --bootloader TEXT               The bootloader firmware file.
  --bootloader-version INTEGER    The bootloader version.
  --hw-version INTEGER            The hardware version.
  --sd-req TEXT                   The SoftDevice requirements. A comma-
                                  separated list of SoftDevice firmware IDs
                                  (1 or more) of which one must be present on
                                  the target device. Each item on the list
                                  must be in hex and prefixed with "0x".A
                                  list of the possible values to use with
                                  this option follows:
                                  |s130_nrf51_1.0.0|0x67|
                                  |s130_nrf51_2.0.0|0x80|
                                  |s132_nrf52_2.0.0|0x81|
                                  |s130_nrf51_2.0.1|0x87|
                                  |s132_nrf52_2.0.1|0x88|
                                  |s132_nrf52_3.0.0|0x8C|
                                  |s132_nrf52_3.1.0|0x91|
                                  |s132_nrf52_4.0.0|0x95|
                                  |s132_nrf52_4.0.2|0x98|
                                  |s132_nrf52_4.0.3|0x99|
                                  |s132_nrf52_4.0.4|0x9E|
                                  |s132_nrf52_5.0.0|0x9D|
  --sd-id TEXT                    The new SoftDevice ID to be used as --sd-
                                  req for the Application update in case the
                                  ZIP contains a SoftDevice and an
                                  Application.
  --softdevice TEXT               The SoftDevice firmware file.
  --key-file PATH                 The private (signing) key in PEM fomat.
                                  [required]
  --help                          Show this message and exit.
