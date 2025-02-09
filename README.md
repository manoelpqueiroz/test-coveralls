# Python Project GH Coveralls

<div align="center">

[![Python support][bp1]][bp2]
[![PyPI Release][bp3]][bp2]
[![Repository][bscm1]][bp4]
[![Releases][bscm2]][bp5]
[![Docker][bdocker1]][bdocker2]
[![Licence][blic1]][blic2]
[![Expand your project structure from atoms of code to galactic dimensions.][bp6]][bp7]

[![Contributions Welcome][bp8]][bp9]
[![Open issues][bscm3]][bp10]
[![Merge Requests][bscm4]][bscm5]

[![BDD][bbbd1]][bbbd2]
[![Poetry][bp11]][bp12]
[![Code style: Ruff][bfo1]][bfo2]
[![Docstrings][bli1]][bli2]

[![Pre-commit][bp13]][bp14]
[![Bandit][bp15]][bp16]
[![isort][bfo3]][bfo4]
[![Editorconfig][bp17]][bp18]

<!-- UPDATEME by toggling this comment off after replacing your project's index in both anchors below
[![OpenSSF Best Practices][boss1]][boss2] -->
<!-- UPDATEME by toggling this comment off after replacing your project's index in both anchors below
[![OSSRank][boss3]][boss4] -->

[![Semantic versions][bp19]][bp5]
[![Coverage][bcov1]][bcov2]
[![Pipelines][bscm6]][bscm7]

_Awesome `python-project-gh-coveralls` is a Python cli/package created with https://gitlab.com/galactipy/galactipy_

</div>

## Very first steps

### Initialize your code

1. Initialize `git` inside your repo:

```bash
cd python-project-gh-coveralls && git init
```

2. If you don't have `Poetry` installed run:

```bash
invoke poetry-download
```

> This installs Poetry as a [standalone application][fs1]. If you prefer, install it through your distribution's package manager.

3. Initialize Poetry and install `pre-commit` hooks:

```bash
invoke install
invoke pre-commit-install
```

4. Run the codestyle:

```bash
invoke codestyle
```

5. Upload initial code to GitHub:

```bash
git add .
git commit -m ":tada: Initial commit"
git branch -M main
git remote add origin https://github.com/galactipy/python-project-gh-coveralls.git
git push -u origin main
```

### Set up bots
- Set up [Dependabot][hub1] to ensure you have the latest dependencies;
- Set up [Stale bot][hub2] for automatic issue closing.

### Poetry

Want to know more about Poetry? Check [its documentation][fs2].

<details>
<summary>Details about Poetry</summary>
<p>

Poetry's [commands][fs3] are very intuitive and easy to learn, like:

- `poetry add numpy@latest`
- `poetry run pytest`
- `poetry publish --build`

etc.
</p>
</details>

### Building and releasing your package

In order to release a new version of the application, a few steps are needed.

Make sure you have a PyPI account and generate an API token, you can then register it in your repository with

```bash
invoke pypi-config <API_token>
```

Then, you're all good to build and publish your package in one go!

```bash
invoke publish
```

You should also [push a tag][fs5] to `GitLab` or `GitHub` and create a `Release` for your application on the platform to ensure users can check the latest version contents.

Of course, you can also rely solely on the CI tools provided by Galactipy to handle building, publishing and releasing automatically, with minimal configuration required! :partying_face:

Pushing a tag to your repository will also set up the automated workflows to build and publish your image to Docker Hub.

## :dart: What's next

Well, that's up to you. :muscle:

For further setting up your project:

- [ ] Look for files and sections marked with `TODO` (which must be addressed in order for your project to run properly) and `UPDATEME` (optional settings if you feel inclined to);
  - If you use VS Code, install the [`Todo Tree`][wn1] extension to easily locate and jump to these marks, they are already configured in your `settings.json` file;
- [ ] Make sure to create your desired Issue labels on your platform before you start tracking them so it ensures you will be able to filter them from the get-go;
- [ ] Make changes to your CI configurations to better suit your needs.

