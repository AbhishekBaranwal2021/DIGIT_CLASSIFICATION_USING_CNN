# DIGIT_CLASSIFICATION_USING_CNN
Hear we are Classifying the Images (as which number is it? )in the DATASET of MNIST using  Convolutional Neural Network ( ConvNet /CNN) 
# Requirements
* PYTHON 
* TENSORFLOW
* NUMPY
* MATPLOTLIB

# DATASETS
* WE HAVE TAKEN THE "MNIST" DATASET WHICH WE CAN FIND IN TENSORFLOW(INBUILD DATASET)
*    ============>>>>>   mnist = tf.keras.datasets.mnist  <<<<<==============
*    FOR MORE INFO GO TO ==>>https://www.tensorflow.org/datasets/catalog/mnist

# DATA PREPARATION
* FIRST WE SPLIT THE DATASET INTO TRAIN AND TEST DATASET
* USING MATPLOTLIB CHECKING THE TRAIN DATA (X_train) AND COMPARING IT'S CORRESPONDING OUTPUT (Y_train) 

## NORMALIZATION OF DATASET
* NORMALIZING THE TRAIN AND TEST DATA i.e. (X_train) AND (X_test)
* CHECKING THE IMAGE AFTER NORMILAZATION USING MATPLOTLIB

# MAKING READY TO TRAINING THE CNN MODEL
### IMPORTANT STEP'S TO DO:-
  1. RESHAPING THE X_train TO MAKE IT USEFULL TO CNN
  2. AFTER TAKING A PARTICULAR IMAGE APPLING THE FILTER ON CONVOLUTION LAYER
  3. THEN APPLY ACTIVATION FUNCTION WHICH IS "RELU" FUNCTION
  4. THEN APPLYING MAXPOOLING TO REDUCE THE COMPLEXITY OF DATA
## NOW REPEAT AGAIN ALL THE STEPS FROM 2 TO 4
  
* AFTER REPEATINE THE ABOVE PROCESS FOR 3 CONVOLUTION LAYERS
1. THEN FLATTEN THE DATA
2. MAKE DENSE LAYER AFTER THAT APPLY ACTIVATION FUNCTION
3. REPEAT THE PROCESS ONE MORE TIME
4. NOW FOR FINAL LAYER
   * MAKE DENSE LAYER AND THEN APPLY ACTIVATION FUNCTION == "SOFTMAX"
   * SOFTMAX FUNCTION ==> IT HELP US TO PREDICT THE OUTPUT USING "PROBABILITY" 

# APPLYING OPTIMIZER , LOSS FUNCTION AND ACCURACY
 1. HEAR WE USE "ADAM" OPTIMIZER
 * WANT TO KNOW ABOUT "ADAM OPTIMIZER" GO TO ===>>https://towardsdatascience.com/adam-latest-trends-in-deep-learning-optimization-6be9a291375c
 
 2. THE WE USE "sparse_categorical_crossentropy" AS PROBABILITIC LOSS FUNCTION .
 * FOR MORE GO TO ===>>https://keras.io/api/losses/probabilistic_losses/#sparse_categorical_crossentropy-function
 
 3. GO FOR  ACCURACY
 
# NOW FITTNG THE MODEL WITH (X_train AND Y_train)
 * USING model.fit() function
 * MODEL FITTING :-Model fitting is the measure of how well a machine learning model generalizes data similar to that with which it was trained
 
# PREDICTING THE MODEL
 * ====>>predictions = model.predict(X_testr)

# TRY ANY INDEX AND CHECK BY YOURSELF !
* YOU CAN TRY THIS CODE AFTER FULFILLING ALL THE REQUIREMENTS

# CHECHING THE ACCURACY ON TEST DATA (VALIDATION ACCURACY)
 * ===>>>test_loss, test_acc = model.evaluate(X_testr,Y_test)

## ACCURACY ON TRAIN DATA IS 0.9851
## ACCURACY ON TEST DATA IS 0.980

