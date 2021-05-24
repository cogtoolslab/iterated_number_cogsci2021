
Where do written numerals come from? Why do they emerge in societies, and take the diverse forms that they do? This repo contains an experiment beginning to answer that question. It involves a simple communication game to see what constraints lead people to use different kinds of graphical representations of number.


Below is a guide to the various directories in this repo.

## analysis
**iternum_analysis.ipynb** - notebook for processing the draw_number task data. Generates dataframe for **stats_iternum.Rmd**

**iternum_recog_analysis.ipynb** - notebook for processing the classify_iternum task data. Generates dataframe for **recog_stats.Rmd**.

**iternum_feature_analysis.ipynb** - notebook for processing the VGG-19 predictions. Generates dataframe for **clf_stats.Rmd**.


**stats_iternum.Rmd** - R markdown for original production task performance.

**recog_stats.Rmd** - R markdown for recognition task performance.

**clf_stats.Rmd** - R markdown for VGG-19 performance.



## experiments
**app.js** - active for draw_number

**app1.js** - active for classify_iternum

**store.js** - must be running to store data during experiment

### draw_number
Experimental code for original, production task, consisting of 4 shapes by 8 cardinalities.
Data collected in early 2020.

### classify_iternum
Experimental code for the recognition study, wherein people classified sketches from the original study either by shape or cardinality.
Data collected from the end of 2020 through early April 2021.



## experiments
### draw_number
Materials for creating the stimuli of the production task.

**animal_silhouettes** contains silhouettes of animals found with Creative Commons licenses.

**stim_generator.ipynb** creates stimuli out of the images found in that directory, while **upload_stims_to_s3.ipynb** stores them on Amazon storage services.

### classify_iternum
Materials for creating stimuli of the recognition task. **catch_trial_stimuli** includes several hand-drawn catch-trial stimuli made to resemble the classification buttons as closely as possible. **generate_metadata.ipynb** accesses stored sketches from the production task and assembles them into groups with one sketch from every participant. Those groups constitute 61 different paradigms, shown at random to participants in the recognition task. **generate_metadata.ipynb** then stores these groups of stimuli on Amazon storage services.



## utils
Contains important code for analysis notebooks.

**extract_features.py** runs the VGG-19 analysis on original production sketches, which must be rendered already from **iternum_analysis.ipynb**; **embeddings.py** is called in that process.

**utils.py** is used by **analysis/iternum_analysis.ipynb**.



