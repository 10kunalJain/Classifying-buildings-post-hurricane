# Classifying-buildings-post-hurricane
After a hurricane in populated as well as sparse areas of human settlements, the very next thing after human rescue is the damage assessment. This is very critical for emergence managers as it helps them in efficint response and proper resource allocation. The only way for doing this is using ground survey or drones to manually quantify the number of flooded or damaged buildings. But this process being highly labour intensive and time taking, other efficint and faster methods have to be developed.

Having access to satellite imagery, its capabilities can easily be harnessed for this task. We can take satellite images of hurricane damaged areas, extract square size images containing one or group of buildings (using building coordinates) and use those square images to train a neural netwrok which can easily predict which building is damaged and which is not, how many buildings in a locality is damaged, etc. for any new satellite images of a particular area. This method will be cost efficint, easier and way faster and will help emergency managers accurately plan the resource requirement and efficiently distribute resources to those in need. In this notebook, we have used the square images of buildings in hurricane hit areas (which has been already extracted from satellite images) to train our model, to see how much accurate a deep learning model can be in classifying damaged and not-damaged buildings, and drawing inferences as to whether this method can be used in the post-hurricane emergency situation.

Our main focus in this notebook is to see how different SOTA models perform on the given dataset for the task of classification, compare them with our custom built model and understand which part of the image any CNN model usually focusses on to be able to classify it as damaged or not-damaged.

Following is the broader description of the work carried out in this notebook:

1.Creating an image data pipeline: To access images as datasets, do necessary transformations and prefetching for optimal utilization computing resourses.

2.Building model architecture: Creating layer by layer whole CNN network in case of custom model or importing a SOTA model, customizing it and compiling it on MultiOptimizer.

3.Training of model using the dataset

4.Extracting inferences and comparison of model performaces: For both balanced and unbalanced test sets.

5.Visualzing which part of the image model uses to make its prediction: Using both Saliency Mapping and GradCam.
