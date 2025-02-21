R Project Template
==================

*Link to the template repository:* `click here <https://github.com/SS-NES/R-template>`_

The R project template was generated using the meta template 
to streamline the adoption of best software development practices in the NES domain.

By leveraging the meta template, essential files that help a project adhere to the FAIR principles, 
such as license files, ``CODEOFCONDUCT.md``, ``README.md``, 
and others were automatically included, eliminating the need for manual setup. 

This also improves maintainability as updates in the meta template, such as changes in license files, 
can easily be synced using the following command:

.. code-block:: bash

   copier update --answers-file .meta-answers.yml

Purpose
-------

This template is designed for R users working on data analysis, statistical 
modeling, or research projects. It provides a structured environment for easier 
maintainability, readability, and encourages reproducibility.

Structural Adjustments
----------------------

While adhering to NES best practices, the following modifications were made to tailor the template for R-based workflows:

- ``R/`` folder – Contains R scripts for functions and analyses.
- ``data/`` folder – Stores raw and processed datasets.
- ``includes/`` folder – Contains additional scripts or configuration files that support project execution.
- ``man/`` folder – Contains documentation for package functions, ensuring proper descriptions and metadata.
- ``tests/`` folder – Houses unit tests for R functions.
- ``vignettes/`` folder – Contains long-form documentation and examples 
  using R Markdown to guide users in utilizing the project effectively.

This structure ensures a well-organized, reproducible, and maintainable environment for R-based research and development.
