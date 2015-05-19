# meta-tnd

meta-tnd is a repository to hold a range of [Yocto project's](https://www.yoctoproject.org)    build configuration files for a number of build projects contained within a common build environment.

It is used in conjunction with [repo](https://code.google.com/p/git-repo), a tool for the management of multiple [git](www.git-scm.com) repositories.

See [Installing Repo](http://source.android.com/source/downloading.html#installing-repo) for the details on how to set Repo up for one's own projects.

Also see [here](http://source.android.com/source/developing.html) for more details on the use of Repo.

##CONFIGURATIONS##

The current configurations are as follows.

    Altera/
        sockit/
            conf/
                bblayers.conf
                local.conf
                local.conf.sample
                template.cfg

    Freescale/
        wandboard-quad/
            conf/
                bblayers.conf
                local.conf
                local.conf.sample
                template.cfg

    Raspberrypi/
        model-b+/
            conf/
                bblayers.conf
                local.conf
                local.conf.sample
                template.cfg

    Xilinx/
        parallella/
            conf/
                bblayers.conf
                local.conf
                local.conf.sample
                template.cfg

Repo installs the above structure such that the Yocto build environment is as follows:

    yocto/
        builds/
            Altera/              holds the different Altera builds        ie sockit etc
            Freescale/           holds the different Freescale builds     ie wandboard-quad etc
            Raspberrypi/         holds the different Raspberrypi builds   ie model-b+ etc
            Xilinx/              holds the different Xilinx builds        ie parallella etc
        sources/                 holds poky, met-layers and recipes
        tarballs/                holds already downloaded tarballs. Speeds up subsequent builds
        .repo                    Git stuff
        README                   Readme file
        setup-environment        Sources script for initialising a build environment.

##Adding more Configurations##

Additional Configurations can be added as required in the appropriate places in the above structure.

      