## Feature Selection

Using [this documentation](https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html) on the exoplanet data, I chose the following measurements to use:

### Star Measurements

* Mass: 'koi_slogg'
* Temperature: 'koi_steff'
* Radius: 'koi_srad'

### 'Planet' Measurements

* Radius: 'koi_depth', 'koi_prad'
* Orbital Speed: 'koi_duration', 'koi_period'
* Temperature: 'koi_teq', 'koi_insol'

I left the rest of the data columns out of my models, as they were more indicative of the measuring process than of the objects of interest themselves.

## Accuracy

* SVC Model: .882
* KNN Model: .846
* Deep Learning Model: .883/.884

## Findings

I would not use this model on its own to find new exoplanets. However, this model could be useful in prioritizing which objects to take a closer and more accurate look at. 

These models could potentially be improved by further narrowing down the features selected, for instance if one measurement of the object of interest's radius is more accurate than the other. It could also be improved by breaking down the results into more clusters. There must be several different types of exoplanets and other, non-planet objects in the dataset, and separating them out could give a better picture of what is making some of these objects hard to classify. There could also be some types of exoplanets that are more distinct, that we would identify with much greater accuracy. The deep learning model consistently does best with the highest number of epochs in the grid, so it could probably be improved with more computing power and time. Of course, more measurements or a more powerful telescope would also improve modeling!

