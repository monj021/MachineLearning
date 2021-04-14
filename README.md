Keras Model
●	Increasing number of epochs improved accuracy.
●	 When loss function is  "categorical_crossentropy" works better than "mean_squared_error" for all cases for exam data.
●	 Increasing number of hidden layers also improve accuracy as shown below
This approach works the best for linearly separable data. 
 Exam dataset analysis:
Layer (type)                 Output Shape              Param #   
=================================================================
dense_25 (Dense)             (None, 30)                90        
_________________________________________________________________
activation_25 (Activation)   (None, 30)                0         
_________________________________________________________________
dense_26 (Dense)             (None, 30)                930       
_________________________________________________________________
activation_26 (Activation)   (None, 30)                0         
_________________________________________________________________
dense_27 (Dense)             (None, 2)                 62        
_________________________________________________________________
activation_27 (Activation)   (None, 2)                 0         
=================================================================
Total params: 1,082
Trainable params: 1,082
Non-trainable params: 0
Analysis with number of hidden layers for ‘Mean squared error’ and ‘categorical_crossentropy’

100 epoch 30 Hidden layers loss='mean_squared_error'
Epoch 100/100 72/72 [==============================] - 0s 2ms/step - loss: 0.2339 - acc: 0.5556 - val_loss: 0.3088 - val_acc: 0.0000e+00 80/80 [==============================] - 0s 100us/step Test score: 0.24059338569641114 Test accuracy: 0.5 array([1, 1, 0, 1], dtype=int64)
400 epoch 30 Hidden layers loss='mean_squared_error'
Epoch 400/400 72/72 [==============================] - 0s 2ms/step - loss: 0.2181 - acc: 0.6389 - val_loss: 0.2650 - val_acc: 0.5000 80/80 [==============================] - 0s 137us/step Test score: 0.22156924605369568 Test accuracy: 0.6375 array([1, 0, 0, 1], dtype=int64)

100 epoch 60 Hidden layers loss='mean_squared_error'
Epoch 100/100 72/72 [==============================] - 0s 2ms/step - loss: 0.2349 - acc: 0.5694 - val_loss: 0.3136 - val_acc: 0.1250 80/80 [==============================] - 0s 112us/step Test score: 0.2387007236480713 Test accuracy: 0.5125 array([1, 0, 0, 1], dtype=int64)
400 epoch 60 Hidden layers loss='mean_squared_error'
Epoch 400/400 72/72 [==============================] - 0s 2ms/step - loss: 0.2143 - acc: 0.6250 - val_loss: 0.2023 - val_acc: 0.7500 80/80 [==============================] - 0s 163us/step Test score: 0.21088625192642213 Test accuracy: 0.6375 array([1, 1, 0, 1], dtype=int64)
100 epoch 30 Hidden layers loss='categorical_crossentropy'
Epoch 100/100 72/72 [==============================] - 0s 2ms/step - loss: 0.6515 - acc: 0.6111 - val_loss: 0.7914 - val_acc: 0.3750 80/80 [==============================] - 0s 137us/step Test score: 0.6593329429626464 Test accuracy: 0.5625 array([0, 0, 0, 0], dtype=int64)
400 epoch 30 Hidden layers loss='categorical_crossentropy'
Epoch 400/400 72/72 [==============================] - 0s 2ms/step - loss: 0.5992 - acc: 0.6806 - val_loss: 0.6280 - val_acc: 0.6250 80/80 [==============================] - 0s 187us/step Test score: 0.5926139712333679 Test accuracy: 0.65 array([0, 0, 0, 0], dtype=int64)

It all depends on the type of data that we consider.Increasing epoch can increase accuracy in this case.

Learning rate i considered to be 0.001. If we increase that accuracy decreased again.





Comparison of Perceptron Vs Keras Model

Perceptron work with thresholds for classification.The perceptron agree that any output above a certain threshold belong to one class while the output lower that that might be the other class. The straight line where output equals the threshold is then boundary of two classes.

On comparing the loss that occur on both the models I made a conclusion that loss is more in case of perceptron, but worked better when the data is linearly separable.

But on comparing the loss of keras to perceptron. Keras model performed better as it was capable to give more accuracy and less loss when we have increased the number of hidden layers and number of epochs.

 
Here for the epochs we have the number of errors reached the threshold.On comparing the graph accordingly we can see there are more error and loss in case of perceptron model when compared to the keras model. Accuracy in case of keras model vary on number of layers and test accuracy reached almost 70. 

Conclusion:

In perceptron we can only represent linearly separable data whereas in keras overcomes the limitation complex decision boundaries.
