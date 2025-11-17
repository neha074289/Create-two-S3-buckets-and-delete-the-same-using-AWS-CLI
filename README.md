# Create-two-S3-buckets-and-delete-the-same-using-AWS-CLI

Youtube link:
https://youtu.be/RLWJ7Jx1aqY

Step 1: Open AWS Console and Create two Buckets
Make sure the bucket names are globally unique. You can leave other settings as default and create buckets.


Step 2: Open Terminal / Command Prompt
Open CloudShell in the console, or a local terminal with AWS CLI configured.
Run the following command in the terminal:
aws configure - to set up the AWS CLI with our credentials and default settings
and click enter on your AWS Access Key, Secret Key, Region, and Output format.


Step 3: List All S3 Buckets
To check if the buckets exist, run the following command:
aws s3 ls
The S3 bucket names should be visible.


Step 4: Delete the First Bucket
“Now, delete the first bucket using the AWS CLI command:
aws s3 rb s3://bucket-name1
If the bucket contains files, add --force at the end:
aws s3 rb s3://bucket-name1 --force


Step 5:
Verify deletion by using the following command:
aws s3 ls
The first bucket should no longer appear.


Step 6: Delete the Second Bucket
Delete the second bucket in the same way:
aws s3 rb s3://bucket-name2 --force


Verify that both buckets are deleted with:
aws s3 ls
