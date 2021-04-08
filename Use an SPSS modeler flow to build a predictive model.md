## Problem
Create a ML model to recommend a drug based on lab measurements.

## Steps
### Creating a Watson Studio project
1. Create an [IBM Cloud Lite account](https://cloud.ibm.com/registration).
2. Login to [IBM Cloud](https://cloud.ibm.com/resources).
3. Create an instance of the [Watson Studio](https://cloud.ibm.com/catalog/services/watson-studio) service.
4. Open the Watson Studio service instance.
5. Click **Create a project**.

![Create a project](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-data-visualization-preparation-transformation/images/project-home-page.png)

5. Click **Create an empty project**.

![Create an empty project](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-data-visualization-preparation-transformation/images/project-create-options.png)

### Adding data to the project
1. Download the sample data set from [DRUG1n.csv](https://github.com/IBMPredictiveAnalytics/ViolinPlots_with_Seaborn/blob/master/example/DRUG1n.csv) (right-click [DRUG1n.csv](https://raw.githubusercontent.com/IBMPredictiveAnalytics/ViolinPlots_with_Seaborn/master/example/DRUG1n.csv) then save as **.csv** file)
2. Add DRUG1n.csv as a data asset in the project.

![Add a data asset](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-data-visualization-preparation-transformation/images/assets-load-data.png)

3. Add a **Modeler flow** to the project.

![Add a modeler flow](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-spss-modeler-flow/images/add-modeler-flow.png)

5. From the *Palette*, under **Import**, add a **Data Asset** node to your flow.

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

![The branch to be saved as the model](https://www.ibm.com/docs/en/SSQNUZ_2.5.0/wsj/streaming-pipelines/images/model_flow_canvas.gif)

8. Right-click the **Table** node, and then select **Save Branch as a Model**. When you save a model.

### Promoting and deploying the model
1. Create a deployment space.

![Create a deployment space](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-spss-modeler-flow/images/deployment-space-create.png)

2. Promote the model.

![Promote the model](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-spss-modeler-flow/images/model-details.png)

3. Deploy the model.

![Deploy the model](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-spss-modeler-flow/images/deployment-list.png)

4. Select **Onlince** deployment.

![Online deployment](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-spss-modeler-flow/images/deploy-model.png)

5. Test the deployment.

## References
* [Tutorial: Using a predictive model from Watson Machine Learning with streaming patient data](https://www.ibm.com/docs/en/cloud-paks/cp-data/2.5.0?topic=manually-spss-model-operator) - IBM Cloud Pak for Data 2.5 documentation
* [Creating SPSS Modeler flows in Watson Studio](https://developer.ibm.com/technologies/data-science/tutorials/watson-studio-spss-modeler-flow) - Graphically build and evaluate machine learning models
* [C5.0 Node](https://www.ibm.com/docs/en/spss-modeler/SaaS?topic=trees-c50-node) - SPSS Modeler documentation.
* [Choosing a tool](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/tools.html) - Cloud Pak for Data as a Service documentation
