The Meta-Template
===================

A tool that helps **template creators** to create **software templates** for research software and adopt best practices on sustainable software for Natural and Engineering Sciences. 
It provides a way to align best practices and reduce maintenance efforts across organisations, while allowing organisation to customize software templates to their needs.

Research organisations want to produce high-quality research software by adopting common best practices, 
but we have to acknowledge that every organisation has practices and workflows that are only important to them. 
Therefore, we facilitate adopting common best practices for research software development through a highly 
customisable tool that allows organisations to create their own software templates, 
while aligning with the best practices of the Natural and Engineering Sciences community in the Netherlands.

The *meta-template* offers a tool for developing custom research software templates using `copier <https://copier.readthedocs.io>`_.
*Software templates* generated using the *meta-template*  an easily aligh and comply with best practices on sustainable software in Natural and Engineering Science. 

Features
----------

- Federation of best practices for research software project. Align with the best practice for research software development of the Natural and Engineering Science community in the Netherlands.
- Reduce maintainabily. Enhancements to the meta-template can be incoorporated with ease in templating projects which reduces the time *template creators* need to maintain and updater templating projects.
- Flexibility. Generate templating projects for any programming languates and customize them for every use case.  
- A curated list of open source licenses for your templating projects.

Key Concepts
------------

- **Best Practices:** a set of best practices for research software development in the Natural and Engineering Sciences. These best practices are defined by the community and are used to guide the development of high-quality research software projects.
- **Meta Template:** a template to start a software templating project. This repository. It contains common features that are shared among software templating projects. 
- **Software Template:**  a template for research software projects generated using the *meta template*. It may contain common and custom features for a particular type of software project. For example, features specific to programming languages  (Python, R, Julia, etc.) or features specific to relevant use cases (Jupyter notebooks, organization A, organization B).
- **Software Project:** the software schaffolding generated using a *software template*. It contains files, directories and scaffolding code to start developing research software. 
- **Template Creator:** a person or team that creates a *software template* using the *meta-template*. Template creators are responsible for maintaining the software template and keeping it up to date with the latest best practices provided by the **meta-template**.
- **Template User:** a person or team that uses a *software template* to start a new  research software project. Template users decide when to update their research software projects with the latest best practices provided by a *software template*.


Structure
------------

The *meta-template*  repository contians **common** and **custom** features for software templates. The common features are shared among all software templates and are used to generate the software scaffolding. The custom features are specific to a particular software template and are used to customize the software scaffolding for a particular use case (e.g. institution-specific).

.. code-block:: text

    meta-template/
    ├── meta
    │   ├── common                          <- Common Questions/Options 
    │   │   ├── citation.yml
    │   │   ├── community.yml
    │   │   ├── licensing.yml
    │   │   ├── messages.yml
    │   │   ├── settings.yaml
    │   │   └── software.yml
    │   ├── custom                          <- Institution-specific Questions/Options
    │   │   └── customize.yml
    │   ├── template                        <- Common templating elements
    │   │   ├── includes
    │   │   ├── tests
    │   │   ├── README.md.jinja
    │   │   ├── {{".gitignore.jinja"}}
    │   │   ├── {{"{% if citation %}CITATION.cff{% endif %}.jinja"}}
    │   │   ├── {{"{% if community %}CONTRIBUTING.md{% endif %}.jinja"}}
    │   │   ├── {{"{{_copier_conf.answers_file}}.jinja"}}
    │   │   ├── {{"CHANGELOG.md.jinja"}}
    │   │   ├── {{"CODE_OF_CONDUCT.md.jinja"}}
    │   │   └── {{"{% if software_license != 'No License' %}LICENSE{% endif %}.jinja"}}
    │   ├── CONTRIBUTING.md.jinja
    │   ├── README.md.jinja
    │   ├── copier.yml.jinja
    │   └── {{_copier_conf.answers_file}}.jinja
    ├── LICENSE
    ├── README.md
    ├── REGISTRY.md
    └── copier.yml                          <- Main copier configuration



