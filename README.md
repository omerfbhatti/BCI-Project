
  
# BCI Project
Brain Computer Interface Project as part of "Programming for DSAI" course at AIT

## Title : Comparative Study of Various Feature Extraction Methods and Machine Learning Models for EEG Signal Analysis

This project is based on Machine Learning and EEG signal Analysis for BCI applications. Online resources are required to explore more about the BCI applications. 

### Major objective
The aim of our group is to do comparative and explorative project for extending horizontal knowledge from previous (cited) studies. The aim of this study is not to find a better performing model (though it would be great if, with some luck, we could manage that). We are going to find reasons and alternative modeling procedures (Feature Engineering, different model constructions and synthetical exploration) for EEG Analysis.    

## Project progress submission on Sunday 17 October 2021

After mid-exam, group members had some discussion of the further procedures to conduct the project. Firstly, we would like to accumulate the resources related to the EEG and BCI theme. To make it easily accessible, we made the google spreadsheet for posting the online resources, textbooks and papers about EEG signal processing and ML association. The link is given below.

<p>--> <a href="https://docs.google.com/spreadsheets/d/1-KQw9Vnvt7zA8GI1qACvUyUk9ErQrjMxxLvYnwLkbng/edit">Literature Review List</a></p>
<p>--> <a href="https://docs.google.com/presentation/d/1onvEbYd8m2fhh_VmNWWfOw9wzkQQEcACitAkmXtwp90/edit?usp=sharing">Project Slides</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/exp%231_load_eeg_data.ipynb">Experiment #1: Load a single EDF file from Motor Movement/Imagery Dataset</a></p>
  
 ## Project progress submission on Sunday 24 October 2021
 
The main tasks of methodology and frameworks was concluded on this week. the main framework is to perform different features (from feature extraction methods) and several ML model sch as genreral ML, CNN, RNN etc. to explore the differences between result with what are the advantages and drawbacks of each analysis ways. References dataset is not summarized yet, but there are 2 intereseting dataset; DEAP and motor imagery datasets.

<br>
<p><img src="https://github.com/omerfbhatti/BCI-Project/blob/main/EEG%20Classification%20Pipeline.png" width="1000" /></p>
<br>

The provided tasks for each member

- **Thantham:** find the dataset, feature extraction methods, related source code, tools and adjust processing frameworks. 
- **Omer:** do experiment on artifact removal, dataset exploration, points of study, and evolve methodology framework  
- **Cedric:** review and construct ML models or any CNN models for statement solutions for comparison in the project
- **Arsha:** Review and search for related source codes about feature extractions for several methods for further comparison

From group discussion, the study will be conducted to implement the available dataset for different features with several models. Then, by comparison we will consider whether the results are improved or not. Exploring the dataset by trying various methods might provide us with points for future studies about BCI and EEG signal analysis with ML.

## Project progress submission on Sunday 31 October 2021

This week focused on implementing EEG signal data extracted on epochs data to perform classification using several ML models. 

<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/EEG%20Motor%20Imagery%20Dataset.png">Brief Description of MI Dataset</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%232.2%20-%20Data%20Loading%20and%20Pre-processing(with%20explanation).ipynb">Experiment #2 (2)Brief Description of MI Dataset</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%232%20-%20Data%20Loading%20and%20Pre-processing.ipynb">Experiment #2: Loading Data from Motor Movement/Imagery Dataset and performing Pre-processing steps</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%232.4%20-%20Data%20Loading%20and%20Pre-processing%20with%20ICA%20and%20CSP.ipynb">Experiment #2.4: Data Loading & Pre-processing class with ICA and CSP</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%233.1%20-%20Classification%20using%20Logistic%20Regression.ipynb">Experiment #3.1: EEG Classification using CSP and Logistic Regression</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%233.2%20-%20Classification%20using%20SVM.ipynb">Experiment #3.2: EEG Classification using CSP and SVM</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%233.3%20-%20Classification%20using%20LDA.ipynb">Experiment #3.3: EEG Classification using CSP and LDA</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%233.4%20-%20Comparison%20of%20Logistic%20Regression%2C%20SVM%20and%20LDA.ipynb">Experiment #3.4: EEG Classification - Comparison of Logistic Regression, SVM and LDA</a></p>
<br>
<p><img src="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Comparison%20of%20ML%20Models%20for%20EEG%20Classification-dpi-100.png" width="500" /></p>
<br>
<br>
<p><img src="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Comparison%20of%20ML%20Models%20for%20EEG%20Classification-dpi-100%20-%20Two%20Subjects.png" width="500" /></p>
<br>
<br>
<p><img src="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Comparison%20of%20ML%20Models%20for%20EEG%20Classification-dpi-100%20-%20Four%20Subjects.png" width="500" /></p>

