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