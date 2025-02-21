Jupyter Notebook Template for Data Analysis Projects
====================================================

The Jupyter notebook template was generated using the meta template 
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

This template is designed for users creating or managing data analysis projects 
in Jupyter notebooks. While maintaining NES best practices, the structure was 
slightly adjusted to better fit the needs of notebook-based workflows.

Structural Adjustments
----------------------

To align with typical Jupyter-based research workflows, 
the following modifications were made:

- ``data/`` folder – Stores datasets used in analysis.
- ``notebooks/`` folder – Contains a template notebook with placeholders that dynamically adjust based on user input during project creation.
- ``tests/`` folder – Organizes and runs validation tests on code or data processing steps.

This ensures a structured, reproducible, and well-documented environment for research software development.
