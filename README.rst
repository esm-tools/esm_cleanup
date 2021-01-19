==========
DISCLAIMER
==========

ESM_CLEANUP is a tool designed to reduce space blocked by simulations produced using ESM-Tools.
Before continuing, please be aware that automatically removing data from your experiment folders
includes the risk of loosing information that you might need in the future. Though some things
might be relatively safe to remove, other (like restart files) might not.
By continuing, you accept that neither the ESM-Tools developers nor anyone else but yourself 
take the responsibility of what happens to your data. 



==========================
Getting ESM_Cleanup To Run
==========================

License
=======

ESM_Cleanup is licensed under GPLv2, so it is free to download, use and adapt. 

Download
========

ESM_Cleanup is part of the ESM-Tools software family, but independent in the sense that it can be installed 
and used without any reference to the rest of the ESM-Tools. It is hosted together in the esm-tools group at
github.com, and can be downloaded using::
        git clone https://github.com/esm-tools/esm_cleanup.git

That will give you a local subfolder named esm_cleanup containing the latest version of the code.

Installation
============

To install esm_cleanup, change into the esm_cleanup and use pip::
        cd esm_cleanup
        pip install .

That should provide you with an executable called esm_cleanup that is available from any folder of the system.
To check if the installation was successfull, you can type::
        esm_cleanup

which will display the disclaimer above, and you can choose "Let me get out of here" to quit the program by hitting
the enter key.


=====
Usage
=====






