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

