# Julia

## Downloading Julia

Go to the [Julia Downloads page](https://julialang.org/downloads/) and download the latest stable release.

Once downloaded, extract the contents of the zip file to a location we want to store the files.
In my case that is `~/julia`.


## Command Line Access

To make the version of Julia you just downloaded and extracted available from the command line, we will want to export the path in our `.bashrc` file.
Let's do this by adding the following lines to the end of the `.bashrc` file:

```{bash}
# julia
export PATH=${PATH}:$HOME/julia/julia-1.3.0/bin
```

Notice that the path uses the location where I decided to store the julia files.

After saving and closing the `.bashrc` file, to activate the changes in our current terminal window:

```{bash}
source .bashrc
```

## Verifying Julia Install

Enter the following into the command line:

```{bash}
julia --version
```

which should yield the following

```{out}
julia version 1.3.0
```