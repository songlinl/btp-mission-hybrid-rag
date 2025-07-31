### Deploy Large Language Models (LLM) 

1. Expand the ML Operations menu on the left and click **Configurations**. 
    
    You need to create a configuration of the model you are going to use. Click **Create** on the top right of the list.

    ![create button](img/create-config-button.png)

    First, let's create a configuration for the **text embedding** model. 

2. In the form, fill in the following information:

    - Configuration Name: **openai-embedding-config**
    - Scenario: **foundation-models**
    - Version: **0.0.1**
    - Executable: **azure-openai**

    ![create config 1](img/emb-01.png)

     Click **Next** to move to the next step. 

3. In the form, fill in the following information:

    - modelName: **text-embedding-ada-002**  
    - modelVersion: **latest**  
    >💡**Tip**: Ensure that the model name matches exactly as specified. Optionally, you may include a version number as outlined in the [SAP Note](https://me.sap.com/notes/3437766). For this exercise, the `latest` version is used.

   ![create config 2](img/emb-02.png)


   Click **Next** to move to the next step.  

4. In our case adding input artifacts is not applicable. Click **Review** to move to the next step.

5. You will see all details you have entered so far. 
    
    If there is nothing to change, click **Create** to move to the next step. 

    ![create config 4](img/emb-03.png)

6. Notice that a Configuration ID is generated.
 
    Click **Create Deployment** to the top right.

    ![create deployment 1](img/emb-04.png)

    You will be automatically navigated to the Deployments screen. 
    Because you continued your workflow from the configuration step, you will automatically skip the deployment steps 1 to 3, and come to step 4 of the process. 

7. You will see two duration options, Standard and Custom.  
   
    The Standard option should be selected already. Click **Review** to move to the next step

    ![create deployment 2](img/emb-04-2.png)

8. Review the details and click **Create** to move on. 

    ![create deployment 3](img/emb-05.png)

    **Now the deployment has started.** Monitor the status changes here. 

    On the deployment screen, you can see the Target Status is **RUNNING** and in the beginning, the Current Status is **UNKNOWN**.  Also, the deployment URL says *URL isn't available* until the model is deployed.  

    >💡**Tip**: The deployment process usually takes between 2 to 10 minutes, depending on the server's status, network, the number of parallel jobs, etc.  You can refresh the status by clicking the refresh icon on the top right of the screen. In the meantime, you can proceed with the following steps.

    ![create deployment 4](img/emb-06.png)

9. While you are waiting for your first model to be deployed, repeat the steps above to deploy a **gpt-4o** model. 

    Again, follow the configuration process. When it comes to "Enter Name and Executable", provide the following:

    - Configuration Name: **openai-gpt-4o-config**
    - Scenario: **foundation-models**
    - Version: **0.0.1**
    - Executable: **azure-openai**

    ![create config4 1](img/gpt4-c1.png)

    When it comes to "Input Parameters", provide the following:

    - modelName: **gpt-4o**  
    - modelVersion: **latest**  
    >💡**Tip**: Ensure that you enter the model name exactly as specified. Optionally, you can include a version number as outlined in the [SAP Note](https://me.sap.com/notes/3437766). For this exercise, the `latest` version is used.

    ![create config4 2](img/gpt4-c2.png)

    Proceed with creating the configuration and deploying the model.


10. While you are waiting for your first two models to be deployed, repeat the steps above to deploy a **claude-3.5** model. 

    Again, follow the configuration process. When it comes to "Enter Name and Executable", provide the following:

    - Configuration Name: **anthropic-claude-3.7-sonnet-config**
    - Scenario: **foundation-models**
    - Version: **0.0.1**
    - Executable: **aws-bedrock**

    ![create config claude 1](img/dp-1-claude35.png) 

    When it comes to "Input Parameters", provide the following:

    - modelName: **anthropic--claude-3.7-sonnet**   
    - modelVersion: **latest**   
    >💡**Tip**: Ensure that you enter the model name exactly as specified. Optionally, you can include a version number as outlined in the [SAP Note](https://me.sap.com/notes/3437766). For this exercise, the `latest` version is used.

    ![create config claude 2](img/dp-2-claude35.png) 

    Proceed with creating configuration and deploying the model.

After some time, you should see all models deployed and running. 

![models deployed](img/dp-4-all-models.png)


