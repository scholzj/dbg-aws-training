# Lab 5: S3 and Lambda functions

* Log into the Amazon AWS console
* Make sure you are in the correct region
* Go into the S3 service

* Create new bucket for input data
* Set the bucket name and region where the data should be stored and press Next
* Add required tags and press Next
* Leave the permission setting unchanged and press Next
* Review and create the S3 bucket

* Go to Lambda and press “Create a Lambda function” button
* Select “s3-get-object-python”
* Select S3 as the source of the trigger and in S3 details select your S3 bucket and event type “Object Created (All)”
* Make sure the “Enable trigger” checkbox is checked and press Next
* Set the name and description of your Lambda function and select Python runtime
* Paste the Python code from http://jsch.cz/ZEWpv as the inline code
* Set handler to “lambda_function.lambda_handler”
* Select “Create new role from template(s)” in role and afterwards set the role name and select the “S3 object read-only permission” template
* Click Next
* Review the function and click create

* Go back to the S3 console
* Open your S3 bucket and upload a new file
* Go back to Lambda, open your Lambda function
* In the Monitoring tab check the number of invocations
* Click the “View logs in Cloud Watch” link to see the details from the execution

* Bonus point: Upload files into S3 from command line
* Bonus point: Enhance the Lambda to do something more useful :-)
