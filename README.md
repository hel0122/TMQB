[![Jupyter Book Badge](https://jupyterbook.org/badge.svg)](https://github.com/TheMulQuaBio/TMQB)

# The Multilingual Quantitative Biologist - Source

This is the main source code repository of the **The Multilingual Quantitative
Biologist** (TMQB) online book.

## Requirements

All code in this project was written in and tested with R 4.xx, Python 3.xx and GNU bash 5.xx. 

To check the software needed to compile and deploy this book or run its jupyter notebooks, please check the  `requirements.txt` file here.

> ⚠️ **Note:** Please read the "Getting Started" section below before installing anything on your local computer!

## Contributing

TMQB is a collaborative project. Contributions are welcome, and they are greatly appreciated! Every little bit
helps, and credit will always be given. You can contribute in the ways listed
below.

### Report Bugs

Report bugs using GitHub issues.

If you are reporting a bug, please include:

* Your operating system name and version.
* Any details about your local setup that might be helpful in troubleshooting.
* Detailed steps to reproduce the bug.

### Fix Bugs

Look through the GitHub issues for bugs. Anything tagged with "bug" and "help
wanted" is open to whoever wants to implement it.

### Implement Features

Look through the GitHub issues for features. Anything tagged with "enhancement"
and "help wanted" is open to whoever wants to implement it.

### Write Documentation

TMQB could always use more documentation, whether as part of the official docs, in docstrings, or even on the web in blog posts, articles, and such.

### Submit Feedback

The best way to send feedback or propose a feature is to file an issue on GitHub.

If you are proposing a feature:

* Explain in detail how it would work.
* Keep the scope as narrow as possible, to make it easier to implement.
* Remember that this is a volunteer-driven project, and that direct contributions are welcome :)

## Getting Started

Ready to contribute? Here's how to set up TMQB for local development.

### Set up the dev environment

Set up your local Jupyter book dev environment. For this it is strongly recommended that you use a virtualenv, e.g., using [`conda`](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)  or the simpler [`venv`](https://docs.python.org/3/library/venv.html).

> ⚠️ **Note:** Specific venv instructions for Ubuntu / Debian Linux-based systems are [here](https://themulquabio.github.io/TMQB/notebooks/Appendix-JupyIntro.html#installing-jupyter).

Once you have activated your virtual environment, run `pip install -r requirements.txt`.

In addition, if you will be contributing content that involves running `R` or or `bash`, you will need to manually install two Jupyter [kernels](https://themulquabio.github.io/TMQB/notebooks/Appendix-JupyIntro.html#language-kernels) in addition to Python (R and bash) (Python is the default Jupyter book kernel). 

### Create local copy

Fork (optional) the repo on GitHub, and clone locally.

### Create a branch and make changes

Create a branch for local development and make changes locally (e.g., to a Jupyter notebook corresponding to a specific chapter). 

## Build the book locally

Test the changes and compile the book locally to make sure it all looks good when rendered in html. To build a local version of the book in your current branch:

- `cd` to its root directory (i.e., `TMQB/`)  
- Run `jupyter-book build content`

A fully-rendered HTML version of the book will be built in `_build/html/`. That is, there should be a collection of newly generated HTML files in the `content/_build/html` folder. 

Check to ensure that HTML has been built of the complete book by loading `_build/html/notebooks/index.html` in a web browser. Also test some of the navigation links within the book.

> ⚠️ **Note:** If you run into any issues with the rendered book, try removing the existing `The Multilingual Quantitative Biologist/_build/` directory and rebuilding the book

### Commit and push

Once you are happy that the book has been built including your updates, `git add`, `commit` and `push` your changes to the branch. 

> ⚠️ **Note:** *Please do not push changes for every little edit you make to the book (e.g., after fixing some typos)*. Push only significant changes. But don't make a whole slew of changes, such as edits / additions to several chapters either! In general, follow [good git practices](https://themulquabio.github.io/TMQB/notebooks/03-Git.html#teamwork-using-git-and-common-branching-mistakes) in this respect. **Remember, you can deploy the book (by pushing to the `gh-pages` branch using `ghp-import` as explained below) without pushing changes to the `master` branch.**


## Create a pull request  

After pushing to your new "feature" branch, submit a [pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/about-pull-requests) through the TMQB GitHub project website (also see [this](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)).

The `master` branch of this repository is protected, so even users with write (push) access need to push changes on a branch and make pull requests.

Note that new commits to a non-master branch *after* a pull request has been made will result in any pull requests from that non-master branch to be discarded. Please [read this](https://gist.github.com/digitaljhelms/4287848) for good practices for branching (and merging).


### Hosting/Deploying the book online

The compiled html rendered version of the book is hosted on the `gh-pages` branch of this repo, which is then  deployed on [https://themulquabio.github.io/TMQB](https://themulquabio.github.io/TMQB/intro.html). 

To deploy the book online manually simply run:

`ghp-import -n -p -f content/_build/html`

This will automatically push the latest build to the `gh-pages` branch. 

Typically after a few minutes the site should be viewable online at [https://themulquabio.github.io/TMQB/intro.html](https://themulquabio.github.io/TMQB/intro.html). If not, check repository settings under Options -> GitHub Pages to ensure that the gh-pages branch is configured as the build source for GitHub Pages.

More information on this hosting process can be found [here](https://jupyterbook.org/en/stable/publish/web.html).

> ⚠️ **Note:** We do not currently use GitHub actions to automatically build and deploy the book to the `gh-pages` branch. This is a [currently pending issue](https://github.com/TheMulQuaBio/TMQB/issues/132)); please feel free to tackle it if you wish!

## Additional notes

* The solutions to the exercises in this book are in a [separate private git repo](https://github.com/TheMulQuaBio/TMQB_Sols) under this organization.

* The `results` directory in `content` is populated when scripts are run, but these are not version controlled (all files in this directory under `.gitignore`).

### Code of Conduct

Please note that TMQB is released with a [Contributor Code of Conduct](CONDUCT.md). By contributing to this project you agree to abide by its terms.

We welcome and recognize all contributions. You can see a list of current contributors in the [contributors tab](https://github.com/TheMulQuaBio/TMQB/graphs/contributors).


## Credits

* This project is created using the excellent open source [Jupyter Book project](https://jupyterbook.org/), initiated using [executablebooks/cookiecutter-jupyter-book template](https://github.com/executablebooks/cookiecutter-jupyter-book).
* The computing sections were originally inspired by, and many of the materials are based on Stefano Allesina's excellent notes back when Samraat was a Postdoc in the Allesina Lab. Check out [the book](https://computingskillsforbiologists.com/)! 
* Most of the chapters under the Data Analysis and Basic Statistics section were originally written by David Orme (<d.orme@imperial.ac.uk>).