<br>

Data Preprocessing steps were carried out. As part of data preprocessing, we bandpass filtered the EEG signals and extracted epochs for training. In addition, feature extraction was performed using spatial filters as per Common Spatial Patterns algorithm (CSP) as first feature extraction method. Python MNE implementation of CSP algorithm was used for this purpose. Three Machine Learning methods were used to analyze the CSP filtered EEG signals. 

Experiment design was to use three different datasets to perform classification of signals. First dataset consisted of EEG signals from only one subject. The second dataset had data from two subjects, and the third dataset had data from four subjects.

Logistic Regression was used as baseline model to do classification. Logistic Regression was carried out using both Raw Signal values and CSP values. The results obtained for raw signal values were not good. The model failed to learn the patterns in the data. However, the accuracy achieved for CSP values is quite good for first and second datasets. But, as we increase the subjects in the dataset, the model fails to generalize well to the data. 

SVM and LDA (Linear Discriminant Analysis) algorithms also provide us with similar results, except LDA's performance is quite subpar for second dataset as compared to the other two algorithms.

In conclusion, these implementations demonstrate that these ML methods are quite effective when the dataset is composed of just one subject. However, as we increase the variance in the EEG signal dataset, these models fail to generalize well to the situation. Deep Learning methods are expected to be able to compensate for the situation. This is what we will attempt next.

<br>

## Project progress submission on Sunday 7 November 2021

<br>
<p><img src="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/results/Comparison%20of%20EEG%20Source%20Subjects%20-%20with%20channel%20selection.png" width="500" /></p>

<br>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%233.5%20-%20Comparison%20of%20Models%20-%20With%20Channel%20Selection.ipynb">Experiment #3.5: Comparison of Classification models: With Channel Selection</a></p>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%233.6%20-%20Classification%20accuracy%20for%20each%20subject.ipynb">Experiment #3.6: EEG Classification accuracy for individual subjects</a></p>

After 1st progress presentation, the grou has considered <a href="https://www.sciencedirect.com/science/article/pii/S1746809420303116">the review paper about motor imagery dataset implementation</a> that instructor guided. Consequenly, group aimed to read mentioned paper and additional documentation to make 2 set of purpose combinations of feature extraction and model. Each member will produce about 2 set of interested combination to do analysis and explorative the results. The list of combinations are by following.

| Member   | Feature extraction 1 | Model 1 | Feature extraction 2 | Model 2 | Reference |
|----------|----------------------|---------|----------------------|---------|-----------|
| Thantham |         CWT             |    CNN+ReLU+GD     |       Tim series             |     RNN    |           |
| Omer     |        CSP           | SVM,LDA,|   Spectogram, Raw         |   CNN   |           |
|          |                      | LogReg  |                      |         |           |
| Cedric   |                |     CNN (2 conv, 2 fc)    |     Raw                 |         |           |
| Arsha    |                      |       CNNs |                      |         |           |

 These combinations are based on the interest of member and reviewing paper about popularity of motor imagery implementations. Members will perform these analyses to explore the reason an related representation about results including support issues. 

## Project progress submission on Sunday 14 November 2021

According to the interesting modeling for each member, some of the modeling can produce the results, but there were some issues regarding training although following the structure of the model in research.

Experiment 3.7 - Perform 10 subjects on fists and feet imagery classification using 64 channels 1-2 second time cue by Modeling of CNN architecture. <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%233.7%20-%20Classification%20of%20CNN%20with%20CWT.ipynb">Experiment #3.7 - Classification of CNN with CWT</a></p>

