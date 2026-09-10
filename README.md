# CDAE 7990 Workspace

Starting-point R project for CDAE 7990 (Applied Data Science & Visualization),
Fall 2026. This is the template used to seed each student's Posit Cloud
workspace via a deployed Assignment. You shouldn't need to touch anything
here beyond running `setup.R` once.

## What's pre-installed

Run this once, in the R console, if packages aren't already available:

```r
source("setup.R")
```

Installs: tidyverse, sf, tidycensus, tigris, ggspatial, rmarkdown, quarto,
terra, mapgl.

## Census API key

`tidycensus` needs a (free) Census API key, but don't share one key across
the class. Get your own at https://api.census.gov/data/key_signup.html and
set it once per session:

```r
tidycensus::census_api_key("YOUR_KEY_HERE", install = TRUE)
```

## Getting updates

When a new homework is released, you'll be told which file to grab. In
RStudio, open the **Terminal** tab (next to Console, *not* the Console
itself) and run these two lines, swapping in the file name you were given:

```bash
git fetch
git checkout origin/main -- homework/hw3.qmd
```

This replaces only the file you name. Everything else in your project
(your other homework, uploaded data, anything you've created) is left alone.

Two rules keep this safe:

- **Don't start a homework file until it's been released.** The command
  above overwrites the file you name, so anything already typed into it
  would be lost.
- **Don't use `git pull` or the Pull button in the Git pane.** They try to
  update every file at once and will refuse to run once you've edited your
  homework.
