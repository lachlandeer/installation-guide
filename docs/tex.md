# LaTeX

Ultimately we all write in TeX.

To install TeX with all the bells and whistles:

```{bash}
sudo apt-get install texlive-full
```

This installation is quite large, and installs tonnes of stuff I don't use, including language packs. 
If you are a light tex user, this one probably suffices:

```{bash}
sudo apt-get install texlive-latex-extra
```

I tried this one, but fontawesome wasn't included (at least this was the first issue I had) - so I had to go the full install in the end.

## Verify Your Install:

Check everything goes according to plan:

```
tex --version
```

which gives the following output:

```{}
TeX 3.14159265 (TeX Live 2019/Debian)
kpathsea version 6.3.1
Copyright 2019 D.E. Knuth.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the TeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the TeX source.
Primary author of TeX: D.E. Knuth.
```

The version numbers might differ as we progress in time.