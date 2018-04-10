r-datamaid
==========

[![Travis-CI Build Status](https://www.travis-ci.org/tobiasraabe/r-datamaid.svg?branch=master)](https://www.travis-ci.org/tobiasraabe/r-datamaid)
[![Appveyor Build Status](https://ci.appveyor.com/api/projects/status/g52xmm1wmoyt51ot?svg=true)](https://ci.appveyor.com/project/tobiasraabe/r-datamaid)
[![Anaconda-Server Badge](https://anaconda.org/brimborium/r-datamaid/badges/version.svg)](https://anaconda.org/brimborium/r-datamaid)
[![Anaconda-Server Badge](https://anaconda.org/brimborium/r-datamaid/badges/platforms.svg)](https://anaconda.org/brimborium/r-datamaid)
[![Anaconda-Server Badge](https://anaconda.org/brimborium/r-datamaid/badges/downloads.svg)](https://anaconda.org/brimborium/r-datamaid)

Build ``r-datamaid`` for Linux, macOS and Windows with MRO and upload it to Anaconda.org.

Note that ``mro-base`` is not available on macOS and 32-bit systems. Up to now,
linux 32-bit is not available, but will be added in future.

If you want to know about how to use R with ``conda`` and how to distribute your own
R package, check out this
[blog post](https://tobiasraabe.github.io/blog/distribute_r_conda/).

Installation
------------

Install the package with ``conda`` by typing

    $ conda install -c brimborium r-datamaid

Get template of recipe
----------------------

    $ conda skeleton cran --cran-url https://mran.microsoft.com/snapshot/2018-04-01/ r-datamaid

Select a newer snapshot by changing the snapshot date. Make sure that the
interpreter in ``r-datamaid/meta.yml`` is changed from ``r-base`` to ``mro-base``.
Otherwise, you cannot use the package with ``mro-base`` from ``conda``.

Forking
-------

If you want to know use this template to provide your own R conda package, just fork
this repo, replace the recipe in ``conda-recipe`` and set ``CONDA_UPLOAD_TOKEN`` as
an secret environment variable in Travis-CI and Appveyor containing the API key with
read and write access to your Anaconda.org account.

A detailed overview of the necessary adjustments can be found
[here](https://tobiasraabe.github.io/blog/distribute_r_conda/).

Credits
-------

This repository is a fork of
https://github.com/rmcgibbo/python-appveyor-conda-example.
