# Meta-Template for Research Software

A tool that helps **template creators** to create **software templates** for research software, and adopt best practices on sustainable software for Natural and Engineering Sciences. It provides a way to align best practices and reduce maintainance efforts across organisations, while allowing organisation to customize software templates to their needs. 

If you came here looking for a template to start your own research software project, you check out the [Software Template Registry](REGISTRY.md) for a list of software templates that are using the *meta-template*.

| [FAIR-Software Recommendations](https://fair-software.nl) | Badges|
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1. Code Repository | [![GitHub Badge](https://img.shields.io/github/v/release/SS-NES/meta-template?color=blue)](https://github.com/SS-NES/meta-template/releases/latest) |
| 2. License |  [![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) |
| 3. Community Registry | [![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-black.json)](https://github.com/copier-org/copier)|


## Why?

Because research organisations can produce high-quality research software by adopting common best practices, and we acknowledge that every organisation has practices and workflows that are only important to them. Therefore, we facilitate the adopting  of common best practices for research software development through a highly customisable tool that allows organisations to create their own software templates, while aligning with the best practices of the Natural and Engineering Sciences community in the Netherlands.

## Features

- Federation of best practices for research software project. Align with the best practice for research software development of the Natural and Engineering Science community in the Netherlands.
- Reduce maintainabily. Enhancements to the meta-template can be incoorporated with ease in templating projects which reduces the time *template creators* need to maintain and updater templating projects.
- Flexibility. Generate templating projects for any programming languates and customize them for every use case.  
- A curated list of open source licenses for your templating projects.

## Key Concepts

- **Meta Template:** a template to start a software templating project. This repository. It contains common features that are shared among software templating projects. 
- **Software Template:**  a template for research software projects generated using the *meta template*. It may contain common and custom features for a particular type of software project. For example, features specific to programming languages  (Python, R, Julia, etc.) or features specific to relevant use cases (Jupyter notebooks, organization A, organization B).
- **Software Project:** the software schaffolding generated using a *software template*. It contains files, directories and scaffolding code to start developing research software. 
- **Template Creator:** a person or team that creates a *software template* using the *meta-template*. Template creators are responsible for maintaining the software template and keeping it up to date with the latest best practices provided by the **meta-template**.
- **Template User:** a person or team that uses a *software template* to start a new  research software project. Template users decide when to update their research software projects with the latest best practices provided by a *software template*.

## How to Create a Software Template
To create a *software template* using the *meta-template*, you need to follow these steps:

1. Install [Copier](https://copier.readthedocs.io) into your development environment.

2. Start a new *software template* by rendering the latest version of this repository. This will generate boiler plate code that can be adapted for your particular use case.

```shell
copier copy https://github.com/SS-NES/meta-template.git <path/to/templating-project>
```

3. Make your *software template* a Git repository. Copier uses Git to track update, therefore, a directory containing a *software template* must be a Git repository. 

```shell
cd <path/to/project-directory>
git init
git add . 
git commit -m 'initial commit'
```

1. Customize your template project. Consult the [Copier Documentation](https://copier.readthedocs.io/en/stable/creating/) and the [Jinja2 Documentation](https://jinja.palletsprojects.com/en/stable/templates/).

2. To test if your software template is producing the results you want, your can render it into a *software project*. Use the `--vsc-ref HEAD` option to rendere all the changes you have made. 

```shell
# from a local Git repository
copier copy --vcs-ref HEAD <path/to/your-software-template> <path/to/new-project/>

# from a remote Git repository
copier copy https://github.com/foo/<your-template>.git <path/to/new-project/>
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

This software was developed as part of the TDCC-NES Bottleneck Project "`Best
Practices for Sustainable Software [SS-NES](https://tdcc.nl/projects/project-initiatives-nes/tdcc-nes-bottleneck-projects/best-practices-for-sustainable-software) funded by the Thematic Digital
Competence Centre [TDCC](https://tdcc.nl/) for the Natural & Engineering Sciences [NES](https://tdcc.nl/about-tddc/nes).

Some features in this software template were inspired by [Serious Scaffold Python](https://github.com/serious-scaffold/ss-python).
