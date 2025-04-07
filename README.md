[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-black.json)](https://github.com/copier-org/copier)

# Research Software Meta Template

A toolkit to start **software templates** for research software and adopt best practices on sustainable software for Natural and Engineering Sciences. It provides a way to align best practices and reduce maintainance efforts across 
organisations, while allowing organisation to customize software templates to their needs. 

## Why?

Because every organisation wants to produce high-quality research software by adopting common best practices, and we acknowledge that every organisation has practices and workflows that are only important to them. Therefore, we facilitate adopting common best practices for research software development through a highly customisable software template.

## Features

- Federation of best practices for research software project. Align with the best practice for research software development of the Natural and Engineering Science community in the Netherlands.
- Reduce maintainabily. Enhancements to the meta-template can be incoorporated with ease in templating projects which reduces the time maintainers of templating projects have to spend in updating their templates.
- Flexibility. Generate templating projects for any programming languates and customize them for every use case.  
- A curated list of open source licenses for your templating projects.

## Key Concepts

- **Meta Template:** a template to start a software templating project. This repository. It contains common features that are shared among software templating projects. 
- **Software Template:**  a template for research software projects generated using the *meta template*. It may contain custome features for a particular type of software project. For example, features specific to programming languages  (Python, R, Julia, etc.) or features specific to relevant use cases (Jupyter notebooks, organization A, organization B).
- **Software Project:** the software schaffolding generated using a *software template*. It contains common features (from the *meta template*) and custom features (from its parent *software tempalte*).

## How to Use

1. Install [Copier](https://copier.readthedocs.io) into your development environment.

2. Start a new templating project.

```shell
copier copy https://github.com/SS-NES/meta-template.git <path/to/templating-project>
```
    This will generate boiler plate code that can be adopted for a particular uses case.

3. Inialize a Git repository in your templating project

```shell
cd <path/to/project-directory>
git init
git add . 
git commit -m 'initial commit'
```
4. Customize your template project. Consult the [Copier Documentation](https://copier.readthedocs.io/en/stable/creating/) and the [Jinja2 Documentation](https://jinja.palletsprojects.com/en/stable/templates/).

5. Generate project templates using your templating project.

```shell
# from a local Git repository
copier copy <path/to/templating-project> <path/to/new-project/>

# from a remote Git repository
copier copy https://github.com/foo/<templating-project>.git <path/to/new-project/>
```

> [!NOTE]
> By default Copier will use versioning tags to copy the latest release of a template. [Read more](https://copier.readthedocs.io/en/stable/generating/#templates-versions). 
> To generate template with the latest saved changes of a template use: 
> ```copier copy --vcs-ref HEAD <path/to/templating-project> <path/to/new-project/>```

## Maintainance

Changes and enhancements to the *meta-template* can be easily be integrated into *templating projects*. Which means that maintainers of *templating projects* can quickly adopt new/review practices into their templates by syncing changes whenever a new version of the meta-template is release.

### Updating

Updating will sync a *templating project* with the lates version of the *meta-template*. Thefore, applying changes to the meta-template into templaring project. Copier uses Git tags on the meta-template to determine the latest version. 

```shell
copier update --answers-file .meta-answers.yml
```

> [!IMPORTANT] 
> Before you are allow to update a project, the templating project must be initialized as a Git repository, all files must be commited, and the status of the repository must show it is clean, i.e., no pending changes to commit.

> [!NOTE]
> If updating results in conflicts, you should resolve them manually before committing. Conflicts are managed the same way as in Git.

## Contributing

You can contribute to this initiative in two ways:

1. Using the *meta-template* create templating projects for your organisation/team. If you do so, we encourage you to registe your templating project in the [Template Registry](REGISTRY.md)
2. Propose changes to the *meta-tempalte* about common best practices for research software projects.  In which case, share your ideas and suggestions by [opening an issue](https://github.com/SS-NES/meta-template/issues).

## Acknowledgements

- This template was inspired by [Serious Scaffold Python](https://github.com/serious-scaffold/ss-python)
