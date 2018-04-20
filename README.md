# Face-Recognition-using-PCA-and-LDA

# Goal
Here we have to evaluate the performance of multi classifier in various modes for Face Recognition using Principal Component Analysis (PCA) and Linear Discriminant Analysis (LDA).
We applied different combination rules and got different accuracy for each case.

## A. Multi-classifier System combining PCA and LDA at score level
Scores of PCA and LDA should be combined using minimum, maximum and average rules.
## B. Multi-instance based System at score level (for both PCA and LDA)
The score belonging to each test sample should be average of the scores obtained on comparing the test sample with all the templates of a particular identity.

# Database
Here we have used the AT&T database which is freely downloadable and contains a set of 400 face images (http://www.cl.cam.ac.uk/research/dtg/attarchive/facedatabase.html). 
There are ten different images of each of 40 distinct subjects .For some subjects, the images were taken
at different times, varying the lighting, facial expressions (open / closed eyes, smiling / not
smiling) and facial details (glasses / no glasses).

# Protocol
Training: 1 to 5 samples of each identity for enrollment samples and eigen/ fisher space generation
Testing: 6 to 10 samples of each identity for testing purpose

# Implementation
1. Given a training set of face images, generate feature vectors from them.
2. First, we performed Principal component analysis (PCA) on the training data set and generated
the eigen space.
3. Then we applied Linear Discriminant Analysis (LDA) on the same data set and generated the
fisher space.
4. Then we generated scores from both PCA and LDA and compared them with the genuine
scores and imposter scores.
5. Finally, the labels from PCA and LDA are compared with the target label and ROC curves are
generated for maximum, minimum and sum rules.
