Usage
=====

This documentation is generated and hosted using readthedocs.org. The source code is hosted on github.
For more information, see readthedocs documentation: https://docs.readthedocs.io/en/stable/index.html

This documentation is written in reStructuredText. We recommend using the following cheatsheet to get started: 

* https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html
* https://sphinx-tutorial.readthedocs.io/cheatsheet/  

.. _installation:

Installation
------------

To install sphinx, readthedocs, etc, use pip to install the neccessary python dependencie:

.. code-block:: console

   $ cd /path/to/this/project
   $ cd docs
   $ pip install -r requirements.txt

Building and Viewing the Documentation
--------------------------------------

To build the documentation, use the following command:

.. code-block:: console

   $ make html

If you are developing in windows:

.. code-block:: powershell

   C:\path\to\this\project\docs> .\make.bat html

then you can view the built html for the project in the ``\build`` directory 
(these can be viewed using any web browser).

Examples
--------

For examples how to document your code, see the following:

toc
