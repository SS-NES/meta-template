[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

# Meta Template for Research software

A template to initialize **templating projects** that comply with
best practices on sustainable software in Natural and Engineering Science.  This template containts boilerplate for developing custom research software templates
using copier.

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

