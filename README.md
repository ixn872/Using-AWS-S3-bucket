# Using-AWS-S3-bucket

Tutorial for using jupyter on S3 bucket from an EC2 instance


What's Here
-----------

This sample includes:

* README.md - this file
 
Getting Started
---------------

You will need to upload your files to S3 bucket

1. Navigate to AWS S3

2. Upload files

What Do I Do Next?
------------------

Open a terminal and connect using ssh similar to this

          > ssh -i "yourkey.pem" -L 8000:localhost:8888 ubuntu@ec2-52-10-141-125.us-west-2.compute.amazonaws.com

          
And run 

          $sudo aws s3 sync s3://<bucket name>/<file name> .

Then you may need to remove the permissions by running

          $chmod +777 <file name>

To download the whole content from the bucket run

          $sudo aws s3 cp s3://<bucket name>/<folder>  <destination>/  --recursive

          
