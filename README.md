### Bioacoustic-Sound-Detector

Intro to the project
“Visionary Perspective Plan (2020-2030) for the conservation of avian diversity, their ecosystems, habitats and landscapes in the country”  proposed by the Indian government to help in the conservation of birds and their habitats inspired me to take up this project . Extinction of bird species is an increasing global concern as it has a huge impact on food chains. Bioacoustic monitoring can  provide a passive, low labor, and cost-effective strategy for studying endangered bird populations. Recent advances in machine learning have made it possible to automatically identify bird songs for common species with ample training data. This innovation makes  it easier for researchers and conservation practitioners to accurately survey population trends and they'll be able to regularly and more effectively evaluate threats and adjust their conservation actions.
The deep learning prototype can process continuous audio data and then acoustically recognize the species .
The goal of the project when I started was to build a basic prototype for monitoring of rare bird species in India . In future I would like to expand the project to monitor other endangered species as well .  


Which Google ML products did you use?

The google ML products which were used are TensorFlow and Cloud TPUs .
The data was converted to TFRecords and the entire code was written in TensorFlow . The model was trained in Cloud TPUs .

How did you build the dataset?

BirdClef 2022 challenge dataset which consists of short recordings of individual bird calls consists of short recordings of individual bird calls generously uploaded by users of xenocanto.org. These files have been downsampled to 32 kHz where applicable to match the test set audio and converted to the ogg format.

Brief overview of the dataset used for training is below

train_metadata.csv - A wide range of metadata is provided for the training data. The most directly relevant fields are:
primary_label - a code for the bird species. You can review detailed information about the bird codes by appending the code to https://ebird.org/species/, such as https://ebird.org/species/amecro for the American Crow.
secondary_labels: Background species as annotated by the recordist. An empty list does not mean that no background birds are audible.
author - the eBird user who provided the recording.
filename: the associated audio file.
rating: Float value between 0.0 and 5.0 as an indicator of the quality rating on Xeno-canto and the number of background species, where 5.0 is the highest and 1.0 is the lowest. 0.0 means that this recording has no user rating yet.
train_audio/ - The training data consists of short recordings of individual bird calls generously 
scored_birds.json - The subset of the species in the dataset that are scored.
eBird_Taxonomy_v2021.csv - Data on the relationships between different species.
 
Link to the dataset : https://www.kaggle.com/competitions/birdclef-2022/data


Trouble-shooting

Conversion of the model to TFJS format was challenging and there were errors which couldn’t be resolved. Hence I used Flask to build browser based applications .

