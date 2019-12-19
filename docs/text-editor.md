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

## Atom

Enter the following information to add a repository that has the Atom installation, then press Return:

```{bash}
sudo add-apt-repository ppa:webupd8team/atom
```

Install Atom by entering the following commands into a terminal and then pressing Return:

```{bash}
sudo apt update
sudo apt install atom
```

### Verifying Atom Installation
We want Atom to be available from the command line. For Mac and Linux Users this is the default after you have started the program once. So please open Atom. Then open your terminal and type the following into the command line:

```{bash}
atom --version
```

followed by pressing Return you should see output like the following

```{out}
Atom    : 1.28.2
Electron: 2.0.5
Chrome  : 61.0.3163.100
Node    : 8.9.3
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