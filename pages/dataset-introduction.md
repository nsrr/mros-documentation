# Dataset introduction

The [MrOS dataset](:files_path:/datasets) posted on the NSRR has gone through various post-processing steps in order to prepare the data for more widespread sharing. The dataset was based upon data prepared by the [San Francisco Coordinating Center](http://coordinatingcenter.ucsf.edu/research/studies.php). Changes and updates to the source data and variable definitions have been coordinated in the [mros-data-dictionary repository](https://github.com/sleepepi/mros-data-dictionary).

## Structure of the dataset

The core dataset is broken down into two (2) files that correspond to the MrOS Sleep encounters:

1. `visit1` (Sleep Visit 1) -- the baseline exam conducted between 2003 and 2005
  - 2,911 rows, corresponding to all subjects that had successful overnight polysomnography at this visit
2. `visit2` (Sleep Visit 2) -- the follow-up exam conducted between 2009 and 2012
  - 2,911 rows, though only 1,026 subjects had repeated sleep measures
