```none
██████╗ ██████╗  █████╗  ██████╗████████╗██╗ ██████╗ █████╗ ██╗     ██╗     ██╗
██╔══██╗██╔══██╗██╔══██╗██╔════╝╚══██╔══╝██║██╔════╝██╔══██╗██║     ██║     ██║
██████╔╝██████╔╝███████║██║        ██║   ██║██║     ███████║██║     ██║     ██║
██╔═══╝ ██╔══██╗██╔══██║██║        ██║   ██║██║     ██╔══██║██║     ██║     ██║
██║     ██║  ██║██║  ██║╚██████╗   ██║   ██║╚██████╗██║  ██║███████╗███████╗██║
╚═╝     ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝   ╚═╝   ╚═╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚══════╝╚═╝
```

## Book status

[![MegaLinter](https://github.com/practicalli/vspacecode/actions/workflows/megalinter.yaml/badge.svg)](https://github.com/practicalli/vspacecode/actions/workflows/megalinter.yaml)[![Publish Book](https://github.com/practicalli/vspacecode/actions/workflows/publish-book.yaml/badge.svg)](https://github.com/practicalli/vspacecode/actions/workflows/publish-book.yaml){target=_blank}
[![pages-build-deployment](https://github.com/practicalli/vspacecode/actions/workflows/pages/pages-build-deployment/badge.svg)](https://github.com/practicalli/vspacecode/actions/workflows/pages/pages-build-deployment){target=_blank}

[![Ideas & Issues](https://img.shields.io/github/issues/practicalli/vspacecode?label=content%20ideas%20and%20issues&logoColor=green&style=for-the-badge)](https://github.com/practicalli/vspacecode/issues){target=_blank}
[![Pull requests](https://img.shields.io/github/issues-pr/practicalli/vspacecode?style=for-the-badge)](https://github.com/practicalli/vspacecode/pulls){target=_blank}

![GitHub commit activity](https://img.shields.io/github/commit-activity/m/practicalli/vspacecode?style=for-the-badge)
![GitHub contributors](https://img.shields.io/github/contributors/practicalli/vspacecode?style=for-the-badge&label=github%20contributors)


## License

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/">
<a href="http://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">
<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"></a>
 <a property="dct:title" rel="cc:attributionURL" href="https://github.com/practicalli/clojure">Practicalli Clojure </a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://practical.li/vscode">Practicalli VSpaceCode</a> is licensed under <a href="http://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-SA 4.0 </a></p>


## Contributing

Issues and pull requests are most welcome.  Please detail issues as much as you can.  Pull requests are simpler to work with when they are specific to a page or at most a section.  The smaller the change the quicker it is to review and merge.

Please [see the detailed contributing section of the book](https://practical.li/introduction/contributing/) before raising an issue or pull request

* [Kanban board of issues](https://github.com/practicalli/vspacecode/projects/1)
* [Current Issues](https://github.com/practicalli/vspacecode/issues)
* [Current pull requests](https://github.com/practicalli/vspacecode/pulls)

[Practicalli Clojure CLI Config](clojure/clojure-cli/practicalli-config.md) provides a user level configuration used in this guide and issues and pull requests can also be made there.

By submitting content ideas and corrections you are agreeing they can be used in this workshop under the [Creative Commons Attribution ShareAlike 4.0 International license](https://creativecommons.org/licenses/by-sa/4.0/).  Attribution will be detailed via [GitHub contributors](https://github.com/practicalli/vspacecode/graphs/contributors).


## Sponsor Practicalli

[![Sponsor Practicalli via GitHub](https://raw.githubusercontent.com/practicalli/graphic-design/live/buttons/practicalli-github-sponsors-button.png)](https://github.com/sponsors/practicalli-johnny/)

The sponsorship funds are used solely for the continued development of [Practicalli series of books and videos](https://practical.li/)

Thank you to [Cognitect](https://www.cognitect.com/), [Nubank](https://nubank.com.br/) and a wide range of other [sponsors](https://github.com/sponsors/practicalli-johnny#sponsors) for your continued support


## GitHub Actions

The megalinter GitHub actions will run when a pull request is created,checking basic markdown syntax.

A review of the change will be carried out by the Practicalli team and the PR merged if the change is acceptable.

The Publish Book GitHub action will run when PR's are merged into main (or the Practicalli team pushes changes to the default branch).

Publish book workflow installs Material for MkDocs version 9


## Local development

Install mkdocs version 9 using the Python pip package manager

```bash
pip install mkdocs-material=="9.*"
```

Install the plugins used by the Practicalli site using Pip (these are also installed in the GitHub Action workflow)

```bash
pip3 install mkdocs-material mkdocs-callouts mkdocs-glightbox mkdocs-git-revision-date-localized-plugin mkdocs-redirects pillow cairosvg
```

> pillow and cairosvg python packages are required for [Social Cards](https://squidfunk.github.io/mkdocs-material/setup/setting-up-social-cards/)

Fork the GitHub repository and clone that fork to your computer,

```bash
git clone https://github.com/<your-github-account>/<repository>.git
```

Run a local server from the root of the cloned project

```bash
make docs
```

The website will open at <http://localhost:8000>

If making smaller changes, then only rebuild the content that changes, speeding up the local development process
```bash
make docs
```

