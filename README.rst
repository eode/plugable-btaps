Plugable PS-BTAPS1 Library and CLI
==================================

Description
___________
This project is a library and command-line interface for communicating with and programming a `Plugable PS-BTAPS1 Bluetooth Home Automation Switch`_.

libbtaps.py 
    Serves as a Python implementation of the BTAPS protocol, either to be used directly in your programs, or to be used as a reference in developing your own implementation in a different language.
btaps.py 
    A simple command-line UI that implements all the features exposed by libbtaps.py.

::

    USAGE:   python btaps.py [Bluetooth address]
    EXAMPLE: python btaps.py 00:00:FF:FF:00:00

Implemented Functionality
_________________________
The following functions of the Plugable PS-BTAPS1 are currently present in the library:
 - Setting Switch On/Off
 - Reading current status of switch (name, on/off state, timer settings)
 - Creating, modifying and deleting timers
 - Changing the device's name
 - Updating the device's date and time to your PC's current date and time
 
TO DO
_____
The following features and items are still to come:
 - NFControl (Device proximity on/off functionality)
 - Security PIN
 - Better error handling
 - Better documentation
 - Mac OS X support

OS Support
__________
Due to PyBluez limitations, this library will currently only work on Linux and Windows systems.

Dependencies
____________
 - `Python 2.7.x or Python 3.3+`_
 - PyBluez_

Installation
____________
First, install PyBluez using the appropriate link or command for your OS:

**Windows**
    Download and install `PyBluez for Python 2.7`_, or `PyBlues on Windows with Python 3.3+`_

**Ubuntu/Debian**::

For Python 2, there's a system package:
    sudo apt install python-bluez

For Python 3, install dependencies, and use pip:
    sudo apt install libbluetooth-dev
    sudo pip install pybluez

**Fedora**::

    sudo yum install pybluez

**Arch**::

    sudo pacman -S python2-pybluez

Then, simply pip install our module:::

    pip install plugable-btaps

libbtaps Docs and Examples
__________________________
Find some usage examples and documentation for libbtaps in our `GitHub Wiki`_

Troubleshooting
_______________
When I try to pip install plugable-btaps I get a compilation error:
    This means that you have not installed PyBluez and pip is trying to compile PyBluez from source, but you don't have the necessary compilation dependencies installed on your system.
    Install PyBluez as outlined above.

.. _Plugable PS-BTAPS1 Bluetooth Home Automation Switch: http://plugable.com/products/ps-btaps1/
.. _PyBluez: https://code.google.com/p/pybluez/
.. _Python 2.7.x or Python 3.3+: https://www.python.org/
.. _PyBluez for Python 2.7: https://code.google.com/p/pybluez/downloads/detail?name=PyBluez-0.20.win32-py2.7.exe
.. _PyBluez on Windows for Python 3.3+: https://stackoverflow.com/questions/48821917/downloading-and-installing-pybluez-for-a-64-bit-windows-10-pc
.. _GitHub Wiki: https://github.com/bernieplug/plugable-btaps/wiki/libbtaps-Documentation-and-Examples
