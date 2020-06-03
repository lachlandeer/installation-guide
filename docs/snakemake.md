# Snakemake

Snakemake is my default workflow manager right now.
Think of it like make - but designed for for the kind or work *we actually do*.

It's a Python library, so install via pip:

```
pip install snakemake
```

## Verify Install

```{bash}
snakemake --version
```

which gives:

```{out}
5.8.1
```


!!! warning
    Notice that the Snakemake developers release new versions *very frequently* - and there can be breaking changes.
    Thus sometimes we may want a specific version installed. 
    In this case, for example:

    ```
    pip install snakemake==5.4.3
    ```
    
    installs version 5.4.3 and uninstalls any existing version in the current environment.
