Quick Start
==============

This is a quick start guide to get you up and running with creating your own software templates using the Meta-Template.

Prerequisites
-----------------

- Python 3.8 or higher
- `Git <https://git-scm.com/docs/git>`_ as version control system
- `copier <https://copier.readthedocs.io>`_ installed
- Familiarity with `Jinja Templating Engine <https://jinja.palletsprojects.com/en/stable/>`_


Getting Started
------------------

1. Use **copier** to create a new software template project from the meta-template:

.. code-block:: bash

   copier copy gh:SS-NES/meta-template.git <my-software-template>
   

Replace `my-software-template` with the name of your new software template project.

1. Navigate to your new software template project directory:

.. code-block:: bash
   
   cd my-software-template

3. Use Git to make your new software template project a Git repository:

.. code-block:: bash

   git init
   git add .
   git commit -m "Initial commit of my software template"

4. You are ready to start creating your software template. You can customize your software template by editing the files in the `custom` directory. 
You can add files and edit the `customize.yml` file. 
Refere to :ref:`create_template` for details on how to customize a software template.


Updating a Software Template
---------------------------------

To update your software template with the latest changes from the meta-template, you can use **copier** again:

.. code-block:: bash

   copier update --answers-file .meta-answers.yml

Replace `<my-software-template>` with the path to your software template project.
This will pull the latest changes from the meta-template and apply them to your software template project, 
allowing you to keep it up to date with the latest best practices and features.

