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

The usage of esm_clean is easy as you are guided by a user dialogue. It is important to start esm_cleanup in the right way. The
easiest way to launch esm_cleanup is from the folder where you have all your experiments, for example if you have experiments exp1, exp2
and exp3 stored in a folder called my_experiments::

        my_experiments> ls 
        exp1    exp2    exp3

you can start esm_cleanup from either my_experiments::

        cd my_experiments
        esm_cleanup

This is a good choice if you don't know yet which experiment to clean, as it will
display the size of each experiment, so that might give you a hint. If you know already that you want to clean exp2, then it is easier
(and quicker) to start esm_cleanup from my_experiments/exp2::

        cd my_experiments/exp2
        esm_cleanup

A second way of calling esm_cleanup is by giving the experiment folder as a command-line argument, like so::

        esm_cleanup -f my_experiments/exp2

And last but not least, if you are in the folder containg your runscript, and you only remember the experiment id, then you can also 
launch esm_cleanup like this::

        esm_cleanup -r my_runscript.yaml -e experiment_id

This will assemble the experiment folder from the information contained in the runscript. Yes, the option -r is needed, and thus it is different 
from esm_runscripts - as another security measure, so that a user who wants to run esm_cleanup needs to think for a split second about it.

From then on, esm_cleanup will ask you in detail what you want to do, while recommending some options. Some other options might be 
unavailable - like removing the whole restart folder, which we consider to be a stupid idea, and thus don't want to support it. If that
is what you need, do it from the shell.

In most of the steps of the user dialogue you can both quit the program and get back to the main menu. Before something is removed, you
will be asked if that is what you really want. And remember that CTRL-C will get you out of the program in any case. ;-)








