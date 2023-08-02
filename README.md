# Procedure
Convert the audio file into a spectrogram to make the input 2D allowing the use of CNNs and LSTMs.  The model starts with a Bi-LSTM to pick up relationships between the unchanged data over time.  CNNs are used to find local patterns like where the signal spikes or drops 
(which for this problem is important).  A Bi-LSTM finishes the process by finding long-range relationships among the patterns found by the CNN layers.  Since the data set is small (much less than 10,000) the model was overfitting itself so dropout and max pooling layers were added
to prevent this.  The model achieved 99% accuracy on both the validation and test data.
