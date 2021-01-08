# Deploy Decision optimization model

 In this tutorial you will Save model for deployment, promote it to deployment space, create deployment and create a job with assets added to space.

### Step 1. Save and promote model for deployment

 - Click Scenario that you need to deploy. From tutorial2 we will use *EmplShiftAssignment_Balance* scenario and deploy it.Click on three dots and click **Save for deployment** Give it a name and description which is option for example: *EmployeeShiftAssignment*
 - A message pops to view the model in project. Click on it and you will see the model under Watson Machine Learning section in assets tab.You can see the model type is docplex and engine is 12.10. Note that this will only use the optimization model. It does not export the data or visualization. We will give the data once we deploy the model.

 ![Step1](../images/Tutorial2-Step1.gif)

- You can look at the input and output schema. The next thing is to promote the model to deployment space. click Promote to deployment space. This is separate space from development. So data scientist can work in Watson studio and then can promote it to separate space.

 ![Step1](../images/Tutorial2-Step1b.png)

- Select deployment space and give name any tags for Example: *CPLEX, decision optimization* and optional description Click **Promote**.

![Step1](../images/Tutorial2-Step1c.png)
![Step1](../images/Tutorial2-Step1d.png)

- Click on deploy icon on right for **EmployeeShiftAssignment** under assets tab. It will take you to a screen where it ask to give it name example:*ShiftAssignment* select the hardware configuration from the dropdown menu and keep the node to 1 (this is to define execution in parallel) and click Create.

![Step1](../images/Tutorial2-Step1e.gif)

You can see the **deployment id** generated which can be used to call from application written in C++, java or python to call this model and execute it.

### Step 2. Add data to deployment space

- Click the *Warehouse production models* on the top left side.

![Step2](../images/Tutorial3-Step2a.png)

- Click the **Drop files here or browse files to upload** on the right side and go to [data folder]() and select all the files and upload. We add the data input and output files so that we can execute the model along with input tables and solution will be populated in the solution tables.
![Step2](../images/Tutorial3-Step2.gif)

### Step 3. Create job to test deployment
- Click Deployment tab to go to the **EmployeeShiftAssignment** that was deployed in step1.
![Step3](../images/Tutorial3-Step3a.png)

- Click **ShiftAssignment**
![Step3](../images/Tutorial3-Step3b.png)

- To create the job Click Create Job button and select input and create output files if they do not exist.
![Step3](../images/Tutorial3-Step3c.gif)

- Click on Jobname **Schedule** and you should see a screen similar to the one shown below where it shows that job completed running in 13 seconds. One can click on the run and look at the log in details.
![Step3](../images/Tutorial3-Step3d.png)

** This is end of this lab **
