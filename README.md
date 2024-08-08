Image_Captioning Using LSTM

Dataset - Flickr_8K
In Flickr_8K dataset, all the images of training, validation and test set are in one folder.

It contains 3 different files i.e Flickr_8k.trainImages.txt,Flickr_8k.testImages.txt, Flickr_8k.devImages.txt corresponding to each type of dataset i.e train, test and validation set, each file having file_name of images conatined in each dataset.

Each image is given 5 different captions by 5 different humans. This is because an image can be described in multiple ways.These captions are stored in 'Flickr8k.token.txt'.

Link to Dataset

https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.zip


Model
ResNet50 was used as an image encoder to encode the images which were then input in the model.

Keras embedding layer was used to generate word embeddings on the captions which were encoded earlier.

The embeddings were then passed into LSTM after which the image and text features were combined and sent to a decoder network to generate the next word.


Average Bleu Score on Test Set

Greedy Search: 0.4776

Beam Search with k=3: 0.4930
