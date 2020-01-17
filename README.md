# Rationale
Every day, we travel with from one place to another on different modes of transportation. Being able to predict the patterns of our citizens' movements using different modes of transport will help urban planning significantly. 

That leads me to ask, can we predict what a user is travelling on based on sensors from our phones? Here is an attempt to use accelerometer, gyrometer and linear acceleration sensor data from our smartphones to predict 4 travel modes: Walking, MRT (Train), Bus and Idle.

# Summary
In this notebook, I collected data using my phones' sensors and manually labelled the travel mode. Next, I visualized the accelerometer and gyrometer data as a time-series data. The subsequent preprocessing steps include slicing the time series data into sliding windows (thereafter 'journeys'). These journeys are then preprocessed with Fourier Transform to obtain information in the frequency-domain. Simultaneously, mathematical summary statistics are extracted from each of these journeys. Eventually, 1102 features were extracted for each journey, which are decomposed by Principal Component Analysis into 141 features. These PCA features are then fed into a SVC Model that predict with has an F1-score of 82.6%.

# Methodology
The methodology outlined in this notebook is heavily reliant on the use of time- and frequency-domains statistical summaries to predict travel modes. This is well-supported as a means of Human Activity Recognition in the paper 'Towards Clustering of Mobile and Smartwatch Accelerometer Data for Physical Activity Recognition' by Chelsea Dobbins.

# Acknowledgement
This project is developed as part of my work at the Data Science Division of the Land Transport Authority. I would like to thank my mentors Ms Rachel and Mr Guangquan for their guidance. I would also like to thank my team mates Qixuan, Denis, Yi Heng, Wilson and Guanlan for their amazing work that has influenced my work.

