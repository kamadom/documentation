.. _tor-mac:

********************
Running Tor on MacOS
********************

Install Homebrew
================

For macOS running on ARM chips (ie. newer macs):
------------------------------------------------

.. warning:: macOS Homebrew running natively on M1/Apple Silicon/ARM has partial functionality. Therefore, some additional steps are needed to setup Homebrew.

#. Open a command line editor (Terminal), and run the following commands:

    .. code-block::

        softwareupdate --install-rosetta
        arch -x86_64 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

For macOS Big Sur/Catalina:
---------------------------

1. If you do not have Homebrew installed, follow the installation instructions `here <https://brew.sh/>`_.

    TLDR: Open the command line editor (Terminal) and paste the following line:

    .. code-block::

        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

2. You will be prompted for your system password before installation; proceed with entering your password:

.. figure:: /_static/images/tor/install_homebrew.png
    :width: 80%
    :alt: Homebrew installation

    Enter your password

3. You will be notified which directories Homebrew is going to create, hit :code:`RETURN`:

.. figure:: /_static/images/tor/install_homebrew1.png
    :width: 80%
    :alt: Homebrew installation

Homebrew creates the directories and downloads any other files it needs e.g. “Command Line Tool for Xcode” and “Homebrew”.

Wait a few minutes while it downloads and installs what it needs.

.. warning:: Surprisingly, Homebrew uses Google Analytics to collect anonymous usage data. You can deselect the option to share usage data by `opting out <https://docs.brew.sh/Analytics#opting-out>`_.

Install Tor
===========

.. warning:: If you have the Tor Browser open, close it and quit the application.

For macOS with ARM chips
------------------------

In the command line type:

    .. code-block::

        arch -x86_64 brew install tor

For macOS Big Sur/Catalina:
---------------------------

In the command line type:

    .. code-block::

        brew install tor


See the `Tor Project <https://2019.www.torproject.org/docs/tor-doc-osx.html.en>`_ for more details.

Once it is finished you have the following options:

.. figure:: /_static/images/tor/install_tor.png
    :width: 80%
    :alt: Tor installation

    Install Tor

In the command line type

.. code-block::

    brew services start tor

or

.. code-block::

    arch -x86_64 brew services start tor

depending on your device (as explained above). This will start Tor and ensure that it is always running, even after a restart.
