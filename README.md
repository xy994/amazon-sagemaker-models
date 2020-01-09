## Create a SageMaker Notebook Instance

1. Open the Amazon SageMaker Console, select 'Notebook instances' on the left and then click on ‘Create notebook instance’ and give the notebook a name. 

2. For the instance type, pick `ml.t2.large` since our example dataset is small and we don’t intend on using GPUs inside the notebook.  We're not planning to use Elastic Inference either, so you can leave the default of ‘None’.

3. For the IAM role, select ‘Create a new role’ and select the options shown below for the role configuration.  We need to access a specific S3 bucket, so specify `amazon-reviews-pds`.

![Amazon SageMaker IAM Role](/img/sm-keras-1.png)

4. Click ‘Create role’ to create a new role. In the ‘Git repositories’ section select the option to clone a public Git repository and use this URL: https://github.com/data-science-on-aws/amazon-sagemaker

![Amazon SageMaker Git Repo](/img/sm-keras-git.png)

5. Hit ‘Create notebook instance’ to create a new notebook instance.  _Note: It usually takes a few minutes for the notebook instance to become available. Once available, the status of the notebook instance will change from ‘Pending’ to ‘InService’._

## Run the Notebook Examples
### Recommendations with Factorization Machines
[factorization/](factorization/)

### Recommendations with BlazingText
[blazingtext/](blazingtext/)

### MNIST with TensorFlow and Keras
[tensorflow/](tensorflow/)

### MNIST with PyTorch
[pytorch/](pytorch/)

### MNIST with MXNet
[mxnet/](mxnet/)
