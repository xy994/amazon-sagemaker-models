#### Use following url to sign in into an AWS Account. Use the hash provided as the login credential. 

```
https://dashboard.eventengine.run/login
```

## Workshop Lab Guide

We will create a model that generates product recommendations based on the [Amazon Review Dataset](https://s3.amazonaws.com/amazon-reviews-pds/readme.html).  This dataset contains a 130+ million product reviews across approximately 50 product categories.

### Create the Notebook

Before we dive into the mechanics of our deep learning model, let’s explore the dataset and see what information we can use to predict the category. For this, we will use a notebook within Amazon SageMaker that we will can also utilize later on as our development machine.

Follow these steps to launch a notebook.

Open the Amazon SageMaker Console, select 'Notebook instances' on the left and then click on ‘Create notebook instance’ and give the notebook a name. For the instance type, I’m going to pick ‘ml.t3.medium’ since our example dataset is small and we don’t intend on using GPUs for training/inference.  We're not planning to use Elastic Inference either, so you can leave the default of ‘none’.

For the IAM role, select ‘Create a new role’ and select the options shown below for the role configuration.  We don't need access to specific S3 buckets, so you can select ‘None’.

![Amazon SageMaker IAM Role](/images/sm-keras-1.png)

Click ‘Create role’ to create a new role. In the ‘Git repositories’ section select the option to clone a public Git repository and use this URL: https://github.com/data-science-on-aws/amazon-reviews-recommendation-workshop

![Amazon SageMaker Git Repo](/images/sm-keras-git.png)

Hit ‘Create notebook instance’ to create a new notebook instance.

**Note:** It usually takes a few minutes for the notebook instance to become available. Once available, the status of the notebook instance will change from ‘Pending’ to ‘InService’. You can move on to the next step while notebook instance is still in 'Pending' state.

### Launch the Notebook
From the Jupyter notebook web UI, please launch the notebook within it.
