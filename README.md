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

When new or revised homework files are posted, pull them into your copy of
this project. In RStudio, open the **Terminal** tab (next to Console) and run:

```bash
git pull
```

You can also click the blue **Pull** arrow in the **Git** pane. Your own work
(finished homework, uploaded data files) won't be touched unless you've
edited a file that the update also changes. If `git pull` complains that
your local changes "would be overwritten," ask before doing anything else.