- In order to reduce user prompts and keep things effective, the template generates files with a few assumptions:
  - It assumes your main git branch is `master`. If you wish to use another branch name for development, be aware of changes you will have to make in the Issue and Merge Request templates and `README.md` file so links won't break when you push them to your repo;
  - It generates a PyPI badge assuming you will be able to publish your project under `python-project-gh-coveralls`, change it otherwise;
  - It generates a Docker badge assuming you also use `galactipy` for Docker Hub and you will push your image under `python-project-gh-coveralls`, change it otherwise.

If you want to put your project on steroids, here are a few Python tools which can help you depending on what you want to achieve with your application:

- [`Typer`][wn2] is great for creating CLI applications;
- [`Rich`][wn3] makes it easy to add beautiful formatting in the terminal;
- [`tqdm`][wn4] is a fast, extensible progress bar for Python and CLI;
- [`Python Prompt Toolkit`][wn5] allows you to create more advanced terminal applications, such as a text editor or even your own shell;
- [`orjson`][wn6], an ultra fast JSON parsing library;
- [`Pydantic`][wn7] is data validation and settings management using Python type hinting;
- [`Returns`][wn8] makes you function's output meaningful, typed, and safe;
- [`Loguru`][wn9] makes logging (stupidly) simple;
- [`IceCream`][wn10] is a little library for sweet and creamy debugging;
- [`Hydra`][wn11] is a framework for elegantly configuring complex applications;
- [`FastAPI`][wn12] is a type-driven asynchronous web framework.

For taking development and exposition of your project to the next level:

- Try out some more badges, not only it looks good, but it also helps people better understand some intricate details on how your project works:
  - You can look at dynamic badges available at [`Shields.io`][wn13];
  - There is a myriad of standardised static badges at [`Simple Badges`][wn14];
  - [`awesome-badges`][wn15] provides a lot of useful resources to help you deal with badges;
- Setup a code coverage service for your tests, popular options include:
  - [`Coveralls`][wn18] and [`Codecov`][wn19] if you need solely test coverage;
  - [`Code Climate`][wn20] and [`Codacy`][wn21] for fully-featured code analysis;
- Add your project to [`OpenSSF Best Practices`][wno1] and [`OSSRank`][wno2] indexes. If you have greater ambitions for your project and/or expects it to scale at some point, it's worth considering adding it to these trackers;
  - There are already badges for those set up in your `README.md` file, just waiting for you to update their URLs with your project's index in both services :beaming_face_with_smiling_eyes:
- Setup a sponsorship page and allow users and organisations who appreciate your project to help raise for its development (and add a badge in the process! :sunglasses:). Popular platforms are:
  - [`Liberapay`][wno3];
  - [`Open Collective`][wno4];
  - [`Ko-fi`][wno5];
  - You can set a [Sponsors account][hubo1] directly integrated into GitHub;
  - Of course, you can also set any kind of gateway you wish, what works best for you and your project!

And here are a few articles which may help you:

