Introduction
============




.. image:: https://img.shields.io/discord/327254708534116352.svg
    :target: https://adafru.it/discord
    :alt: Discord


.. image:: https://github.com/CedarGroveStudios/Cedargrove_CircuitPython_DRV8830/workflows/Build%20CI/badge.svg
    :target: https://github.com/CedarGroveStudios/Cedargrove_CircuitPython_DRV8830/actions
    :alt: Build Status


.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/psf/black
    :alt: Code Style: Black

A cCircuitPython driver for the DRV8830 DC motor controller.


Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://circuitpython.org/libraries>`_
or individual libraries can be installed using
`circup <https://github.com/adafruit/circup>`_.


Installing to a Connected CircuitPython Device with Circup
==========================================================

Make sure that you have ``circup`` installed in your Python environment.
Install it with the following command if necessary:

.. code-block:: shell

    pip3 install circup

With ``circup`` installed and your CircuitPython device connected use the
following command to install:

.. code-block:: shell

    circup install drv8830

Or the following command to update an existing version:

.. code-block:: shell

    circup update

Usage Example
=============

.. code-block:: python

    import time
    import board
    import cedargrove_drv8830

    # Instantiate motor controller; clear any faults
    motor = cedargrove_drv8830.DRV8830(board.I2C())
    motor.clear_faults()

    motor.throttle = 1.0  # Full speed forward
    time.sleep(1)
    motor.throttle = None  # Coast to a stop

Documentation
=============
`DRV8830 CircuitPython Driver API Class Description <https://github.com/CedarGroveStudios/Cedargrove_CircuitPython_DRV8830/blob/media/pseudo%20readthedocs%20cedargrove_drv8830.pdf>`_


`CedarGrove DRV8830/INA260 FeatherWing <https://oshpark.com/shared_projects/ETZ24BDm>`_

.. image:: https://github.com/CedarGroveStudios/CircuitPython_DRV8830/blob/master/media/Motor_Tester_DRV8830-INA260_Wing_glam.png


`CedarGrove DRV8830/INA271 FeatherWing <https://oshpark.com/shared_projects/L9cZfhJ8>`_

.. image:: https://github.com/CedarGroveStudios/CircuitPython_DRV8830/blob/master/media/Motor_Tester_DRV8830-INA271_Wing_glam.png


Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/CedarGroveStudios/Cedargrove_CircuitPython_DRV8830/blob/HEAD/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.
