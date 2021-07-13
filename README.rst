Lumache
=======

**Lumache** (/lu'make/) is a Python library for cooks and food lovers that
creates recipes mixing random ingredients.


## Project structure

docs
├── build
├── make.bat
├── Makefile
└── source
   ├── conf.py
   ├── index.rst
   ├── _static
   └── _templates

/build -> an empty directory (for now) that will hold the rendered documentation

make.bat and Makefile -> convenience scripts to simplify some common Sphinx operations, such as rendering the content

source/conf.py -> a python script holding the configuration of the Sphinx project. It contains the project name and release you specified to sphinx-quickstart, as well as some extra configuration keys.

source/index.rst -> the root document of the project, which serves as welcome page and contains the root of the "table of contents tree" (or toctree)


## Building your documentation in other formats
Sphinx supports a variety of formats apart from HTML, including PDF, EPUB, and more.

## Sphinx customization
By using core Sphinx: extensions and themes.

## Using a third-party HTML theme
To customize the appearence of your documentation.
Sphinx has several built-in themes, and there are also third-party ones.

For example, to use the `Furo` theme you will need to install it in your python environment like this:
`$pip install furo`

And then locate the `html_theme`on your `conf.py` to set it up.

## Multiple pages
The file `index.rst` is the `root document` serving as a welcome page and contain the root of the "table of contents tree" (or toctree).
But, Sphinx allows you to assemble a project from different files.
And remember to add a `toctree` directive at the end of `index.rst` including the new files.

> Note: documents outisde `toctree` will result in **WARNING**.