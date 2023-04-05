AutoSteper
==========

Automated Stepwise Addition Procedure for Extrafullerene.

A detailed description could be found in the article: Exploring
exohedral functionalization of fullerene with Automation and Neural
Network Potential.

.. raw:: html

   <html xmlns="http://www.w3.org/1999/xhtml"><head></head><body><center>Overview of the Stepwise model.</center></body></html>

Demonstration of core functions could be found in ``./tests``.

Documentation could be found in ``./doc``.

Install
-------

For users
---------

Autosteper has an dependency on multiple python packages, namely, the
importlib-metadata, ase, numpy, pandas, networkx, tqdm, matplotlib,
seaborn, and dpdispatcher. Installation of all of them along with this
project has been integrated into a single command line:

.. code:: 

   pip install autosteper

Besides, Autosteper relies on open source project
`FullereneDataParser <https://github.com/XJTU-ICP/FullereneDataParser>`__
to convert 3D coordinates to graph6str format and properly visualize
isomers, pathways, and SWR pairs.
`FullereneDataParser <https://github.com/XJTU-ICP/FullereneDataParser>`__
has not been published on Pypi. According to `Pypi
policy <https://setuptools.pypa.io/en/latest/userguide/dependency_management.html#direct-url-dependencies>`__,
the unpublished project **could not** be used as a dependency for the
published package. Therefore, it needs to be installed separately:

.. code:: 

   pip install git+https://github.com/XJTU-ICP/FullereneDataParser


--------------

📝 Note

`FullereneDataParser <https://github.com/XJTU-ICP/FullereneDataParser>`__
contains part of C++ code, to properly install, an advanced compiler
version is required. Simply load the highest available version of
compiler will avoid most of the problems.

--------------


.. note::

   This project is under active development.



.. tip::

   This project is under active development.



.. warnning::

   This project is under active development.



see

.. figure:: ./docs/test/fig/addon.png
   :alt: 


Note:
`FullereneDataParser <https://github.com/XJTU-ICP/FullereneDataParser>`__
contains part of C++ code, to properly install, an advanced compiler
version is required. Simply load the highest available version of
compiler will avoid most of the problems. See below.

Finally, the in-house built C++ project
`usenauty <https://github.com/Franklalalala/usenauty>`__ needs to be
collected. `usenauty <https://github.com/Franklalalala/usenauty>`__ is a
lightweight tool to enumerate non-isomorphic addition patterns with
`nauty <https://doi.org/10.1016/j.cpc.2020.107206>`__ algorithm which is
created by Brendan D. McKay. The original modification is performed in
`usenauty <https://github.com/saltball/usenauty>`__ by XJTU-ICP member
Y. B. Han. Here we employ a branch version of it.

Unlike previously mentioned packages, the installation of
`usenauty <https://github.com/Franklalalala/usenauty>`__ is different
for Linux and Windows. **There are two pre-compiled** releases for two
platforms, users are encouraged to
`download <https://github.com/Franklalalala/usenauty/releases>`__ the
corresponding releases.

For example, linux users could download the gcc-8.4.0 version with
command line as below:

.. code:: 

   wget https://github.com/Franklalalala/usenauty/releases/download/linux/cagesearch

After downloading, users need to assign execution permissions and load a
gcc environment:

.. code:: 

   chmod +x path/to/cagesearch
   module load compiler/gcc/8.4.0

Note that, any gcc version above 8.4.0 is technically suitable.

If everything goes well, a gentle notation is expected after executing
this binary file:

.. code:: 

   path/to/cagesearch

.. raw:: html

   <html xmlns="http://www.w3.org/1999/xhtml"><head></head><body><center>The usenauty notation.</center></body></html>

The absolute path of this file corresponds to the ``gen_core_path`` in
the generator module, as demonstrated in
`test_step.py <https://github.com/Franklalalala/AutoSteper/blob/b1ae14e734b2013628ffca241ab44eba6510f970/tests/test_step/test_step.py#L38>`__.

Tips for users from Chinese Mainland
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A `GitHub Proxy <https://ghproxy.com/>`__ will speed up the installation
from github:

.. code:: 

   pip install git+https://ghproxy.com/https://github.com/XJTU-ICP/FullereneDataParser
   wget https://ghproxy.com/https://github.com/Franklalalala/usenauty/releases/download/linux/cagesearch

For developers
--------------

Any contribution is greatly appreciated. To install from the source
code, the AutoSteper package:

.. code:: 

   git clone https://github.com/Franklalalala/AutoSteper
   cd AutoSteper
   pip install . -e

The FullereneDataParser package:

.. code:: 

   git clone https://github.com/XJTU-ICP/FullereneDataParser
   cd FullereneDataParser
   pip install . -e

To compile the usenauty project, please follow instructions in
`usenauty <https://github.com/Franklalalala/usenauty>`__.

Note
----

Issues are welcomed if you have any questions.

Contributions needs to stay in line with `Conventional Commit
messages <https://www.conventionalcommits.org/>`__.

Contact me: 1660810667@qq.com
