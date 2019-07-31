# Build a Galaxy server on AWS
## Step 1. Get AWS credentials
* register [here](https://portal.aws.amazon.com/billing/signup#/start) for an Amazon Web Services (AWS) account.
* Once you have created an account, log into the AWS Management Console.
* Create the API access credentials. Do this by creating an IAM user: click on Services → IAM → Users → Add user.
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+16.59.14.png)


![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+17.00.04.png)
* Give the user a name (e.g., cloud_demo)
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+17.02.31.png)

* attach existing policies for EC2FullAccess and S3FullAccess. After reviewing the configuration, create the user. 
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+17.16.33.png)

* Once created, make a note of and download the API access credentials. Keep these credentials safe because they are all that is required to use your cloud account.
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+17.22.37.png)

## Step 2. Launch your cluster
In this step, I will create a new cluster by launching a virtual server in the cloud, which will act as the access point for Galaxy and the cluster.
* Head to the [CloudLaunch application](https://launch.usegalaxy.org/catalog) and login through one of the available authentication providers. 

* Once logged in, choose the Galaxy CloudMan appliance.
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+17.32.34.png)

* We now need to configure the appliance launch properties. This means choosing one of the available appliance versions, the target cloud infrastructure and providing the cloud access credentials. For the Amazon cloud, the access credentials are the API keys we obtained in step 1 above. After supplying the credentials, click Test and use these credentials.
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+17.36.15.png)

* Before launching, we need to give our cluster a name. A default one is provided but feel free to replace it with something more suitable and descriptive. We also need to supply a password of choice that will protect access to the cluster once launched. Next is setting the size of storage to be associated with the cluster. The value here is in gigabytes and depends on the intended usage. We can also choose the type of virtual hardware our server will use. Then click Launch.
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-31+at+17.42.32.png)

* Initiating the launch process will take us to the My appliances page, which is a log of all instances we have launched. Now we just wait for the cluster to start.

## Step 3. Access CloudMan and Galaxy
After the cluster has started, we can access it by clicking the provided URL. For the case of CloudMan, log in with username ubuntu and the password you chose during the launch process. It may take a few more minutes to setup the cluster and start Galaxy. Once the cluster is ready, a message will be shown saying so. 
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-24+at+17.05.36.png)

* At that point, click Access Galaxy and start using Galaxy. You will probably want to register a new account.
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-24+at+17.02.12.png)

* You can see the instance is running in AWS console.
![image](https://bco-gwu.s3.amazonaws.com/images/Screen+Shot+2019-07-24+at+17.05.49.png)





