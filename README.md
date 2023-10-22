# predict_qualitative_properties_of_a_solar_panel

To predict qualitative properties (data-set B) of a solar panel using quantitative properties (data-set A or I-V curve) of the same solar panel (module)

# Background: 
PV Diagnostics is solar power plant quality control and diagnostics startup. As part of the testing of solar panels, two different tests are conducted. On the basis of Test-A, Dataset-A is collected (each module will have one CSV file and the CSV file contains data set A). On the basis of a separate Test-B, Dataset-B is collected.

# Problem statement: 
Build a model to predict results of Test-B (Dataset-B) based on results of Test-A (Dataset-A). You are required to divide the data into 2 parts: 60% for training and 40% for testing (you can also vary this ratio slightly). Then you have to do following:
1. Make classification model based on Test-A (Data-set A) to classify solar panels in just 2 categories of Test-B(Dataset-B): normal and defect (includes all defects)
2. Upgrade this classification model to classify Data-set A into defect wise category of Dataset-B (defect_C, defect_P, defect_S)

# Description of quantitative Dataset-A (I-V curve)
Dataset-A is available in folder name “Test-A” of zip file. This folder contain CSV files of ~200 solar panels. Name of each CSV file is the identification number of the panel and the respective CSV file has data collected from Test-A i.e. Dataset-A of that panel.

# How to read the CSV file:
Each solar panel data is stored in a CSV file. There are around 5-6 key-fields:
Voc : ‘Voc (stc)[V]’
Isc : ‘Isc (stc)[A]’
Vm : ‘Vpm (stc)[V]’
Im : ‘Ipm (stc)[A]’
Pmax : ‘Pm (stc)[W]’
Make a new variable FF = Pmax / (Voc * Isc)
The same CSV file also contains complete set of I-V curve points (starting from Row 36). Following figure shows these key-fields on the I-V curve of a solar panel.


# Useful points in the dataset:
Ratio of Im/Isc, Vm/Voc
Slope of curve near point-1
Radius of curvature near point-2
Slope of curve near point-3
All the individual curve points
Normalization parameter for voltage and current: Voc_d = 37.8, Isc_d = 8.8 (you may need to normalize all curve-points using V/Voc_d and I/Isc_d)

# Description of Dataset-B
Each of the solar panel is categorized in 2 buckets either normal or defected. Defects are further categorized in various types as mentioned earlier:
1. normal
2. defect_C
3. defect_P
4. defect_S
Dataset-B is available in folder name “Test-B” of zip file. This folder contains an excel file with panel identification number and it’s respective category (Dataset-B).
As mentioned in the objective you are required to predict Dataset-B from Dataset-A.

# General instructions:
You are required to complete the work on Python (Spyder or Jupyter Notebook)
Please feel free to speak with us in case you have any doubts.
By participating in our recruitment process, you agree to our data confidentiality policy and you are expected not to share this assignment and its data with anybody else.
Do not upload any of your work related to this assignment on any of the public repositories like GitHub.


