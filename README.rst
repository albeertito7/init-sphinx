Sphinx documentation
====================

This an initiation project about the Sphinx python documentation generator, being majorly influenced by the *getting-started* beginners `tutorial <https://www.sphinx-doc.org/en/master/tutorial/index.html>`__.

The aim is to acquire the fundamentals of how projects are created and structured and to give a quick taste of what Sphinx is and how you might use it to those willing to learn.

Besides, feel free to leave `feedback <https://github.com/albeertito7/init-sphinx/issues/new>`__ if any improvement, or `email <mailto:albertperezdatsira@gmail.com>`__ me with questions.

Table of contents
-----------------

.. contents::
    :backlinks: none
    :depth: 2
    :class: title


Getting started
---------------

Cloning the repository
^^^^^^^^^^^^^^^^^^^^^^

Once you get the repository on your local machine, let's create your own python environment

.. _above:

.. code-block:: bash

    $ python -m venv .venv
    $ source .venv/bin/activate # if using Windows, just type `.venv/bin/activate.bat` in the command-prompt

Then, you should get all the dependencies via

.. code-block:: bash

    (.venv) $ pip install -r requirements.txt

In this way, all the dependencies specified in the *requirements.txt* to work with will be added into the new python environment.


From scratch
^^^^^^^^^^^^

If you prefer to create your own project from scratch, just in a new directory, create a file called *README.rst* and generate a python virtual environment just like above.

Then you should install the python module *sphinx* as follows:

.. code-block:: bash

    (.venv) $ pip install sphinx


Finally, for creating the documentation is easy as:

.. code-block:: bash

    (.venv) $ sphinx-quickstart docs


This will present you a series of questions relatives to the project and will generate the project strucuture.


Project structure
-----------------

.. code-block:: raw

    init-sphinx
    ├── docs
    |   ├── build                <- Empty directory (for now) that will hold the rendered documentation.
    |   ├── source
    |   |   ├── conf.py          <- Configuration Sphinx project. Contains some configuration keys.
    |   |   ├── index.rst        <- The root document of the project serving as a welcome page.
    |   |   ├── _static          <- For custom stylesheets and other static files.
    |   |   └── _templates       <- For custom HTML templates.
    |   |
    |   ├── Makefile             <- Makefile and make.bat are convenience scripts to simplify some common Sphinx operations, such as rendering.
    |   └── make.bat
    |
    ├── .gitignore
    ├── README.rst               <- The top-level README for developers using this project.
    └── requirements.txt         <- Python virtual environment requirements generated with `pip freeze > requirements.txt`


Rendering the documentation
---------------------------

You may use the *sphinx-build* command:

.. code-block:: bash

    (.venv) $ sphinx-build -b html docs/source/ docs/build/html

or leverage the convenience script as follows:

.. code-block:: bash

    cd docs
    make html

**Note** these are examples for HTML, but Sphinx supports a variety of formats including PDF, EPUB and `more <https://www.sphinx-doc.org/en/master/usage/builders/index.html#builders>`__.

Visualization
-------------

Run on your browser the *docs/build/html/index.html* to visualize the project documentation.

**Note** this is using the *build/html* directory, but if any other format is rendered you may find the *index.html* in its corresponding folder.


Sphinx customization
--------------------

By using core Sphinx: extensions and themes.

Using a third-party HTML theme
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To customize the appearence of your documentation.
Sphinx has several built-in themes, and there are also third-party ones.

For example, to use the **Furo** theme you will need to install it in your python environment like this:

.. code-block:: bash

    $ pip install furo

And then locate the **html_theme** on your *conf.py* to set it up.

Multiple pages
^^^^^^^^^^^^^^

The file *index.rst* is the **root document** serving as a welcome page and contain the root of the "table of contents tree" (or toctree).
But, Sphinx allows you to assemble a project from different files.
And remember to add a *toctree* directive at the end of *index.rst* including the new files.

**Note:** documents outisde *toctree* will result in **WARNING**.

Where to go from here
---------------------

This are the first steps to create a documentation project with Sphinx.
To continue learning more, check out the `rest of the documentation <https://www.sphinx-doc.org/en/master/contents.html#contents>`__.