Experiment 3.8 -  Perform 10 subjects on fists and feet imagery classification using 64 channels 1-2 second time cue by Modeling of LSTM architecture. <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%233.8%20-%20Classification%20of%20LSTM%20with%20raw%20signal.ipynb">Experiment #3.8 - Classification of LSTM with raw signal</a></p>

The problem was found that the training loss and validation loss on CNN + Continuous Wavelet Transform (CWT) implementation was very good despite bad validation accuracy while good accuracy of training. However, LSTM implementation showed very bad validation metrics and loss while training is very well. These problems will be held in discussion on progress presentation.

<br>
<p><img src="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/results/CNN%20with%20channel%20selection%2C%20C1%20%26%20C2%20-%20Loss%20curves%20Five%20Subjects.png" width="500" /></p>

<br>
<p><img src="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/results/CNN%20with%20channel%20selection%2C%20C1%20%26%20C2%20-%20Accuracy%20with%20Five%20Subjects.png" width="500" /></p>

<br>
<p>--> <a href="https://github.com/omerfbhatti/BCI-Project/blob/main/Experiments/Experiment%20%234.0%20-%20CNN%20%2B%20RAW%20%2B%20Channel%20Selection.ipynb">Experiment #4.0: CNN + RAW + Channel Selection</a></p>

Training accuracy on the dataset seems to increase to above 99%, however the validation accuracy is still ~ 50%. This seems to indicate that our model is not able to generalize well to the data which it has not seen before. Dropoff layers have been used in this model and batch normalization has been applied as well. The dataset is composed of 5 subjects (both hands, both feet task) using only <a href=https://www.frontiersin.org/articles/10.3389/fnhum.2020.00338/full>a single electrode pair C1, C2</a>. This does not seem to affect the training accuracy, which is an improvement over the previous attempt with CSP+SVM/LDA algorithm, however we still cannot predict unseen data with any sort of accuracy. Next we may try using more electrode pairs in conjunction with this data.

## Project progress submission on Sunday 21 November 2021

_Conclude all of the experiments and explorations found about the feature extraction along with each modeling..._

<hr />

## Current tasks
  - <s>Search for related documentation, online resources, research papers and textbooks</s>
  - <s>Search for established procedures of EEG signal analysis along with Machine Learning implementation</s>
  - <s>Explore Sample code + Dataset from open-source material or tutorials and go through previous research to **Find the gaps**</s>
  - <s>Search for available source code or example to implement te process of EEG signal analysis</s>
  - Explore the CNN models with and related researches about CNN implementation
  - <s>Artifact handling process</s>
  - <s>Construct an experiment for feature extraction 1 method and ML model 1 method</s>
  - <s>Do different feature extractions out from CSP (Wavelet or Fourier Transform)</s>
  - **Adjust the domain knowledge with members in the group**
  - Follow the architecture in similar research and adjust the model implementing to construct that model
  - Find more related models described in similar researches about validation metric problem

## Current issues (problem and struggling)
 - <s>More knowledge required about EEG signal processing</s>
 - <s>Difficulties in understanding other research/tutorials</s>
 - <s>Reconstruct the process of EEG signal analysis</s>
 - <s>Appropriate Dataset used in this project</s>
 - <s>Will the same reconstructed function (from searching) be reused for our project?</s>
 - <s>As deep as the process is on going, there is much more unclearity on proper process of EEG Signal</s>
 - Members comprehensive and domain knowledge in a group have not perfectly adjusted for conducting study together
 - Experiments of the models have unexplainable reasons of training set and validations metrics
 
## Future tasks (including expected, some tentative)
  - <s>Revise the gaps (recommendation) from previous studies</s>
  - <s>List out and choose most appropriate ways to conduct analysis</s>
  - <s>Construct more modules (Feature extraction and ML models) into experiments</s>
  - Solve the training set and validation metrics problem as soon as possible
  - **Add/Drop** the conduction method for feature extraction and model comprison
  - Implement and test the selected procedure as per previous studies suggestions
  - Compare, Discuss and Explore the EEG signal processing using ML in several ways
  - Conclude the project

 
