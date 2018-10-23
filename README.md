# Amazon Rekognition

This repository contains a collection of Jupyter notebooks that walks you through various APIs of Amazon Rekognition.

## Learning Objectives

* Learn about various Amazon Rekognition APIs including Labels, Moderation Labels, Faces, Text etc.

## Modules

## Create SageMaker Notebook Instance

In this step we will create a SageMaker Notebook instance using CloudFormation template. SageMaker is not required to use Rekognition, but we will use SageMaker as IDE for quick prototyping and to learn various Rekognition APIs.

1. Click on one of the buttons below to launch CloudFormation template in an AWS region.

Region| Launch
------|-----
US East (N. Virginia) | [![Create IAM Role for SageMaker us-east-1](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformation-launch-stack-button.png)](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/review?stackName=SageMaker&templateURL=https://s3.amazonaws.com/ki-reinvent-content/SageMaker.yaml)


2. Under Create stack, check the checkbox for "I acknowledge that AWS CloudFormation might create IAM resources with custom names" and click Create.

![](assets/cf-1.png)


3. You should now see the screen with status CREATE_IN_PROGRESS. Click on the Stacks link in the top navigation to see current CloudFormation stacks.

![](assets/cf-2.png)


4. Click on the checkbox next to the stack to see additional details below.

![](assets/cf-3.png)


5. Wait until CloudFormation stack has the status CREATE_COMPLETE.

![](assets/cf-4.png)


## Open SageMaker Notebook Instance

1. Go to SageMaker in AWS Console at https://console.aws.amazon.com/sagemaker/

2. Click on Notebook instances in the left navigation.

![](assets/sm-home.png)

3.  You should see list of SageMaker instances. Click on the Open link next to the SageMaker instance.

![](assets/sm-instances.png)

4. You will now be redirected to the Jupyter UI.

![](assets/jupyter-home.png)

5. Click on New and then Terminal.

![](assets/sagemaker-new-terminal.png)

6. You should now see Terminal like below:

![](assets/sagemaker-terminal.png)

7. In the terminal type:
- cd SageMaker
- git clone https://github.com/darwaishx/rekognition-notebooks.git

![](assets/sagemaker-gitclone.png)

8. Go back to Jupyter home screen by clicking on the Jupyter logo on the top left and refresh to see the folder celebrity-recognition.

![](assets/git-folder.png)

9. Click on celebrity-recognition, then 1-celebrity-recognition and then CelebrityRecognition.ipynb to open the notebook.

![](assets/m1-notebook.png)

10. Follow the directions in the notebook to run each cell and review it's output.


## Cleanup
After you have completed the workshop, you can delete all of the resources using the following steps:
1. Delete all Lambda functions created manually
2. Delete all CloudFormation stacks created in the first module