- [Open Source Guides][wno6];
- [A handy guide to financial support for open source][wno7];
- [GitHub Actions Documentation][hub3];
- [A Comprehensive Look at Testing in Software Development][wn22] is an article that lays out why testing is crucial for development success. Eric's blog is actually a great reference, covering topics ranging from the basics to advanced techniques and best practices;
- [Robust Exception Handling][wn23];
- [Why Your Mock Doesn't Work][wn24];
- [Managing TODOs in a codebase][wn25];
- Maybe you would like to add [gitmoji][wn26] to commit names. This is really funny. :grin:

## :rocket: Features

### Development features

- Support for `Python 3.9` and higher;
- Uses [`Poetry`][ft1] as the dependency manager and extends functionality with [`dynamic versioning`][new1], [`virtual environment bundling`][new2], dependency [`export`][new3] and [`update resolution`][new4]. See configuration in [`pyproject.toml`][ft2];
- Automatic code formatting with [`ruff`][fo1], with ready-to-use [`pre-commit`][fo2] hooks and several rules already selected for linting;
- Type checks with [`mypy`][ft3], security checks with [`safety`][ft4] and [`bandit`][ft5];
- Testing with [`pytest`][ft6] and [`behaviour-driven development`][bdd1] configuration for managing scenarios; more details in the [Behaviour-Driven Development][bdd2] section;
- Code quality integrations with [`Coveralls`][ft7] via CI/CD;
- Predefined VS Code [`settings.json`][ft8] with quality-of-life configuration for editor, workbench, debugging and more;
- Ready-to-use [`.editorconfig`][ft9], [`.dockerignore`][docker1] and [`.gitignore`][ft10] files. You don't have to worry about those things.

### Deployment features

- Predefined CI/CD build workflow with [`Github Actions`][hub4];
- Automatic package uploads to [`PyPI`][ft11] test and production repositories;
- Everything is already set up for security checks, codestyle checks, code formatting, testing, linting, docker builds etc with [`Invoke`][ft12]. More details in [Invoke Usage][ft13];
- [`Dockerfile`][docker2] for your package, with CI/CD workflows to publish your image to a container registry;
- Always up-to-date dependencies with [`Dependabot`][hub5]. You will only need to [enable it][hub1];
- Automatic drafts of new releases with [`Release Drafter`][hub6]. You may see the list of labels in [`release-drafter.yml`][hub7].

### Project management features

- Issue and Pull Request templates for easy integration with GitHub;
- Workflows to mark and close abandoned issues after a period of inactivity with [`Stale Bot`][hub8].

### Open source community features

- Ready-to-use [Pull Request templates][ft14] and several [Issue templates][ft15];
- Files such as: `LICENCE`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, and `SECURITY.md` are generated automatically;
- **Loads** of predefined [badges][ft16] to make your project stand out, you can either keep them, remove as you wish or be welcome to add even more.

## Installation

```bash
pip install -U python-project-gh-coveralls
```

or install with `Poetry`:

```bash
poetry add python-project-gh-coveralls
```
Then you can run

```bash
python-project-gh-coveralls --help
```

or with `Poetry`:

```bash
poetry run python-project-gh-coveralls --help
```

### Invoke usage

[`invoke`][ft12] contains a lot of functions for faster development.

<details>
<summary>1. Download or remove Poetry</summary>
<p>

To download and install Poetry as a [standalone application][fs1] run:

```bash
invoke poetry-download
```

To uninstall

```bash
invoke poetry-remove
```

Alternatively, you can install it via your package manager (preferred) or any method provided by the [documentation][inv1].

</p>
</details>

<details>
<summary>2. Install all dependencies and pre-commit hooks</summary>
<p>

Install requirements with

```bash
invoke install
```

And then add Poetry plugins to make development easier with

```bash
invoke poetry-plugins
```

Pre-commit hooks could be installed after `git init` via

```bash
invoke pre-commit-install
```

</p>
</details>

<details>
<summary>3. Codestyle</summary>
<p>

Automatic formatting uses `ruff`, and can be run with

```bash
invoke codestyle

# or use synonym
invoke format
```

For formatting checks only, without rewriting files:

```bash
invoke codestyle --check
```

Aside from the formatter, you can also use `ruff` to lint project files with several preconfigured rules defined in `pyproject.toml`:

```bash
invoke check-linter
```

</p>
</details>

<details>
<summary>4. Code security</summary>
<p>

```bash
invoke check-safety
```

This command launches `Poetry` integrity checks as well as identifies security issues with `Safety` and `Bandit`.

Update all dev libraries to the latest version using one command:

```bash
invoke update-dev-deps
```

</p>
</details>

<details>
<summary>5. Type checks</summary>
<p>

Run `mypy` static type checker with

```bash
invoke mypy
```

</p>
</details>

<details>
<summary>6. Tests</summary>
<p>

Run `pytest` with all essential parameters predefined with

```bash
invoke test
```

</p>
</details>

<details>
<summary>7. All code-related checks</summary>
<p>

Of course there is a command to ~~rule~~ run all linters in one:

```bash
invoke sweep
```

The same as:

```bash
invoke test check-linter codestyle mypy check-safety
```

</p>
</details>

<details>
<summary>8. Docker</summary>
<p>

Build your Docker image with the `latest` tag preconfigured with

```bash
invoke docker-build
```

Remove docker image with

```bash
invoke docker-remove
```

More information about Docker [here][docker3].

</p>
</details>

<details>
<summary>9. Cleanup</summary>
<p>

Delete pycache files:

```bash
invoke pycache-remove
```

Remove package build:

```bash
invoke build-remove
```

Delete .DS_STORE files:

```bash
invoke dsstore-remove
```

Remove .mypycache:

```bash
invoke mypycache-remove
```

Or to remove all above run:

```bash
invoke cleanup
```

</p>
</details>


# Behaviour-Driven Development

A `features` directory is placed under `tests`, with [`pytest-bdd`][bdd3] added as a dependency. You should create `.feature` files inside this folder to specify them and describe scenarios using the [Gherkin][bdd4] language:

```
# tests/features/divide.feature
Feature: Divide numbers
  Scenario: Full division
    When I ask the calculator to divide "21" by "7"
    Then the screen should return "3" as an integer

  Scenario: Division by zero
    When I ask the calculator to divide any number by "0"
    Then the screen should return an error message
```

You would then use `pytest-bdd` to wrap each scenario referred in the feature file as a step by step validation:

```py
from mypackage import divide
from pytest_bdd import scenario, when, then

@scenario("divide.feature", "Full Division")
def test_full_division():
    pass

@when("I ask the calculator to divide \"21\" by \"7\"")
def divide_21_7():
    calculation = divide(21, 7)

    return calculation

@then("The screen should return \"3\" as an integer")
def return_integer():
    assert calculation.display == "3"


@scenario("divide.feature", "Division by Zero")
def test_zero_division():
    pass

@when("I ask the calculator to divide any number by \"0\"")
def divide_by_zero():
    calculation = divide(15, 0)

    return calculation

@then("The screen should return an error message")
def return_integer():
    assert calculation.display == "Error"
```

Then you can simply use `pytest` as you normally would to run the test suite and check the results.

For more information on behaviour-driven development and more advanced cases, please check out the [Cucumber documentation][bdd5].


## :chart_with_upwards_trend: Releases

You can see the list of available releases on the [GitHub Releases][r1] page.

We follow [Semantic Versions][fs4] specification.

We use [`Release Drafter`][hub6]. As pull requests are merged, a draft release is kept up-to-date listing the changes, ready to publish when you’re ready. With the categories option, you can categorize pull requests in release notes using labels.

### List of labels and corresponding titles

|               **Label**               |      **Title in Releases**      |
| :-----------------------------------: | :-----------------------------: |
| `enhancement`, `feature`              | :rocket: Features               |
| `bug`, `refactoring`, `bugfix`, `fix` | :wrench: Fixes & Refactoring    |
| `build`, `ci`, `testing`              | :package: Build System & CI/CD  |
| `breaking`                            | :boom: Breaking Changes         |
| `documentation`                       | :memo: Documentation            |
| `dependencies`                        | :arrow_up: Dependencies updates |

You can update it in [`release-drafter.yml`][hub7].

GitHub creates the `bug`, `enhancement`, and `documentation` labels for you. Dependabot creates the `dependencies` label. Create the remaining labels on the Issues tab of your GitHub repository, when you need them.

## :shield: Licence

[![Licence][blic1]][blic2]

This project is licenced under the terms of the `MIT` licence. See [LICENCE][blic2] for more details.

## :page_with_curl: Citation

```bibtex
@misc{Python Project GH Coveralls,
  author = {The Galactipy Contributors},
  title = {Awesome `python-project-gh-coveralls` is a Python cli/package created with https://gitlab.com/galactipy/galactipy},
  year = {2025},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/galactipy/python-project-gh-coveralls}}
}
```

## Credits [![Expand your project structure from atoms of code to galactic dimensions.][bp6]][bp7]

This project was generated with [`galactipy`][bp7].

<!-- Anchors -->

[bp1]: https://img.shields.io/pypi/pyversions/python-project-gh-coveralls?style=for-the-badge
[bp2]: https://pypi.org/project/python-project-gh-coveralls/
[bp3]: https://img.shields.io/pypi/v/python-project-gh-coveralls?style=for-the-badge&logo=pypi&color=3775a9
[bp4]: https://github.com/galactipy/python-project-gh-coveralls
[bp5]: https://github.com/galactipy/python-project-gh-coveralls/releases
[bp6]: https://img.shields.io/badge/made%20with-galactipy%20%F0%9F%8C%8C-179287?style=for-the-badge&labelColor=193A3E
[bp7]: https://kutt.it/7fYqQl
[bp8]: https://img.shields.io/static/v1.svg?label=Contributions&message=Welcome&color=0059b3&style=for-the-badge
[bp9]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/CONTRIBUTING.md
[bp10]: https://github.com/galactipy/python-project-gh-coveralls/issues
[bp11]: https://img.shields.io/endpoint?url=https://python-poetry.org/badge/v0.json&style=for-the-badge
[bp12]: https://python-poetry.org/
[bp13]: https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white&style=for-the-badge
[bp14]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.pre-commit-config.yaml
[bp15]: https://img.shields.io/badge/security-bandit-yellow?style=for-the-badge
[bp16]: https://bandit.readthedocs.io/en/latest/
[bp17]: https://img.shields.io/badge/Editorconfig-E0EFEF?style=for-the-badge&logo=editorconfig&logoColor=000
[bp18]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.editorconfig
[bp19]: https://img.shields.io/badge/semantic%20versions-4053D6?style=for-the-badge&logo=semver

[blic1]: https://img.shields.io/github/license/galactipy/python-project-gh-coveralls?style=for-the-badge
[blic2]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/LICENCE

<!-- TODO Replace the `100` ID with your project's index at https://www.bestpractices.dev/en
[boss1]: https://img.shields.io/cii/level/100?style=for-the-badge&logo=linux-foundation&label=openssf%20best%20practices
[boss2]: https://www.bestpractices.dev/en/projects/100 -->
<!-- TODO Replace the `200` ID with your project's index at https://ossrank.com/
[boss3]: https://shields.io/endpoint?url=https://ossrank.com/shield/200&style=for-the-badge
[boss4]: https://ossrank.com/p/200 -->


[bcov1]: https://img.shields.io/coverallsCoverage/github/galactipy/python-project-gh-coveralls?style=for-the-badge&logo=coveralls
[bcov2]: https://coveralls.io/github/galactipy/python-project-gh-coveralls

[fs1]: https://github.com/python-poetry/install.python-poetry.org
[fs2]: https://python-poetry.org/docs/
[fs3]: https://python-poetry.org/docs/cli/#commands
[fs4]: https://semver.org/
[fs5]: https://git-scm.com/book/en/v2/Git-Basics-Tagging

[wn1]: https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree
[wn2]: https://github.com/tiangolo/typer
[wn3]: https://github.com/willmcgugan/rich
[wn4]: https://github.com/tqdm/tqdm
[wn5]: https://github.com/prompt-toolkit/python-prompt-toolkit
[wn6]: https://github.com/ijl/orjson
[wn7]: https://github.com/samuelcolvin/pydantic/
[wn8]: https://github.com/dry-python/returns
[wn9]: https://github.com/Delgan/loguru
[wn10]: https://github.com/gruns/icecream
[wn11]: https://github.com/facebookresearch/hydra
[wn12]: https://github.com/tiangolo/fastapi
[wn13]: https://shields.io/badges/static-badge
[wn14]: https://badges.pages.dev/
[wn15]: https://github.com/badges/awesome-badges
[wn16]: https://www.bestpractices.dev/en
[wn17]: https://ossrank.com/
[wn18]: https://coveralls.io/
[wn19]: https://about.codecov.io/
[wn20]: https://codeclimate.com/velocity/what-is-velocity
[wn21]: https://www.codacy.com/
[wn22]: https://pytest-with-eric.com/introduction/types-of-software-testing/
[wn23]: https://eli.thegreenplace.net/2008/08/21/robust-exception-handling/
[wn24]: https://nedbatchelder.com/blog/201908/why_your_mock_doesnt_work.html
[wn25]: https://medium.com/babylon-engineering/todo-find-a-title-for-the-article-fee79708ca15
[wn26]: https://gitmoji.dev/

[wno3]: https://liberapay.com/
[wno4]: https://opencollective.com/
[wno5]: https://ko-fi.com/
[wno6]: https://opensource.guide/
[wno7]: https://github.com/nayafia/lemonade-stand

[ft1]: https://python-poetry.org/
[ft2]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/pyproject.toml
[ft3]: https://mypy.readthedocs.io
[ft4]: https://docs.safetycli.com/safety-2/
[ft5]: https://bandit.readthedocs.io/en/latest/
[ft6]: https://docs.pytest.org/en/latest/
[ft7]: https://coveralls.io/
[ft8]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.vscode/settings.json
[ft9]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.editorconfig
[ft10]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.gitignore
[ft11]: https://pypi.org/
[ft12]: https://docs.pyinvoke.org/en/stable/
[ft13]: #invoke-usage
[ft14]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.github/PULL_REQUEST_TEMPLATE.md
[ft15]: https://github.com/galactipy/python-project-gh-coveralls/tree/master/.github/ISSUE_TEMPLATE
[ft16]: https://shields.io/

[inv1]: https://python-poetry.org/docs/#installation

[r1]: https://github.com/galactipy/python-project-gh-coveralls/releases

[bscm1]: https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white
[bscm2]: https://img.shields.io/github/v/release/galactipy/python-project-gh-coveralls?style=for-the-badge&logo=semantic-release&color=347d39
[bscm3]: https://img.shields.io/github/issues/galactipy/python-project-gh-coveralls?style=for-the-badge&color=bc4c00
[bscm4]: https://img.shields.io/github/issues-pr/galactipy/python-project-gh-coveralls?style=for-the-badge&color=1f883d
[bscm5]: https://github.com/galactipy/python-project-gh-coveralls/pulls
[bscm6]: https://img.shields.io/github/actions/workflow/status/galactipy/python-project-gh-coveralls/build.yml?style=for-the-badge&logo=github
[bscm7]: https://github.com/galactipy/python-project-gh-coveralls/actions/workflows/build.yml

[hub1]: https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuring-dependabot-version-updates#enabling-dependabot-version-updates
[hub2]: https://github.com/marketplace/actions/close-stale-issues
[hub3]: https://help.github.com/en/actions
[hub4]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.github/workflows/build.yml
[hub5]: https://docs.github.com/en/code-security/dependabot
[hub6]: https://github.com/marketplace/actions/release-drafter
[hub7]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.github/release-drafter.yml
[hub8]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.github/.stale.yml

[hubo1]: https://github.com/sponsors

[bdocker1]: https://img.shields.io/docker/v/galactipy/python-project-gh-coveralls?style=for-the-badge&logo=docker&logoColor=lightblue&label=image&color=lightblue
[bdocker2]: https://hub.docker.com/r/galactipy/python-project-gh-coveralls

[docker1]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/.dockerignore
[docker2]: https://github.com/galactipy/python-project-gh-coveralls/blob/master/docker/Dockerfile
[docker3]: https://github.com/galactipy/python-project-gh-coveralls/tree/master/docker

[bfo1]: https://img.shields.io/badge/code%20style-ruff-261230?style=for-the-badge&labelColor=grey
[bfo2]: https://docs.astral.sh
[bfo3]: https://img.shields.io/badge/imports-isort-1674b1?style=for-the-badge&labelColor=ef8336
[bfo4]: https://pycqa.github.io/isort/

[fo1]: https://black.readthedocs.io/en/stable/
[fo2]: https://pre-commit.com/

[bli1]: https://img.shields.io/badge/docstrings-numpydoc-4dabcf?style=for-the-badge&labelColor=4d77cf
[bli2]: https://numpydoc.readthedocs.io/en/latest/format.html

[bbbd1]: https://img.shields.io/badge/BDD-23D96C?style=for-the-badge&logo=cucumber&logoColor=white
[bbbd2]: https://cucumber.io/

[bdd1]: https://cucumber.io/
[bdd2]: #behaviour-driven-development
[bdd3]: https://pytest-bdd.readthedocs.io/en/latest/
[bdd4]: https://cucumber.io/docs/gherkin/reference
[bdd5]: https://cucumber.io/docs
