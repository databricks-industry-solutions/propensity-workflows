![image](https://raw.githubusercontent.com/databricks-industry-solutions/.github/main/profile/solacc_logo_wide.png)

[![CLOUD](https://img.shields.io/badge/CLOUD-ALL-blue?logo=googlecloud&style=for-the-badge)](https://cloud.google.com/databricks)
[![POC](https://img.shields.io/badge/POC-10_days-green?style=for-the-badge)](https://databricks.com/try-databricks)

The purpose of this solution accelerator is to setup a high-level workflow with which household (customer) propensity scores for various product categories can be updated on a regular basis. Such scores could be used by a variety of marketing systems to identify classes of products or product-aligned promotional offers to present to users as they interact with a website, mobile app or email messages sent to them.

We envision this workflow as consisting of three principal tasks:
</p>

1. Feature Generation (addressed in notebook *Task__Feature_Engineering*)
2. Model Training  (addressed in notebook *TASK__Model_Training*)
3. Propensity Scoring (addressed in notebook *TASK__Propensity_Estimation*)


**NOTE** Our focus in the numbered notebooks will be on workflow enablement. To understand the details of the work involved in each of these steps, please review the content in each of the task-aligned notebooks.

At the time of solution initialization, the team responsible for the solution will need to create the backlog of features required to support model training and then complete a first pass on the model training itself.  At that point, propensity scores can be created through a two-part workflow, one of which operates daily and the other of which operates less frequently, most likely weekly.

In the daily workflow, features are calculated from the latest information available in the system.  Those features are used in combination with available models to assemble the set of propensity scores to be used by marketers.

In the weekly workflow, models are retrained using pre-calculated features.  The models are moved into production-ready status so that the next iteration of the daily workflow can leverage them for their work.

In the notebooks numbered 1 & 2, we will tackle the initialization steps, calling tasks associated with the three stages identified above in a slightly different sequence in order to setup our environment.  In notebook 3, we will setup the daily and weekly workflows as described above.

___
<tian.tan@databricks.com> <bryan.smith@databricks.com>

___


<img src='https://brysmiwasb.blob.core.windows.net/demos/images/prop_workflow.png' width=800>

___

&copy; 2023 Databricks, Inc. All rights reserved. The source in this notebook is provided subject to the Databricks License [https://databricks.com/db-license-source].  All included or referenced third party libraries are subject to the licenses set forth below.

## Getting started

Although specific solutions can be downloaded as .dbc archives from our websites, we recommend cloning these repositories onto your databricks environment. Not only will you get access to latest code, but you will be part of a community of experts driving industry best practices and re-usable solutions, influencing our respective industries. 

<img width="500" alt="add_repo" src="https://user-images.githubusercontent.com/4445837/177207338-65135b10-8ccc-4d17-be21-09416c861a76.png">

To start using a solution accelerator in Databricks simply follow these steps: 

1. Clone solution accelerator repository in Databricks using [Databricks Repos](https://www.databricks.com/product/repos)
2. Attach the `RUNME` notebook to any cluster and execute the notebook via Run-All. A multi-step-job describing the accelerator pipeline will be created, and the link will be provided. The job configuration is written in the RUNME notebook in json format. 
3. Execute the multi-step-job to see how the pipeline runs. 
4. You might want to modify the samples in the solution accelerator to your need, collaborate with other users and run the code samples against your own data. To do so start by changing the Git remote of your repository  to your organization’s repository vs using our samples repository (learn more). You can now commit and push code, collaborate with other user’s via Git and follow your organization’s processes for code development.

The cost associated with running the accelerator is the user's responsibility.


## Project support 

Please note the code in this project is provided for your exploration only, and are not formally supported by Databricks with Service Level Agreements (SLAs). They are provided AS-IS and we do not make any guarantees of any kind. Please do not submit a support ticket relating to any issues arising from the use of these projects. The source in this project is provided subject to the Databricks [License](./LICENSE). All included or referenced third party libraries are subject to the licenses set forth below.

Any issues discovered through the use of this project should be filed as GitHub Issues on the Repo. They will be reviewed as time permits, but there are no formal SLAs for support. 
