## Create a SageMaker Notebook Instance
1. Open the Amazon SageMaker Console, select 'Notebook instances' on the left and then click on ‘Create notebook instance’ and give the notebook a name. 

2. For the instance type, pick `ml.t2.large` or larger (ie. `ml.t3.2xlarge`) since our example dataset is small and we don’t intend on using GPUs inside the notebook.  We're not planning to use Elastic Inference either, so you can leave the default of ‘None’.

3. For the IAM role, select ‘Create a new role’ and select the options shown below for the role configuration.  We need to access a specific S3 bucket, so specify the following:  `amazon-reviews-pds`

![Amazon SageMaker IAM Role](/img/sm-keras-1.png)

4. Click ‘Create role’ to create a new role. In the ‘Git repositories’ section select the option to clone a public Git repository and use this URL:  `https://github.com/data-science-on-aws/amazon-sagemaker`

![Amazon SageMaker Git Repo](/img/sm-keras-git.png)

5. Hit ‘Create notebook instance’ to create a new notebook instance.  _Note: It usually takes a few minutes for the notebook instance to become available. Once available, the status of the notebook instance will change from ‘Pending’ to ‘InService’._

## Run the Notebook Examples
_Note:  You may need to modify the instance types (ie. `ml.c5.xlarge`, etc) based on instance availability in your specific AWS account._

1. [Recommendations with Factorization Machines](factorization/)

2. [Recommendations with BlazingText](blazingtext/)

3. [MNIST with TensorFlow and Keras](tensorflow/)

4. [MNIST with PyTorch](pytorch/)

5. [MNIST with MXNet](mxnet/)

## Shut Down the SageMaker Notebook Instance
Avoid unexpected costs by shutting down the notebook when you're finished.
