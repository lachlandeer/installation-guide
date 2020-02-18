# Text Editors

Here are two alternatives:

* VS Code - which I am currently using / transitioning towards
* Atom - what I used to use, and still feel attached to

## VS Code

```{bash}
sudo snap install --classic code # or code-insiders
```

### Verifying VS Code Install

```{bash}
code --version
```

yields something like:

```{out}
1.41.0
9579eda04fdb3a9bba2750f15193e5fafe16b959
x64
```

### Extra VS Code packages

Here's what I am running at the moment:

* Nord Wave (color theme)
* Bracket Pair Colorizer 2
* Code Spell Checker
* Git Graph
* Git History
* Julia
* Julia Formatter
* LaTeX Workshop
* Markdown All in One
* Markdown PDF
* Markdown Preview Enhanced
* markdownlint
* Python
* R
* r-check
* TODO Highlight
* vscode-icons
* vscode-pdf
* Whitespacer
* YAML


## Atom

Enter the following information to add a repository that has the Atom installation, then press Return:

```{bash}
wget -qO - https://packagecloud.io/AtomEditor/atom/gpgkey | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] https://packagecloud.io/AtomEditor/atom/any/ any main" > /etc/apt/sources.list.d/atom.list'
sudo apt-get update
```

Install Atom by entering the following commands into a terminal and then pressing Return:

```{bash}
sudo apt-get install atom
```

### Verifying Atom Installation

We want Atom to be available from the command line. Then open your terminal and type the following into the command line:

```{bash}
atom --version
```

followed by pressing Return you should see output like the following

```{out}
Atom    : 1.44.0
Electron: 4.2.7
Chrome  : 69.0.3497.128
Node    : 10.11.0
```

But expect the version numbers to have changed

### Extra Atom Packages

Here's a non-exhaustive list of packages I typically add to Atom:

* autocomplete-R
* autocomplete-python (choose Jedi as your engine when asked)
* autoflow
* language-r
* linter
* linter-lintr
* tablr
* platformio-ide-terminal
* project-plus
* language-markdown
* markdown-table-editor
* markdown-preview-plus
* autocomplete-citeproc
* open-unsupported-files
* advanced-open-file
* language-latex
* atom-latex
* whitespace