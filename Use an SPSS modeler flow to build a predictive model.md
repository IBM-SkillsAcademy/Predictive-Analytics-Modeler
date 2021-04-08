## Problem
Create a ML model to recommend a drug based on lab measurements.

## Steps
### Creating a Watson Studio project
1. Login to IBM CLoud.
2. Create an instance of the Watson Studio service.
3. Open the Watson Studio service instance
4. Create a new blanck Watson Studio project

### Adding data to the project
1. Download the sample data set from [DRUG1n.csv](https://github.com/IBMPredictiveAnalytics/ViolinPlots_with_Seaborn/blob/master/example/DRUG1n.cs) (right-click [DRUG1n.csv](https://raw.githubusercontent.com/IBMPredictiveAnalytics/ViolinPlots_with_Seaborn/master/example/DRUG1n.csv) then save as **.csv** file)
2. Add DRUG1n.csv as a data asset in the project.
3. Add a modeler flow to the Watson Studio project.
4. From the *Palette*, under **Import**, add a **Data Asset** node to your flow.

### Exploratory data analysis (EDA)
1. Explore **Drug** with a **Distribution** node.
2. Explore **Drug** distribution over **Na** and **K** using a **Plot** node.
![Scatterplot of drug distribution over Na and K](https://www.ibm.com/docs/en/SSBFT6_1.1.0/wsd/images/tut_drug_scatterplot.png)
3. Explore associations between different categories from categorical fields **BP** (blood pressure) and **Drug** using a **Web** node .
![Web graph of drugs vs. blood pressure](https://www.ibm.com/docs/en/SSBFT6_1.1.0/wsd/images/tut_drug_web.png)
4. Add a **Data Audit** node to view general data statistics and charts for all fields.
![Data Audit node output](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-spss-modeler-flow/images/21-fields-output.png)
5. You can use the **Charts** node to create advanced charts to explore your data from different perspectives and identify patterns, connections, and relationships.
![Chart builder for advanced visualizations](https://www.ibm.com/docs/en/SSBFT6_1.1.0/wsd/images/tut_drug_viz.png)

Reference: [Drug treatment - exploratory graphs](https://www.ibm.com/docs/en/wsd?topic=tutorials-drug-treatment-exploratory-graphs) - IBM Watson Studio Desktop

### Feature engineering
1. Derive a new field **Na_to_K = Na / K** using a **Derive** node.
2. Check the distribution of **Na_to_K** using a **Histogram** node, display **Na_to_K** colored by **Drug**.
![Histogram of Na_to_K colored by Drug](https://www.ibm.com/docs/en/SSBFT6_1.1.0/wsd/images/tut_drug_histogram.png)
3. Filter out the *Na* and *K* fields.

The ratio of sodium to potassium in the blood seems to affect the choice of drug, as does blood pressure.

### Building the model
1. Add a **Type** node with **Drug** as **Target** and all other fields as **Inputs**.

![The Type node](https://www.ibm.com/docs/en/SSBFT6_1.1.0/wsd/images/tut_drug_build_flow2.png)
2. Add a **Partition** node to splits the data set into a training set (70%) and a testing set (30%).
4. Add a **C5.0** node to traing the model.
5. **Run** the modeling node to create its model nugget.
6. To browse the model, right-click the model nugget and choose **View Model** to open the model viewer.

![Tree diagram of the model](https://www.ibm.com/docs/en/SSBFT6_1.1.0/wsd/images/tut_drug_browse_tree.png)
5. Add an **Analysis** node after the nugget to see the model performance.

![Analysis node](https://www.ibm.com/docs/en/SSBFT6_1.1.0/wsd/images/tut_drug_analysis.png)

6. Add a **Table** node after the nugget to display predictions.
7. Right-click the **Table** node, and then select **Save Branch as a Model**. When you save a model.

## References
* [Tutorial: Using a predictive model from Watson Machine Learning with streaming patient data](https://www.ibm.com/docs/en/cloud-paks/cp-data/2.5.0?topic=manually-spss-model-operator)
* [Creating SPSS Modeler flows in Watson Studio](https://developer.ibm.com/technologies/data-science/tutorials/watson-studio-spss-modeler-flow) - Graphically build and evaluate machine learning models
* [Tutorial: Using a predictive model from Watson Machine Learning with streaming patient data](https://www.ibm.com/docs/en/cloud-paks/cp-data/2.5.0?topic=manually-spss-model-operator) - IBM Cloud Pak for Data 2.5.
