![MIT license](https://img.shields.io/badge/License-MIT-green.svg)

The below is an explanation of what and how we work in Text Corpus Labs.
It serves as a reminder of the team's global research goals.

# Raison d'être

We are a collection of researchers focused on _collecting_ different modes of human communication through text.
We want to share our work and ways of working with the broader academic community.

To this end we:

* Create guidance on how to standardize the format of a text corpus.
  All the members of our lab have come to an understanding as to how a text corpus should look _prior_ to being analyzed.
* Create processes to automate the collection of text corpora from _existing_ resources.
  Scraping and parsing can be challenging at times.
  Our goals are to allow the reuse of a text corpus with the lowest barrier to entry for a new analysis.
* Curate _unique_ corpora.
  It has been well known for quite some time that humans have different modes of communication.
  Text corpora reflect this difference.
  When a new mode of communication is believed to exist, we try to capture a sample of that mode.
* Provide a "Methods and Materials" boilerplate describing how the corpus was collected.
* Provide a citable [DOI](https://guides.github.com/activities/citable-code/) for the _process_.
  For _unique_ corpora, we provide the [DOI](https://www.doi.org/) to the _article_ where the text corpus was introduced.

So that you can:

* Get a text corpus on your local device with as little effort as possible.

# Citations

It is always nice to see others build upon your efforts.
If you use our work, please cite it using the provided [DOI](https://www.doi.org/).

# Getting the code to work

As of now, all members of our lab work on Windows PCs and program in Python.
If that changes in the future, we will likely update this section to include other methods.

## Prerequisites

The following packages need to be installed.
You can use any method to install the prerequisites.
On a Windows device, I recommend using [Chocolatey](https://chocolatey.org/install).
If you decide to use Chocolatey, open an _admin_ PowerShell prompt, and run the code snippet below.

* [7-zip](https://www.7-zip.org/)
* [Python](https://www.python.org/downloads/)
  
```{ps1}
if('Unrestricted' -ne (Get-ExecutionPolicy)) { Set-ExecutionPolicy Bypass -Scope Process -Force }
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
refreshenv

choco install 7zip -y
choco install python3 -y
```

## Python

Unless otherwise noted in the repository directly, all scripts have been tested on Python 3.9.x.
In addtion to the steps below, each repository's `README.md` will contain a list of any special instructions.
After running the steps here, run the special instructions.

1. Clone this repository then open an _Admin_ shell to the `~/code` directory.
2. Install the required modules.
   ```{shell}
   pip install -r requirements.txt
   ```
  
When writing any code that uses an external dependency, the version of that dependency needs to be declared.
All the version information can be found in the repository’s `~/code/requirements.txt` file.
You _may_ be able to run different versions, especially if it is just a _minor_ revision, but if the _exact_ version is not used, YMMV.

## Steps

All the repositories contain a "Steps" section in the `README.md`.
Please follow those guides to retrieve the text corpus.

You will likely want to perform additional text processing _after_ retrieving the text corpus.
Our goal is to provide you with a clean _base_ to perform an analysis, **not** to be opinionated on what you do next.
When completing your study, please remember to keep track of this difference.
Doing so will better allow you to write your "Methods and Materials" section; using (and citing) our steps, then applying (and highlighting) your unique contribution.
