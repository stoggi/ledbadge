# LED Badge

ledbadge is a script to control a B1248 LED Name Badge (http://www.tbdled.com/en/productshow.asp?ID=P385U64S7U)

The USB driver is just a generic Virtual Serial port driver from Prolific PL2303 (VID:067B, PID:2303)

## Dependencies

 * pyserial (2.7)
 * begins (0.9)

## Features

Currently it can only send text and clear the display (by sending an empty string).

## Usage

    $ ledbadge --help
    usage: ledbadge [-h] [-v | -q] [--loglvl {DEBUG,INFO,WARNING,ERROR,CRITICAL}]
                    [--logfile LOGFILE] [--logfmt LOGFMT]
                    [--serial-port SERIAL_PORT]
                    {clear,text} ...

    optional arguments:
      -h, --help            show this help message and exit
      -v, --verbose         Increse logging output
      -q, --quiet           Decrease logging output
      --serial-port SERIAL_PORT, -s SERIAL_PORT
                            (default: /dev/tty.usbserial)

    Available subcommands:
      {clear,text}
        clear               Clear the LED screen
        text                Display text on the LED screen

    logging:
      Detailed control of logging output

      --loglvl {DEBUG,INFO,WARNING,ERROR,CRITICAL}
                            Set explicit log level
      --logfile LOGFILE     Ouput log messages to file
      --logfmt LOGFMT       Log message format

## TODO:

 * Multiple lines of text
 * Set the speed
 * Use icons
 * Send images