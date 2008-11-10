# Kate Director Project

  forked from a project of Christopher J Bottaro


---


# Installation

## Pate (http://paul.giannaros.org/pate/)

### Requirements

    sudo apt-get install cmake sip4 build-essential python-sip4-dev python-kde3 python-kde3-dev python-qt-dev kate-plugins kdelibs kdelibs4-dev kdebase-dev


### Get Pate

    wget http://paul.giannaros.org/pate/releases/source/pate-0.5.1.tar.gz
    tar zxf pate-0.5.1.tar.gz
    cd pate-0.5.1/
    ./configure
    cd build/
    make && sudo make install


### Activate Pate

Start kate and activate Pate in Settings -> Configure Kate ... -> Application -> Plugins -> Pate


## Install Kate Directory Project

### Get the project

    git clone git://github.com/jorrel/kate_directory_project.git
    cd kate_directory_project
    ./install

### Activate the plugin

Restart kate and make sure the plugin is activated at Settings -> Configure Python Plugins
-> Directory Project


---


# Usage
- Press Ctrl-Shift-O to open a project directory.
- Press Ctrl-H to find files in the project directory.
- Press Shift+F5 to reload/re-scan the project directory.


---


# Personnal Notes (might also apply to you)

## Missing pykdeconfig

pykdeconfig is installed by python-kde3-dev

    $ dpkg -L python-kde3-dev | grep pykdeconfig
   
    /usr/lib/python-2.4/site-packages/pykdeconfig_d.py
    /usr/lib/python-2.4/site-packages/pykdeconfig_nd.py
    /usr/lib/python-2.4/site-packages/pykdeconfig.py
    /usr/lib/python-2.5/site-packages/pykdeconfig_nd.py
    /usr/lib/python-2.5/site-packages/pykdeconfig.py

Thanks to commenters 'jan' and 'oliver'  at Christopher's blog, a workaround is:

    $ cp /usr/lib/python-2.5/site-packages/pykdeconfig* /usr/lib/python2.5/site-packages/ 

