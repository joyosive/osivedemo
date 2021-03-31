ReadTheDocs Install
===================

    1. Remove Python2

        .. code-block:: bash

            sudo apt purge python
            sudo apt purge python-minimal
    
    2. Install Python3 and set it as default

        .. code-block:: bash
        
            sudo apt install -y python 3 python3-pip
            sudo ln -s /usr/bin/python3 /usr/bin/python
            sudo ln -s /usr/bin/pip3 /usr/bin/pip

    3. Install sphinx

        .. code-block:: bash

            pip install --user pipenv
            pip install virtualenv virtualenvwrapper
            python --version 
            pip install sphinx sphinx_rtd_theme
        
    4. Create your project 

        .. code-block:: bash

            sphinx-quickstart

    5. Then in ``conf.py`` file edit 

        .. code-block:: python

            extensions = ['recommonmark', 'sphinx_rtd_theme']
            
            html_theme= 'sphinx_rtd_theme'


    6. Compile the code

        .. code-block:: bash

            make html
        