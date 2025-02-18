[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

# Meta Template for Research software

A template to initialize **templating projects** that comply with
best practices on sustainable software in Natural and Engineering Science.  This template containts boilerplate code for developing custom research software templates using [Copier](https://copier.readthedocs.io).

## Features

- Federation of best practices for research software project. Align with the best practice for research software development of the Natural and Engineering Science community in the Netherlands.
- Reduce maintainabily. Enhancements to the meta-template can be incoorporated with ease in templating projects which reduces the time maintainers of templating projects have to spend in updating their templates.
- Flexibility. Generate software template projects for any programming languates and use cases. 
- Library of common open source licenses for your templating projects.

## How to Use

**Requirements**

- Python 3.11 or higher
- [Copier](https://copier.readthedocs.io)

### Start a templating project

```shell
copier copy https://github.com/SS-NES/meta-template.git <path/to/project-directory>
```

### Updating an existing software project

Update the generated project by changing your answers. At the root of the software project, do:

```shell
copier update
```
> IMPORTANT: Before you are allow to update a project, the sofware project must be initialized as a Git repository, all files must be commited, and the status of the repository must show it is clean, i.e., no pending changes to commit.



## Acknowledgements

- This template was inspired by [Serious Scaffold Python](https://github.com/serious-scaffold/ss-python)

