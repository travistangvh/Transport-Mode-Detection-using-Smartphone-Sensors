Every day, we travel with from one place to another on different modes of transportation. Being able to predict the patterns of our citizens' movements using different modes of transport will help urban planning significantly. 

That leads me to ask, can we predict what a user is travelling on based on sensors from our phones? Here is an attempt to use accelerometer, gyrometer and linear acceleration sensor data from our smartphones to predict 4 travel modes: Walking, MRT (Train), Bus and Idle.

In this notebook, I collected data using my phones' sensors and manually labelled the travel mode. Next, I visualized the accelerometer and gyrometer data as a time-series data. The subsequent preprocessing steps include slicing the time series data into sliding windows (thereafter 'journeys'). These journeys are then preprocessed with Fourier Transform to obtain information in the frequency-domain. Simultaneously, mathematical summary statistics are extracted from each of these journeys. Eventually, 1102 features were extracted for each journey, which are decomposed by Principal Component Analysis into 141 features. These PCA features are then fed into a SVC Model that predict with has an F1-score of 82.6%.