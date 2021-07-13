Sphinx documentation
====================

.. contents:: :backlinks: none
    Table of contents

Project structure
-----------------

.. code-block:: raw

    init-sphinx
    ├── docs
    |   ├── build                       <- Empty directory (for now) that will hold the rendered documentation.
    |   ├── source
    |   |   ├── conf.py                 <- Configuration Sphinx project. Contains some configuration keys.
    |   |   ├── index.rst               <- The root document of the project serving as a welcome page.
    |   |   ├── _static                 <- For custom stylesheets and other static files.
    |   |   └── _templates              <- For custom HTML templates.
    |   |
    |   ├── Makefile                    <- Makefile and make.bat are convenience scripts to simplify some common Sphinx operations, such as rendering.
    |   └── make.bat
    |
    ├── .gitignore
    ├── README.rst                       <- The top-level README for developers using this project.
    └── requirements.txt                 <- Python virtual environment requirements generated with `pip freeze > requirements.txt`


Building your documentation in other formats
--------------------------------------------

Sphinx supports a variety of formats apart from HTML, including PDF, EPUB, and more.

Sphinx customization
--------------------

By using core Sphinx: extensions and themes.

Using a third-party HTML theme
------------------------------

To customize the appearence of your documentation.
Sphinx has several built-in themes, and there are also third-party ones.

For example, to use the `Furo` theme you will need to install it in your python environment like this:

.. code-block:: bash

    $pip install furo

And then locate the `html_theme`on your `conf.py` to set it up.

Multiple pages
--------------

The file `index.rst` is the `root document` serving as a welcome page and contain the root of the "table of contents tree" (or toctree).
But, Sphinx allows you to assemble a project from different files.
And remember to add a `toctree` directive at the end of `index.rst` including the new files.

> Note: documents outisde `toctree` will result in **WARNING**.

Where to go from here
---------------------

This are the first steps to create a documentation project with Sphinx.
To continue learning more, check out the rest of the documentation.