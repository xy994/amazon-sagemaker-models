## Workshop Lab Guide

We will create a model that generates product recommendations based on the [Amazon Review Dataset](https://s3.amazonaws.com/amazon-reviews-pds/readme.html).  This dataset contains a 130+ million product reviews across approximately 50 product categories.

Before we dive into the mechanics of our deep learning model, let’s explore the dataset and see what information we can use to predict the category. For this, we will use a notebook within Amazon SageMaker that we will can also utilize later on as our development machine.

Follow these steps to create and launch the notebook:

1. Open the Amazon SageMaker Console, select 'Notebook instances' on the left and then click on ‘Create notebook instance’ and give the notebook a name. 

2. For the instance type, pick `ml.t2.large` since our example dataset is small and we don’t intend on using GPUs for training/inference.  We're not planning to use Elastic Inference either, so you can leave the default of ‘none’.

3. For the IAM role, select ‘Create a new role’ and select the options shown below for the role configuration.  We need to access a specific S3 bucket, so specify `amazon-reviews-pds`.

![Amazon SageMaker IAM Role](/img/sm-keras-1.png)

4. Click ‘Create role’ to create a new role. In the ‘Git repositories’ section select the option to clone a public Git repository and use this URL: https://github.com/data-science-on-aws/amazon-reviews-recommendation-workshop

![Amazon SageMaker Git Repo](/img/sm-keras-git.png)

5. Hit ‘Create notebook instance’ to create a new notebook instance.  _Note: It usually takes a few minutes for the notebook instance to become available. Once available, the status of the notebook instance will change from ‘Pending’ to ‘InService’._

6. Launch the Notebook from the Jupyter notebook web UI.
