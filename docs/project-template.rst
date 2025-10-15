.. _create_template:

Creating a Software Template
===============================

To create a software template using the meta-template, you need to follow these steps:

.. Note::

   Meta-Template uses `copier <https://copier.readthedocs.io/en/stable>`_, a Python-based templating tool to create and manage templates; however, *templates created using the meta-template are languge agnostic and can be used for any programming language.*

1. **Create a new software template project** using the meta-template as a base. You can do this by running the following command:

   .. code-block:: bash

      copier copy gh:SS-NES/meta-template.git <my-software-template>

   Replace `<my-software-template>` with the name of your new software template project.

   You will be prompted to answer a few questions about your new software template project. For example, the name of the project, the license, and other options. You can choose to accept the default values or provide your own.

   .. code-block:: text

      Thanks for using SS NES research software templates.
      This meta-template help template developers to create custom
      templates for different purposes or programming languages, and
      maintain consistency with the best practices adopted by the
      SS NES community in the Netherlands.

      🎤 A name to your template project.
        My Template Project
      🎤 A brief description of your template including its purpose, and for whom it is intended.
        A description for my template project
      ...


2. **Initialize a Git repository** in your new software template project directory:

   .. code-block:: bash

      cd <my-software-template>
      git init
      git add .
      git commit -m "Initial commit of my software template"


Custimizing a Software Template
--------------------------------

To customize your software template, you can edit the files in the `custom/` directory.
The `custom/` directory contains the `customize.yml` file, which is used to define the questions and options for your software template. You can add new questions and options to this file. The file is in YAML format, and it be structured as a `copier.yml` file. Refere to the `copier documentation <https://copier.readthedocs.io/en/stable/faq.html#how-to-define-a-question>`_ for more details. The example below shows how to add a new question to the `customize.yml` file:


1. Edit the `customize.yml` file in the `custom/` directory. 
   
    .. code-block:: yaml

        # custom/customize.yml
        ---

        my_question:
            type: str
            default: "default value"
            help: "This is a custom question for my software template."
            choices:
                - choice1
                - choice2
                - choice3

2.  Include the `customize.yml` file in the `copier.yml` file in the root directory of your software template project, by uncommening the `!include` line. This will attached your question and options in `customize.yml` in the `copier.yml` file. Such questions and options will be prompted to users of your software template when they run the `copier` command to generate a new software project.

    .. code-block:: yaml

        # copier.yml
        ...
        ---
        # Inlcudes customized # UNCOMMENT TO INCLUDE CUSTOME FEATURES
        !include custom/customize.yml

Publishing a Software Template
--------------------------------

To publish your software template, you can push it to a Git repository. You can use any Git hosting service, such as GitHub or GitLab. Once you have pushed your software template to a Git repository, you can share it with others.


.. code-block:: bash

   git remote add origin <your-git-repo-url>
   git push -u origin main


.. important::

   Before publishing your software template, make sure you add a tag with the version number of your software template. Tags is the way **copier** keeps track of the version that template users are using in their software projects. Tags also enable users to incoorporate updates you make on software template into their software projects. You can add a tag using the following command:

.. code-block:: bash

   git tag -a v0.1.0 -m "Initial release of my software template"
   git push origin v0.1.0

Replace `v0.1.0` with the version number of your software template. 


Using a Software Template
-----------------------------

User of your software template to create a new research software project in the same way you created a software template project. That is, using the `copier copy` as follows:

.. code-block:: bash

   # GitHub
   copier copy gh:<your-namespace>/<your-git-repo>.git <my-new-software-project>

   # GitLab
   copier copy gl:<your-namespace>/<your-git-repo>.git <my-new-software-project>

.. note::

   Software templates created using the meta-template can be applied to preexisting research software projects. Consult the `copier documentation <https://copier.readthedocs.io/en/stable/faq/#can-copier-be-applied-over-a-preexisting-project>`_ for more details.
