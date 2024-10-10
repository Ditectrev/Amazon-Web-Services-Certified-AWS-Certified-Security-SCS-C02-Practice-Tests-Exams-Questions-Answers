### A business requires a forensic logging solution for hundreds of Docker-based apps running on Amazon EC2. The solution must analyze logs in real time, provide message replay, and persist logs. Which Amazon Web Offerings (IAM) services should be employed to satisfy these requirements? (Select TWO)

- [ ] Amazon Athena.
- [x] Amazon Kinesis.
- [ ] Amazon SQS.
- [x] Amazon Elasticsearch.
- [ ] Amazon EMR.

### A company developed an application by using AWS Lambda, Amazon S3, Amazon Simple Notification Service (Amazon SNS), and Amazon DynamoDB. An external application puts objects into the company's S3 bucket and tags the objects with date and time. A Lambda function periodically pulls data from the company's S3 bucket based on date and time tags and inserts specific values into a DynamoDB table for further processing. The data includes personally identifiable information (Pll). The company must remove data that is older than 30 days from the S3 bucket and the DynamoDB table. Which solution will meet this requirement with the MOST operational efficiency?

- [ ] Update the Lambda function to add a TTL S3 flag to S3 objects. Create an S3 Lifecycle policy to expire objects that are older than 30 days by using the TTL S3 flag.
- [x] Create an S3 Lifecycle policy to expire objects that are older than 30 days. Update the Lambda function to add the TTL attribute in the DynamoDB table. Enable TTL on the DynamoDB table to expire entires that are older than 30 days based on the TTL attribute.
- [ ] Create an S3 Lifecycle policy to expire objects that are older than 30 days and to add all prefixes to the S3 bucket. Update the Lambda function to delete entries that are older than 30 days.
- [ ] Create an S3 Lifecycle policy to expire objects that are older than 30 days by using object tags. Update the Lambda function to delete entries that are older than 30 days.

### A company is hosting a static website on Amazon S3 The company has configured an Amazon CloudFront distribution to serve the website contents. The company has associated an IAM WAF web ACL with the CloudFront distribution. The Web ACL ensures that requests originate from the United States to address compliance restrictions. THE company is worried that the S3 URL might still be accessible directly and that requests can bypass the CloudFront distribution. Which combination of steps should the company take to remove direct access to the S3 URL? (Select TWO)

- [x] Select `Restrict Bucket Access` in the origin settings of the CloudFront distribution
- [x] Create an origin access identity (OAI) for the S3 origin.
- [ ] Update the S3 bucket policy to allow s3 GetObject with a condition that the IAM Referer key matches the secret value Deny all other.
- [ ] Configure the S3 bucket poky so that only the origin access identity (OAI) has read permission for objects in the bucket.
- [ ] Add an origin custom header that has the name Referer to the CloudFront distribution Give the header a secret value.

### A company is testing its incident response plan for compromised credentials. The company runs a database on an Amazon EC2 instance and stores the sensitive data-base credentials as a secret in AWS Secrets Manager. The secret has rotation configured with an AWS Lambda function that uses the generic rotation function template. The EC2 instance and the Lambda function are deployed in the same private subnet. The VPC has a Secrets Manager VPC endpoint. A security engineer discovers that the secret cannot rotate. The security engineer determines that the VPC endpoint is working as intended. The Amazon Cloud-Watch logs contain the following error: `"setSecret: Unable to log into database"`. Which solution will resolve this error?

- [ ] Use the AWS Management Console to edit the JSON structure of the secret in Secrets Manager so that the secret automatically conforms with the structure that the database requires.
- [x] Ensure that the security group that is attached to the Lambda function al-lows outbound connections to the EC2 instance. Ensure that the security group that is attached to the EC2 instance allows inbound connections from the security group that is attached to the Lambda function.
- [ ] Use the Secrets Manager list-secrets command in the AWS CLI to list the secret. Identify the database
credentials. Use the Secrets Manager rotate-secret command in the AWS CLI to force the immediate rotation of the secret.
- [ ] Add an internet gateway to the VPC. Create a NAT gateway in a public sub-net. Update the VPC route tables so that traffic from the Lambda function and traffic from the EC2 instance can reach the Secrets Manager public endpoint.

### A company needs a forensic-logging solution for hundreds of applications running in Docker on Amazon EC2 The solution must perform real-time analytics on the togs must support the replay of messages and must persist the logs. Which IAM services should be used to meet these requirements? (Select TWO)

- [ ] Amazon Athena.
- [x] Amazon Kinesis.
- [ ] Amazon SQS.
- [x] Amazon Elasticsearch.
- [ ] Amazon EMR.

### A company is evaluating the use of AWS Systems Manager Session Manager to gam access to the company's Amazon EC2 instances. However, until the company implements the change, the company must protect the key file for the EC2 instances from read and write operations by any other users. When a security administrator tries to connect to a critical EC2 Linux instance during an emergency, the security administrator receives the following error. `"Error Unprotected private key file – Permissions for' ssh/my_private_key pern' are too open"`. Which command should the security administrator use to modify the private key Me permissions to resolve this error?

- [ ] chmod 0040 ssh/my_private_key pern.
- [x] chmod 0400 ssh/my_private_key pern.
- [ ] chmod 0004 ssh/my_private_key pern.
- [ ] chmod 0777 ssh/my_private_key pern.

### A company deploys a set of standard IAM roles in AWS accounts. The IAM roles are based on job functions within the company. To balance operational efficiency and security, a security engineer implemented AWS Organizations SCPs to restrict access to critical security services in all company accounts. All of the company's accounts and OUs within AWS Organizations have a default FullAWSAccess SCP that is attached. The security engineer needs to ensure that no one can disable Amazon GuardDuty and AWS Security Hub. The security engineer also must not override other permissions that are granted by IAM policies that are defined in the accounts. Which SCP should the security engineer attach to the root of the organization to meet these requirements?

- [x] Option A.
![Question 7 option A](images/question7_A.jpg)
- [ ] Option B.
![Question 7 option B](images/question7_B.jpg)
- [ ] Option C.
![Question 7 option C](images/question7_C.jpg)
- [ ] Option D.
![Question 7 option D](images/question7_D.jpg)

### A company is building a data processing application mat uses AWS Lambda functions. The application's Lambda functions need to communicate with an Amazon RDS OB instance that is deployed within a VPC in the same AWS accountWhich solution meets these requirements in the MOST secure way?

- [ ] Configure the DB instance to allow public access Update the DB instance security group to allow access from the Lambda public address space for the AWS Region.
- [ ] Deploy the Lambda functions inside the VPC Attach a network ACL to the Lambda subnet Provide outbound rule access to the VPC CIDR range only Update the DB instance security group to allow traffic from 0.0.0.0/0.
- [x] Deploy the Lambda functions inside the VPC Attach a security group to the Lambda functions Provide outbound rule access to the VPC CIDR range only Update the DB instance security group to allow traffic from the Lambda security group.
- [ ] Peer the Lambda default VPC with the VPC that hosts the DB instance to allow direct network access without the need for security groups.

### A company has an application that uses an Amazon RDS PostgreSQL database. The company is developing an application feature that will store sensitive information for an individual in the database. During a security review of the environment, the company discovers that the RDS DB instance is not encrypting data at rest. The company needs a solution that will provide encryption at rest for all the existing data and for any new data that is entered for an individual. Which combination of options can the company use to meet these requirements? (Select TWO)

- [x] Create a snapshot of the DB instance. Copy the snapshot to a new snapshot, and enable encryption for the copy process. Use the new snapshot to restore the DB instance.
- [ ] Modify the configuration of the DB instance by enabling encryption. Create a snapshot of the DB instance. Use the snapshot to restore the DB instance.
- [ ] Use IAM Key Management Service (AWS KMS) to create a new default IAM managed awards key. Select this key as the encryption key for operations with Amazon RDS.
- [x] Use IAM Key Management Service (AWS KMS) to create a new CMK. Select this key as the encryption key for operations with Amazon RDS.
- [ ] Create a snapshot of the DB instance. Enable encryption on the snapshoVUse the snapshot to restore the DB instance.

### Which of the following bucket policies will ensure that objects being uploaded to a bucket called 'demo' are encrypted.

- [x] Option A.
![Question 10 option A](images/question10_A.jpg)
- [ ] Option B.
![Question 10 option B](images/question10_B.jpg)
- [ ] Option C.
![Question 10 option C](images/question10_C.jpg)
- [ ] Option D.
![Question 10 option D](images/question10_D.jpg)

### A company uses AWS Organizations to manage a multi-account AWS environment in a single AWS Region. The organization's management account is named management-01. The company has turned on AWS Config in all accounts in the organization. The company has designated an account named security-01 as the delegated administrator for AWS Config. All accounts report the compliance status of each account's rules to the AWS Config delegated administrator account by using an AWS Config aggregator. Each account administrator can configure and manage the account's own AWS Config rules to handle each account's unique compliance requirements. A security engineer needs to implement a solution to automatically deploy a set of 10 AWS Config rules to all existing and future AWS accounts in the organization. The solution must turn on AWS Config automatically during account creation. Which combination of steps will meet these requirements? (Select TWO)

- [ ] Create an AWS CloudFormation template that contains the 1 0 required AVVS Config rules. Deploy the template by using CloudFormation StackSets in the security-01 account.
- [x] Create a conformance pack that contains the 10 required AWS Config rules. Deploy the conformance pack from the security-01 account.
- [ ] Create a conformance pack that contains the 10 required AWS Config rules. Deploy the conformance pack from the management-01 account.
- [ ] Create an AWS CloudFormation template that will activate AWS Config. Deploy the template by using CloudFormation StackSets in the security-01 ac-count.
- [x] Create an AWS CloudFormation template that will activate AWS Config. Deploy the template by using CloudFormation StackSets in the management-01 account.

### A company has two IAM accounts within IAM Organizations. In Account-1. Amazon EC2 Auto Scaling is launched using a service-linked role. In Account-2. Amazon EBS volumes are encrypted with an AWS KMS key. A Security Engineer needs to ensure that the service-linked role can launch instances with these encrypted volumesWhich combination of steps should the Security Engineer take in both accounts? (Select TWO)

- [x] Allow Account-1 to access the KMS key in Account-2 using a key policy
- [ ] Attach an IAM policy to the service-linked role in Account-1 that allows these actions CreateGrant. DescnbeKey, Encrypt, GenerateDataKey, Decrypt, and ReEncrypt
- [x] Create a KMS grant for the service-linked role with these actions CreateGrant, DescnbeKey Encrypt GenerateDataKey Decrypt, and ReEncrypt
- [ ] Attach an IAM policy to the role attached to the EC2 instances with KMS actions and then allow Account-1 in the KMS key policy.
- [ ] Attach an IAM policy to the user who is launching EC2 instances and allow the user to access the KMS key policy of Account-2.

### Which of the following are valid configurations for using SSL certificates with Amazon CloudFront? (Select THREE)

- [ ] Default AWS Certificate Manager certificate.
- [ ] Custom SSL certificate stored in AWS KMS.
- [x] Default CloudFront certificate.
- [x] Custom SSL certificate stored in AWS Certificate Manager.
- [ ] Default SSL certificate stored in AWS Secrets Manager.
- [x] Custom SSL certificate stored in AWS IAM.

### A Security Engineer is troubleshooting an issue with a company's custom logging application. The application logs are written to an Amazon S3 bucket with event notifications enabled to send events to an Amazon SNS topic. All logs are encrypted at rest using an AWS KMS CMK. The SNS topic is subscribed to an encrypted Amazon SQS queue. The logging application polls the queue for new messages that contain metadata about the S3 object. The application then reads the content of the object from the S3 bucket for indexing. The Logging team reported that Amazon CloudWatch metrics for the number of messages sent or received is showing zero. No tags are being received. What should the Security Engineer do to troubleshoot this issue?

- [ ] Option A: Add the following statement to the IAM managed CMKs.
![Question 14 option A](images/question14_A.jpg)
- [ ] Option B: Add the following statement to the CMK key policy.
![Question 14 option B](images/question14_B.jpg)
- [ ] Option C: Add the following statement to the CMK key policy.
![Question 14 option C](images/question14_C.jpg)
- [x] Option D: Add the following statement to the CMK key policy.
![Question 14 option D](images/question14_D.jpg)

### A security engineer needs to implement a write-once-read-many (WORM) model for data that a company will store in Amazon S3 buckets. The company uses the S3 Standard storage class for all of its S3 buckets. The security engineer must ensure that objects cannot be overwritten or deleted by any user, including the AWS account root user. Which solution will meet these requirements?

- [x] Create new S3 buckets with S3 Object Lock enabled in compliance mode. Place objects in the S3 buckets.
- [ ] Use S3 Glacier Vault Lock to attach a Vault Lock policy to new S3 buckets. Wait 24 hours to complete the Vault Lock process. Place objects in the S3 buckets.
- [ ] Create new S3 buckets with S3 Object Lock enabled in governance mode. Place objects in the S3 buckets.
- [ ] Create new S3 buckets with S3 Object Lock enabled in governance mode. Add a legal hold to the S3 buckets. Place objects in the S3 buckets.

### A development team is attempting to encrypt and decode a secure string parameter from the IAM Systems Manager Parameter Store using an IAM Key Management Service (AWS KMS) CMK. However, each attempt results in an error message being sent to the development team. Which CMK-related problems possibly account for the error? (Select TWO)

- [x] The CMK is used in the attempt does not exist.
- [ ] The CMK is used in the attempt needs to be rotated.
- [ ] The CMK is used in the attempt is using the CMKs key ID instead of the CMK ARN.
- [x] The CMK is used in the attempt is not enabled.
- [ ] The CMK is used in the attempt is using an alias.

### A security engineer logs in to the AWS Lambda console with administrator permissions. The security engineer is trying to view logs in Amazon CloudWatch for a Lambda function that is named my Function. When the security engineer chooses the option in the Lambda console to view logs in CloudWatch, an `error loading Log Streams` message appears. The IAM policy for the Lambda function's execution role contains the following. How should the security engineer correct the error?

![Question 17](images/question17.jpg)

- [ ] Move the logs:CreateLogGroup action to the second Allow statement.
- [ ] Add the logs:PutDestination action to the second Allow statement.
- [ ] Add the logs:GetLogEvents action to the second Allow statement.
- [x] Add the logs:GetLogEvents action to the second Allow statement.

### A company plans to create individual child accounts within an existing organization in IAM Organizations for each of its DevOps teams. AWS CloudTrail has been enabled and configured on all accounts to write audit logs to an Amazon S3 bucket in a centralized IAM account. A security engineer needs to ensure that DevOps team members are unable to modify or disable this configuration. How can the security engineer meet these requirements?

- [ ] Create an IAM policy that prohibits changes to the specific CloudTrail trail and apply the policy to the IAM account root user.
- [ ] Create an S3 bucket policy in the specified destination account for the CloudTrail trail that prohibits configuration changes from the IAM account root user in the source account.
- [x] Create an SCP that prohibits changes to the specific CloudTrail trail and apply the SCP to the appropriate organizational unit or account in Organizations.
- [ ] Create an IAM policy that prohibits changes to the specific CloudTrail trail and apply the policy to a new IAM group. Have team members use individual IAM accounts that are members of the new IAM group.

### A company uses Amazon RDS for MySQL as a database engine for its applications. A recent security audit revealed an RDS instance that is not compliant with company policy for encrypting data at rest. A security engineer at the company needs to ensure that all existing RDS databases are encrypted using server-side encryption and that any future deviations from the policy are detected. Which combination of steps should the security engineer take to accomplish this? (Select TWO)

- [x] Create an AWS Config rule to detect the creation of encrypted RDS databases. Create an Amazon EventBridge (Amazon CloudWatch Events) rule to trigger on the AWS Config rules compliance state change and use Amazon Simple Notification Service (Amazon SNS) to notify the security operations team.
- [ ] Use AWS System Manager State Manager to detect RDS database encryption configuration drift. Create an Amazon EventBridge (Amazon CloudWatch Events) rule to track state changes and use Amazon Simple Notification Service (Amazon SNS) to notify the security operations team.
- [ ] Create a read replica for the existing unencrypted RDS database and enable replica encryption in the process. Once the replica becomes active, promote it into a standalone database instance and terminate the unencrypted database instance.
- [x] Take a snapshot of the unencrypted RDS database. Copy the snapshot and enable snapshot encryption in the process. Restore the database instance from the newly created encrypted snapshot. Terminate the unencrypted database instance.
- [ ] Enable encryption for the identified unencrypted RDS instance by changing the configurations of the existing database.

### A company has a large fleet of Linux Amazon EC2 instances and Windows EC2 instances that run in private subnets. The company wants all remote administration to be performed as securely as possible in the AWS Cloud. Which solution will meet these requirements?

- [x] Do not use SSH-RSA private keys during the launch of new instances. Implement AWS Systems Manager Session Manager.
- [ ] Generate new SSH-RSA private keys for existing instances. Implement AWS Systems Manager Session Manager.
- [ ] Do not use SSH-RSA private keys during the launch of new instances. Configure EC2 Instance Connect.
- [ ] Generate new SSH-RSA private keys for existing instances. Configure EC2 Instance Connect.

### A company has an AWS Lambda function that creates image thumbnails from larger images. The Lambda function needs read and write access to an Amazon S3 bucket in the same AWS account. Which solutions will provide the Lambda function this access? (Select TWO)

- [ ] Create an IAM user that has only programmatic access. Create a new access key pair. Add environmental variables to the Lambda function with the access key ID and secret access key. Modify the Lambda function to use the environmental variables at run time during communication with Amazon S3.
- [ ] Generate an Amazon EC2 key pair. Store the private key in AWS Secrets Man-ager. Modify the Lambda function to retrieve the private key from Secrets Manager and to use the private key during communication with Amazon S3.
- [x] Create an IAM role for the Lambda function. Attach an IAM policy that al-lows access to the S3 bucket.
- [x] Create an IAM role for the Lambda function. Attach a bucket policy to the S3 bucket to allow access. Specify the function's IAM role as the principal.
- [ ] Create a security group. Attach the security group to the Lambda function. Attach a bucket policy that allows access to the S3 bucket through the security group ID.

### A security engineer is designing an IAM policy for a script that will use the AWS CLI. The script currently assumes an IAM role that is attached to three AWS managed IAM policies: AmazonEC2FullAccess, AmazonDynamoDBFullAccess, and Ama-zonVPCFull Access. The security engineer needs to construct a least privilege IAM policy that will replace the AWS managed IAM policies that are attached to this role. Which solution will meet these requirements in the MOST operationally efficient way?

- [x] In AWS CloudTrail, create a trail for management events. Run the script with the existing AWS managed IAM policies. Use IAM Access Analyzer to generate a new IAM policy that is based on access activity in the trail. Replace the existing AWS managed IAM policies with the generated IAM poli-cy for the role.
- [ ] Remove the existing AWS managed IAM policies from the role. Attach the IAM Access Analyzer Role Policy Generator to the role. Run the script. Return to IAM Access Analyzer and generate a least privilege IAM policy. Attach the new IAM policy to the role.
- [ ] Create an account analyzer in IAM Access Analyzer. Create an archive rule that has a filter that checks whether the Principal Arn value matches the ARN of the role. Run the script. Remove the existing AWS managed IAM policies from the role.
- [ ] In AWS CloudTrail, create a trail for management events. Remove the existing AWS managed IAM policies from the role. Run the script. Find the authorization failure in the trail event that is associated with the script. Create a new IAM policy that includes the action and resource that caused the authorization failure. Repeat the process until the script succeeds. Attach the new IAM policy to the role.

### A company that uses AWS Organizations wants to see AWS Security Hub findings for many AWS accounts and AWS Regions. Some of the accounts are in the company's organization, and some accounts are in organizations that the company manages for customers. Although the company can see findings in the Security Hub administrator account for accounts in the company's organization, there are no findings from accounts in other organizations. Which combination of steps should the company take to see findings from accounts that are outside the organization that includes the Security Hub administrator account? (Select TWO)

- [ ] Use a designated administration account to automatically set up member accounts.
- [ ] Create the AWS Service Role ForSecurrty Hub service-linked rote for Security Hub.
- [x] Send an administration request from the member accounts.
- [ ] Enable Security Hub for all member accounts.
- [x] Send invitations to accounts that are outside the company's organization from the Security Hub administrator account.

### A company uses identity federation to authenticate users into an identity account (987654321987) where the users assume an IAM role named IdentityRole. The users then assume an IAM role named JobFunctionRole in the target IAM account (123456789123) to perform their job functions. A user is unable to assume the IAM role in the target account. The policy attached to the role in the identity account is. What should be done to enable the user to assume the appropriate role in the target account?

![Question 24](images/question24.jpg)

- [ ] Option A: Update the IAM policy attached to the role in the identity account to be.
![Question 24 option A](images/question24_A.png)
- [x] Option B: Update the trust policy on the role in the target account to be.
![Question 24 option B](images/question24_B.png)
- [ ] Option C: Update the trust policy on the role in the identity account to be.
![Question 24 option C](images/question24_C.png)
- [ ] Option D: Update the IAM policy attached to the role in the target account to be.
![Question 24 option D](images/question24_D.png)

### A company hosts a web application on an Apache Web server. The application runs on Amazon EC2 instances that are in an Auto Scaling group. The company configured the EC2 instances to send the Apache Web server logs to an Amazon CloudWatch Logs group that the company has configured to expire after 1 year. Recently, the company discovered in the Apache Web server logs that a specific IP address is sending suspicious requests to the Web application. A security engineer wants to analyze the past week of Apache Web server logs to determine how many requests that the IP address sent and the corresponding URLs that the IP address requested. What should the security engineer do to meet these requirements with the LEAST effort?

- [ ] Export the CloudWatch Logs group data to Amazon S3. Use Amazon Macie to query the logs for the specific IP address and the requested URLs.
- [ ] Configure a CloudWatch Logs subscription to stream the log group to an Amazon OpenSearch Service cluster. Use OpenSearch Service to analyze the logs for the specific IP address and the requested URLs.
- [x] Use CloudWatch Logs Insights and a custom query syntax to analyze the CloudWatch logs for the specific IP address and the requested URLs.
- [ ] Export the CloudWatch Logs group data to Amazon S3. Use AWS Glue to crawl the S3 bucket for only the log entries that contain the specific IP ad-dress. Use AWS Glue to view the results.

### A company has multiple Amazon S3 buckets encrypted with customer-managed CMKs Due to regulatory requirements the keys must be rotated every year. The company's Security Engineer has enabled automatic key rotation for the CMKs; however the company wants to verity that the rotation has occurred. What should the Security Engineer do to accomplish this?

- [x] Filter AWS CloudTrail logs for KeyRotaton events.
- [ ] Monitor Amazon CloudWatch Events for any AWS KMS CMK rotation events.
- [ ] Using the IAM CLI run the `IAM kms gel-key-relation-status` operation with the `–key-id` parameter to check the CMK rotation date.
- [ ] Use Amazon Athena to query AWS CloudTrail logs saved in an S3 bucket to filter Generate New Key events.

### A company has implemented IAM WAF and Amazon CloudFront for an application. The application runs on Amazon EC2 instances that are part of an Auto Scaling group. The Auto Scaling group is behind an Application Load Balancer (ALB). The IAM WAF web ACL uses an IAM Managed Rules rule group and is associated with the CloudFront distribution. CloudFront receives the request from IAM WAF and then uses the ALB as the distribution's origin. During a security review, a security engineer discovers that the infrastructure is susceptible to a large, layer 7 DDoS attack. How can the security engineer improve the security at the edge of the solution to defend against this type of attack?

- [ ] Configure the CloudFront distribution to use the Lambda@Edge feature. Create an IAM Lambda function that imposes a rate limit on CloudFront viewer requests. Block the request if the rate limit is exceeded.
- [ ] Configure the IAM WAF web ACL so that the Web ACL has more capacity units to process all IAM WAF rules faster.
- [x] Configure IAM WAF with a rate-based rule that imposes a rate limit that automatically blocks requests when the rate limit is exceeded.
- [ ] Configure the CloudFront distribution to use IAM WAF as its origin instead of the ALB.

### A company has multiple accounts in the AWS Cloud. Users in the developer account need to have access to specific resources in the production account. What is the MOST secure way to provide this access?

- [ ] Create one IAM user in the production account. Grant the appropriate permissions to the resources that are needed. Share the password only with the users that need access.
- [ ] Create cross account access with an IAM role in the developer account. Grant the appropriate permissions to this role. Allow users in the developer account to assume this role to access the production resources.
- [ ] Create cross-account access with an IAM user account in the production account. Grant the appropriate permissions to this user account. Allow users in the developer account to use this user account to access the production resources.
- [x] Create cross-account access with an IAM role in the production account. Grant the appropriate permissions to this role. Allow users in the developer account to assume this role to access the production resources.

### A System Administrator is unable to start an Amazon EC2 instance in the eu-west-1 Region using an IAM role The same System Administrator is able to start an EC2 instance in the eu-west-2 and eu-west-3 Regions. The IAMSystemAdministrator access policy attached to the System Administrator IAM role allows unconditional access to all IAM services and resources within the account. Which configuration caused this issue?

- [ ] Option A: An SCP is attached to the account with the following permission statement.
![Question 29 option A](images/question29_A.jpg)
- [x] Option B: A permission boundary policy is attached to the System Administrator role with the following permission statement.
![Question 29 option B](images/question29_B.jpg)
- [ ] Option C: A permission boundary is attached to the System Administrator role with the following permission statement.
![Question 29 option C](images/question29_C.jpg)
- [ ] Option D: An SCP is attached to the account with the following statement.
![Question 29 option D](images/question29_D.jpg)

### Amazon GuardDuty has detected communications to a known command and control endpoint from a company's Amazon EC2 instance. The instance was found to be running a vulnerable version of a common web framework. The company's security operations team wants to quickly identity other compute resources with the specific version of that framework installed. Which approach should the team take to accomplish this task?

- [ ] Scan all the EC2 instances for noncompliance with IAM Config. Use Amazon Athena to query AWS CloudTrail logs for the framework installation.
- [ ] Scan all the EC2 instances with the Amazon Inspector Network Reachability rules package to identity instances running a web server with RecognizedPortWithListener findings.
- [x] Scan all the EC2 instances with IAM Systems Manager to identify the vulnerable version of the Web framework.
- [ ] Scan an the EC2 instances with IAM Resource Access Manager to identify the vulnerable version of the Web framework.

### A company stores sensitive documents in Amazon S3 by using server-side encryption with an AWS Key Management Service (AWS KMS) CMK. A new requirement mandates that the CMK that is used for these documents can be used only for S3 actions. Which statement should the company add to the key policy to meet this requirement?

- [ ] Option A.
![Question 31 option A](images/question31_A.png)
- [ ] Option B.
![Question 31 option B](images/question31_B.png)
- [x] Option C.
![Question 31 option C](images/question31_C.png)
- [ ] Option D.
![Question 31 option D](images/question31_D.png)

### A company finds that one of its Amazon EC2 instances suddenly has a high CPU usage. The company does not know whether the EC2 instance is compromised or whether the operating system is performing background cleanup. Which combination of steps should a security engineer take before investigating the issue? (Select THREE)

- [ ] Disable termination protection for the EC2 instance if termination protection has not been disabled.
- [x] Enable termination protection for the EC2 instance if termination protection has not been enabled.
- [x] Take snapshots of the Amazon Elastic Block Store (Amazon EBS) data volumes that are attached to the EC2 instance.
- [ ] Remove all snapshots of the Amazon Elastic Block Store (Amazon EBS) data volumes that are attached to the EC2 instance.
- [x] Capture the EC2 instance metadata, and then tag the EC2 instance as under quarantine.
- [ ] Immediately remove any entries in the EC2 instance metadata that contain sensitive information.

### A company hosts an application on Amazon EC2 that is subject to specific rules for regulatory compliance. One rule states that traffic to and from the workload must be inspected for network-level attacks. This involves inspecting the whole packet. To comply with this regulatory rule, a security engineer must install intrusion detection software on a c5n.4xlarge EC2 instance. The engineer must then configure the software to monitor traffic to and from the application instances. What should the security engineer do next?

- [ ] Place the network interface in promiscuous mode to capture the traffic.
- [ ] Configure VPC Flow Logs to send traffic to the monitoring EC2 instance using a Network Load Balancer.
- [x] Configure VPC traffic mirroring to send traffic to the monitoring EC2 instance using a Network Load Balancer.
- [ ] Use Amazon Inspector to detect network-level attacks and trigger an IAM Lambda function to send the suspicious packets to the EC2 instance.

### A company has a relational database workload that runs on Amazon Aurora MySQL. According to new compliance standards the company must rotate all database credentials every 30 days. The company needs a solution that maximizes security and minimizes development effort. Which solution will meet these requirements?

- [x] Store the database credentials in AWS Secrets Manager. Configure automatic credential rotation for every 30 days.
- [ ] Store the database credentials in AWS Systems Manager Parameter Store. Create an AWS Lambda function to rotate the credentials every 30 days.
- [ ] Store the database credentials in an environment file or in a configuration file. Modify the credentials every 30 days.
- [ ] Store the database credentials in an environment file or in a configuration file. Create an AWS Lambda function to rotate the credentials every 30 days.

### A company uses AWS Organizations to manage a small number of AWS accounts. However, the company plans to add 1 000 more accounts soon. The company allows only a centralized security team to create IAM roles for all AWS accounts and teams. Application teams submit requests for IAM roles to the security team. The security team has a backlog of IAM role requests and cannot review and provision the IAM roles quickly. The security team must create a process that will allow application teams to provision their own IAM roles. The process must also limit the scope of IAM roles and prevent privilege escalation. Which solution will meet these requirements with the LEAST operational overhead?

- [ ] Create an IAM group for each application team. Associate policies with each IAM group. Provision IAM users for each application team member. Add the new IAM users to the appropriate IAM group by using role-based access control (RBAC).
- [ ] Delegate application team leads to provision IAM rotes for each team. Conduct a quarterly review of the IAM rotes the team leads have provisioned. Ensure that the application team leads have the appropriate training to review IAM roles.
- [ ] Put each AWS account in its own OU. Add an SCP to each OU to grant access to only the AWS services that the teams plan to use. Include conditions tn the AWS account of each team.
- [x] Create an SCP and a permissions boundary for IAM roles. Add the SCP to the root OU so that only roles that have the permissions boundary attached can create any new IAM roles.

### A company's security engineer is developing an incident response plan to detect suspicious activity in an AWS account for VPC hosted resources. The security engineer needs to provide visibility for as many AWS Regions as possible. Which combination of steps will meet these requirements MOST cost-effectively? (Select TWO)

- [ ] Turn on VPC Flow Logs for all VPCs in the account.
- [x] Activate Amazon GuardDuty across all AWS Regions.
- [ ] Activate Amazon Detective across all AWS Regions.
- [x] Create an Amazon Simple Notification Service (Amazon SNS) topic. Create an Amazon EventBridge rule that responds to findings and publishes the findings to the SNS topic.
- [ ] Create an AWS Lambda function. Create an Amazon EventBridge rule that invokes the Lambda function to publish findings to Amazon Simple Email Ser-vice (Amazon SES).

### A team is using AWS Secrets Manager to store an application database password. Only a limited number of IAM principals within the account can have access to the secret. The principals who require access to the secret change frequently. A security engineer must create a solution that maximizes flexibility and scalability. Which solution will meet these requirements?

- [ ] Use a role-based approach by creating an IAM role with an inline permissions policy that allows access to the secret. Update the IAM principals in the role trust policy as required.
- [ ] Deploy a VPC endpoint for Secrets Manager. Create and attach an endpoint policy that specifies the IAM principals that are allowed to access the secret. Update the list of IAM principals as required.
- [x] Use a tag-based approach by attaching a resource policy to the secret. Apply tags to the secret and the IAM principals. Use the `aws:PrincipalTag` and `aws:ResourceTag` IAM condition keys to control access.
- [ ] Use a deny-by-default approach by using IAM policies to deny access to the secret explicitly. Attach the policies to an IAM group. Add all IAM principals to the IAM group. Remove principals from the group when they need access. Add the principals to the group again when access is no longer allowed.

### A company uses AWS Organizations to run workloads in multiple AWS accounts. Currently the individual team members at the company access all Amazon EC2 instances remotely by using SSH or Remote Desktop Protocol (RDP) The company does not have any audit trails and security groups are occasionally open. The company must secure access management and implement a centralized togging solution. Which solution will meet these requirements MOST securely?

- [ ] Configure trusted access for AWS System Manager in Organizations. Configure a bastion host from the management account. Replace SSH and RDP by using Systems Manager Session Manager from the management account Configure Session Manager logging to Amazon CloudWatch Logs.
- [ ] Replace SSH and RDP with AWS Systems Manager Session Manager. Install Systems Manager Agent (SSM Agent) on the instances Attach the.
- [x] AmazonSSMManagedlnstanceCore role to the instances. Configure session data streaming to Amazon CloudWatch Logs. Create a separate logging account that has appropriate cross-account permissions to audit the log data.
- [ ] Install a bastion host in the management account. Reconfigure all SSH and RDP to allow access only from the bastion host Install AWS Systems Manager Agent (SSM Agent) on the bastion host Attach the AmazonSSMManagedlnstanceCore role to the bastion host. Configure session data streaming to Amazon CloudWatch Logs in a separate logging account to audit log data.
- [ ] Replace SSH and RDP with AWS Systems Manager State Manager. Install Systems Manager Agent (SSM Agent) on the instances Attach the AmazonSSMManagedlnstanceCore role to the instances. Configure session data streaming to Amazon CloudTrail. Use CloudTrail Insights to analyze the trail data.

### A company became aware that one of its access keys was exposed on a code sharing website 11 days ago. A Security Engineer must review all use of the exposed access keys to determine the extent of the exposure. The company enabled AWS CloudTrail m an regions when it opened the account. Which of the following will allow the Security Engineer 10 complete the task?

- [x] Filter the event history on the exposed access key in the CloudTrail console Examine the data from the past 11 days.
- [ ] Use the IAM CLI to generate an IAM credential report Extract all the data from the past 11 days.
- [ ] Use Amazon Athena to query the CloudTrail logs from Amazon S3 Retrieve the rows for the exposed access key for the past 11 days.
- [ ] Use the Access Advisor tab in the IAM console to view all of the access key activity for the past 11 days.

### An application team wants to use IAM Certificate Manager (ACM) to request public certificates to ensure that data is secured in transit. The domains that are being used are not currently hosted on Amazon Route 53 The application team wants to use an IAM managed distribution and caching solution to optimize requests to its systems and provide better points of presence to customers The distribution solution will use a primary domain name that is customized The distribution solution also will use several alternative domain names The certificates must renew automatically over an indefinite period of time. Which combination of steps should the application team take to deploy this architecture? (Select THREE)

- [x] Request a certificate for ACM in the `us-west-2` Region Add the domain names that the certificate will secure.
- [ ] Send an email message to the domain administrators to request vacation of the domains for ACM.
- [x] Request validation of the domains for ACM through DNS Insert CNAME records into each domain's DNS zone.
- [ ] Create an Application Load Balancer for me caching solution Select the newly requested certificate from ACM to be used for secure connections.
- [x] Create an Amazon CloudFront distribution for the caching solution Enter the main CNAME record as the Origin Name Enter the subdomain names or alternate names in the Alternate Domain Names Distribution Settings Select the newly requested certificate from ACM to be used for secure connections.
- [ ] Request a certificate from ACM in the `us-east-1` Region Add the domain names that the certificate. Wil secure.

### A company uses Amazon API Gateway to present REST APIs to users. An API developer wants to analyze API access patterns without the need to parse the log files. Which combination of steps will meet these requirements with the LEAST effort? (Select TWO)

- [x] Configure access logging for the required API stage.
- [ ] Configure an AWS CloudTrail trail destination for API Gateway events. Configure filters on the userldentity, userAgent, and sourcelPAddress fields.
- [ ] Configure an Amazon S3 destination for API Gateway logs. Run Amazon Athena queries to analyze API access information.
- [x] Use Amazon CloudWatch Logs Insights to analyze API access information.
- [ ] Select the Enable Detailed CloudWatch Metrics option on the required API stage.

### There are currently multiple applications hosted in a VPC. During monitoring it has been noticed that multiple port scans are coming in from a specific IP Address block. The internal security team has requested that all offending IP Addresses be denied for the next 24 hours. Which of the following is the best method to quickly and temporarily deny access from the specified IP Address's.

- [ ] Create an AD policy to modify the. Windows Firewall settings on all hosts in the VPC to deny access from the IP Address block.
- [x] Modify the Network ACLs associated with all public subnets in the VPC to deny access from the IP Address block.
- [ ] Add a rule to all of the VPC Security Groups to deny access from the IP Address block.
- [ ] Modify the. Windows Firewall settings on all AMI'S that your organization uses in that VPC to deny access from the IP address block.

### A company needs to store multiple years of financial records. The company wants to use Amazon S3 to store copies of these documents. The company must implement a solution to prevent the documents from being edited, replaced, or deleted for 7 years after the documents are stored in Amazon S3. The solution must also encrypt the documents at rest. A security engineer creates a new S3 bucket to store the documents. What should the security engineer do next to meet these requirements?

- [ ] Configure S3 server-side encryption. Create an S3 bucket policy that has an explicit deny rule for all users for `s3:DeleteObject` and `s3:PutObject` API calls. Configure S3 Object Lock to use governance mode with a retention period of 7 years.
- [x] Configure S3 server-side encryption. Configure S3 Versioning on the S3 bucket. Configure S3 Object Lock to use compliance mode with a retention period of 7 years.
- [ ] Configure S3 Versioning. Configure S3 Intelligent-Tiering on the S3 bucket to move the documents to S3 Glacier Deep Archive storage. Use S3 server-side encryption immediately. Expire the objects after 7 years.
- [ ] Set up S3 Event Notifications and use S3 server-side encryption. Configure S3 Event Notifications to target an AWS Lambda function that will review any S3 API call to the S3 bucket and deny the `s3:DeleteObject` and `s3:PutObject` API calls. Remove the S3 event notification after 7 years.

### There is a requirement for a company to transfer large amounts of data between IAM and an on-premise location. There is an additional requirement for low latency and high consistency traffic to IAM. Given these requirements how would you design a hybrid architecture?

- [x] Provision a Direct Connect connection to an IAM region using a Direct Connect partner.
- [ ] Create a VPN tunnel for private connectivity, which increases network consistency and reduces latency.
- [ ] Create an IPsec tunnel for private connectivity, which increases network consistency and reduces latency.
- [ ] Create a VPC peering connection between IAM and the Customer gateway.

### A company uses a third-party identity provider and SAML-based SSO for its AWS accounts. After the third-party identity provider renewed an expired signing certificate, users saw the following message. When trying to log in: Error: `Response Signature Invalid (Service: AWSSecurityTokenService; Status Code: 400; Error Code:InvalidldentityToken)`. A security engineer needs to provide a solution that corrects the error and minimizes operational overhead. Which solution meets these requirements?

- [ ] Upload the third-party signing certificate's new private key to the AWS identity provider entity defined in AWS Identity and Access Management (IAM) by using the AWS Management Console.
- [ ] Sign the identity provider's metadata file with the new public key. Upload the signature to the AWS identity provider entity defined in AWS Identity and Access Management (IAM) by using the AWS CU.
- [x] Download the updated SAML metadata file from the identity service provider. Update the file in the AWS identity provider entity defined in AWS Identity and Access Management (IAM) by using the AWS CLI.
- [ ] Configure the AWS identity provider entity defined in AWS Identity and Access Management (IAM) to synchronously fetch the new public key by using the AWS Management Console.

### An AWS account that is used for development projects has a VPC that contains two subnets. The first subnet is named public-subnet-1 and has the CIDR block 192.168.1.0/24 assigned. The other subnet is named private-subnet-2 and has the CIDR block 192.168.2.0/24 assigned. Each subnet contains Amazon EC2 instances. Each subnet is currently using the VPC's default network ACL. The security groups that the EC2 instances in these subnets use have rules that allow traffic between each instance. Where required. Currently, all network traffic flow is working as expected between the EC2 instances that are using these subnets. A security engineer creates a new network ACL that is named subnet-2-NACL with default entries. The security engineer immediately configures private-subnet-2 to use the new network ACL and makes no other changes to the infrastructure. The security engineer starts to receive reports that the EC2 instances in public-subnet-1 and public-subnet-2 cannot communicate with each other. Which combination of steps should the security engineer take to allow the EC2 instances that are running in these two subnets to communicate again? (Select TWO)

- [ ] Add an outbound allow rule for 192.168.2.0/24 in the VPC's default network ACL.
- [ ] Add an inbound allow rule for 192.168.2.0/24 in the VPC's default network ACL.
- [ ] Add an outbound allow rule for 192.168.2.0/24 in subnet-2-NACL.
- [x] Add an inbound allow rule for 192.168.1.0/24 in subnet-2-NACL.
- [x] Add an outbound allow rule for 192.168.1.0/24 in subnet-2-NACL.

### Within a VPC, a corporation runs an Amazon RDS Multi-AZ DB instance. The database instance is connected to the internet through a NAT gateway via two subnets. Additionally, the organization has application servers that are hosted on Amazon EC2 instances and use the RDS database. These EC2 instances have been deployed onto two more private subnets inside the same VPC. These EC2 instances connect to the internet through a default route via the same NAT gateway. Each VPC subnet has its own route table. The organization implemented a new security requirement after a recent security examination. Never allow the database instance to connect to the internet. A security engineer must perform this update promptly without interfering with the network traffic of the application servers. How will the security engineer be able to comply with these requirements?

- [ ] Remove the existing NAT gateway. Create a new NAT gateway that only the application server subnets can use.
- [ ] Configure the DB instances inbound network ACL to deny traffic from the security group ID of the NAT gateway.
- [x] Modify the route tables of the DB instance subnets to remove the default route to the NAT gateway.
- [ ] Configure the route table of the NAT gateway to deny connections to the DB instance subnets.

### An audit determined that a company's Amazon EC2 instance security group violated company policy by allowing unrestricted incoming SSH traffic. A security engineer must implement a near-real-time monitoring and alerting solution that will notify administrators of such violations. Which solution meets these requirements with the MOST operational efficiency?

- [ ] Create a recurring Amazon Inspector assessment run that runs every day and uses the Network Reachability package. Create an Amazon CloudWatch rule that invokes an IAM Lambda function when an assessment run starts. Configure the Lambda function to retrieve and evaluate the assessment run report when it completes. Configure the Lambda function also to publish an Amazon Simple Notification Service (Amazon SNS) notification if there are any violations for unrestricted incoming SSH traffic.
- [x] Use the restricted-ssh IAM Config managed rule that is invoked by security group configuration changes that are not compliant. Use the IAM Config remediation feature to publish a message to an Amazon Simple Notification Service (Amazon SNS) topic.
- [ ] Configure VPC Flow Logs for the VPC. and specify an Amazon CloudWatch Logs group. Subscribe the CloudWatch Logs group to an IAM Lambda function that parses new log entries, detects successful connections on port 22, and publishes a notification through Amazon Simple Notification Service (Amazon SNS).
- [ ] Create a recurring Amazon Inspector assessment run that runs every day and uses the Security Best Practices package. Create an Amazon CloudWatch rule that invokes an IAM Lambda function when an assessment run starts. Configure the Lambda function to retrieve and evaluate the assessment run report when it completes. Configure the Lambda function also to publish an Amazon Simple Notification Service (Amazon SNS) notification if there are any violations for unrestricted incoming SSH traffic.

### A company is using Amazon Elastic Container Service (Amazon ECS) to deploy an application that deals with sensitive data During a recent security audit, the company identified a security issue in which Amazon RDS credentials were stored with the application code In the company's source code repository. A security engineer needs to develop a solution to ensure that database credentials are stored securely and rotated periodically. The credentials should be accessible to the application only. The engineer also needs to prevent database administrators from sharing database credentials as plaintext with other teammates. The solution must also minimize administrate overhead. Which solution meets these requirements?

- [ ] Use the IAM Systems Manager Parameter Store to generate database credentials. Use an IAM profile for ECS tasks to restrict access to database credentials to specific containers only.
- [ ] Use IAM Secrets Manager to store database credentials. Use an IAM inline policy for ECS tasks to restrict access to database credentials to specific containers only.
- [ ] Use the IAM Systems Manager Parameter Store to store database credentials. Use IAM roles for ECS tasks to restrict access to database credentials to specific containers only
- [x] Use IAM Secrets Manager to store database credentials. Use IAM roles for ECS tasks to restrict access to database credentials to specific containers only.

### A company discovers a billing anomaly in its AWS account. A security consultant investigates the anomaly and discovers that an employee. Who left the company 30 days ago still has access to the account. The company has not monitored account activity in the past. The security consultant needs to determine. Which resources have been deployed or reconfigured by the employee as quickly as possible. Which solution will meet these requirements?

- [ ] In AWS Cost Explorer, filter chart data to display results from the past 30 days. Export the results to a data table. Group the data table by re-source.
- [ ] Use AWS Cost Anomaly Detection to create a cost monitor. Access the detection history. Set the time frame to Last 30 days. In the search area, choose the service category.
- [x] In AWS CloudTrail, filter the event history to display results from the past 30 days. Create an Amazon Athena table that contains the data. Partition the table by event source.
- [ ] Use AWS Audit Manager to create an assessment for the past 30 days. Apply a usage-based framework to the assessment. Configure the assessment to assess by resource.

### A company wants to monitor the deletion of AWS Key Management Service (AWS KMS) customer managed keys. A security engineer needs to create an alarm that will notify the company before a KMS key is deleted. The security engineer has configured the integration of AWS CloudTrail with Amazon CloudWatch. What should the security engineer do next to meet these requirements?

- [ ] Specify the deletion time of the key material during KMS key creation. Create a custom AWS Config rule to assess the key's scheduled deletion. Configure the rule to trigger upon a configuration change. Send a message to an Amazon Simple Notification Service (Amazon SNS) topic if the key is scheduled for deletion.
- [ ] Create an Amazon EventBridge rule to detect KMS API calls of DeleteAlias. Create an AWS Lambda function to send an Amazon Simple Notification Service (Amazon SNS) message to the company. Add the Lambda function as the target of the EventBridge rule.
- [x] Create an Amazon EventBridge rule to detect KMS API calls of DisableKey and ScheduleKeyDeletion. Create an AWS Lambda function to send an Amazon Simple Notification Service (Amazon SNS) message to the company. Add the Lambda function as the target of the EventBridge rule.
- [ ] Create an Amazon Simple Notification Service (Amazon SNS) policy to detect KMS API calls of RevokeGrant and ScheduleKeyDeletion. Create an AWS Lambda function to generate the alarm and send the notification to the company. Add the Lambda function as the target of the SNS policy.

### A company accidentally deleted the private key for an Amazon Elastic Block Store (Amazon EBS)-backed Amazon EC2 instance. A security engineer needs to regain access to the instance. Which combination of steps will meet this requirement? (Choose TWO)

- [x] Stop the instance. Detach the root volume. Generate a new key pair.
- [ ] Keep the instance running. Detach the root volume. Generate a new key pair.
- [x] When the volume is detached from the original instance, attach the volume to another instance as a data volume. Modify the authorized_keys file with a new public key. Move the volume back to the original instance. Start the instance.
- [ ] When the volume is detached from the original instance, attach the volume to another instance as a data volume. Modify the authorized_keys file with a new private key. Move the volume back to the original instance. Start the instance.
- [ ] When the volume is detached from the original instance, attach the volume to another instance as a data volume. Modify the authorized_keys file with a new public key. Move the volume back to the original instance that is running.

### A company deployed Amazon GuardDuty in the `us-east-1` Region. The company wants all DNS logs that relate to the company's Amazon EC2 instances to be inspected. What should a security engineer do to ensure that the EC2 instances are logged?

- [ ] Use IPv6 addresses that are configured for hostnames.
- [ ] Configure external DNS resolvers as internal resolvers that are visible only to IAM.
- [x] Use IAM DNS resolvers for all EC2 instances.
- [ ] Configure a third-party DNS resolver with logging for all EC2 instances.

### An ecommerce website was down for 1 hour following a DDoS attack Users were unable to connect to the website during the attack period. The ecommerce company's security team is worried about future potential attacks and wants to prepare for such events The company needs to minimize downtime in its response to similar attacks in the future. Which steps would help achieve this9 (Select TWO)

- [ ] Enable Amazon GuardDuty to automatically monitor for malicious activity and block unauthorized access.
- [x] Subscribe to AWS Shield Advanced and reach out to IAM Support in the event of an attack.
- [ ] Use VPC Flow Logs to monitor network: traffic and an IAM Lambda function to automatically block an attacker's IP using security groups.
- [ ] Set up an Amazon CloudWatch Events rule to monitor the AWS CloudTrail events in real time use IAM Config rules to audit the configuration, and use IAM Systems Manager for remediation.
- [x] Use IAM WAF to create rules to respond to such attacks.

### A security engineer receives an IAM abuse email message. According to the message, an Amazon EC2 instance that is running in the security engineer's IAM account is sending phishing email messages.  The EC2 instance is part of an application that is deployed in production. The application runs on many EC2 instances behind an Application Load Balancer. The instances run in an Amazon EC2 Auto Scaling group across multiple subnets and multiple Availability Zones. The instances normally communicate only over the HTTP. HTTPS, and MySQL protocols. Upon investigation, the security engineer discovers that email messages are being sent over port 587. All other traffic is normal. The security engineer must create a solution that contains the compromised EC2 instance, preserves forensic evidence for analysis, and minimizes application downtime. Which combination of steps must the security engineer take to meet these requirements? (Select THREE)

- [x] Add an outbound rule to the security group that is attached to the compromised EC2 instance to deny traffic to 0.0.0.0/0 and port 587.
- [ ] Add an outbound rule to the network ACL for the subnet that contains the compromised EC2 instance to deny traffic to 0.0.0.0/0 and port 587.
- [x] Gather volatile memory from the compromised EC2 instance. Suspend the compromised EC2 instance from the Auto Scaling group. Then take a snapshot of the compromised EC2 instance.
- [ ] Take a snapshot of the compromised EC2 instance. Suspend the compromised EC2 instance from the Auto Scaling group. Then gather volatile memory from the compromised EC2 instance.
- [x] Move the compromised EC2 instance to an isolated subnet that has a network ACL that has no inbound rules or outbound rules.
- [ ] Replace the existing security group that is attached to the compromised EC2 instance with a new security group that has no inbound rules or outbound rules.

### You need to create a policy and apply it for just an individual user. How could you accomplish this in the right way?

- [ ] Add an IAM managed policy for the user.
- [ ] Add a service policy for the user.
- [ ] Add an IAM role for the user.
- [x] Add an inline policy for the user.

### Company A has an AWS account that is named Account A. Company A recently acquired Company B, which has an AWS account that is named Account B. Company B stores its files in an Amazon S3 bucket. The administrators need to give a user from Account A full access to the S3 bucket in Account B. After the administrators adjust the IAM permissions for the user in Account A to access the S3 bucket in Account B, the user still cannot access any files in the S3 bucket. Which solution will resolve this issue?

- [ ] In Account B, create a bucket ACL to allow the user from Account A to access the S3 bucket in Account B.
- [ ] In Account B, create an object ACL to allow the user from Account A to access all the objects in the S3 bucket in Account B.
- [x] In Account B, create a bucket policy to allow the user from Account A to access the S3 bucket in Account B.
- [ ] In Account B, create a user policy to allow the user from Account A to access the S3 bucket in Account B.

### A company has a web-based application using Amazon CloudFront and running on Amazon Elastic Container Service (Amazon ECS) behind an Application Load Balancer (ALB). The ALB is terminating TLS and balancing load across ECS service tasks A security engineer needs to design a solution to ensure that application content is accessible only through CloudFront and that I is never accessible directly. How should the security engineer build the MOST secure solution?

- [ ] Add an origin custom header. Set the viewer protocol policy to HTTP and HTTPS. Set the origin protocol pokey to HTTPS only. Update the application to validate the CloudFront custom header.
- [x] Add an origin custom header. Set the viewer protocol policy to HTTPS only. Set the origin protocol policy to match viewer. Update the application to validate the CloudFront custom header.
- [ ] Add an origin custom header. Set the viewer protocol policy to redirect HTTP to HTTPS. Set the origin protocol policy to HTTP only. Update the application to validate the CloudFront custom header.
- [ ] Add an origin custom header. Set the viewer protocol policy to redirect HTTP to HTTPS. Set the origin protocol policy to HTTPS only. Update the application to validate the CloudFront custom header.

### A company is using IAM Secrets Manager to store secrets for its production Amazon RDS database. The Security Officer has asked that secrets be rotated every 3 months. Which solution would allow the company to securely rotate the secrets? (Select TWO)

- [ ] Place the RDS instance in a public subnet and an IAM Lambda function outside the VPC. Schedule the Lambda function to run every 3 months to rotate the secrets.
- [x] Place the RDS instance in a private subnet and an IAM Lambda function inside the VPC in the private subnet. Configure the private subnet to use a NAT gateway. Schedule the Lambda function to run every 3 months to rotate the secrets.
- [ ] Place the RDS instance in a private subnet and an IAM Lambda function outside the VPC. Configure the private subnet to use an internet gateway. Schedule the Lambda function to run every 3 months to rotate the secrets.
- [ ] Place the RDS instance in a private subnet and an IAM Lambda function inside the VPC in the private subnet. Schedule the Lambda function to run quarterly to rotate the secrets.
- [x] Place the RDS instance in a private subnet and an IAM Lambda function inside the VPC in the private subnet. Configure a Secrets Manager interface endpoint. Schedule the Lambda function to run every 3 months to rotate the secrets.

### You work at a company that makes use of IAM resources. One of the key security policies is to ensure that all data i encrypted both at rest and in transit. Which of the following is one of the right ways to implement this.

- [x] Use S3 SSE and use SSL for data in transit.
- [ ] SSL termination on the ELB.
- [ ] Enabling Proxy Protocol.
- [ ] Enabling sticky sessions on your load balancer.

### A security engineer configures Amazon S3 Cross-Region Replication (CRR) for all objects that are in an S3 bucket in the `us-east-1`. Region Some objects in this S3 bucket use server-side encryption with AWS KMS keys (SSE-KMS) for encryption at test. The security engineer creates a destination S3 bucket in the `us-west-2` Region. The destination S3 bucket is in the same AWS account as the source S3 bucket. The security engineer also creates a customer managed key in `us-west-2` to encrypt objects at rest in the destination S3 bucket. The replication configuration is set to use the key in `us-west-2` to encrypt objects in the destination S3 bucket. The security engineer has provided the S3 replication configuration with an IAM role to perform the replication in Amazon S3. After a day, the security engineer notices that no encrypted objects from the source S3 bucket are replicated to the destination S3 bucket. However, all the unencrypted objects are replicated. Which combination of steps should the security engineer take to remediate this issue? (Select THREE)

- [ ] Change the replication configuration to use the key in `us-east-1` to encrypt the objects that are in the destination S3 bucket.
- [ ] Grant the IAM role the kms. Encrypt permission for the key in `us-east-1` that encrypts source objects.
- [x] Grant the IAM role the `s3:GetObjectVersionForReplication` permission for objects that are in the source S3 bucket.
- [x] Grant the IAM role the `kms:Decrypt` permission for the key in `us-east-1` that encrypts source objects.
- [ ] Change the key policy of the key in `us-east-1` to grant the kms. Decrypt permission to the security engineer's IAM account.
- [x] Grant the IAM role the `kms:Encrypt` permission for the key in `us-west-2` that encrypts objects that are in the destination S3 bucket.

### A company uses an Amazon S3 bucket to store reports Management has mandated that all new objects stored in this bucket must be encrypted at rest using server-side encryption with a client-specified IAM Key Management Service (AWS KMS) CMK owned by the same account as the S3 bucket. The IAM account number is 111122223333, and the bucket name is report bucket. The company's security specialist must write the S3 bucket policy to ensure the mandate can be Implemented. Which statement should the security specialist include in the policy?

- [ ] Option A.
![Question 62 option A](images/question62_A.jpg)
- [ ] Option B.
![Question 62 option B](images/question62_B.jpg)
- [ ] Option C.
![Question 62 option C](images/question62_C.jpg)
- [x] Option D.
![Question 62 option D](images/question62_D.jpg)

### A Security Engineer is working with the development team to design a supply chain application that stores sensitive inventory data in an Amazon S3 bucket. The application will use an AWS KMS customer master key (CMK) to encrypt the data on Amazon S3. The inventory data on Amazon S3 will be shared of vendors. All vendors will use AWS principals from their own AWS accounts to access the data on Amazon S3. The vendor list may change weekly, and the solution must support cross-account access. What is the MOST efficient way to manage access control for the KMS CMK7?

- [x] Use KMS grants to manage key access. Programmatically create and revoke grants to manage vendor access.
- [ ] Use an IAM role to manage key access. Programmatically update the IAM role policies to manage vendor access.
- [ ] Use KMS key policies to manage key access. Programmatically update the KMS key policies to manage vendor access.
- [ ] Use delegated access across AWS accounts by using IAM roles to manage key access. Programmatically update the IAM trust policy to manage cross- account vendor access.

### A developer 15 building a serverless application hosted on IAM that uses Amazon Redshift in a data store. The application has separate modules for read/write and read-only functionality. The modules need their own database users for compliance reasons. Which combination of steps should a security engineer implement to grant appropriate access? (Select TWO)

- [ ] Configure cluster security groups for each application module to control access to database users that are required for read-only and read/write.
- [ ] Configure a VPC endpoint for Amazon Redshift Configure an endpoint policy that maps database users to each application module, and allow access to the tables that are required for read-only and read/write.
- [x] Configure an IAM policy for each module Specify the ARN of an Amazon Redshift database user that allows the `GetClusterCredentials` API call.
- [x] Create focal database users for each module.
- [ ] Configure an IAM policy for each module Specify the ARN of an IAM user that allows the `GetClusterCredentials` API call.

### Your company uses AWS to host its resources. They have the following requirements: 1. Record all API calls and Transitions. 2. Help in understanding what resources are there in the account. 3. Facility to allow auditing credentials and logins. Which services would suffice the above requirements.

- [ ] 1. IAM Inspector. 2. CloudTrail. 3. IAM Credential Reports.
- [ ] 1. CloudTrail. 2. IAM Credential Reports. 3. IAM SNS.
- [x] 1. CloudTrail. 2. IAM Config. 3. IAM Credential Reports.
- [ ] 1. IAM SQS. 2. IAM Credential Reports. 3. CloudTrail.

### A company is designing a multi-account structure for its development teams. The company is using AWS Organizations and AWS Single Sign-On (AWS SSO). The company must implement a solution so that the development teams can use only specific AWS Regions and so that each AWS account allows access to only specific AWS services. Which solution will meet these requirements with the LEAST operational overhead?

- [ ] Use AWS SSO to set up service-linked roles with IAM policy statements that include the Condition, Resource, and NotAction elements to allow access to only the Regions and services that are needed.
- [ ] Deactivate AWS Security Token Service (AWS STS) in Regions that the developers are not allowed to use.
- [x] Create SCPs that include the Condition, Resource, and NotAction elements to allow access to only the Regions and services that are needed.
- [ ] For each AWS account, create tailored identity-based policies for AWS SSO. Use statements that include the Condition, Resource, and NotAction elements to allow access to only the Regions and services that are needed.

### A company has deployed Amazon GuardDuty and now wants to implement automation for potential threats. The company has decided to start with RDP brute force attacks that come from Amazon EC2 instances in the company's AWS environment. A security engineer needs to implement a solution that blocks the detected communication from a suspicious instance until investigation and potential remediation can occur. Which solution will meet these requirements?

- [ ] Configure GuardDuty to send the event to an Amazon Kinesis data stream. Process the eventwith an Amazon Kinesis Data Analytics for Apache Flink application that sends a notification to the company through Amazon Simple Notification Service (Amazon SNS). Add rules to the network ACL to block traffic to and from the suspicious instance.
- [ ] Configure GuardDuty to send the event to Amazon EventBridge (Amazon CloudWatch Events). Deploy an AWS WAF web ACL. Process the event with an AWS Lambda function that sends a notification to the company through Amazon Simple Notification Service (Amazon SNS) and adds a web ACL rule to block traffic to and from the suspicious instance.
- [x] Enable AWS Security Hub to ingest GuardDuty findings and send the event to Amazon EventBridge (Amazon CloudWatch Events). Deploy AWS Network Firewall. Process the event with an AWS Lambda function that adds a rule to a Network Firewall firewall policy to block traffic to and from the suspicious instance.
- [ ] Enable AWS Security Hub to ingest GuardDuty findings. Configure an Amazon Kinesis data stream as an event destination for Security Hub. Process the event with an AWS Lambda function that replaces the security group of the suspicious instance with a security group that does not allow any connections.

### A company uses an external identity provider to allow federation into different IAM accounts. A security engineer for the company needs to identify the federated user that terminated a production Amazon EC2 instance a week ago. What is the FASTEST way for the security engineer to identify the federated user?

- [ ] Review the AWS CloudTrail event history logs in an Amazon S3 bucket and look for the Terminatelnstances event to identify the federated user from the role session name.
- [x] Filter the AWS CloudTrail event history for the Terminatelnstances event and identify the assumed IAM role. Review the AssumeRoleWithSAML event call in CloudTrail to identify the corresponding username.
- [ ] Search the AWS CloudTrail logs for the Terminatelnstances event and note the event time. Review the IAM Access Advisor tab for all federated roles. The last accessed time should match the time when the instance was terminated.
- [ ] Use Amazon Athena to run a SQL query on the AWS CloudTrail logs stored in an Amazon S3 bucket and filter on the Terminatelnstances event. Identify the corresponding role and run another query to filter the AssumeRoleWithWebldentity event for the user name.

### A company is planning to use Amazon Elastic File System (Amazon EFS) with its on-premises servers. The company has an existing IAM Direct Connect connection established between its on-premises data center and an IAM Region Security policy states that the company's on-premises firewall should only have specific IP addresses added to the allow list and not a CIDR range. The company also wants to restrict access so that only certain data center-based servers have access to Amazon EFS. How should a security engineer implement this solution?

- [ ] Add the file-system-id efs IAM-region amazonIAM com URL to the allow list for the data center firewall. Install the IAM CLI on the data center-based servers to mount the EFS file system in the EFS security group add the data center IP range to the allow list. Mount the EFS using the EFS file system name.
- [ ] Assign an Elastic IP address to Amazon EFS and add the Elastic IP address to the allow list for the data center firewall. Install the IAM CLI on the data center-based servers to mount the EFS file system. In the EFS security group, add the IP addresses of the data center servers to the allow list. Mount the EFS using the Elastic IP address.
- [x] Add the EFS file system mount target IP addresses to the allow list for the data center firewall. In the EFS security group, add the data center server IP addresses to the allow list. Use the Linux terminal to mount the EFS file system using the IP address of one of the mount targets.
- [ ] Assign a static range of IP addresses for the EFS file system by contacting IAM Support. In the EFS security group add the data center server IP addresses to the allow list. Use the Linux terminal to mount the EFS file system using one of the static IP addresses.

### A website currently runs on Amazon EC2, with mostly static content on the site. Recently, the site was subjected to a DDoS attack, and a Security Engineer was tasked with redesigning the edge security to help mitigate this risk in the future. What are some ways the Engineer could achieve this? (Select THREE)

- [ ] Use AWS X-Ray to inspect the traffic going to the EC2 instances.
- [x] Move the static content to Amazon S3, and front this with an Amazon CloudFront distribution.
- [ ] Change the security group configuration to block the source of the attack traffic.
- [x] Use AWS WAF security rules to inspect the inbound traffic.
- [ ] Use Amazon Inspector assessment templates to inspect the inbound traffic.
- [x] Use Amazon Route 53 to distribute traffic.

### A company needs to use HTTPS when connecting to its web applications to meet compliance requirements. These web applications run in Amazon VPC on Amazon EC2 instances behind an Application Load Balancer (ALB). A security engineer wants to ensure that the load balancer win only accept connections over port 443. even if the ALB is mistakenly configured with an HTTP listener. Which configuration steps should the security engineer take to accomplish this task?

- [ ] Create a security group with a rule that denies Inbound connections from 0.0.0.0/0 on port 00. Attach this security group to the ALB to overwrite more permissive rules from the ALB's default security group.
- [ ] Create a network ACL that denies inbound connections from 0 0.0.0/0 on port 80 Associate the network ACL with the VPC s internet gateway.
- [ ] Create a network ACL that allows outbound connections to the VPC IP range on port 443 only. Associate the network ACL with the VPC's internet gateway.
- [x] Create a security group with a single inbound rule that allows connections from 0.0.0.0/0 on port 443. Ensure this security group is the only one associated with the ALB.

### Example.com is hosted on Amazon EC2 instances behind an Application Load Balancer (ALB). Third-party host intrusion detection system (HIDS) agents that capture the traffic of the EC2 instance are running on each host. The company must ensure they are using privacy enhancing technologies for users, without losing the assurance the third-party solution offers. What is the MOST secure way to meet these requirements?

- [ ] Enable TLS pass through on the ALB, and handle decryption at the server using Elliptic Curve Diffie-Hellman (ECDHE) cipher suites.
- [ ] Create a listener on the ALB that uses encrypted connections with Elliptic Curve Diffie-Hellman (ECDHE) cipher suites, and pass the traffic in the clear to the server.
- [x] Create a listener on the ALB that uses encrypted connections with Elliptic Curve Diffie-Hellman (ECDHE) cipher suites, and use encrypted connections to the servers that do not enable Perfect Forward Secrecy (PFS).
- [ ] Create a listener on the ALB that does not enable Perfect Forward Secrecy (PFS) cipher suites, and use encrypted connections to the servers using Elliptic Curve Diffie-Hellman (ECDHE) cipher suites.

### A company has an AWS Key Management Service (AWS KMS) customer managed key with imported key material Company policy requires all encryption keys to be rotated every year. What should a security engineer do to meet this requirement for this customer managed key?

- [ ] Enable automatic key rotation annually for the existing customer managed key.
- [ ] Use the AWS CLI to create an AWS Lambda function to rotate the existing customer managed key annually.
- [ ] Import new key material to the existing customer managed key. Manually rotate the key.
- [x] Create a new customer managed key. Import new key material to the new key. Point the key alias to the new key.

### A company's on-premises networks are connected to VPCs using an IAM Direct Connect gateway. The company's on-premises application needs to stream data using an existing Amazon Kinesis Data Firehose delivery stream. The company's security policy requires that data be encrypted in transit using a private network. How should the company meet these requirements?

- [x] Create a VPC endpoint for Kinesis Data Firehose. Configure the application to connect to the VPC endpoint.
- [ ] Configure an IAM policy to restrict access to Kinesis Data Firehose using a source IP condition. Configure the application to connect to the existing Firehose delivery stream.
- [ ] Create a new TLS certificate in IAM Certificate Manager (ACM). Create a public-facing Network Load Balancer (NLB) and select the newly created TLS certificate. Configure the NLB to forward all traffic to Kinesis Data Firehose. Configure the application to connect to the NLB.
- [ ] Peer the on-premises network with the Kinesis Data Firehose VPC using Direct Connect. Configure the application to connect to the existing Firehose delivery stream.

### A security team is using Amazon EC2 Image Builder to build a hardened AMI with forensic capabilities. An AWS Key Management Service (AWS KMS) key will encrypt the forensic AMI EC2 Image Builder successfully installs the required patches and packages in the security team's AWS account. The security team uses a federated IAM role m the same AWS account to sign in to the AWS Management Console and attempts to launch the forensic AMI. The EC2 instance launches and immediately terminates. What should the security learn do to launch the EC2 instance successfully

- [ ] Update the policy that is associated with the federated IAM role to allow the ec2. Describelmages action for the forensic AMI.
- [ ] Update the policy that is associated with the federated IAM role to allow the ec2 Start Instances action m the security team's AWS account.
- [x] Update the policy that is associated with the KMS key that is used to encrypt the forensic AMI. Configure the policy to allow the kms. Encrypt and kms Decrypt actions for the federated IAM role.
- [ ] Update the policy that is associated with the federated IAM role to allow the kms. DescribeKey action for the KMS key that is used to encrypt the forensic AMI.

### A company wants to monitor the deletion of customer managed CMKs. A security engineer must create an alarm that will notify the company before a CMK is deleted. The security engineer has configured the integration of AWS CloudTrail with Amazon CloudWatch. What should the security engineer do next to meet this requirement?

- [ ] Within AWS Key Management Service (AWS KMS), specify the deletion time of the key material during CMK creation. AWS KMS will automatically create a CloudWatch alarm.
- [ ] Create an Amazon EventBridge (Amazon CloudWatch Events) rule to look for API calls of DeleteAlias. Create an AWS Lambda function to send an Amazon Simple Notification Service (Amazon SNS) message to the company. Add the Lambda function as the target of the Eventbridge (CloudWatch Events) rule.
- [x] Create an Amazon EventBridge (Amazon CloudWatch Events) rule to look for API calls of DisableKey and ScheduleKeyDeletion. Create an AWS Lambda function to send an Amazon Simple Notification Service (Amazon SNS) message to the company. Add the Lambda function as the target of the Eventbridge (CloudWatch Events) rule.
- [ ] Create an Amazon Simple Notification Service (Amazon SNS) policy to look for AWS Key Management Service (AWS KMS) API calls of RevokeGrant and ScheduleKeyDeletion. Create an AWS Lambda function to generate the alarm and send the notification to the company. Add the Lambda function as the target of the SNS policy.

### A company is building an application on AWS that will store sensitive information. The company has a support team with access to the IT infrastructure, including databases. The company's security engineer must introduce measures to protect the sensitive data against any data breach while minimizing management overhead. The credentials must be regularly rotated. What should the security engineer recommend?

- [ ] Enable Amazon RDS encryption to encrypt the database and snapshots. Enable Amazon Elastic Block Store (Amazon EBS) encryption on Amazon EC2 instances. Include the database credential in the EC2 user data field. Use an AWS Lambda function to rotate database credentials. Set up TLS for the connection to the database.
- [ ] Install a database on an Amazon EC2 instance. Enable third-party disk encryption to encrypt Amazon Elastic Block Store (Amazon EBS) volume. Store the database credentials in AWS CloudHSM with automatic rotation. Set up TLS for the connection to the database.
- [x] Enable Amazon RDS encryption to encrypt the database and snapshots. Enable Amazon Elastic Block Store (Amazon EBS) encryption on Amazon EC2 instances. Store the database credentials in AWS Secrets Manager with automatic rotation. Set up TLS for the connection to the RDS hosted database.
- [ ] Set up an AWS CloudHSM cluster with AWS Key Management Service (AWS KMS) to store KMS keys. Set up Amazon RDS encryption using AWS KSM to encrypt the database. Store the database credentials in AWS Systems Manager Parameter Store with automatic rotation. Set up TLS for the connection to the RDS hosted database.

### A company deployed IAM Organizations to help manage its increasing number of IAM accounts. A security engineer wants to ensure only principals in the Organization structure can access a specic Amazon S3 bucket. The solution must also minimize operational overhead. Which solution will meet these requirements?

- [ ] Put all users into an IAM group with an access policy granting access to the bucket.
- [ ] Have the account creation trigger an IAM Lambda function that manages the bucket policy, allowing access to accounts listed in the policy only.
- [ ] Add an SCP to the Organizations master account, allowing all principals access to the bucket.
- [x] Specify the organization ID in the global key condition element of a bucket policy, allowing all principals access.

### A company is undergoing a layer 3 and layer 4 DDoS attack on its web servers running on IAM. Which combination of IAM services and features will provide protection in this scenario? (Select THREE)

- [x] Amazon Route 53.
- [ ] IAM Certificate Manager (ACM).
- [ ] Amazon S3.
- [x] AWS Shield.
- [x] Elastic Load Balancer.
- [ ] Amazon Guard Duty.

### Your CTO thinks your IAM account was hacked. What is the only way to know for certain if there was unauthorized access and what they did, assuming your hackers are very sophisticated IAM engineers and doing everything they can to cover their tracks?

- [x] Use CloudTrail Log File Integrity Validation.
- [ ] Use IAM Config SNS Subscriptions and process events in real time.
- [ ] Use CloudTrail backed up to IAM S3 and Glacier.
- [ ] Use IAM Config Timeline forensics.

### A company is developing a highly resilient application to be hosted on multiple Amazon EC2 instances. The application will store highly sensitive user data in Amazon RDS tables The application must. Include migration to a different IAM Region in the application disaster recovery plan. Provide a full audit trail of encryption key administration events. Allow only company administrators to administer keys. Protect data at rest using application layer encryption A Security Engineer is evaluating options for encryption key management. Why should the Security Engineer choose AWS CloudHSM over AWS KMS for encryption key management in this situation?

- [ ] The key administration event logging generated by CloudHSM is significantly more extensive than AWS KMS.
- [ ] CloudHSM ensures that only company support staff can administer encryption keys, whereas AWS KMS allows IAM staff to administer keys.
- [ ] The ciphertext produced by CloudHSM provides more robust protection against brute force decryption attacks than the ciphertext produced by AWS KMS.
- [x] CloudHSM provides the ability to copy keys to a different Region, whereas AWS KMS does not.

### A company wants to ensure that its IAM resources can be launched only in the `us-east-1` and `us-west-2` Regions. What is the MOST operationally efficient solution that will prevent developers from launching Amazon EC2 instances in other Regions?

- [ ] Enable Amazon GuardDuty in all Regions. Create alerts to detect unauthorized activity outside `us-east-1` and `us-west-2`.
- [x] Use an organization in IAM Organizations. Attach an SCP that allows all actions when the IAM: Requested Region condition key is either `us-east-1` or `us-west-2`. Delete the FullIAMAccess policy.
- [ ] Provision EC2 resources by using IAM Cloud Formation templates through IAM CodePipeline. Allow only the values of `us-east-1` and `us-west-2` in the IAM CloudFormation template's parameters.
- [ ] Create an IAM Config rule to prevent unauthorized activity outside `us-east-1` and `us-west-2`.

### A company's Security Team received an email notification from the Amazon EC2 Abuse team that one or more of the company's Amazon EC2 instances may have been compromised. Which combination of actions should the Security team take to respond to be current modem? (Select TWO)

- [ ] Open a support case with the IAM Security team and ask them to remove the malicious code from the affected instance.
- [x] Respond to the notification and list the actions that have been taken to address the incident.
- [ ] Delete all IAM users and resources in the account.
- [x] Detach the internet gateway from the VPC remove aft rules that contain 0.0.0.0/0 from the security groups, and create a NACL rule to deny all traffic Inbound from the internet.
- [ ] Delete the identified compromised instances and delete any associated resources that the Security team did not create.

### A company is using Amazon Macie, AWS Firewall Manager, Amazon Inspector, and AWS Shield Advanced in its AWS account. The company wants to receive alerts if a DDoS attack occurs against the account. Which solution will meet this requirement?

- [ ] Use Macie to detect an active DDoS event. Create Amazon CloudWatch alarms that respond to Macie findings.
- [ ] Use Amazon Inspector to review resources and to invoke Amazon CloudWatch alarms for any resources that are vulnerable to DDoS attacks.
- [ ] Create an Amazon CloudWatch alarm that monitors Firewall Manager metrics for an active DDoS event.
- [ ] Create an Amazon CloudWatch alarm that monitors Shield Advanced metrics for an active DDoS event.

### A company is running internal microservices on Amazon Elastic Container Service (Amazon ECS) with the Amazon EC2 launch type. The company is using Amazon Elastic Container Registry (Amazon ECR) private repositories. A security engineer needs to encrypt the private repositories by using AWS Key Management Service (AWS KMS). The security engineer also needs to analyze the container images for any common vulnerabilities and exposures (CVEs). Which solution will meet these requirements?

- [ ] Enable KMS encryption on the existing ECR repositories. Install Amazon Inspector Agent from the ECS container instances' user data. Run an assessment with the CVE rules.
- [x] Recreate the ECR repositories with KMS encryption and ECR scanning enabled. Analyze the scan report after the next push of images.
- [ ] Recreate the ECR repositories with KMS encryption and ECR scanning enabled. Install AWS Systems
Manager Agent on the ECS container instances. Run an inventory report.
- [ ] Enable KMS encryption on the existing ECR repositories. Use AWS Trusted Advisor to check the ECS container instances and to verily the findings against a list of current CVEs.

### A business stores website images in an Amazon S3 bucket. The firm serves the photos to end users through Amazon CloudFront. The firm learned lately that the photographs are being accessible from nations in which it does not have a distribution license. Which steps should the business take to safeguard the photographs and restrict their distribution? (Select TWO)

- [x] Update the S3 bucket policy to restrict access to a CloudFront origin access identity (OAI).
- [ ] Update the website DNS record to use an Amazon Route 53 geolocation record deny list of countries where the company lacks a license.
- [x] Add a CloudFront geo restriction deny list of countries where the company lacks a license.
- [ ] Update the S3 bucket policy with a deny list of countries where the company lacks a license.
- [ ] Enable the Restrict Viewer Access option in CloudFront to create a deny list of countries where the company lacks a license.

### A company wants to remove all SSH keys permanently from a specific subset of its Amazon Linux 2 Amazon EC2 instances that are using the same IAM instance profile However three individuals who have IAM user accounts will need to access these instances by using an SSH session to perform critical duties How can a security engineer provide the access to meet these requirements?

- [ ] Assign an IAM policy to the instance profile to allow the EC2 instances to be managed by AWS Systems Manager. Provide the IAM user accounts with permission to use Systems Manager. Remove the SSH keys from the EC2 instances. Use Systems Manager Inventory to select the EC2 instance and connect.
- [ ] Assign an IAM policy to the IAM user accounts to provide permission to use AWS Systems Manager. Run Command. Remove the SSH keys from the EC2 instances. Use Run Command to open an SSH connection to the EC2 instance.
- [x] Assign an IAM policy to the instance profile to allow the EC2 instances to be managed by AWS Systems Manager. Provide the IAM user accounts with permission to use Systems Manager. Remove the SSH keys from the EC2 instances Use Systems Manager Session Manager to select the EC2 instance and connect.
- [ ] Assign an IAM policy to the IAM user accounts to provide permission to use the EC2 service in the AWS Management Console. Remove the SSH keys from the EC2 instances. Connect to the EC2 instance as the ec2-user through the AWS Management Console's EC2 SSH client method.

### A security engineer is using AWS Organizations and wants to optimize SCPs. The security engineer needs to ensure that the SCPs conform to best practices. Which approach should the security engineer take to meet this requirement?

- [x] Use AWS IAM Access Analyzer to analyze the policies. View the findings from policy validation checks.
- [ ] Review AWS Trusted Advisor checks for all accounts in the organization.
- [ ] Set up AWS Audit Manager. Run an assessment for all AWS Regions for all accounts.
- [ ] Ensure that Amazon Inspector agents are installed on all Amazon EC2 in-stances in all accounts.

### A company is using AWS Organizations to manage multiple accounts. The company needs to allow an IAM user to use a role to access resources that are in another organization's AWS account. Which combination of steps must the company perform to meet this requirement? (Select TWO)

- [ ] Create an identity policy that allows the `sts:AssumeRole` action in the AWS account that contains the resources. Attach the identity policy to the IAM user.
- [x] Ensure that the `sts:AssumeRole` action is allowed by the SCPs of the organization that owns the resources that the IAM user needs to access.
- [x] Create a role in the AWS account that contains the resources. Create an entry in the role's trust policy that allows the IAM user to assume the role. Attach the trust policy to the role.
- [ ] Establish a trust relationship between the IAM user and the AWS account that contains the resources.
- [ ] Create a role in the IAM user's AWS account. Create an identity policy that allows the `sts:AssumeRole` action. Attach the identity policy to the role.

### A company's AWS CloudTrail logs are all centrally stored in an Amazon S3 bucket. The security team controls the company's AWS account. The security team must prevent unauthorized access and tampering of the CloudTrail logs. Which combination of steps should the security team take? (Choose THREE)

- [x] Configure server-side encryption with AWS KMS managed encryption keys (SSE-KMS).
- [ ] Compress log file with secure gzip.
- [ ] Create an Amazon EventBridge (Amazon CloudWatch Events) rule to notify the security team of any modifications on CloudTrail log files.
- [x] Implement least privilege access to the S3 bucket by configuring a bucket policy.
- [x] Configure CloudTrail log file integrity validation.
- [ ] Configure Access Analyzer for S3.

### A security engineer receives a notice from the AWS Abuse team about suspicious activity from a Linux-based Amazon EC2 instance that uses Amazon Elastic Block Store (Amazon EBS)-based storage. The instance is making connections to known malicious addresses. The instance is in a development account within a VPC that is in the us-east-1 Region. The VPC contains an internet gateway and has a subnet in us-east-1a and us-east-1 b. Each subnet is associate with a route table that uses the internet gateway as a default route. Each subnet also uses the default network ACL. The suspicious EC2 instance runs within the us-east-1 b subnet. During an initial investigation, a security engineer discovers that the suspicious instance is the only instance that runs in the subnet. Which response will immediately mitigate the attack and help investigate the root cause?

- [ ] Log in to the suspicious instance and use the netstat command to identify remote connections. Use the IP addresses from these remote connections to create deny rules in the security group of the instance. Install diagnostic tools on the instance for investigation. Update the outbound network ACL for the subnet in us-east-1b to explicitly deny all connections as the first rule during the investigation of the instance.
- [x] Update the outbound network ACL for the subnet in us-east-1b to explicitly deny all connections as the first rule. Replace the security group with a new security group that allows connections only from a diagnostics security group. Update the outbound network ACL for the us-east-1b subnet to remove the deny all rule. Launch a new EC2 instance that has diagnostic tools. Assign the new security group to the new EC2 instance. Use the new EC2 instance to investigate the suspicious instance.
- [ ] Ensure that the Amazon Elastic Block Store (Amazon EBS) volumes that are attached to the suspicious EC2 instance will not delete upon termination. Terminate the instance. Launch a new EC2 instance in us-east-1a that has diagnostic tools. Mount the EBS volumes from the terminated instance for investigation.
- [ ] Create an AWS WAF web ACL that denies traffic to and from the suspicious instance. Attach the AWS WAF web ACL to the instance to mitigate the attack. Log in to the instance and install diagnostic tools to investigate the instance.

### A Security Engineer receives alerts that an Amazon EC2 instance on a public subnet is under an SFTP brute force attack from a specific IP address, which is a known malicious bot. What should the Security Engineer do to block the malicious bot?

- [x] Add a deny rule to the public VPC security group to block the malicious IP.
- [ ] Add the malicious IP to IAM WAF backhsted IPs.
- [ ] Configure Linux iptables or Windows Firewall to block any traffic from the malicious IP.
- [ ] Modify the hosted zone in Amazon Route 53 and create a DNS sinkhole for the malicious IP.

### A systems engineer deployed containers from several custom-built images that an application team provided through a QA workflow The systems engineer used Amazon Elastic Container Service (Amazon ECS) with the Fargate launch type as the target platform The system engineer now needs to collect logs from all containers into an existing Amazon CloudWatch log group. Which solution will meet this requirement?

- [x] Turn on the awslogs log driver by specifying parameters for awslogs-group and awslogs-region m the LogConfiguration property.
- [ ] Download and configure the CloudWatch agent on the container instances.
- [ ] Set up Fluent Bit and FluentO as a DaemonSet to send logs to Amazon CloudWatch Logs.
- [ ] Configure an IAM policy that includes the togs CreateLogGroup action Assign the policy to the container instances.

### A recent security audit found that AWS CloudTrail logs are insufficiently protected from tampering and unauthorized access. Which actions must the Security Engineer take to address these audit findings? (Select THREE)

- [x] Ensure CloudTrail log file validation is turned on.
- [ ] Configure an S3 lifecycle rule to periodically archive CloudTrail logs into Glacier for long-term storage.
- [x] Use an S3 bucket with tight access controls that exists m a separate account.
- [ ] Use Amazon Inspector to monitor the file integrity of CloudTrail log files.
- [ ] Request a certificate through ACM and use a generated certificate private key to encrypt CloudTrail log files.
- [x] Encrypt the CloudTrail log files with server-side encryption with AWS KMS-managed keys (SSE-KMS).

### Auditors for a health care company have mandated that all data volumes be encrypted at rest Infrastructure is deployed mainly via IAM CloudFormation however third-party frameworks and manual deployment are required on some legacy systems. What is the BEST way to monitor, on a recurring basis, whether all EBS volumes are encrypted?

- [ ] On a recurring basis, update an IAM user policies to require that EC2 instances are created with an encrypted volume.
- [x] Configure an IAM Config rule to run on a recurring basis for volume encryption.
- [ ] Set up Amazon Inspector rules for volume encryption to run on a recurring schedule.
- [ ] Use CloudWatch Logs to determine whether instances were created with an encrypted volume.

### A startup company is using a single AWS account that has resources in a single AWS Region. A security engineer configures an AWS CloudTrail trail in the same Region to deliver log files to an Amazon S3 bucket by using the AWS CLI. Because of expansion, the company adds resources in multiple Regions. The security engineer notices that the logs from the new Regions are not reaching the S3 bucket. What should the security engineer do to fix this issue with the LEAST amount of operational overhead?

- [ ] Create a new CloudTrail trail. Select the new Regions where the company added resources.
- [ ] Change the S3 bucket to receive notifications to track all actions from all Regions.
- [ ] Create a new CloudTrail trail that applies to all Regions.
- [x] Change the existing CloudTrail trail so that it applies to all Regions.

### A company's cloud operations team is responsible for building effective security for IAM cross-account access. The team asks a security engineer to help troubleshoot why some developers in the developer account (123456789012) in the developers group are not able to assume a cross-account role (ReadS3) into a production account (999999999999) to read the contents of an Amazon S3 bucket (productionapp). The two account policies are as follows. Which recommendations should the security engineer make to resolve this issue? (Select TWO)

![Question 97](images/question97.jpg)

- [ ] Ask the developers to change their password and use a different web browser.
- [ ] Ensure that developers are using multi-factor authentication (MFA) when they log in to their developer account as the developer role.
- [ ] Modify the production account ReadS3 role policy to allow the PutBucketPolicy action on the productionapp S3 bucket.
- [x] Update the trust relationship policy on the production account S3 role to allow the account number of the developer account.
- [x] Update the developer group permissions in the developer account to allow access to the productionapp S3 bucket.

### A company deploys a distributed web application on a fleet of Amazon EC2 instances. The fleet is behind an Application Load Balancer (ALB) that will be configured to terminate the TLS connection. All TLS traffic to the ALB must stay secure, even if the certificate private key is compromised. How can a security engineer meet this requirement?

- [ ] Create an HTTPS listener that uses a certificate that is managed by IAM Certificate Manager (ACM).
- [x] Create an HTTPS listener that uses a security policy that uses a cipher suite with perfect toward secrecy (PFS).
- [ ] Create an HTTPS listener that uses the Server Order Preference security feature.
- [ ] Create a TCP listener that uses a custom security policy that allows only cipher suites with perfect forward secrecy (PFS).

### A company's public Application Load Balancer (ALB) recently experienced a DDoS attack. To mitigate this issue. the company deployed Amazon CloudFront in front of the ALB so that users would not directly access the Amazon EC2 instances behind the ALB. The company discovers that some traffic is still coming directly into the ALB and is still being handled by the EC2 instances. Which combination of steps should the company take to ensure that the EC2 instances will receive traffic only from CloudFront? (Choose TWO)

- [ ] Configure CloudFront to add a cache key policy to allow a custom HTTP header that CloudFront sends to the ALB.
- [x] Configure CloudFront to add a custom HTTP header to requests that CloudFront sends to the ALB.
- [x] Configure the ALB to forward only requests that contain the custom HTTP header.
- [ ] Configure the ALB and CloudFront to use the X-Forwarded-For header to check client IP addresses.
- [ ] Configure the ALB and CloudFront to use the same X.509 certificate that is generated by AWS Certificate Manager (ACM).

### A company has a legacy application that runs on a single Amazon EC2 instance. A security audit shows that the application has been using an IAM access key within its code to access an Amazon S3 bucket that is named DOC-EXAMPLE-BUCKET1 in the same AWS account. This access key pair has the `s3:GetObject` permission to all objects in only this S3 bucket. The company takes the application offline because the application is not compliant with the company's security policies for accessing other AWS resources from Amazon EC2. A security engineer validates that AWS CloudTrail is turned on in all AWS Regions. CloudTrail is sending logs to an S3 bucket that is named DOC-EXAMPLE-BUCKET2. This S3 bucket is in the same AWS account as DOC-EXAMPLE-BUCKET1. However, CloudTrail has not been configured to send logs to Amazon CloudWatch Logs. The company wants to know if any objects in DOC-EXAMPLE-BUCKET1 were accessed with the IAM access key in the past 60 days. If any objects were accessed, the company wants to know if any of the objects that are text files (.txt extension) contained personally identifiable information (PII). Which combination of steps should the security engineer take to gather this information? (Choose TWO)

- [x] Configure Amazon Macie to identify any objects in DOC-EXAMPLE-BUCKET1 that contain PII and that were available to the access key.
- [ ] Use Amazon CloudWatch Logs Insights to identify any objects in DOC-EXAMPLE-BUCKET1 that contain PII and that were available to the access key.
- [ ] Use Amazon OpenSearch Service (Amazon Elasticsearch Service) to query the CloudTrail logs in DOC-EXAMPLE-BUCKET2 for API calls that used the access key to access an object that contained PII.
- [x] Use Amazon Athena to query the CloudTrail logs in DOC-EXAMPLE-BUCKET2 for any API calls that used the access key to access an object that contained PII.
- [ ] Use AWS Identity and Access Management Access Analyzer to identify any API calls that used the access key to access objects that contained PII in DOC-EXAMPLE-BUCKET1.

### A security engineer is configuring a new website that is named example.com. The security engineer wants to secure communications with the website by requiring users to connect to example.com through HTTPS. Which of the following is a valid option for storing SSL/TLS certificates?

- [ ] Custom SSL certificate that is stored in AWS Key Management Service (AWS KMS).
- [ ] Default SSL certificate that is stored in Amazon CloudFront.
- [x] Custom SSL certificate that is stored in AWS Certificate Manager (ACM).
- [ ] Default SSL certificate that is stored in Amazon S3.

### A security engineer needs to develop a process to investigate and respond to potential security events on a company's Amazon EC2 instances. All the EC2 instances are backed by Amazon Elastic Block Store (Amazon EBS). The company uses AWS Systems Manager to manage all the EC2 instances and has installed Systems Manager Agent (SSM Agent) on all the EC2 instances. The process that the security engineer is developing must comply with AWS security best practices and must meet the following requirements: A compromised EC2 instance's volatile memory and non-volatile memory must be preserved for forensic purposes. A compromised EC2 instance's metadata must be updated with corresponding incident ticket information. A compromised EC2 instance must remain online during the investigation but must be isolated to prevent the spread of malware. Any investigative activity during the collection of volatile data must be captured as part of the process. Which combination of steps should the security engineer take to meet these requirements with the LEAST operational overhead? (Choose THREE)

- [x] Gather any relevant metadata for the compromised EC2 instance. Enable termination protection. Isolate the instance by updating the instance's security groups to restrict access. Detach the instance from any Auto Scaling groups that the instance is a member of. Deregister the instance from any Elastic Load Balancing (ELB) resources.
- [ ] Gather any relevant metadata for the compromised EC2 instance. Enable termination protection. Move the instance to an isolation subnet that denies all source and destination traffic. Associate the instance with the subnet to restrict access. Detach the instance from any Auto Scaling groups that the instance is a member of. Deregister the instance from any Elastic Load Balancing (ELB) resources.
- [x] Use Systems Manager Run Command to invoke scripts that collect volatile data.
- [ ] Establish a Linux SSH or Windows Remote Desktop Protocol (RDP) session to the compromised EC2 instance to invoke scripts that collect volatile data.
- [x] Create a snapshot of the compromised EC2 instance's EBS volume for follow-up investigations. Tag the instance with any relevant metadata and incident ticket information.
- [ ] Create a Systems Manager State Manager association to generate an EBS volume snapshot of the compromised EC2 instance. Tag the instance with any relevant metadata and incident ticket information.

### A company has an organization in AWS Organizations. The company wants to use AWS CloudFormation StackSets in the organization to deploy various AWS design patterns into environments. These patterns consist of Amazon EC2 instances, Elastic Load Balancing (ELB) load balancers, Amazon RDS databases, and Amazon Elastic Kubernetes Service (Amazon EKS) clusters or Amazon Elastic Container Service (Amazon ECS) clusters. Currently, the company's developers can create their own CloudFormation stacks to increase the overall speed of delivery. A centralized CI/CD pipeline in a shared services AWS account deploys each CloudFormation stack. The company's security team has already provided requirements for each service in accordance with internal standards. If there are any resources that do not comply with the internal standards, the security team must receive notification to take appropriate action. The security team must implement a notification solution that gives developers the ability to maintain the same overall delivery speed that they currently have. Which solution will meet these requirements in the MOST operationally efficient way?

- [ ] Create an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the security team's email addresses to the SNS topic. Create a custom AWS Lambda function that will run the aws cloudformation validate-template AWS CLI command on all CloudFormation templates before the build stage in the CI/CD pipeline. Configure the CI/CD pipeline to publish a notification to the SNS topic if any issues are found.
- [x] Create an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the security team's email addresses to the SNS topic. Create custom rules in CloudFormation Guard for each resource configuration. In the CI/CD pipeline, before the build stage, configure a Docker image to run the cfn-guard command on the CloudFormation template. Configure the CI/CD pipeline to publish a notification to the SNS topic if any issues are found.
- [ ] Create an Amazon Simple Notification Service (Amazon SNS) topic and an Amazon Simple Queue Service (Amazon SQS) queue. Subscribe the security team's email addresses to the SNS topic. Create an Amazon S3 bucket in the shared services AWS account. Include an event notification to publish to the SQS queue when new objects are added to the S3 bucket. Require the developers to put their CloudFormation templates in the S3 bucket. Launch EC2 instances that automatically scale based on the SQS queue depth. Configure the EC2 instances to use CloudFormation Guard to scan the templates and deploy the templates if there are no issues. Configure the CI/CD pipeline to publish a notification to the SNS topic if any issues are found.
- [ ] Create a centralized CloudFormation stack set that includes a standard set of resources that the developers can deploy in each AWS account. Configure each CloudFormation template to meet the security requirements. For any new resources or configurations, update the CloudFormation template and send the template to the security team for review. When the review is completed, add the new CloudFormation stack to the repository for the developers to use.

### A company is migrating one of its legacy systems from an on-premises data center to AWS. The application server will run on AWS, but the database must remain in the on-premises data center for compliance reasons. The database is sensitive to network latency. Additionally, the data that travels between the on-premises data center and AWS must have IPsec encryption. Which combination of AWS solutions will meet these requirements? (Choose TWO)

- [x] AWS Site-to-Site VPN.
- [x] AWS Direct Connect.
- [ ] AWS VPN CloudHub.
- [ ] VPC peering.
- [ ] NAT gateway.

### A company has an application that uses dozens of Amazon DynamoDB tables to store data. Auditors find that the tables do not comply with the company's data protection policy. The company's retention policy states that all data must be backed up twice each month: once at midnight on the 15th day of the month and again at midnight on the 25th day of the month. The company must retain the backups for 3 months. Which combination of steps should a security engineer take to meet these requirements? (Choose TWO)

- [ ] Use the DynamoDB on-demand backup capability to create a backup plan. Configure a lifecycle policy to expire backups after 3 months.
- [ ] Use AWS DataSync to create a backup plan. Add a backup rule that includes a retention period of 3 months.
- [x] Use AWS Backup to create a backup plan. Add a backup rule that includes a retention period of 3 months.
- [x] Set the backup frequency by using a cron schedule expression. Assign each DynamoDB table to the backup plan.
- [ ] Set the backup frequency by using a rate schedule expression. Assign each DynamoDB table to the backup plan.

### A company needs a security engineer to implement a scalable solution for multi-account authentication and authorization. The solution should not introduce additional user-managed architectural components. Native AWS features should be used as much as possible. The security engineer has set up AWS Organizations with all features activated and AWS IAM Identity Center (AWS Single Sign-On) enabled. Which additional steps should the security engineer take to complete the task?

- [ ] Use AD Connector to create users and groups for all employees that require access to AWS accounts. Assign AD Connector groups to AWS accounts and link to the IAM roles in accordance with the employees' job functions and access requirements. Instruct employees to access AWS accounts by using the AWS Directory Service user portal.
- [x] Use an IAM Identity Center default directory to create users and groups for all employees that require access to AWS accounts. Assign groups to AWS accounts and link to permission sets in accordance with the employees' job functions and access requirements. Instruct employees to access AWS accounts by using the IAM Identity Center user portal.
- [ ] Use an IAM Identity Center default directory to create users and groups for all employees that require access to AWS accounts. Link IAM Identity Center groups to the IAM users present in all accounts to inherit existing permissions. Instruct employees to access AWS accounts by using the IAM Identity Center user portal.
- [ ] Use an IAM Identity Center default directory to create users and groups for all employees that require access to AWS accounts. Link IAM Identity Center groups to the IAM users present in all accounts to inherit existing permissions. Instruct employees to access AWS accounts by using the IAM Identity Center user portal.

### A company has an AWS account that hosts a production application. The company receives an email notification that Amazon GuardDuty has detected an Impact:IAMUser/AnomalousBehavior finding in the account. A security engineer needs to run the investigation playbook for this security incident and must collect and analyze the information without affecting the application. Which solution will meet these requirements MOST quickly?

- [ ] Log in to the AWS account by using read-only credentials. Review the GuardDuty finding for details about the IAM credentials that were used. Use the IAM console to add a DenyAll policy to the IAM principal.
- [x] Log in to the AWS account by using read-only credentials. Review the GuardDuty finding to determine which API calls initiated the finding. Use Amazon Detective to review the API calls in context.
- [ ] Log in to the AWS account by using administrator credentials. Review the GuardDuty finding for details about the IAM credentials that were used. Use the IAM console to add a DenyAll policy to the IAM principal.
- [ ] Log in to the AWS account by using read-only credentials. Review the GuardDuty finding to determine which API calls initiated the finding. Use AWS CloudTrail Insights and AWS CloudTrail Lake to review the API calls in context.

### A company wants to receive an email notification about critical findings in AWS Security Hub. The company does not have an existing architecture that supports this functionality. Which solution will meet the requirement?

- [ ] Create an AWS Lambda function to identify critical Security Hub findings. Create an Amazon Simple Notification Service (Amazon SNS) topic as the target of the Lambda function. Subscribe an email endpoint to the SNS topic to receive published messages.
- [ ] Create an Amazon Kinesis Data Firehose delivery stream. Integrate the delivery stream with Amazon EventBridge. Create an EventBridge rule that has a filter to detect critical Security Hub findings. Configure the delivery stream to send the findings to an email address.
- [x] Create an Amazon EventBridge rule to detect critical Security Hub findings. Create an Amazon Simple Notification Service (Amazon SNS) topic as the target of the EventBridge rule. Subscribe an email endpoint to the SNS topic to receive published messages.
- [ ] Create an Amazon EventBridge rule to detect critical Security Hub findings. Create an Amazon Simple Email Service (Amazon SES) topic as the target of the EventBridge rule. Use the Amazon SES API to format the message. Choose an email address to be the recipient of the message.

### An international company has established a new business entity in South Korea. The company also has established a new AWS account to contain the workload for the South Korean region. The company has set up the workload in the new account in the ap-northeast-2 Region. The workload consists of three Auto Scaling groups of Amazon EC2 instances. All workloads that operate in this Region must keep system logs and application logs for 7 years. A security engineer must implement a solution to ensure that no logging data is lost for each instance during scaling activities. The solution also must keep the logs for only the required period of 7 years. Which combination of steps should the security engineer take to meet these requirements? (Choose THREE)

- [x] Ensure that the Amazon CloudWatch agent is installed on all the EC2 instances that the Auto Scaling groups launch. Generate a CloudWatch agent configuration file to forward the required logs to Amazon CloudWatch Logs.
- [x] Set the log retention for desired log groups to 7 years.
- [x] Attach an IAM role to the launch configuration or launch template that the Auto Scaling groups use. Configure the role to provide the necessary permissions to forward logs to Amazon CloudWatch Logs.
- [ ] Attach an IAM role to the launch configuration or launch template that the Auto Scaling groups use. Configure the role to provide the necessary permissions to forward logs to Amazon S3.
- [ ] Ensure that a log forwarding application is installed on all the EC2 instances that the Auto Scaling groups launch. Configure the log forwarding application to periodically bundle the logs and forward the logs to Amazon S3.
- [ ] Configure an Amazon S3 Lifecycle policy on the target S3 bucket to expire objects after 7 years.

### A security engineer is designing an IAM policy to protect AWS API operations. The policy must enforce multi-factor authentication (MFA) for IAM users to access certain services in the AWS production account. Each session must remain valid for only 2 hours. The current version of the IAM policy is as follows. Which combination of conditions must the security engineer add to the IAM policy to meet these requirements? (Choose TWO)

![Question 110](images/question110.png)

- [x] `"Bool": {"aws:MultiFactorAuthPresent": "true"}`.
- [ ] `"Bool": {"aws:MultiFactorAuthPresent": "false"}`.
- [x] `"NumericLessThan": {"aws:MultiFactorAuthAge": "7200"}`.
- [ ] `"NumericGreaterThan": {"aws:MultiFactorAuthAge": "7200"}`.
- [ ] `"NumericLessThan": {"MaxSessionDuration": "7200"}`.

### A company uses AWS Organizations and has production workloads across multiple AWS accounts. A security engineer needs to design a solution that will proactively monitor for suspicious behavior across all the accounts that contain production workloads. The solution must automate remediation of incidents across the production accounts. The solution also must publish a notification to an Amazon Simple Notification Service (Amazon SNS) topic when a critical security finding is detected. In addition, the solution must send all security incident logs to a dedicated account. Which solution will meet these requirements?

- [ ] Activate Amazon GuardDuty in each production account. In a dedicated logging account, aggregate all GuardDuty logs from each production account. Remediate incidents by configuring GuardDuty to directly invoke an AWS Lambda function. Configure the Lambda function to also publish notifications to the SNS topic.
- [ ] Activate AWS Security Hub in each production account. In a dedicated logging account, aggregate all Security Hub findings from each production account. Remediate incidents by using AWS Config and AWS Systems Manager. Configure Systems Manager to also publish notifications to the SNS topic.
- [x] Activate Amazon GuardDuty in each production account. In a dedicated logging account, aggregate all GuardDuty logs from each production account. Remediate incidents by using Amazon EventBridge to invoke a custom AWS Lambda function from the GuardDuty findings. Configure the Lambda function to also publish notifications to the SNS topic.
- [ ] Activate AWS Security Hub in each production account. In a dedicated logging account, aggregate all Security Hub findings from each production account. Remediate incidents by using Amazon EventBridge to invoke a custom AWS Lambda function from the Security Hub findings. Configure the Lambda function to also publish notifications to the SNS topic.

### A company is developing an ecommerce application. The application uses Amazon EC2 instances and an Amazon RDS MySQL database. For compliance reasons, data must be secured in transit and at rest. The company needs a solution that minimizes operational overhead and minimizes cost. Which solution meets these requirements?

- [x] Use TLS certificates from AWS Certificate Manager (ACM) with an Application Load Balancer. Deploy self-signed certificates on the EC2 instances. Ensure that the database client software uses a TLS connection to Amazon RDS. Enable encryption of the RDS DB instance. Enable encryption on the Amazon Elastic Block Store (Amazon EBS) volumes that support the EC2 instances.
- [ ] Use TLS certificates from a third-party vendor with an Application Load Balancer. Install the same certificates on the EC2 instances. Ensure that the database client software uses a TLS connection to Amazon RDS. Use AWS Secrets Manager for client-side encryption of application data.
- [ ] Use AWS CloudHSM to generate TLS certificates for the EC2 instances. Install the TLS certificates on the EC2 instances. Ensure that the database client software uses a TLS connection to Amazon RDS. Use the encryption keys from CloudHSM for client-side encryption of application data.
- [ ] Use Amazon CloudFront with AWS WAF. Send HTTP connections to the origin EC2 instances. Ensure that the database client software uses a TLS connection to Amazon RDS. Use AWS Key Management Service (AWS KMS) for client-side encryption of application data before the data is stored in the RDS database.

### A security engineer is working with a company to design an ecommerce application. The application will run on Amazon EC2 instances that run in an Auto Scaling group behind an Application Load Balancer (ALB). The application will use an Amazon RDS DB instance for its database. The only required connectivity from the internet is for HTTP and HTTPS traffic to the application. The application must communicate with an external payment provider that allows traffic only from a preconfigured allow list of IP addresses. The company must ensure that communications with the external payment provider are not interrupted as the environment scales. Which combination of actions should the security engineer recommend to meet these requirements? (Choose THREE)

- [x] Deploy a NAT gateway in each private subnet for every Availability Zone that is in use.
- [ ] Place the DB instance in a public subnet.
- [x] Place the DB instance in a private subnet.
- [ ] Configure the Auto Scaling group to place the EC2 instances in a public subnet.
- [x] Configure the Auto Scaling group to place the EC2 instances in a private subnet.
- [ ] Deploy the ALB in a private subnet.

### A company uses several AWS CloudFormation stacks to handle the deployment of a suite of applications. The leader of the company's application development team notices that the stack deployments fail with permission errors when some team members try to deploy the stacks. However, other team members can deploy the stacks successfully. The team members access the account by assuming a role that has a specific set of permissions that are necessary for the job responsibilities of the team members. All team members have permissions to perform operations on the stacks. Which combination of steps will ensure consistent deployment of the stacks MOST securely? (Choose THREE)

- [ ] Create a service role that has a composite principal that contains each service that needs the necessary permissions. Configure the role to allow the `sts:AssumeRole` action.
- [x] Create a service role that has `cloudformation.amazonaws.com` as the service principal. Configure the role to allow the `sts:AssumeRole` action.
- [ ] For each required set of permissions, add a separate policy to the role to allow those permissions. Add the ARN of each CloudFormation stack in the resource field of each policy.
- [ ] For each required set of permissions, add a separate policy to the role to allow those permissions. Add the ARN of each service that needs the permissions in the resource field of the corresponding policy.
- [x] Update each stack to use the service role.
- [x] Add a policy to each member role to allow the `iam:PassRole` action. Set the policy's resource field to the ARN of the service role.

### A company used a lift-and-shift approach to migrate from its on-premises data centers to the AWS Cloud. The company migrated on-premises VMs to Amazon EC2 instances. Now the company wants to replace some of components that are running on the EC2 instances with managed AWS services that provide similar functionality. Initially, the company will transition from load balancer software that runs on EC2 instances to AWS Elastic Load Balancers. A security engineer must ensure that after this transition, all the load balancer logs are centralized and searchable for auditing. The security engineer must also ensure that metrics are generated to show which ciphers are in use. Which solution will meet these requirements?

- [ ] Create an Amazon CloudWatch Logs log group. Configure the load balancers to send logs to the log group. Use the CloudWatch Logs console to search the logs. Create CloudWatch Logs filters on the logs for the required metrics.
- [ ] Create an Amazon S3 bucket. Configure the load balancers to send logs to the S3 bucket. Use Amazon Athena to search the logs that are in the S3 bucket. Create Amazon CloudWatch filters on the S3 log files for the required metrics.
- [x] Create an Amazon S3 bucket. Configure the load balancers to send logs to the S3 bucket. Use Amazon Athena to search the logs that are in the S3 bucket. Create Athena queries for the required metrics. Publish the metrics to Amazon CloudWatch.
- [ ] Create an Amazon CloudWatch Logs log group. Configure the load balancers to send logs to the log group. Use the AWS Management Console to search the logs. Create Amazon Athena queries for the required metrics. Publish the metrics to Amazon CloudWatch.

### A security engineer creates an Amazon S3 bucket policy that denies access to all users. A few days later, the security engineer adds an additional statement to the bucket policy to allow read-only access to one other employee. Even after updating the policy, the employee sill receives an access denied message. What is the likely cause of this access denial?

- [ ] The ACL in the bucket needs to be updated.
- [ ] The IAM policy does not allow the user to access the bucket.
- [ ] It takes a few minutes for a bucket policy to take effect.
- [x] The allow permission is being overridden by the deny.

### A company needs complete encryption of the traffic between external users and an application. The company hosts the application on a fleet of Amazon EC2 instances that run in an Auto Scaling group behind an Application Load Balancer (ALB). How can a security engineer meet these requirements?

- [ ] Create a new Amazon-issued certificate in AWS Secrets Manager. Export the certificate from Secrets Manager. Import the certificate into the ALB and the EC2 instances.
- [ ] Create a new Amazon-issued certificate in AWS Certificate Manager (ACM). Associate the certificate with the ALExport the certificate from ACM. Install the certificate on the EC2 instances.
- [ ] Import a new third-party certificate into AWS Identity and Access Management (IAM). Export the certificate from IAM. Associate the certificate with the ALB and the EC2 instances.
- [x] Import a new third-party certificate into AWS Certificate Manager (ACM). Associate the certificate with the ALB. Install the certificate on the EC2 instances.

### While securing the connection between a company's VPC and its on-premises data center, a security engineer sent a ping command from an on-premises host (IP address 203.0.113.12) to an Amazon EC2 instance (IP address 172.31.16.139). The ping command did not return a response. The flow log in the VPC showed the following: What action should be performed to allow the ping to work?

![Question 118](images/question118.jpg)

- [ ] In the security group of the EC2 instance, allow inbound ICMP traffic.
- [ ] In the security group of the EC2 instance, allow outbound ICMP traffic.
- [ ] In the VPC's NACL, allow inbound ICMP traffic.
- [x] In the VPC's NACL, allow outbound ICMP traffic.

### What are the MOST secure ways to protect the AWS account root user of a recently opened AWS account? (Choose TWO)

- [ ] Use the AWS account root user access keys instead of the AWS Management Console.
- [ ] Enable multi-factor authentication for the AWS IAM users with the AdministratorAccess managed policy attached to them.
- [ ] Use AWS KMS to encrypt all AWS account root user and AWS IAM access keys and set automatic rotation to 30 days.
- [x] Do not create access keys for the AWS account root user; instead, create AWS IAM users.
- [x] Enable multi-factor authentication for the AWS account root user.

### A company is expanding its group of stores. On the day that each new store opens, the company wants to launch a customized web application for that store. Each store's application will have a non-production environment and a production environment. Each environment will be deployed in a separate AWS account. The company uses AWS Organizations and has an OU that is used only for these accounts. The company distributes most of the development work to third-party development teams. A security engineer needs to ensure that each team follows the company's deployment plan for AWS resources. The security engineer also must limit access to the deployment plan to only the developers who need access. The security engineer already has created an AWS CloudFormation template that implements the deployment plan. What should the security engineer do next to meet the requirements in the MOST secure way?

- [x] Create an AWS Service Catalog portfolio in the organization's management account. Upload the CloudFormation template. Add the template to the portfolio's product list. Share the portfolio with the OU.
- [ ] Use the CloudFormation CLI to create a module from the CloudFormation template. Register the module as a private extension in the CloudFormation registry. Publish the extension. In the OU, create an SCP that allows access to the extension.
- [ ] Create an AWS Service Catalog portfolio in the organization's management account. Upload the CloudFormation template. Add the template to the portfolio's product list. Create an IAM role that has a trust policy that allows cross-account access to the portfolio for users in the OU accounts. Attach the AWSServiceCatalogEndUserFullAccess managed policy to the role.
- [ ] Use the CloudFormation CLI to create a module from the CloudFormation template. Register the module as a private extension in the CloudFormation registry. Publish the extension. Share the extension with the OU.

### A company is hosting a web application on Amazon EC2 instances behind an Application Load Balancer (ALB). The application has become the target of a DoS attack. Application logging shows that requests are coming from a small number of client IP addresses, but the addresses change regularly. The company needs to block the malicious traffic with a solution that requires the least amount of ongoing effort. Which solution meets these requirements?

- [x] Create an AWS WAF rate-based rule, and attach it to the ALB.
- [ ] Update the security group that is attached to the ALB to block the attacking IP addresses.
- [ ] Update the ALB subnet's network ACL to block the attacking client IP addresses.
- [ ] Create an AWS WAF rate-based rule, and attach it to the security group of the EC2 instances.

### A company has hundreds of AWS accounts in an organization in AWS Organizations. The company operates out of a single AWS Region. The company has a dedicated security tooling AWS account in the organization. The security tooling account is configured as the organization's delegated administrator for Amazon GuardDuty and AWS Security Hub. The company has configured the environment to automatically enable GuardDuty and Security Hub for existing AWS accounts and new AWS accounts. The company is performing control tests on specific GuardDuty findings to make sure that the company's security team can detect and respond to security events. The security team launched an Amazon EC2 instance and attempted to run DNS requests against a test domain, example.com, to generate a DNS finding. However, the GuardDuty finding was never created in the Security Hub delegated administrator account. Why was the finding was not created in the Security Hub delegated administrator account?

- [ ] VPC flow logs were not turned on for the VPC where the EC2 instance was launched.
- [x] The VPC where the EC2 instance was launched had the DHCP option configured for a custom OpenDNS resolver.
- [ ] The GuardDuty integration with Security Hub was never activated in the AWS account where the finding was generated.
- [ ] Cross-Region aggregation in Security Hub was not configured.

### An ecommerce company has a web application architecture that runs primarily on containers. The application containers are deployed on Amazon Elastic Container Service (Amazon ECS). The container images for the application are stored in Amazon Elastic Container Registry (Amazon ECR). The company's security team is performing an audit of components of the application architecture. The security team identifies issues with some container images that are stored in the container repositories. The security team wants to address these issues by implementing continual scanning and on-push scanning of the container images. The security team needs to implement a solution that makes any findings from these scans visible in a centralized dashboard. The security team plans to use the dashboard to view these findings along with other security-related findings that they intend to generate in the future. There are specific repositories that the security team needs to exclude from the scanning process. Which solution will meet these requirements?

- [x] Use Amazon Inspector. Create inclusion rules in Amazon ECR to match repositories that need to be scanned. Push Amazon Inspector findings to AWS Security Hub.
- [ ] Use ECR basic scanning of container images. Create inclusion rules in Amazon ECR to match repositories that need to be scanned. Push findings to AWS Security Hub.
- [ ] Use ECR basic scanning of container images. Create inclusion rules in Amazon ECR to match repositories that need to be scanned. Push findings to Amazon Inspector.
- [ ] Use Amazon Inspector. Create inclusion rules in Amazon Inspector to match repositories that need to be scanned. Push Amazon Inspector findings to AWS Config.

### A company has a single AWS account and uses an Amazon EC2 instance to test application code. The company recently discovered that the instance was compromised. The instance was serving up malware. The analysis of the instance showed that the instance was compromised 35 days ago. A security engineer must implement a continuous monitoring solution that automatically notifies the company's security team about compromised instances through an email distribution list for high severity findings. The security engineer must implement the solution as soon as possible. Which combination of steps should the security engineer take to meet these requirements? (Choose THREE)

- [ ] Enable AWS Security Hub in the AWS account.
- [x] Enable Amazon GuardDuty in the AWS account.
- [x] Create an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe the security team's email distribution list to the topic.
- [ ] Create an Amazon Simple Queue Service (Amazon SQS) queue. Subscribe the security team's email distribution list to the queue.
- [x] Create an Amazon EventBridge rule for GuardDuty findings of high severity. Configure the rule to publish a message to the topic.
- [ ] Create an Amazon EventBridge rule for Security Hub findings of high severity. Configure the rule to publish a message to the queue.

### A company is using AWS Organizations to manage multiple AWS accounts for its human resources, finance, software development, and production departments. All the company's developers are part of the software development AWS account. The company discovers that developers have launched Amazon EC2 instances that were preconfigured with software that the company has not approved for use. The company wants to implement a solution to ensure that developers can launch EC2 instances with only approved software applications and only in the software development AWS account. Which solution will meet these requirements?

- [ ] In the software development account, create AMIs of preconfigured instances that include only approved software. Include the AMI IDs in the condition section of an AWS CloudFormation template to launch the appropriate AMI based on the AWS Region. Provide the developers with the CloudFormation template to launch EC2 instances in the software development account.
- [ ] Create an Amazon EventBridge rule that runs when any EC2 RunInstances API event occurs in the software development account. Specify AWS Systems Manager Run Command as a target of the rule. Configure Run Command to run a script that will install all approved software onto the instances that the developers launch.
- [x] Use an AWS Service Catalog portfolio that contains EC2 products with appropriate AMIs that include only approved software. Grant the developers permission to access only the Service Catalog portfolio to launch a product in the software development account.
- [ ] In the management account, create AMIs of preconfigured instances that include only approved software. Use AWS CloudFormation StackSets to launch the AMIs across any AWS account in the organization. Grant the developers permission to launch the stack sets within the management account.

### A company has enabled Amazon GuardDuty in all AWS Regions as part of its security monitoring strategy. In one of its VPCs, the company hosts an Amazon EC2 instance that works as an FTP server. A high number of clients from multiple locations contact the FTP server. GuardDuty identifies this activity as a brute force attack because of the high number of connections that happen every hour. The company has flagged the finding as a false positive, but GuardDuty continues to raise the issue. A security engineer must improve the signal-to-noise ratio without compromising the company's visibility of potential anomalous behavior. Which solution will meet these requirements?

- [ ] Disable the FTP rule in GuardDuty in the Region where the FTP server is deployed.
- [ ] Add the FTP server to a trusted IP list. Deploy the list to GuardDuty to stop receiving the notifications.
- [x] Create a suppression rule in GuardDuty to filter findings by automatically archiving new findings that match the specified criteria.
- [ ] Create an AWS Lambda function that has the appropriate permissions to delete the finding whenever a new occurrence is reported.

### A company's security engineer has been tasked with restricting a contractor's IAM account access to the company's Amazon EC2 console without providing access to any other AWS services. The contractor's IAM account must not be able to gain access to any other AWS service, even if the IAM account is assigned additional permissions based on IAM group membership. What should the security engineer do to meet these requirements?

- [ ] Create an inline IAM user policy that allows for Amazon EC2 access for the contractor's IAM user.
- [x] Create an IAM permissions boundary policy that allows Amazon EC2 access. Associate the contractor's IAM account with the IAM permissions boundary policy.
- [ ] Create an IAM group with an attached policy that allows for Amazon EC2 access. Associate the contractor's IAM account with the IAM group.
- [ ] Create a IAM role that allows for EC2 and explicitly denies all other services. Instruct the contractor to always assume this role.

### A company manages multiple AWS accounts using AWS Organizations. The company's security team notices that some member accounts are not sending AWS CloudTrail logs to a centralized Amazon S3 logging bucket. The security team wants to ensure there is at least one trail configured for all existing accounts and for any account that is created in the future. Which set of actions should the security team implement to accomplish this?

- [ ] Create a new trail and configure it to send CloudTrail logs to Amazon S3. Use Amazon EventBridge to send notification if a trail is deleted or stopped.
- [ ] Deploy an AWS Lambda function in every account to check if there is an existing trail and create a new trail, if needed.
- [x] Edit the existing trail in the Organizations management account and apply it to the organization.
- [ ] Create an SCP to deny the `cloudtrail:Delete*` and `cloudtrail:Stop*` actions. Apply the SCP to all accounts.

### A company recently had a security audit in which the auditors identified multiple potential threats. These potential threats can cause usage pattern changes such as DNS access peak, abnormal instance traffic, abnormal network interface traffic, and unusual Amazon S3 API calls. The threats can come from different sources and can occur at any time. The company needs to implement a solution to continuously monitor its system and identify all these incoming threats in near-real time. Which solution will meet these requirements?

- [ ] Enable AWS CloudTrail logs, VPC flow logs, and DNS logs. Use Amazon CloudWatch Logs to manage these logs from a centralized account.
- [ ] Enable AWS CloudTrail logs, VPC flow logs, and DNS logs. Use Amazon Macie to monitor these logs from a centralized account.
- [x] Enable Amazon GuardDuty from a centralized account. Use GuardDuty to manage AWS CloudTrail logs, VPC flow logs, and DNS logs.
- [ ] Enable Amazon Inspector from a centralized account. Use Amazon Inspector to manage AWS CloudTrail logs, VPC flow logs, and DNS logs.

### A company that uses AWS Organizations is using AWS IAM Identity Center (AWS Single Sign-On) to administer access to AWS accounts. A security engineer is creating a custom permission set in IAM Identity Center. The company will use the permission set across multiple accounts. An AWS managed policy and a customer managed policy are attached to the permission set. The security engineer has full administrative permissions and is operating in the management account. When the security engineer attempts to assign the permission set to an IAM Identity Center user who has access to multiple accounts, the assignment fails. What should the security engineer do to resolve this failure?

- [x] Create the customer managed policy in every account where the permission set is assigned. Give the customer managed policy the same name and same permissions in each account.
- [ ] Remove either the AWS managed policy or the customer managed policy from the permission set. Create a second permission set that includes the removed policy. Apply the permission sets separately to the user.
- [ ] Evaluate the logic of the AWS managed policy and the customer managed policy. Resolve any policy conflicts in the permission set before deployment.
- [ ] Do not add the new permission set to the user. Instead, edit the user's existing permission set to include the AWS managed policy and the customer managed policy.

### A company has thousands of AWS Lambda functions. While reviewing the Lambda functions, a security engineer discovers that sensitive information is being stored in environment variables and is viewable as plaintext in the Lambda console. The values of the sensitive information are only a few characters long. What is the MOST cost-effective way to address this security issue?

- [ ] Set up IAM policies from the Lambda console to hide access to the environment variables.
- [ ] Use AWS Step Functions to store the environment variables. Access the environment variables at runtime. Use IAM permissions to restrict access to the environment variables to only the Lambda functions that require access.
- [ ] Store the environment variables in AWS Secrets Manager, and access them at runtime. Use IAM permissions to restrict access to the secrets to only the Lambda functions that require access.
- [x] Store the environment variables in AWS Systems Manager Parameter Store as secure string parameters, and access them at runtime. Use IAM permissions to restrict access to the parameters to only the Lambda functions that require access.

### A company has recently recovered from a security incident that required the restoration of Amazon EC2 instances from snapshots. The company uses an AWS Key Management Service (AWS KMS) customer managed key to encrypt all Amazon Elastic Block Store (Amazon EBS) snapshots. The company performs a gap analysis of its disaster recovery procedures and backup strategies. A security engineer needs to implement a solution so that the company can recover the EC2 instances if the AWS account is compromised and the EBS snapshots are deleted. Which solution will meet this requirement?

- [ ] Create a new Amazon S3 bucket. Use EBS lifecycle policies to move EBS snapshots to the new S3 bucket. Use lifecycle policies to move snapshots to the S3 Glacier Instant Retrieval storage class. Use S3 Object Lock to prevent deletion of the snapshots.
- [ ] Use AWS Systems Manager to distribute a configuration that backs up all attached disks to Amazon S3.
- [x] Create a new AWS account that has limited privileges. Allow the new account to access the KMS key that encrypts the EBS snapshots. Copy the encrypted snapshots to the new account on a recurring basis.
- [ ] Use AWS Backup to copy EBS snapshots to Amazon S3. Use S3 Object Lock to prevent deletion of the snapshots.

### A company's security engineer is designing an isolation procedure for Amazon EC2 instances as part of an incident response plan. The security engineer needs to isolate a target instance to block any traffic to and from the target instance, except for traffic from the company's forensics team. Each of the company's EC2 instances has its own dedicated security group. The EC2 instances are deployed in subnets of a VPC. A subnet can contain multiple instances. The security engineer is testing the procedure for EC2 isolation and opens an SSH session to the target instance. The procedure starts to simulate access to the target instance by an attacker. The security engineer removes the existing security group rules and adds security group rules to give the forensics team access to the target instance on port 22. After these changes, the security engineer notices that the SSH connection is still active and usable. When the security engineer runs a ping command to the public IP address of the target instance, the ping command is blocked. What should the security engineer do to isolate the target instance?

- [ ] Add an inbound rule to the security group to allow traffic from 0.0.0.0/0 for all ports. Add an outbound rule to the security group to allow traffic to 0.0.0.0/0 for all ports. Then immediately delete these rules.
- [x] Remove the port 22 security group rule. Attach an instance role policy that allows AWS Systems Manager Session Manager connections so that the forensics team can access the target instance.
- [ ] Create a network ACL that is associated with the target instance's subnet. Add a rule at the top of the inbound rule set to deny all traffic from 0.0.0.0/0. Add a rule at the top of the outbound rule set to deny all traffic to 0.0.0.0/0.
- [ ] Create an AWS Systems Manager document that adds a host-level firewall rule to block all inbound traffic and outbound traffic. Run the document on the target instance.

### A company has five AWS accounts and wants to use AWS CloudTrail to log API calls. The log files must be stored in an Amazon S3 bucket that resides in a new account specifically built for centralized services with a unique top-level prefix for each trail. The configuration must also enable detection of any modification to the logs. Which of the following steps will implement these requirements? (Choose three.)

- [x] Create a new S3 bucket in a separate AWS account for centralized storage of CloudTrail logs, and enable Log File Validation on all trails.
- [ ] Use an existing S3 bucket in one of the accounts, apply a bucket policy to the new centralized S3 bucket that permits the CloudTrail service to use the `s3: PutObject` action and the `s3 GetBucketACL` action, and specify the appropriate resource ARNs for the CloudTrail trails.
- [x] Apply a bucket policy to the new centralized S3 bucket that permits the CloudTrail service to use the `s3 PutObject` action and the `s3 GelBucketACL` action, and specify the appropriate resource ARNs for the CloudTrail trails.
- [x] Use unique log file prefixes for trails in each AWS account.
- [ ] Configure CloudTrail in the centralized account to log all accounts to the new centralized S3 bucket.
- [ ] Enable encryption of the log files by using AWS Key Management Service.

### A security engineer is checking an AWS CloudFormation template for vulnerabilities. The security engineer finds a parameter that has a default value that exposes an application's API key in plaintext. The parameter is referenced several times throughout the template. The security engineer must replace the parameter while maintaining the ability to reference the value in the template. Which solution will meet these requirements in the MOST secure way?

- [ ] Store the API key value as a SecureString parameter in AWS Systems Manager Parameter Store. In the template, replace all references to the value with `{{resolve:ssm:MySSMParameterName:1}}`.
- [x] Store the API key value in AWS Secrets Manager. In the template, replace all references to the value with `{{resolve:secretsmanager:MySecretId:SecretString}}`.
- [ ] Store the API key value in Amazon DynamoDB. In the template, replace all references to the value with `{{resolve:dynamodb:MyTableName:MyPrimaryKey}}`.
- [ ] Store the API key value in a new Amazon S3 bucket. In the template, replace all references to the value with `{{resolve:s3:MyBucketName:MyObjectName}}`.

### A company has several petabytes of data. The company must preserve this data for 7 years to comply with regulatory requirements. The company's compliance team asks a security officer to develop a strategy that will prevent anyone from changing or deleting the data. Which solution will meet this requirement MOST cost-effectively?

- [ ] Create an Amazon S3 bucket. Configure the bucket to use S3 Object Lock in compliance mode. Upload the data to the bucket. Create a resource-based bucket policy that meets all the regulatory requirements.
- [ ] Create an Amazon S3 bucket. Configure the bucket to use S3 Object Lock in governance mode. Upload the data to the bucket. Create a user-based IAM policy that meets all the regulatory requirements.
- [x] Create a vault in Amazon S3 Glacier. Create a Vault Lock policy in S3 Glacier that meets all the regulatory requirements. Upload the data to the vault.
- [ ] Create an Amazon S3 bucket. Upload the data to the bucket. Use a lifecycle rule to transition the data to a vault in S3 Glacier. Create a Vault Lock policy that meets all the regulatory requirements.

### A company has several workloads running on AWS. Employees are required to authenticate using on-premises ADFS and SSO to access the AWS Management Console. Developers migrated an existing legacy web application to an Amazon EC2 instance. Employees need to access this application from anywhere on the internet, but currently, there is no authentication system built into the application. How should the security engineer implement employee-only access to this system without changing the application?

- [x] Place the application behind an Application Load Balancer (ALB). Use Amazon Cognito as authentication for the ALB. Define a SAML-based Amazon Cognito user pool and connect it to ADFS.
- [ ] Implement AWS IAM Identity Center (AWS Single Sign-On) in the management account and link it to ADFS as an identity provider. Define the EC2 instance as a managed resource, then apply an IAM policy on the resource.
- [ ] Define an Amazon Cognito identity pool, then install the connector on the Active Directory server. Use the Amazon Cognito SDK on the application instance to authenticate the employees using their Active Directory user names and passwords.
- [ ] Create an AWS Lambda custom authorizer as the authenticator for a reverse proxy on Amazon EC2. Ensure the security group on Amazon EC2 only allows access from the Lambda function.

### A company is using AWS to run a long-running analysis process on data that is stored in Amazon S3 buckets. The process runs on a fleet of Amazon EC2 instances that are in an Auto Scaling group. The EC2 instances are deployed in a private subnet of a VPC that does not have internet access. The EC2 instances and the S3 buckets are in the same AWS account. The EC2 instances access the S3 buckets through an S3 gateway endpoint that has the default access policy. Each EC2 instance is associated with an instance profile role that has a policy that explicitly allows the `s3:GetObject` action and the `s3:PutObject` action for only the required S3 buckets. The company learns that one or more of the EC2 instances are compromised and are exfiltrating data to an S3 bucket that is outside the company's organization in AWS Organizations. A security engineer must implement a solution to stop this exfiltration of data and to keep the EC2 processing job functional. Which solution will meet these requirements?

- [ ] Update the policy on the S3 gateway endpoint to allow the S3 actions only if the values of the `aws:ResourceOrgID` and `aws:PrincipalOrgID` condition keys match the company's values.
- [ ] Update the policy on the instance profile role to allow the S3 actions only if the value of the `aws:ResourceOrgID` condition key matches the company's value.
- [ ] Add a network ACL rule to the subnet of the EC2 instances to block outgoing connections on port 443.
- [x] Apply an SCP on the AWS account to allow the S3 actions only if the values of the `aws:ResourceOrgID` and `aws:PrincipalOrgID` condition keys match the company's values.

### A company that operates in a hybrid cloud environment must meet strict compliance requirements. The company wants to create a report that includes evidence from on-premises workloads alongside evidence from AWS resources. A security engineer must implement a solution to collect, review, and manage the evidence to demonstrate compliance with company policy. Which solution will meet these requirements?

- [x] Create an assessment in AWS Audit Manager from a prebuilt framework or a custom framework. Upload manual evidence from the on-premises workloads. Add the evidence to the assessment. Generate an assessment report after Audit Manager collects the necessary evidence from the AWS resources.
- [ ] Install the Amazon CloudWatch agent on the on-premises workloads. Use AWS Config to deploy a conformance pack from a sample conformance pack template or a custom YAML template. Generate an assessment report after AWS Config identifies noncompliant workloads and resources.
- [ ] Set up the appropriate security standard in AWS Security Hub. Upload manual evidence from the on-premises workloads. Wait for Security Hub to collect the evidence from the AWS resources. Download the list of controls as a .csv file.
- [ ] Install the Amazon CloudWatch agent on the on-premises workloads. Create a CloudWatch dashboard to monitor the on-premises workloads and the AWS resources. Run a query on the workloads and resources. Download the results.

### A company's security team has defined a set of AWS Config rules that must be enforced globally in all AWS accounts the company owns. What should be done to provide a consolidated compliance overview for the security team?

- [ ] Use AWS Organizations to limit AWS Config rules to the appropriate Regions, and then consolidate the Amazon CloudWatch dashboard into one AWS account.
- [x] Use AWS Config aggregation to consolidate the views into one AWS account, and provide role access to the security team.
- [ ] Consolidate AWS Config rule results with an AWS Lambda function and push data to Amazon SQS. Use Amazon SNS to consolidate and alert when some metrics are triggered.
- [ ] Use Amazon GuardDuty to load data results from the AWS Config rules compliance status, aggregate GuardDuty findings of all AWS accounts into one AWS account, and provide role access to the security team.

### A security engineer is designing an incident response plan to address the risk of a compromised Amazon EC2 instance. The plan must recommend a solution to meet the following requirements: A trusted forensic environment must be provisioned. Automated response processes must be orchestrated. Which AWS services should be included in the plan? (Select TWO)

- [x] AWS CloudFormation.
- [ ] Amazon GuardDuty.
- [ ] Amazon Inspector.
- [ ] Amazon Macie.
- [x] AWS Step Functions.

### A security engineer has been tasked with implementing a solution that allows the company's development team to have interactive command line access to Amazon EC2 Linux instances using the AWS Management Console. Which steps should the security engineer take to satisfy this requirement while maintaining least privilege?

- [x] Enable AWS Systems Manager in the AWS Management Console and configure for access to EC2 instances using the default AmazonEC2RoleforSSM role. Install the Systems Manager Agent on all EC2 Linux instances that need interactive access. Configure IAM user policies to allow development team access to the Systems Manager Session Manager and attach to the team's IAM users.
- [ ] Enable console SSH access in the EC2 console. Configure IAM user policies to allow development team access to the AWS Systems Manager Session Manager and attach to the development team's IAM users.
- [ ] Enable AWS Systems Manager in the AWS Management Console and configure to access EC2 instances using the default AmazonEC2RoleforSSM role. Install the Systems Manager Agent on all EC2 Linux instances that need interactive access. Configure a security group that allows SSH port 22 from all published IP addresses. Configure IAM user policies to allow development team access to the AWS Systems Manager Session Manager and attach to the team's IAM users.
- [ ] Enable AWS Systems Manager in the AWS Management Console and configure to access EC2 instances using the default AmazonEC2RoleforSSM role Install the Systems Manager Agent on all EC2 Linux instances that need interactive access. Configure IAM policies to allow development team access to the EC2 console and attach to the teams IAM users.

### A large government organization is moving to the cloud and has specific encryption requirements. The first workload to move requires that a customer's data be immediately destroyed when the customer makes that request. Management has asked the security team to provide a solution that will securely store the data, allow only authorized applications to perform encryption and decryption and allow for immediate destruction of the data. Which solution will meet these requirements?

- [ ] Use AWS Secrets Manager and an AWS SDK to create a unique secret for the customer-specific data.
- [ ] Use AWS Key Management Service (AWS KMS) and the AWS Encryption SDK to
generate and store a data encryption key for each customer.
- [ ] Use AWS Key Management Service (AWS KMS) with service-managed keys to generate and store customer-specific data encryption keys.
- [x] Use AWS Key Management Service (AWS KMS) and create an AWS CloudHSM custom key store Use CloudHSM to generate and store a new CMK for each customer.

### Unapproved changes were previously made to a company's Amazon S3 bucket. A security engineer configured AWS Config to record configuration changes made to the company's S3 buckets. The engineer discovers there are S3 configuration changes being made, but no Amazon SNS notifications are being sent. The engineer has already checked the configuration of the SNS topic and has confirmed the configuration is valid. Which combination of steps should the security engineer take to resolve the issue? (Select TWO)

- [ ] Configure the S3 bucket ACLs to allow AWS Config to record changes to the buckets.
- [x] Configure policies attached to S3 buckets to allow AWS Config to record changes to the buckets.
- [ ] Attach the AmazonS3ReadOnryAccess managed policy to the IAM user.
- [ ] Verify the security engineer's IAM user has an attached policy that allows all AWS Config actions.
- [x] Assign the AWSConfigRole managed policy to the AWS Config role.

### A company is operating an open-source software platform that is internet facing. The legacy software platform no longer receives security updates. The software platform operates using Amazon route 53 weighted load balancing to send traffic to two Amazon EC2 instances that connect to an Amazon POS cluster a recent report suggests this software platform is vulnerable to SQL injection attacks. with samples of attacks provided. The company's security engineer must secure this system against SQL injection attacks within 24 hours. The secure, engineer's solution involve the least amount of effort and maintain normal operations during implementation. What should the security engineer do to meet these requirements?

- [x] Create an Application Load Balancer with the existing EC2 instances as a target group Create an AWS WAF web ACL containing rules mat protect the application from this attach. then apply it to the ALB Test to ensure me vulnerability has been mitigated, then redirect thee Route 53 records to point to the ALB Update security groups on the EC 2 instances to prevent direct access from the internet.
- [ ] Create an Amazon CloudFront distribution specifying one EC2 instance as an origin Create an AWS WAF web ACL containing rules that protect the application from this attack, then apply it to me distribution Test to ensure the vulnerability has mitigated, then redirect the Route 53 records to point to CloudFront.
- [ ] Obtain me latest source code for the platform and make ire necessary updates Test me updated code to ensure that the vulnerability has been irrigated, then deploy me patched version of the platform to the EC2 instances.
- [ ] Update the security group mat is attached to the EC2 instances, removing access from the internet to the TCP port used by the SQL database Create an AWS WAF web ACL containing rules mat protect me application from this attack, men apply it to the EC2 instances Test to ensure me vulnerability has been mitigated. then restore the security group to me onginal setting.

### A security engineer has noticed that VPC Flow Logs are getting a lot REJECT traffic originating from a single Amazon EC2 instance in an Auto Scaling group. The security engineer is concerned that this EC2 instance may be compromised. What immediate action should the security engineer take?

- [x] Remove the instance from the Auto Seating group Close me security group mm ingress only from a single forensic P address to perform an analysis.
- [ ] Remove the instance from the Auto Seating group Change me network ACL rules to allow traffic only from a single forensic IP address to perform en analysis Add a rule to deny all other traffic.
- [ ] Remove the instance from the Auto Scaling group Enable Amazon GuardDuty in that AWS account Install the Amazon Inspector agent cm the suspicious EC 2 instance to perform a scan.
- [ ] Take a snapshot of the suspicious EC2 instance. Create a new EC2 instance from me snapshot in a closed security group with ingress only from a single forensic IP address to perform an analysis.

### A company is collecting AWS CloudTrail log data from multiple AWS accounts by managing individual trails in each account and forwarding log data to a centralized Amazon S3 bucket residing in a log archive account. After CloudTrail introduced support for AWS Organizations trails, the company decided to further centralize management and automate deployment of the CloudTrail logging capability across all of its AWS accounts. The company's security engineer created an AWS Organizations trail in the master account, enabled server-side encryption with AWS KMS managed keys (SSE-KMS) for the log files, and specified the same bucket as the storage location. However, the engineer noticed that logs recorded by the new trail were not delivered to the bucket. Which factors could cause this issue? (Select TWO)

- [ ] The CMK key policy does not allow CloudTrail to make encrypt and decrypt API calls against the key.
- [x] The CMK key policy does not allow CloudTrail to make GenerateDataKey API calls against the key.
- [ ] The IAM role used by the CloudTrail trail does not have permissions to make PutObject API calls against a folder created for the Organizations trail.
- [x] The S3 bucket policy does not allow CloudTrail to make PutObject API calls against a folder created for the Organizations trail.
- [ ] The CMK key policy does not allow the IAM role used by the CloudTrail trail to use the key for crypto graphicaI operations.

### A company has implemented centralized logging and monitoring of AWS CloudTrail logs from all Regions in an Amazon S3 bucket. The log Hies are encrypted using AWS KMS. A Security Engineer is attempting to review the log files using a third-party tool hosted on an Amazon EC2 instance. The Security Engineer is unable to access the logs in the S3 bucket and receives an access denied error message. What should the Security Engineer do to fix this issue?

- [ ] Check that the role the Security Engineer uses grants permission to decrypt objects using the KMS CMK.
- [ ] Check that the role the Security Engineer uses grants permission to decrypt objects using the KMS CMK and gives access to the S3 bucket and objects.
- [x] Check that the role the EC2 instance profile uses grants permission to decrypt objects using the KMS CMK and gives access to the S3 bucket and objects.
- [ ] Check that the role the EC2 instance profile uses grants permission to decrypt objects using the KMS CMK.

### A company has a VPC with several Amazon EC2 instances behind a NAT gateway. The company's security policy states that all network traffic must be logged and must include the original source and destination IP addresses. The existing VPC Flow Logs do not include this information. A security engineer needs to recommend a solution. Which combination of steps should the security engineer recommend? (Select TWO)

- [ ] Edit the existing VPC Flow Logs. Change the log format of the VPC Flow Logs from the Amazon default format to a custom format.
- [x] Delete and recreate the existing VPC Flow Logs. Change the log format of the VPC Flow Logs from the Amazon default format to a custom format.
- [ ] Change the destination to Amazon CloudWatch Logs.
- [x] Include the pkt-srcaddr and pkt-dstaddr fields in the log format.
- [ ] Include the subnet-id and instance-id fields in the log format.

### A company recently performed an annual security assessment of its AWS environment. The assessment showed that audit logs are not available beyond 90 days and that unauthorized changes to IAM policies are made without detection. How should a security engineer resolve these issues?

- [ ] Create an Amazon S3 lifecycle policy that archives AWS CloudTrail trail logs to Amazon S3 Glacier after 90 days. Configure Amazon Inspector to provide a notification when a policy change is made to resources.
- [ ] Configure AWS Artifact to archive AWS CloudTrail logs Configure AWS Trusted Advisor to provide a notification when a policy change is made to resources.
- [ ] Configure Amazon CloudWatch to export log groups to Amazon S3. Configure AWS CloudTrail to provide a notification when a policy change is made to resources.
- [x] Create an AWS CloudTrail trail that stores audit logs in Amazon S3. Configure an AWS Config rule to provide a notif cation when a policy change is made to resources.

### A company has several critical applications running on a large fleet of Amazon EC2 instances. As part of a security operations review, the company needs to apply a critical operating system patch to EC2 instances within 24 hours of the patch becoming available from the operating system vendor. The company does not have a patching solution deployed on AWS, but does have AWS Systems Manager configured. The solution must also minimize administrative overhead. What should a security engineer recommend to meet these requirements?

- [ ] Create an AWS Config rule defining the patch as a required configuration for EC2 instances.
- [ ] Use the AWS Systems Manager Run Command to patch affected instances.
- [x] Use an AWS Systems Manager Patch Manager predefined baseline to patch affected instances.
- [ ] Use AWS Systems Manager Session Manager to log in to each affected instance and apply the patch.

### A security engineer is asked to update an AW3 CoudTrail log file prefix for an existing trail. When attempting to save the change in the CloudTrail console, the security engineer receives the following error message. `There is a problem with the bucket policy.`. What will enable the security engineer to saw the change?

- [ ] Create a new trail with the updated log file prefix, and then delete the original nail Update the existing bucket policy in the Amazon S3 console with the new log the prefix, and then update the log file prefix in the CloudTrail console.
- [ ] Update the existing bucket policy in the Amazon S3 console to allow the security engineers principal to perform PutBucketPolicy, and then update the log file prefix in the CloudTrail console.
- [x] Update the existing bucket policy in the Amazon S3 console with the new log file prefix, and then update the log file prefix in the CloudTrail console.
- [ ] Update the existing bucket policy in the Amazon S3 console to allow the security engineers principal to perform GetBucketPolicy, and then update the log file prefix in the CloudTrail console.

### The rule set in the virtual appliance is correct. Which of the following are other valid items to troubleshoot in this scenario? (Choose TWO)

- [ ] Verify that the 0.0.0.0/0 route in the route table for the Web server subnet points to a NAT gateway.
- [x] Verify which Security Group is applied to the particular web server's elastic network interface (ENI).
- [ ] Verify that the 0.0.0.0/0 route in the route table for the Web server subnet points to the virtual security appliance.
- [x] Verify the registered targets in the ALB.
- [ ] Verify that the 0.0.0.0/0 route in the public subnet points to a NAT gateway.

### A Web Administrator for the website example.com has created an Amazon CloudFront distribution for dev.example.com, with a requirement to configure HTTPS using a custom TLS certificate imported to AWS Certificate Manager. Which combination of steps is required to ensure availability of the certificate in the CloudFront console? (Choose TWO)

- [ ] Call UploadServerCertificate with /cloudfront/dev/ in the path parameter.
- [ ] Import the certificate with a 4,096-bit RSA public key.
- [ ] Ensure that the certificate, private key, and certificate chain are PKCS #12-encoded.
- [x] Import the certificate in the `us-east-1` (N. Virginia) Region.
- [x] Ensure that the certificate, private key, and certificate chain are PEM-encoded.

### A company's Security Engineer has been asked to monitor and report all AWS account root user activities. Which of the following would enable the Security Engineer to monitor and report all root user activities? (Select TWO)

- [ ] Configuring AWS Organizations to monitor root user API calls on the paying account.
- [x] Creating an Amazon CloudWatch Events rule that will trigger when any API call from the root user is reported.
- [ ] Configuring Amazon Inspector to scan the AWS account for any root user activity.
- [ ] Configuring AWS Trusted Advisor to send an email to the Security team when the root user logs in to the console.
- [x] Using Amazon SNS to notify the target group.

### A company is building a data lake on Amazon S3. The data consists of millions of small files containing sensitive information. The security team has the following requirements for the architecture: Data must be encrypted in transit. Data must be encrypted at rest. The bucket must be private, but if the bucket is accidentally made public, the data must remain confidential. Which combination of steps would meet the requirements? (Select THREE)

- [ ] Enable AES-256 encryption using server-side encryption with Amazon S3-managed encryption keys (SSE-S3) on the S3 bucket.
- [x] Enable default encryption with server-side encryption with AWS KMS-managed keys (SSE-KMS) on the S3 bucket.
- [x] Add a bucket policy that includes a deny if a PutObject request does not include `aws:SecureTransport`.
- [ ] Add a bucket policy with `aws:SourceIp` to Allow uploads and downloads from the corporate intranet only.
- [x] Add a bucket policy that includes a deny if a PutObject request does not include `s3:x-amz-server-side-encryption: "aws: kms"`.
- [ ] Enable Amazon Macie to monitor and act on changes to the data lake's S3 bucket.

### A recent security audit identified that a company's application team injects database credentials into the environment variables of an AWS Fargate task. The company's security policy mandates that all sensitive data be encrypted at rest and in transit. When combination of actions should the security team take to make the application compliant within the security policy? (Select THREE)

- [ ] Store the credentials securely in a file in an Amazon S3 bucket with restricted access to the application team IAM role Ask the application team to read the credentials from the S3 object instead.
- [x] Create an AWS Secrets Manager secret and specify the key/value pairs to be stored in this secret.
- [x] Modify the application to pull credentials from the AWS Secrets Manager secret instead of the environment variables.
- [ ] Add the following statement to the container instance IAM role policy.
- [x] Add the following statement to the execution role policy.
- [ ] Log in to the AWS Fargate instance, create a script to read the secret value from AWS Secret Manager, and inject the environment variables. Ask the application team to redeploy the application.

### A company is designing the securely architecture for a global latency-sensitive. Web application it plans to deploy to AWS. A Security Engineer needs to configure a highly available and secure two-tier architecture. The security design must include controls to prevent common attacks such as DDoS, cross-site scripting, and SQL injection. Which solution meets these requirements?

- [x] Create an Application Load Balancer (ALB) that uses public subnets across multiple Availability Zones within a single Region. Point the ALB to an Auto Scaling group with Amazon EC2 instances in private subnets across multiple Availability Zones within the same Region. Create an Amazon CloudFront distribution that uses the ALB as its origin. Create appropriate AWS WAF ACLs and enable them on the CloudFront distribution.
- [ ] Create an Application Load Balancer (ALB) that uses private subnets across multiple Availability Zones within a single Region. Point the ALB to an Auto Scaling group with Amazon EC2 instances in private subnets across multiple Availability Zones within the same Region. Create an Amazon CloudFront distribution that uses the ALB as its origin. Create appropriate AWS WAF ACLs and enable them on the CloudFront distribution.
- [ ] Create an Application Load Balancer (ALB) that uses public subnets across multiple Availability Zones within a single Region. Point the ALB to an Auto Scaling group with Amazon EC2 instances in private subnets across multiple Availability Zones within the same Region. Create appropriate AWS WAF ACLs and enable them on the ALB.
- [ ] Create an Application Load Balancer (ALB) that uses private subnets across multiple Availability Zones within a single Region. Point the ALB to an Auto Scaling group with Amazon EC2 instances in private subnets across multiple Availability Zones within the same Region. Create appropriate AWS WAF ACLs and enable them on the ALB.

### A company is running an application on Amazon EC2 instances in an Auto Scaling group. The application stores logs locally. A security engineer noticed that logs were lost after a scale-in event. The security engineer needs to recommend a solution to ensure the durability and availability of log data All logs must be kept for a minimum of 1 year for auditing purposes. What should the security engineer recommend?

- [ ] Within the Auto Scaling lifecycle, add a hook to create and attach an Amazon Elastic Block Store (Amazon EBS) log volume each time an EC2 instance is created. When the instance is terminated, the EBS volume can be reattached to another instance for log review.
- [ ] Create an Amazon Elastic File System (Amazon EFS) file system and add a command in the user data section of the Auto Scaling launch template to mount the EFS file system during EC2 instance creation Configure a process on the instance to copy the logs once a day from an instance Amazon Elastic Block Store (Amazon EBS) volume to a directory in the EFS file system.
- [x] Build the Amazon CloudWatch agent into the AMI used in the Auto Scaling group. Configure the CloudWatch agent to send the logs to Amazon CloudWatch Logs for review.
- [ ] Within the Auto Scaling lifecycle, add a lifecycle hook at the terminating state transition and alert the engineering team by using a lifecycle notification to Amazon Simple Notification Service (Amazon SNS). Configure the hook to remain in the Terminating: Wait state for 1 hour to allow manual review of the security logs prior to instance termination.

### A company has multiple production AWS accounts. Each account has AWS CloudTrail configured to log to a single Amazon S3 bucket in a central account. Two of the production accounts have trails that are not logging anything to the S3 bucket. Which steps should be taken to troubleshoot the issue? (Choose THREE)

- [ ] Verify that the log file prefix is set to the name of the S3 bucket where the logs should go.
- [x] Verify that the S3 bucket policy allows access for CloudTrail from the production AWS account IDs.
- [ ] Create a new CloudTrail configuration in the account, and configure it to log to the account's S3 bucket.
- [x] Confirm in the CloudTrail Console that each trail is active and healthy.
- [ ] Open the global CloudTrail configuration in the master account, and verify that the storage location is set to the correct S3 bucket.
- [x] Confirm in the CloudTrail Console that the S3 bucket name is set correctly.

### A company has a website with an Amazon CloudFront HTTPS distribution, an Application Load Balancer (ALB) with multiple Web instances for dynamic website content, and an Amazon S3 bucket for static website content. The company's security engineer recently updated the website security requirements: HTTPS needs to be enforced for all data in transit with specific ciphers. The CloudFront distribution needs to be accessible from the internet only. Which solution will meet these requirements?

- [ ] Set up an S3 bucket policy with the awssecuretransport key Configure the CloudFront origin access identity (OAI) with the S3 bucket Configure CloudFront to use specific ciphers. Enforce the ALB with an HTTPS listener only and select the appropriate security policy for the ciphers Link the ALB with AWS WAF to allow access from the CloudFront IP ranges.
- [x] Set up an S3 bucket policy with the `aws:securetransport` key. Configure the CloudFront origin access identity (OAI) with the S3 bucket. Enforce the ALB with an HTTPS listener only and select the appropriate security policy for the ciphers.
- [ ] Modify the CloudFront distribution to use AWS WAF. Force HTTPS on the S3 bucket with specific ciphers in the bucket policy. Configure an HTTPS listener only for the ALB. Set up a security group to limit access to the ALB from the CloudFront IP ranges.
- [ ] Modify the CloudFront distribution to use the ALB as the origin. Enforce an HTTPS listener on the ALB. Create a path-based routing rule on the ALB with proxies that connect to Amazon S3. Create a bucket policy to allow access from these proxies only.

### A company is trying to replace its on-premises bastion hosts used to access on-premises Linux servers with AWS Systems Manager Session Manager. A security engineer has installed the Systems Manager Agent on all servers. The security engineer verifies that the agent is running on all the servers, but Session Manager cannot connect to them. The security engineer needs to perform verification steps before Session Manager will work on the servers. Which combination of steps should the security engineer perform? (Select THREE)

- [ ] Open inbound port 22 to 0 0.0.0/0 on all Linux servers.
- [ ] Open inbound port 22 to 0 0.0.0/0 on all Linux servers.
- [x] Create a managed-instance activation for the on-premises servers.
- [x] Reconfigure the Systems Manager Agent with the activation code and ID.
- [x] Assign an IAM role to all of the on-premises servers.
- [ ] Initiate an inventory collection with Systems Manager on the on-premises servers.

### A company has recently recovered from a security incident that required the restoration of Amazon EC2 instances from snapshots. After performing a gap analysis of its disaster recovery procedures and backup strategies, the company is concerned that, next time, it will not be able to recover the EC2 instances if the AWS account was compromised and Amazon EBS snapshots were deleted. All EBS snapshots are encrypted using an AWS KMS CMK. Which solution would solve this problem?

- [ ] Create a new Amazon S3 bucket Use EBS lifecycle policies to move EBS snapshots to the new S3 bucket. Move snapshots to Amazon S3 Glacier using lifecycle policies, and apply Glacier Vault Lock policies to prevent deletion
- [ ] Use AWS Systems Manager to distribute a configuration that performs local backups of all attached disks to Amazon S3.
- [x] Create a new AWS account with limited privileges. Allow the new account to access the AWS KMS key used to encrypt the EBS snapshots, and copy the encrypted snapshots to the new account on a recuning basis.
- [ ] Use AWS Backup to copy EBS snapshots to Amazon S3.

### A Security Engineer manages AWS Organizations for a company. The Engineer would like to restrict AWS usage to allow Amazon S3 only in one of the organizational units (OUs). The Engineer adds the following SCP to the OU:

![Question 164](images/question164.png)

- [ ] Move the account to a new OU and deny IAM:* permissions.
- [ ] Add a Deny policy for all non-S3 services at the account level.
- [ ] Change the policy to:
![Question 164 option C](images/question164_C.png)
- [x] Detach the default FullAWSAccess SCP.

### A company has a serverless application for internal users deployed on AWS. The application uses AWS Lambda for the front end and for business logic. The Lambda function accesses an Amazon RDS database inside a VPC. The company uses AWS Systems Manager Parameter Store for storing database credentials. A recent security review highlighted the following issues. The Lambda function has internet access. The relational database is publicly accessible. The database credentials are not stored in an encrypted state. Which combination of steps should the company take to resolve these security issues? (Select THREE)

- [x] Disable public access to the RDS database inside the VPC.
- [x] Move all the Lambda functions inside the VPC.
- [ ] Edit the IAM role used by Lambda to restrict internet access.
- [ ] Create a VPC endpoint for Systems Manager. Store the credentials as a string parameter. Change the parameter type to an advanced parameter.
- [ ] Edit the IAM role used by RDS to restrict internet access.
- [x] Create a VPC endpoint for Systems Manager. Store the credentials as a Secure String parameter.

### A company has decided to migrate sensitive documents from on-premises data centers to Amazon S3. Currently, the hard drives are encrypted to meet a compliance requirement regarding data encryption. The CISO wants to improve security by encrypting each file using a different key instead of a single key. Using a different key would limit the security impact of a single exposed key. Which of the following requires the LEAST amount of configuration when implementing this approach?

- [ ] Place each file into a different S3 bucket. Set the default encryption of each bucket to use a different AWS KMS customer managed key.
- [ ] Put all the files in the same S3 bucket. Using S3 events as a trigger, write an AWS Lambda function to encrypt each file as it is added using different AWS KMS data keys.
- [ ] Use the S3 encryption client to encrypt each file individually using S3-generated data keys.
- [x] Place all the files in the same S3 bucket. Use server-side encryption with AWS KMS-managed keys (SSE-KMS) to encrypt the data.

### A company hosts a web-based application that captures and stores sensitive data in an Amazon DynamoDB table. A security audit reveals that the application does not provide end-to-end data protection or the ability to detect unauthorized data changes. The software engineering team needs to make changes that will address the audit findings. Which set of steps should the software engineering team take?

- [ ] Use an AWS Key Management Service (AWS KMS) CMK. Encrypt the data at rest.
- [ ] Use AWS Certificate Manager (ACM) Private Certificate Authority Encrypt the data in transit.
- [x] Use a DynamoDB encryption client. Use client-side encryption and sign the table items.
- [ ] Use the AWS Encryption SDK. Use client-side encryption and sign the table items.

### A company has a compliance requirement to rotate its encryption keys on an annual basis. A Security Engineer needs a process to rotate the KMS Customer Master Keys (CMKs) that were created using imported key material. How can the Engineer perform the key rotation process MOST efficiently?

- [x] Create a new CMK, and redirect the existing Key Alias to the new CMK.
- [ ] Select the option to auto-rotate the key.
- [ ] Upload new key material into the existing CMK.
- [ ] Create a new CMK, and change the application to point to the new CMK.

### A company's Developers plan to migrate their on-premises applications to Amazon EC2 instances running Amazon Linux AMIs. The applications are accessed by a group of partner companies. The Security Engineer needs to implement the following host-based security measures for these instances: Block traffic from documented known bad IP addresses. Detect known software vulnerabilities and CIS Benchmarks compliance. Which solution addresses these requirements?

- [ ] Launch the EC2 instances with an IAM role attached. Include a user data script that uses the AWS CLI to retrieve the list of bad IP addresses from AWS Secrets Manager and uploads it as a threat list in Amazon GuardDuty. Use Amazon Inspector to scan the instances for known software vulnerabilities and CIS Benchmarks compliance
- [ ] Launch the EC2 instances with an IAM role attached. Include a user data script that uses the AWS CLl to create NACLs blocking ingress traffic from the known bad IP addresses in the EC2 instance's subnets. Use AWS Systems Manager to scan the instances for known software vulnerabilities, and AWS Trusted Advisor to check instances for CIS Benchmarks compliance
- [ ] Launch the EC2 instances with an IAM role attached. Include a user data script that uses the AWS CLl to create and attach security groups that only allow an allow listed source IP address range inbound. Use Amazon Inspector to scan the instances for known software vulnerabilities, and AWS Trusted Advisor to check instances for CIS Benchmarks compliance
- [x] Launch the EC2 instances with an IAM role attached. Include a user data script that creates a cron job to periodically retrieve the list of bad IP addresses from Amazon S3, and configures iptabies on the instances blocking the list of bad IP addresses. Use Amazon inspector to scan the instances for known software vulnerabilities and CIS Benchmarks compliance.

### A Security Engineer noticed an anomaly within a company EC2 instance as shown in the image The Engineer must now investigate. What is causing the anomaly. What are the MOST effective steps to take to ensure that the instance is not further manipulated while allowing the Engineer to understand what happened?

![Question 170](images/question170.png)

- [ ] Remove the instance from the Auto Scaling group Place the instance within an isolation security group, detach the EBS volume launch an EC2 instance with a forensic toolkit and attach the E8S volume to investigate.
- [ ] Remove the instance from the Auto Scaling group and the Elastic Load Balancer Place the instance within an isolation security group, launch an EC2 instance with a forensic toolkit, and allow the forensic toolkit image to connect to the suspicious Instance to perform the Investigation.
- [ ] Remove the instance from the Auto Scaling group Place the Instance within an isolation security group, launch an EC2 Instance with a forensic toolkit and use the forensic toolkit imago to deploy an ENI as a network span port to inspect all traffic coming from the suspicious instance.
- [x] Remove the instance from the Auto Scaling group and the Elastic Load Balancer Place the instance within an isolation security group, make a copy of the EBS volume from a new snapshot, launch an EC2 Instance with a forensic toolkit and attach the copy of the EBS volume to investigate.

### A security engineer needs to configure monitoring and auditing for AWS Lambda. Which combination of actions using AWS services should the security engineer take to accomplish this goal? (Select TWO)

- [x] Use AWS Config to track configuration changes to Lambda functions, runtime environments, tags, handler names, code sizes, memory allocation, timeout settings, and concurrency settings, along with Lambda IAM execution role, subnet, and security group associations.
- [x] Use AWS CloudTrail to implement governance, compliance, operational, and risk auditing for Lambda.
- [ ] Use Amazon Inspector to automatically monitor for vulnerabilities and perform governance, compliance, operational, and risk auditing for Lambda.
- [ ] Use AWS Resource Access Manager to track configuration changes to Lambda functions, runtime environments, tags, handler names, code sizes, memory allocation, timeout settings, and concurrency settings, along with Lambda IAM execution role, subnet, and security group associations.
- [ ] Use Amazon Macie to discover, classify, and protect sensitive data being executed inside the Lambda function.

### A company has an AWS account and allows a third-party contractor who uses another AWS account, to assume certain IAM roles. The company wants to ensure that IAM roles can be assumed by the contractor only if the contractor has multi-factor authentication enabled on their IAM user accounts. What should the company do to accomplish this?

- [x] Add the following condition to the IAM policy attached to all IAM roles: `"Effect": "Deny", "Condition" : { "BoolItExists" : { "aws:MultiFactorAuthPresent" : false } }`.
- [ ] Add the following condition to the IAM policy attached to all IAM roles: `"Effect": "Deny", "Condition" : { "Bool" : { "aws:MultiFactorAuthPresent" : false } }`.
- [ ] Add the following condition to the IAM policy attached to all IAM roles: `"Effect": "Allow", "Condition" : { "Null" : { "aws:MultiFactorAuthPresent" : false } }`.
- [ ] Add the following condition to the IAM policy attached to all IAM roles: `"Effect": "Allow", "Condition" : { "BoolItExists" : { "aws:MultiFactorAuthPresent" : false } }`.

### A company uses Microsoft Active Directory for access management for on-premises resources and wants to use the same mechanism for accessing its AWS accounts. Additionally, the development team plans to launch a public-facing application for which they need a separate authentication solution. When coma nation of the following would satisfy these requirements? (Select TWO)

- [ ] Set up domain controllers on Amazon EC2 to extend the on-premises directory to AWS
- [ ] Establish network connectivity between on-premises and the user's VPC
- [x] Use Amazon Cognito user pools for application authentication
- [ ] Use AD Connector for application authentication.
- [x] Set up federated sign-in to AWS through ADFS and SAML.

### A company wants to encrypt data locally while meeting regulatory requirements related to key exhaustion. The encryption key can be no more than 10 days old or encrypt more than 2^16 objects Any encryption key must be generated on a FlPS-validated hardware security module (HSM). The company is cost-conscious, as plans to upload an average of 100 objects to Amazon S3 each second for sustained operations across 5 data producers. When approach MOST efficiently meets the company's needs?

- [ ] Use the AWS Encryption SDK and set the maximum age to 10 days and the minimum number of messages encrypted to 3^16. Use AWS Key Management Service (AWS KMS) to generate the master key and data key Use data key caching with the Encryption SDk during the encryption process.
- [ ] Use AWS Key Management Service (AWS KMS) to generate an AWS managed CMK. Then use Amazon S3 client-side encryption configured to automatically rotate with every object.
- [x] Use AWS CloudHSM to generate the master key and data keys. Then use Boto 3 and
Python to locally encrypt data before uploading the object Rotate the data key every 10 days or after 2^16 objects have been Uploaded to Amazon 33.
- [ ] Use server-side encryption with Amazon S3 managed encryption keys (SSE-S3) and set the master key to automatically rotate.

### A company plans to use custom AMIs to launch Amazon EC2 instances across multiple AWS accounts in a single Region to perform security monitoring and analytics tasks. The EC2 instances are launched in EC2 Auto Scaling groups. To increase the security of the solution, a Security Engineer will manage the lifecycle of the custom AMIs in a centralized account and will encrypt them with a centrally managed AWS KMS CMK. The Security Engineer configured the KMS key policy to allow cross-account access. However, the EC2 instances are still not being properly launched by the EC2 Auto Scaling groups. Which combination of configuration steps should the Security Engineer take to ensure the EC2 Auto Scaling groups have been granted the proper permissions to execute tasks?

- [ ] Create a customer-managed CMK in the centralized account. Allow other applicable accounts to use that key for cryptographical operations by applying proper cross-account permissions in the key policy. Create an IAM role in all applicable accounts and configure its access policy to allow the use of the centrally managed CMK for cryptographical operations. Configure EC2 Auto Scaling groups within each applicable account to use the created IAM role to launch EC2 instances.
- [x] Create a customer-managed CMK in the centralized account. Allow other applicable accounts to use that key for cryptographical operations by applying proper cross-account permissions in the key policy. Create an IAM role in all applicable accounts and configure its access policy with permissions to create grants for the centrally managed CMK. Use this IAM role to create a grant for the centrally managed CMK with permissions to perform cryptographical operations and with the EC2 Auto Scaling service-linked role defined as the grantee principal.
- [ ] Create a customer-managed CMK or an AWS managed CMK in the centralized account. Allow other applicable accounts to use that key for cryptographical operations by applying proper cross-account permissions in the key policy. Use the CMK administrator to create a CMK grant that includes permissions to perform cryptographical operations that define EC2 Auto Scaling service-linked roles from all other accounts as the grantee principal.
- [ ] Create a customer-managed CMK or an AWS managed CMK in the centralized account. Allow other applicable accounts to use that key for cryptographical operations by applying proper cross-account permissions in the key policy. Modify the access policy for the EC2 Auto Scaling roles to perform cryptographical operations against the centrally managed CMK.

### A security engineer is designing a solution that will provide end-to-end encryption between clients and Docker containers running In Amazon Elastic Container Service (Amazon ECS). This solution will also handle volatile traffic patterns. Which solution would have the MOST scalability and LOWEST latency?

- [ ] Configure a Network Load Balancer to terminate the TLS traffic and then re-encrypt the traffic to the containers.
- [ ] Configure an Application Load Balancer to terminate the TLS traffic and then re-encrypt the traffic to the containers.
- [x] Configure a Network Load Balancer with a TCP listener to pass through TLS traffic to the containers.
- [ ] Configure Amazon Route 53 to use multivalue answer routing to send traffic to the containers.

### A security engineer has noticed an unusually high amount of traffic coming from a single IP address. This was discovered by analyzing the Application Load Balancer's access logs. How can the security engineer limit the number of requests from a specific IP address without blocking the IP address?

- [ ] Add a rule to the Application Load Balancer to route the traffic originating from the IP address in question and show a static webpage.
- [x] Implement a rate-based rule with AWS WAF.
- [ ] Use AWS Shield to limit the originating traffic hit rate.
- [ ] Implement the GeoLocation feature in Amazon Route 53.

### A Security Engineer has several thousand Amazon EC2 instances split across production and development environments. Each instance is tagged with its environment. The Engineer needs to analyze and patch all the development EC2 instances to ensure they are not currently exposed to any common vulnerabilities or exposures (CVEs). Which combination of steps is the MOST efficient way for the Engineer to meet these requirements? (Select TWO)

- [ ] Log on to each EC2 instance, check and export the different software versions installed, and verify this against a list of current CVEs.
- [ ] Install the Amazon Inspector agent on all development instances. Build a custom rule package, and configure Inspector to perform a scan using this custom rule on all instances tagged as being in the development environment.
- [x] Install the Amazon Inspector agent on all development instances. Configure Inspector to perform a scan using the CVE rule package on all instances tagged as being in the development environment.
- [x] Install the Amazon EC2 System Manager agent on all development instances. Issue the Run command to EC2 System Manager to update all instances.
- [ ] Use AWS Trusted Advisor to check that all EC2 instances have been patched to the most recent version of operating system and installed software.

### An application running on Amazon EC2 instances generates log files in a folder on a Linux file system. The instances block access to the console and file transfer utilities, such as Secure Copy Protocol (SCP) and Secure File Transfer Protocol (SFTP). The Application Support team wants to automatically monitor the application log files so the team can set up notifications in the future. A Security Engineer must design a solution that meets the following requirements: Make the log files available through an AWS managed service. Allow for automatic monitoring of the logs. Provide an Interlace for analyzing logs. Minimize effort. Which approach meets these requirements?

- [ ] Modify the application to use the AWS SDK. Write the application logs to an Amazon S3 bucket.
- [x] Install the unified Amazon CloudWatch agent on the instances. Configure the agent to collect the application log files on the EC2 file system and send them to Amazon CloudWatch Logs.
- [ ] Install AWS Systems Manager Agent on the instances. Configure an automation document to copy the application log files to AWS DeepLens.
- [ ] Install Amazon Kinesis Agent on the instances. Stream the application log files to Amazon Kinesis Data Firehose and set the destination to Amazon Elasticsearch Service.

### To meet regulatory requirements, a Security Engineer needs to implement an IAM policy that restricts the use of AWS services to the `us-east-1` Region. What policy should the Engineer implement?

- [ ] Option A.
![Question 180 option A](images/question180_A.png)
- [ ] Option B.
![Question 180 option B](images/question180_B.png)
- [x] Option C.
![Question 180 option C](images/question180_C.png)
- [ ] Option D.
![Question 180 option D](images/question180_D.png)

### A company has a VPC with an IPv6 address range and a public subnet with an IPv6 address block. The VPC currently hosts some public Amazon EC2 instances but a Security Engineer needs to migrate a second application into the VPC that also requires IPv6 connectivity. This new application will occasionally make API requests to an external, internet-accessible endpoint to receive updates However, the Security team does not want the application's EC2 instance exposed directly to the internet The Security Engineer intends to create a private subnet with a custom route table and to associate the route table with the private subnet. What else does the Security Engineer need to do to ensure the application will not be exposed directly to the internet, but can still communicate as required.

- [ ] Launch a NAT instance in the public subnet Update the custom route table with a new
route to the NAT instance.
- [ ] Remove the internet gateway, and add AWS PrivateLink to the VPC Then update the custom route table with a new route to AWS PrivateLink.
- [ ] Add a managed NAT gateway to the VPC Update the custom route table with a new route to the gateway.
- [x] Add an egress-only internet gateway to the VPC. Update the custom route table with a new route to the gateway.

### A Security Engineer accidentally deleted the imported key material in an AWS KMS CMK. What should the Security Engineer do to restore the deleted key material?

- [ ] Create a new CMK. Download a new wrapping key and a new import token to import the original key material.
- [ ] Create a new CMK Use the original wrapping key and import token to import the original key material.
- [x] Download a new wrapping key and a new import token Import the original key material into the existing CMK.
- [ ] Use the original wrapping key and import token Import the original key material into the existing CMK.

### Authorized Administrators are unable to connect to an Amazon EC2 Linux bastion host using SSH over the internet. The connection either fails to respond or generates the following error message: `Network error: Connection timed out`. What could be responsible for the connection failure? (Select THREE)

- [ ] The NAT gateway in the subnet where the EC2 instance is deployed has been misconfigured.
- [x] The internet gateway of the VPC has been reconfigured.
- [ ] The security group denies outbound traffic on ephemeral ports.
- [x] The route table is missing a route to the internet gateway.
- [ ] The NACL denies outbound traffic on ephemeral ports.
- [x] The host-based firewall is denying SSH traffic.

### A company is setting up products to deploy in AWS Service Catalog. Management is concerned that when users launch products, elevated IAM privileges will be required to create resources. How should the company mitigate this concern?

- [ ] Add a template constraint to each product in the portfolio.
- [x] Add a launch constraint to each product in the portfolio.
- [ ] Define resource update constraints for each product in the portfolio.
- [ ] Update the AWS CloudFormalion template backing the product to include a service role configuration.

### A company is configuring three Amazon EC2 instances with each instance in a separate Availability Zone. The EC2 instances wilt be used as transparent proxies for outbound internet traffic for ports 80 and 443 so the proxies can block traffic to certain internet destinations as required by the company's security policies. A Security Engineer completed the following: Set up the proxy software on the EC2 instances. Modified the route tables on the private subnets to use the proxy EC2 instances as the default route. Created a security group rule opening inbound port 80 and 443 TCP protocols on the proxy EC2 instance security group. However, the proxy EC2 instances are not successfully forwarding traffic to the internet. What should the Security Engineer do to make the proxy EC2 instances route traffic to the internet?

- [ ] Put all the proxy EC2 instances in a cluster placement group.
- [x] Disable source and destination checks on the proxy EC2 instances.
- [ ] Open all inbound ports on the proxy EC2 instance security group.
- [ ] Change the VPC's DHCP domain-name-servers options set to the IP addresses of proxy EC2 instances.

### A financial institution has the following security requirements: Cloud-based users must be contained in a separate authentication domain. Cloud-based users cannot access on-premises systems. As part of standing up a cloud environment, the financial institution is creating a number of Amazon managed databases and Amazon EC2 instances. An Active Directory service exists on-premises that has all the administrator accounts, and these must be able to access the databases and instances. How would the organization manage its resources in the MOST secure manner? (Choose TWO)

- [x] Configure an AWS Managed Microsoft AD to manage the cloud resources.
- [ ] Configure an additional on-premises Active Directory service to manage the cloud resources.
- [ ] Establish a one-way trust relationship from the existing Active Directory to the new Active Directory service.
- [x] Establish a one-way trust relationship from the new Active Directory to the existing Active Directory service.
- [ ] Establish a two-way trust between the new and existing Active Directory services.

### An application developer is using an AWS Lambda function that must use AWS KMS to perform encrypt and decrypt operations for API keys that are less than 2 KB. Which key policy would allow the application to do this while granting least privilege?

- [ ] Option A.
![Question 187 option A](images/question187_A.png)
- [x] Option B.
![Question 187 option B](images/question187_B.png)
- [ ] Option C.
![Question 187 option C](images/question187_C.png)
- [ ] Option D.
![Question 187 option D](images/question187_D.png)

### A Developer is creating an AWS Lambda function that requires environment variables to store connection information and logging settings. The Developer is required to use an AWS KMS Customer Master Key (CMK) supplied by the Information Security department in order to adhere to company standards for securing Lambda environment variables. Which of the following are required for this configuration to work? (Choose two.)

- [ ] The Developer must configure Lambda access to the VPC using the `--vpc-config` parameter.
- [x] The Lambda function execution role must have the kms:Decrypt permission added in the AWS IAM policy.
- [x] The KMS key policy must allow permissions for the Developer to use the KMS key.
- [ ] The AWS IAM policy assigned to the Developer must have the kms:GenerateDataKey permission added.
- [ ] The Lambda execution role must have the kms:Encrypt permission added in the AWS IAM policy.

### A Developer is building a serverless application that uses Amazon API Gateway as the front end. The application will not be publicly accessible. Other legacy applications running on Amazon EC2 will make calls to the application A Security Engineer Has been asked to review the security controls for authentication and authorization of the application. Which combination of actions would provide the MOST secure solution? (Select TWO)

- [x] Configure an IAM policy that allows the least permissive actions to communicate with the API Gateway Attach the policy to the role used by the legacy EC2 instances.
- [ ] Enable AWS WAF for API Gateway Configure rules to explicitly allow connections from the legacy EC2 instances.
- [x] Create a VPC endpoint for API Gateway Attach an IAM resource policy that allows the role of the legacy EC2 instances to call specific APIs.
- [ ] Create a usage plan Generate a set of API keys for each application that needs to call the API.
- [ ] Create a usage plan Generate a set of API keys for each application that needs to call the API.

### A company has an encrypted Amazon S3 bucket. An Application Developer has an IAM policy that allows access to the S3 bucket, but the Application Developer is unable to access objects within the bucket. What is a possible cause of the issue?

- [ ] The S3 ACL for the S3 bucket fails to explicitly grant access to the Application Developer.
- [ ] The AWS KMS key for the S3 bucket fails to list the Application Developer as an administrator.
- [ ] The S3 bucket policy fails to explicitly grant access to the Application Developer.
- [x] The S3 bucket policy explicitly denies access to the Application Developer.

### A company's web application is hosted on Amazon EC2 instances running behind an Application Load Balancer (ALB) in an Auto Scaling group. An AWS WAF web ACL is associated with the ALB. AWS CloudTrail is enabled, and stores logs in Amazon S3 and Amazon CloudWatch Logs. The operations team has observed some EC2 instances reboot at random. After rebooting, all access logs on the instances have been deleted. During an investigation, the operations team found that each reboot happened just after a PHP error occurred on the new-user-creation.php file. The operations team needs to view log information to determine if the company is being attacked. Which set of actions will identify the suspect attacker's IP address for future occurrences?

- [ ] Configure VPC Flow Logs on the subnet where the ALB is located, and stream the data CloudWatch. Search for the new-user-creation.php occurrences in CloudWatch.
- [ ] Configure the CloudWatch agent on the ALB Configure the agent to send application logs to CloudWatch Update the instance role to allow CloudWatch Logs access. Export the logs to CloudWatch Search for the new-user-creation.php occurrences in CloudWatch.
- [ ] Configure the ALB to export access logs to an Amazon Elasticsearch Service cluster, and use the service to search for the new-user-creation.php occurrences.
- [x] Configure the Web ACL to send logs to Amazon Kinesis Data Firehose, which delivers the logs to an S3 bucket Use Amazon Athena to query the logs and find the new-user-creation php occurrences.

### After a recent security audit involving Amazon S3, a company has asked assistance reviewing its S3 buckets to determine whether data is properly secured. The first S3 bucket on the list has the following bucket policy. Is this bucket policy sufficient to ensure that the data is not publicity accessible?

![Question 192](images/question192.jpg)

- [ ] Yes, the bucket policy makes the whole bucket publicly accessible despite now the S3 bucket ACL or object ACLs are configured.
- [ ] Yes, none of the data in the bucket is publicity accessible, regardless of how the S3 bucket ACL and object ACLs are configured.
- [ ] No, the IAM user policy would need to be examined first to determine whether any data is publicly accessible.
- [x] No, the S3 bucket ACL and object ACLs need to be examined first to determine whether any data is publicly accessible.

### A company's security engineer is configuring Amazon S3 permissions to ban all current and future public buckets However, the company hosts several websites directly off S3 buckets with public access enabled. The engineer needs to bock me pubic S3 buckets without causing any outages on me easting websites. The engineer has set up an Amazon CloudFrom distribution or each website. Which set or steps should the security engineer implement next?

- [x] Configure an S3 bucket as the origin an origin access identity (OAI) for the CloudFront distribution. Switch the DNS records from websites to point to the CloudFront distribution. Enable Lock public access settings at the account level.
- [ ] Configure an S3 bucket as the origin with an origin access identity (OAI) for the CloudFront distribution. Switch the DNS records for the websites to point to the CloudFront disinfection. Then, for each S3 bucket enable block public access settings.
- [ ] Configure an S3 bucket as the origin with an origin access identity (OAI) for the CloudFront distribution. Enable block public access settings at the account level.
- [ ] Configure an S3 bucket as the origin for me CloudFront distribution. Configure the S3 bucket policy to accept connections from the CloudFront points of presence only. Switch the DNS records for the websites to point to the CloudFront distribution Enable block public access settings at me account level.

### An application is currently secured using network access control lists and security groups. Web servers are located in public subnets behind an Application Load Balancer (ALB); application servers are located in private subnets. How can edge security be enhanced to safeguard the Amazon EC2 instances against attack? (Choose TWO)

- [ ] Configure the application's EC2 instances to use NAT gateways for all inbound traffic.
- [x] Move the Web servers to private subnets without public IP addresses.
- [x] Configure AWS WAF to provide DDoS attack protection for the ALB.
- [ ] Require all inbound network traffic to route through a bastion host in the private subnet.
- [ ] Require all inbound and outbound network traffic to route through an AWS Direct Connect connection.

### A company wants to encrypt the private network between its orvpremises environment and AWS. The company also wants a consistent network experience for its employees. What should the company do to meet these requirements?

- [ ] Establish an AWS Direct Connect connection with AWS and set up a Direct Connect gateway. In the Direct Connect gateway configuration, enable IPsec and BGP, and then leverage native AWS network encryption between Availability Zones and Regions.
- [ ] Establish an AWS Direct Connect connection with AWS and set up a Direct Connect gateway. Using the Direct Connect gateway, create a private virtual interface and advertise the customer gateway private IP addresses. Create a VPN connection using the customer gateway and the virtual private gateway.
- [ ] Establish a VPN connection with the AWS virtual private cloud over the internet.
- [x] Establish an AWS Direct Connect connection with AWS and establish a public virtual interface. For prefixes that need to be advertised, enter the customer gateway public IP addresses. Create a VPN connection over Direct Connect using the customer gateway and the virtual private gateway.

### A company has decided to use encryption in its AWS account to secure the objects in Amazon S3 using server-side encryption. Object sizes range from 16.000 B to 5 MB. The requirements are as follows. The key material must be generated and stored in a certified Federal Information Processing Standard (FIPS) 140-2 Level 3 machine. The key material must be available in multiple Regions. Which option meets these requirements?

- [x] Use an AWS KMS customer managed key and store the key material in AWS with replication across Regions.
- [ ] Use an AWS customer managed key, import the key material into AWS KMS using in-house AWS CloudHSM. and store the key material securely in Amazon S3.
- [ ] Use an AWS KMS custom key store backed by AWS CloudHSM clusters, and copy backups across Regions.
- [ ] Use AWS CloudHSM to generate the key material and backup keys across Regions Use the Java Cryptography Extension (JCE) and Public Key Cryptography Standards #11 (PKCS #11) encryption libraries to encrypt and decrypt the data.

### A global company that deals with International finance is investing heavily in cryptocurrencies and wants to experiment with mining technologies using AWS. The company's security team has enabled Amazon GuardDuty and is concerned by the number of findings being generated by the accounts. The security team wants to minimize the possibility of GuardDuty finding false negatives for compromised instances that are performing mining How can the security team continue using GuardDuty while meeting these requirements?

- [ ] In the GuardDuty console, select the CryptoCurrency:EC2/BitcoinTool B'DNS finding and use the suppress findings option.
- [ ] Create a custom AWS Lambda function to process newly detected GuardDuty alerts Process the CryptoCurrency EC2/BitcoinTool BIDNS alert and filter out the high-severity finding types only.
- [ ] When creating a new Amazon EC2 Instance, provide the instance with a specific tag that indicates it is performing mining operations Create a custom AWS Lambda function to process newly detected GuardDuty alerts and filter for the presence of this tag.
- [x] When GuardDuty produces a cryptocurrency finding, process the finding with a custom AWS Lambda function to extract the instance ID from the finding Then use the AWS Systems Manager Run Command to check for a running process performing mining operations.

### A security engineer must use AWS Key Management Service (AWS KMS) to design a key management solution for a set of Amazon Elastic Block Store (Amazon EBS) volumes that contain sensitive data. The solution needs to ensure that the key material automatically expires in 90 days. Which solution meets these criteria?

- [x] A customer managed CMK that uses customer provided key material.
- [ ] A customer managed CMK that uses AWS provided key material.
- [ ] An AWS managed CMK.
- [ ] Operating system-native encryption that uses GnuPG.

### A company's application runs on Amazon EC2 and stores data in an Amazon S3 bucket. The company wants additional security controls in place to limit the likelihood of accidental exposure of data to external parties. Which combination of actions will meet this requirement? (Select THREE)

- [ ] Encrypt the data in Amazon S3 using server-side encryption with Amazon S3 managed encryption keys (SSE-S3)
- [x] Encrypt the data in Amazon S3 using server-side encryption with AWS KMS managed encryption keys (SSE-KMS)
- [ ] Create a new Amazon S3 VPC endpoint and modify the VPC's routing tables to use the new endpoint.
- [x] Use the Amazon S3 Block Public Access feature.
- [x] Configure the bucket policy to allow access from the application instances only.
- [ ] Use a NACL to filter traffic to Amazon S3.

### A company's application runs on an Amazon EC2 instance and stores objects in an Amazon S3 bucket. The EC2 instance is using an instance profile that provides access to read and write objects in the S3 bucket. The S3 bucket contains objects and has not been configured for any encryption at rest. The company is adopting a new security policy that mandates encryption at rest for all S3 buckets, encryption at rest for all objects in S3 buckets, and key rotation once every year. What should a security engineer do to meet these requirements?

- [ ] Enable server-side encryption with Amazon S3 managed encryption keys (SSE-S3) for the S3 bucket. Configure annual automatic key rotation. Use an S3 Batch Operations job with the COPY command to change all the objects in the S3 bucket to use the SSE-S3 key. Configure the EC2 instance profile with permissions to use the SSE-S3 key. Configure S3 data events to encrypt an object during a write operation.
- [ ] Create a new AWS Key Management Service (AWS KMS) customer managed key. Configure annual automatic key rotation. Enable server-side encryption with AWS KMS keys (SSE-KMS) for the S3 bucket. Add a bucket policy to the S3 bucket to enforce SSE-KMS encryption. Configure the EC2 instance profile with permissions to use the customer managed key.
- [x] Create a new AWS Key Management Service (AWS KMS) customer managed key. Configure annual automatic key rotation. Enable server-side encryption with AWS KMS keys (SSE-KMS) for the S3 bucket. Use an S3 Batch Operations job with the COPY command to change all the objects in the S3 bucket to use the customer managed key. Configure the EC2 instance profile with permissions to use the customer managed key.
- [ ] Enable server-side encryption with Amazon S3 managed encryption keys (SSE-S3) for the S3 bucket. Configure annual automatic key rotation. Configure the EC2 instance profile with permissions to use the SSE-S3 key. Use the AWS CLI to copy the S3 objects in place by specifying the SSE-S3 key as the encryption key. Configure S3 data events to encrypt an object during a write operation.

### A Security Administrator at a university is configuring a fleet of Amazon EC2 instances. The EC2 instances are shared among students, and non-root SSH access is allowed. The Administrator is concerned about students attacking other AWS account resources by using the EC2 instance metadata service. What can the Administrator do to protect against this potential attack?

- [ ] Disable the EC2 instance metadata service.
- [ ] Log all student SSH interactive session activity.
- [x] Implement iptables-based restrictions on the instances.
- [ ] Install the Amazon Inspector agent on the instances.

### An employee accidentally exposed an AWS access key and secret access key during a public presentation. The company Security Engineer immediately disabled the key. How can the Engineer assess the impact of the key exposure and ensure that the credentials were not misused? (Choose TWO)

- [x] Analyze AWS CloudTrail for activity.
- [ ] Analyze Amazon CloudWatch Logs for activity.
- [ ] Download and analyze the IAM Use report from AWS Trusted Advisor.
- [ ] Analyze the resource inventory in AWS Config for IAM user activity.
- [x] Download and analyze a credential report from IAM.

### A company has several production AWS accounts and a central security AWS account. The security account is used for centralized monitoring and has IAM privileges to all resources in every corporate account. All of the company's Amazon S3 buckets are tagged with a value denoting the data classification of their contents. A Security Engineer is deploying a monitoring solution in the security account that will enforce bucket policy compliance. The system must monitor S3 buckets in all production accounts and confirm that any policy change is in accordance with the bucket's data classification. If any change is out of compliance; the Security team must be notified quickly. Which combination of actions would build the required solution? (Choose THREE)

- [x] Configure Amazon CloudWatch Events in the production accounts to send all S3 events to the security account event bus.
- [ ] Enable Amazon GuardDuty in the security account. and join the production accounts as members.
- [x] Configure an Amazon CloudWatch Events rule in the security account to detect S3 bucket creation or modification events.
- [ ] Enable AWS Trusted Advisor and activate email notifications for an email address assigned to the security contact.
- [x] Invoke an AWS Lambda function in the security account to analyze S3 bucket settings in response to S3 events, and send non-compliance notifications to the Security team.
- [ ] Configure event notifications on S3 buckets for PUT; POST, and DELETE events.

### A security engineer is auditing a production system and discovers several additional IAM roles that are not required and were not previously documented during the last audit 90 days ago. The engineer is trying to find out who created these IAM roles and when they were created. The solution must have the lowest operational overhead. Which solution will meet this requirement?

- [ ] Import AWS CloudTrail logs from Amazon S3 into an Amazon Elasticsearch Service cluster, and search through the combined logs for CreateRole events.
- [ ] Create a table in Amazon Athena for AWS CloudTrail events. Query the table in Amazon Athena for CreateRole events.
- [x] Use AWS Config to look up the configuration timeline for the additional IAM roles and view the linked AWS CloudTrail event.
- [ ] Download the credentials report from the IAM console to view the details for each IAM entity, including the creation dates.

### A company has a new AWS account that does not have AWS CloudTrail configured. The account has an IAM access key that was issued by AWS Security Token Service (AWS STS). A security engineer discovers that the IAM access key has been compromised within the last 24 hours. The security engineer must stop the compromised IAM access key from being used. The security engineer also must determine which activities the key has been used for so far. What should the security engineer do to meet these requirements?

- [ ] In the CloudTrail console, under CloudTrail event history, search by access key for the compromised key, with the correlated events, and identify which IAM user the key belongs to. In the IAM console, revoke all active sessions for that IAM user.
- [ ] Create a new CloudTrail trail. In the CloudTrail console, under CloudTrail event history, search by access key for the compromised key, view the correlated events, and identify which IAM user the key belongs to. In the IAM console, revoke all active sessions for that IAM user.
- [ ] Create a new CloudTrail trail. In the CloudTrail console, under CloudTrail event history, search by access key for the compromised key, view the correlated events, and identify which IAM role the key belongs to. In the IAM console, delete that IAM role.
- [x] In the CloudTrail console, under CloudTrail event history, search by access key for the compromised key, view the correlated events, and identify which IAM role the key belongs to. In the IAM console, revoke all active sessions for that IAM role.

### After multiple compromises of its Amazon EC2 instances, a company's Security Officer is mandating that memory dumps of compromised instances be captured for further analysis. A Security Engineer just received an EC2 abuse notification report from AWS stating that an EC2 instance running the most recent. Windows Server 2019 Base AMI is compromised. How should the Security Engineer collect a memory dump of the EC2 instance for forensic analysis?

- [ ] Give consent to the AWS Security team to dump the memory core on the compromised instance and provide it to AWS Support for analysis.
- [ ] Review memory dump data that the AWS Systems Manager Agent sent to Amazon CloudWatch Logs.
- [x] Download and run the EC2Rescue for Windows Server utility from AWS.
- [ ] Reboot the EC2 Windows Server, enter safe mode, and select memory dump.

### A Security Engineer received an AWS Abuse Notice listing EC2 instance IDs that are reportedly abusing other hosts. Which action should the Engineer take based on this situation? (Choose three.)

- [ ] Use AWS Artifact to capture an exact image of the state of each instance.
- [x] Create EBS Snapshots of each of the volumes attached to the compromised instances.
- [x] Capture a memory dump.
- [ ] Log in to each instance with administrative credentials to restart the instance.
- [x] Revoke all network ingress and egress except for to/from a forensics workstation.
- [ ] Run Auto Recovery for Amazon EC2.

### A company had one of its Amazon EC2 key pairs compromised. A Security Engineer must identify which current Linux EC2 instances were deployed and used the compromised key pair. How can this task be accomplished?

- [x] Obtain the list of instances by directly querying Amazon EC2 using: `aws ec2 describe-instances –fi1ters "Name=key-name,Values=KEYNAMEHERE"`.
- [ ] Obtain the fingerprint for the key pair from the AWS Management Console, then search for the fingerprint in the Amazon Inspector logs.
- [ ] Obtain the output from the EC2 instance metadata using: `curl http: //169.254.169.254/latest/meta-data/public- keys/0/`.
- [ ] Obtain the fingerprint for the key pair from the AWS Management Console, then search for the fingerprint in Amazon CloudWatch Logs using: `aws logs filter-log-events`.

### A security engineer must develop an encryption tool for a company. The company requires a cryptographic solution that supports the ability to perform cryptographic erasure on all resources protected by the key material in 15 minutes or less. Which AWS Key Management Service (AWS KMS) key solution will allow the security engineer to meet these requirements?

- [x] Use imported key material with CMK.
- [ ] Use an AWS KMS CMK.
- [ ] Use an AWS managed CMK.
- [ ] Use an AWS KMS customer managed CMK.

### A company plans to use AWS Key Management Service (AWS KMS) to implement an encryption strategy to protect data at rest. The company requires client-side encryption for company projects. The company is currently conducting multiple projects to test the company's use of AWS KMS. These tests have led to a sudden increase in the company's AWS resource consumption. The test projects include applications that issue multiple requests each second to KMS endpoints for encryption activities. The company needs to develop a solution that does not throttle the company's ability to use AWS KMS. The solution must improve key usage for client-side encryption and must be cost optimized. Which solution will meet these requirements?

- [ ] Use keyrings with the AWS Encryption SDK. Use each keyring individually or combine keyrings into a multi-keyring. Decrypt the data by using a keyring that has the primary key in the multi-keyring.
- [x] Use data key caching. Use the local cache that the AWS Encryption SDK provides with a caching cryptographic materials manager.
- [ ] Use KMS key rotation. Use a local cache in the AWS Encryption SDK with a caching cryptographic materials manager.
- [ ] Use keyrings with the AWS Encryption SDK. Use each keyring individually or combine keyrings into a multi-keyring. Use any of the wrapping keys in the multi-keyring to decrypt the data.

### A company is using AWS Organizations to manage multiple AWS member accounts. All of these accounts have Amazon GuardDuty enabled in all Regions. The company's AW5 Security Operations Center has a centralized security account for logging and monitoring. One of the member accounts has received an excessively high bill A security engineer discovers that a compromised Amazon EC2 instance is being used to mine crypto currency. The Security Operations Center did not receive a GuardDuty finding in the central security account. but there was a GuardDuty finding in the account containing the compromised EC2 instance. The security engineer needs to ensure an GuardDuty finding are available in the security account. What should the security engineer do to resolve this issue?

- [ ] Set up an Amazon CloudWatch Event rule to forward ail GuardDuty findings to the security account Use an AWS Lambda function as a target to raise findings.
- [ ] Set up an Amazon CloudWatch Events rule to forward all GuardDuty findings to the security account Use an AWS Lambda function as a target to raise findings in AWS Security Hub.
- [ ] Check that GuardDuty in the security account is able to assume a role in the compromised account using the GuardDuty fast findings permission Schedule an Amazon CloudWatch Events rule and an AWS Lambda function to periodically check for GuardDuty findings.
- [x] Use the aws GuardDuty `get-members` AWS CLI command m the security account to see if the account is listed Send an invitation from GuardDuty m the security account to GuardDuty in the compromised account Accept the invitation to forward all future GuardDuty findings.

### A company's on-premises data center forwards DNS logs to a third-party security incident events management (SIEM) solution that alerts on suspicious behavior. The company wants to introduce a similar capability to its AWS accounts that includes automatic remediation. The company expects to double in size within the next few months. Which solution meets the company's current and future logging requirements?

- [x] Enable Amazon GuardDuty and AWS Security Hub in all Regions and all accounts. Designate a master security account to receive all alerts from the child accounts. Set up specific rules within Amazon EventBridge to trigger an AWS Lambda function for remediation steps.
- [ ] Ingest all AWS CloudTrail logs, VPC Flow Logs, and DNS logs into a single Amazon S3 bucket in a designated security account. Use the current on-premises SIEM to monitor the logs and send a notification to an Amazon SNS topic to alert the security team of remediation steps.
- [ ] Ingest all AWS CloudTrail logs, VPC Flow Logs, and DNS logs into a single Amazon S3 bucket in a designated security account. Launch an Amazon EC2 instance and install the current SIEM to monitor the logs and send a notification to an Amazon SNS topic to alert the security team of remediation steps.
- [ ] Enable Amazon GuardDuty and AWS Security Hub in all Regions and all accounts. Designate a master security account to receive all alerts from the child accounts. Create an AWS Organizations SCP that denies access to certain API calls that are on an ignore list.

### An external auditor finds that a company's user passwords have no minimum length. The company is currently using two identity providers: AWS IAM federated with on-premises Active Directory. Amazon Cognito user pools to accessing an AWS Cloud application developed by the company. Which combination o1 actions should the Security Engineer take to solve this issue? (Select TWO)

- [x] Update the password length policy in the on-premises Active Directory configuration.
- [ ] Update the password length policy in the IAM configuration.
- [ ] Enforce an IAM policy in Amazon Cognito and AWS IAM with a minimum password length condition.
- [x] Update the password length policy in the Amazon Cognito configuration.
- [ ] Create an SCP with AWS Organizations that enforces a minimum password length for AWS IAM and Amazon Cognito.

### A Developer signed in to a new account within an AWS Organizations organizations unit (OU) containing multiple accounts. Access to the Amazon S3 service is restricted with the following SCP: How can the Security Engineer provide the Developer with Amazon S3 access without affecting other accounts?

![Question 214](images/question214.png)

- [ ] Move the SCP to the root OU of Organizations to remove the restriction to access Amazon S3.
- [ ] Add an IAM policy for the Developer, which grants S3 access.
- [x] Create a new OU without applying the SCP restricting S3 access. Move the Developer account to this new OU.
- [ ] Add an allow list for the Developer account for the S3 service.

### A company's development team is designing an application using AWS Lambda and Amazon Elastic Container Service (Amazon ECS). The development team needs to create IAM roles to support these systems. The company's security team wants to allow the developers to build IAM roles directly, but the security team wants to retain control over the permissions the developers can delegate to those roles. The development team needs access to more permissions than those required for the application's AWS services. The solution must minimize management overhead. How should the security team prevent privilege escalation for both teams?

- [ ] Enable AWS CloudTrail. Create a Lambda function that monitors the event history for privilege escalation events and notifies the security team.
- [x] Create a managed IAM policy for the permissions required. Reference the IAM policy as a permissions boundary within the development team's IAM role.
- [ ] Enable AWS Organizations Create an SCP that allows the IAM CreateUser action but that has a condition that prevents API calls other than those required by the development team.
- [ ] Create an IAM policy with a deny on the IAMCreateUser action and assign the policy to the development team. Use a ticket system to allow the developers to request new IAM roles for their applications. The IAM roles will then be created by the security team.

### A company that uses AWS Organizations is migrating workloads to AWS. The company's application team determines that the workloads will use Amazon EC2 instances, Amazon S3 buckets, Amazon DynamoDB tables, and Application Load Balancers. For each resource type, the company mandates that deployments must comply with the following requirements: All EC2 instances must be launched from approved AWS accounts. All DynamoDB tables must be provisioned with a standardized naming convention. All infrastructure that is provisioned in any accounts in the organization must be deployed by AWS CloudFormation templates. Which combination of steps should the application team take to meet these requirements? (Choose two.)

- [x] Create CloudFormation templates in an administrator AWS account. Share the stack sets with an application AWS account. Restrict the template to be used specifically by the application AWS account.
- [ ] Create CloudFormation templates in an application AWS account. Share the output with an administrator AWS account ta review compliant resources. Restrict output to only the administrator AWS account.
- [ ] Use permissions boundaries to prevent the application AWS account from provisioning specific resources unless conditions for the internal compliance requirements are met.
- [x] Use SCPs to prevent the application AWS account from provisioning specific resources unless conditions for the internal compliance requirements are met.
- [ ] Activate AWS Config managed rules for each service in the application AWS account.

### A Developer reported that AWS CloudTrail was disabled on their account. A Security Engineer investigated the account and discovered the event was undetected by the current security solution. The Security Engineer must recommend a solution that will detect future changes to the CloudTrail configuration and send alerts when changes occur. What should the Security Engineer do to meet these requirements?

- [ ] Use AWS Resource Access Manager (AWS RAM) to monitor the AWS CloudTrail configuration. Send notifications using Amazon SNS.
- [x] Create an Amazon CloudWatch Events rule to monitor Amazon GuardDuty findings.
Send email notifications using Amazon SNS.
- [ ] Update security contact details in AWS account settings for AWS Support to send alerts when suspicious activity is detected.
- [ ] Use Amazon Inspector to automatically detect security issues. Send alerts using Amazon SNS.

### A company suspects that an attacker has exploited an overly permissive role to export credentials from Amazon EC2 instance metadata. The company uses Amazon GuardDuty and AWS Audit Manager. The company has enabled AWS CloudTrail logging and Amazon CloudWatch logging for all of its AWS accounts. A security engineer must determine if the credentials were used to access the company's resources from an external account. Which solution will provide this information?

- [x] Review GuardDuty findings to find `InstanceCredentialExfiltration` events.
- [ ] Review assessment reports in the Audit Manager console to find `InstanceCredentialExfiltration` events.
- [ ] Review CloudTrail logs for `GetSessionToken` API calls to AWS Security Token Service (AWS STS) that come from an account ID from outside the company.
- [ ] Review CloudWatch logs for `GetSessionToken` API calls to AWS Security Token Service (AWS STS) that come from an account ID from outside the company.

### A security engineer need to ensure their company's uses of AWS meets AWS security best practices. As part of this, the AWS account root user must not be used for daily work. The root user must be monitored for use, and the Security team must be alerted as quickly as possible if the root user is used. Which solution meets these requirements?

- [x] Set up an Amazon CloudWatch Events rule that triggers an Amazon SNS notification.
- [ ] Set up an Amazon CloudWatch Events rule that triggers an Amazon SNS notification logs from S3 and generate notifications using Amazon SNS.
- [ ] Set up a rule in AWS config to trigger root user events. Trigger an AWS Lambda function and generate notifications using Amazon SNS.
- [ ] Use Amazon Inspector to monitor the usage of the root user and generate notifications using Amazon SNS.

### A security engineer has enabled AWS Security Hub in their AWS account, and has enabled the Center for Internet Security (CIS) AWS Foundations compliance standard. No evaluation results on compliance are returned in the Security Hub console after several hours. The engineer wants to ensure that Security Hub can evaluate their resources for CIS AWS Foundations compliance. Which steps should the security engineer take to meet these requirements?

- [ ] Add full Amazon Inspector IAM permissions to the Security Hub service role to allow it to perform the CIS compliance evaluation.
- [ ] Ensure that AWS Trusted Advisor is enabled in the account, and that the Security Hub service role has permissions to retrieve the Trusted Advisor security- related recommended actions.
- [x] Ensure that AWS Config is enabled in the account, and that the required AWS Config rules have been created for the CIS compliance evaluation.
- [ ] Ensure that the correct trail in AWS CloudTrail has been configured for monitoring by Security Hub, and that the Security Hub service role has permissions to perform the GetObject operation on CloudTrail's Amazon S3 bucket.

### A company has secured the AWS account root user for its AWS account by following AWS best practices. The company also has enabled AWS CloudTrail, which is sending its logs to Amazon S3. A security engineer wants to receive notification in near-real time if a user uses the AWS account root user credentials to sign in to the AWS Management Console. Which solutions will provide this notification? (Choose two.)

- [ ] Use AWS Trusted Advisor and its security evaluations for the root account. Configure an Amazon EventBridge event rule that is invoked by the Trusted Advisor API. Configure the rule to target an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe any required endpoints to the SNS topic so that these endpoints can receive notification.
- [ ] Use AWS IAM Access Analyzer. Create an Amazon Cloud Watch Logs metric filter to evaluate log entries from Access Analyzer that detect a successful root account login. Create an Amazon CloudWatch alarm that monitors whether a root login has occurred. Configure the CloudWatch alarm to notify an Amazon Simple Notification Service (Amazon SNS) topic when the alarm enters the ALARM state. Subscribe any required endpoints to this SNS topic so that these endpoints can receive notification.
- [x] Configure AWS CloudTrail to send its logs to Amazon CloudWatch Logs. Configure a metric filter on the CloudWatch Logs log group used by CloudTrail to evaluate log entries for successful root account logins. Create an Amazon CloudWatch alarm that monitors whether a root login has occurred. Configure the CloudWatch alarm to notify an Amazon Simple Notification Service (Amazon SNS) topic when the alarm enters the ALARM state. Subscribe any required endpoints to this SNS topic so that these endpoints can receive notification.
- [ ] Configure AWS CloudTrail to send log notifications to an Amazon Simple Notification Service (Amazon SNS) topic. Create an AWS Lambda function that parses the CloudTrail notification for root login activity and notifies a separate SNS topic that contains the endpoints that should receive notification. Subscribe the Lambda function to the SNS topic that is receiving log notifications from CloudTrail.
- [x] Configure an Amazon EventBridge event rule that runs when Amazon CloudWatch API calls are recorded for a successful root login. Configure the rule to target an Amazon Simple Notification Service (Amazon SNS) topic. Subscribe any required endpoints to the SNS topic so that these endpoints can receive notification.

### A company always needs its Amazon Elastic Block Store (Amazon EBS) volumes to be encrypted During a security incident. EBS snapshots of suspicious instances are shared to a forensics account for analysis A security engineer attempting to share a suspicious EBS snapshot to the forensics account receives the following error `"Unable to share snapshot: An error occurred (OperationNotPermitted) when calling the ModifySnapshotAttribute operation: Encrypted snapshots with EBS default key cannot be shared`. Which combination of steps should the security engineer take in the incident account to complete the sharing operation? (Select THREE)

- [x] Create a customer managed CMK Copy the EBS snapshot encrypting the destination snapshot using the new CMK.
- [x] Allow forensics accounting principals to use the CMK by modifying its policy.
- [ ] Create an Amazon EC2 instance. Attach the encrypted and suspicious EBS volume. Copy data from the suspicious volume to an unencrypted volume. Snapshot the unencrypted volume.
- [ ] Copy the EBS snapshot to the new decrypted snapshot.
- [ ] Restore a volume from the suspicious EBS snapshot. Create an unencrypted EBS volume of the same size.
- [x] Share the target EBS snapshot with the forensics account.

### A company is testing an application that runs on an Amazon EC2 Linux instance. A single 500 GB Amazon Elastic Block Store (Amazon EBS) General Purpose SSO (gp2) volume is attached to the EC2 instance. The company will deploy the application on multiple EC2 instances in an Auto Scaling group. All instances require access to the data that is stored in the EBS volume. The company needs a highly available and resilient solution that does not introduce significant changes to the application's code. Which solution will meet these requirements?

- [ ] Provision an EC2 instance that uses NFS server software. Attach a single 500 GB gp2 EBS volume to the instance.
- [ ] Provision an Amazon FSx for Windows File Server file system. Configure the file system as an SMB file store within a single Availability Zone.
- [ ] Provision an EC2 instance with two 250 GB Provisioned IOPS SSD EBS volumes.
- [x] Provision an Amazon Elastic File System (Amazon EFS) file system. Configure the file system to use General Purpose performance mode.

### A Security Engineer has launched multiple Amazon EC2 instances from a private AMI using an AWS CloudFormation template. The Engineer notices instances terminating right after they are launched. What could be causing these terminations?

- [ ] The IAM user launching those instances is missing `ec2:Runinstances` permission.
- [x] The AMI used as encrypted and the IAM does not have the required AWS KMS permissions.
- [ ] The instance profile used with the EC2 instances in unable to query instance metadata.
- [ ] AWS currently does not have sufficient capacity in the Region.

### A Security Engineer has discovered that, although encryption was enabled on the Amazon S3 bucket example bucket, anyone who has access to the bucket has the ability to retrieve the files. The Engineer wants to limit access to each IAM user can access an assigned folder only. What should the Security Engineer do to achieve this?

- [ ] Use envelope encryption with the AWS-managed CMK aws/s3.
- [ ] Create a customer-managed CMK with a key policy granting `kms:Decrypt` based on the `'${aws:username}'` variable.
- [ ] Create a customer-managed CMK for each user. Add each user as a key user in their corresponding key policy.
- [x] Change the applicable IAM policy to grant S3 access to `'Resource': 'arn:aws:s3:::examplebucket/${aws:username}/*'`.

### Users report intermittent availability of a web application hosted on AWS. Monitoring systems report an excess of abnormal network traffic followed by high CPU utilization on the application web tier. Which of the following techniques will improve the availability of the application? (Select TWO)

- [ ] Deploy AWS WAF to block all unsecured web applications from accessing the internet.
- [x] Deploy an Intrusion Detection/Prevention System (IDS/IPS) to monitor or block unusual incoming network traffic.
- [ ] Configure security groups to allow outgoing network traffic only from hosts that are protected with up-to-date antivirus software.
- [x] Create Amazon CloudFront distribution and configure AWS WAF rules to protect the Web applications from malicious traffic.
- [ ] Use the default Amazon VPC for externakfacing systems to allow AWS to actively block malicious network traffic affecting Amazon EC2 instances.

### An AWS account administrator created an IAM group and applied the following managed policy to require that each individual user authenticate using multi-factor authentication: After implementing the policy, the administrator receives reports that users are unable to perform Amazon EC2 commands using the AWS CLI. What should the administrator do to resolve this problem while still enforcing multi-factor authentication?

![Question 227](images/question227.png)

- [ ] Change the value of `aws:MultiFactorAuthPresent` to `true`.
- [x] Instruct users to run the `aws sts get-session-token` CLI command and pass the multi-factor authentication `―-serial-number` and `-―token-code` parameters. Use these resulting values to make API/CLI calls.
- [ ] Implement federated API/CLI access using SAML 2.0, then configure the identity provider to enforce multi-factor authentication.
- [ ] Create a role and enforce multi-factor authentication in the role trust policy Instruct users to run the `aws sts assume-role` CLI command and pass `–-serial-number` and `―-token-code` parameters Store the resulting values in environment variables. Add `sts:AssumeRole` to NotAction in the policy.

### The Security Engineer is managing a traditional three-tier web application that is running on Amazon EC2 instances. The application has become the target of increasing numbers of malicious attacks from the Internet. What steps should the Security Engineer take to check for known vulnerabilities and limit the attack surface? (Choose TWO)

- [ ] Use AWS Certificate Manager to encrypt all traffic between the client and application servers.
- [x] Review the application security groups to ensure that only the necessary ports are open.
- [ ] Use Elastic Load Balancing to offload Secure Sockets Layer encryption.
- [x] Use Amazon Inspector to periodically scan the backend instances.
- [ ] Use AWS Key Management Services to encrypt all the traffic between the client and application servers.

### A Security Engineer discovered a vulnerability in an application running on Amazon ECS. The vulnerability allowed attackers to install malicious code. Analysis of the code shows it exfiltrates data on port 5353 in batches at random time intervals. While the code of the containers is being patched, how can Engineers quickly identify all compromised hosts and stop the egress of data on port 5353?

- [ ] Enable AWS Shield Advanced and AWS WAF. Configure an AWS WAF custom filter for egress traffic on port 5353
- [ ] Enable Amazon Inspector on Amazon ECS and configure a custom assessment to evaluate containers that have port 5353 open. Update the NACLs to block port 5353 outbound.
- [x] Create an Amazon CloudWatch custom metric on the VPC Flow Logs identifying egress traffic on port 5353. Update the NACLs to block port 5353 outbound.
- [ ] Use Amazon Athena to query AWS CloudTrail logs in Amazon S3 and look for any traffic on port 5353. Update the security groups to block port 5353 outbound.

### A company's Director of information Security wants a daily email report from AWS that contains recommendations for each company account to meet AWS Security best practices. Which solution would meet these requirements?

- [x] In every AWS account, configure AWS Lambda to query me AWS Support API for AWS Trusted Advisor security checks Send the results from Lambda to an Amazon SNS topic to send reports.
- [ ] Configure Amazon GuardDuty in a master account and invite all other accounts to be managed by the master account Use GuardDuty's integration with Amazon SNS to report on findings.
- [ ] Use Amazon Athena and Amazon QuickSight to build reports off of AWS CloudTrail Create a daily Amazon CloudWatch trigger to run the report dally and email It using Amazon SNS.
- [ ] Use AWS Artifact's prebuilt reports and subscriptions Subscribe the Director of Information Security to the reports by adding the Director as the security alternate contact for each account.

### A company wants to deploy a continuous security threat-detection service at scale to automatically analyze all the company's member accounts in AWS Organizations within the `ap-east-1` Region. The company's organization includes a management account, a security account, and many member accounts. When the company creates a new member account, the threat-detection service should automatically analyze the new account so that the company can review any findings from the security account. Which solution uses AWS security best practices and meets these requirements with the LEAST effort?

- [x] Activate Amazon GuardDuty in `ap-east-1`. Designate the security account as the GuardDuty delegated administrator by using the console.
- [ ] Activate Amazon GuardDuty in `ap-east-1` with trusted access to AWS Organizations. Designate the management account as the GuardDuty organization administrator.
- [ ] Activate AWS Security Hub in `ap-east-1`. Designate the management account as the Security Hub delegated administrator by using the console.
- [ ] Activate AWS Control Tower in `ap-east-1` with trusted access to AWS Organizations. Designate the security account as the organization administrator.

### Two Amazon EC2 instances in different subnets should be able to connect to each other but cannot. It has been confirmed that other hosts in the same subnets are able to communicate successfully, and that security groups have valid ALLOW rules in place to permit this traffic. Which of the following troubleshooting steps should be performed?

- [ ] Check inbound and outbound security groups, looking for `DENY` rules.
- [x] Check inbound and outbound Network ACL rules, looking for `DENY` rules.
- [ ] Review the rejected packet reason codes in the VPC Flow Logs.
- [ ] Use AWS X-Ray to trace the end-to-end application flow.

### A company's Security Officer is concerned about the risk of AWS account root user logins and has assigned a Security Engineer to implement a notification solution for near-real-time alerts upon account root user logins. How should the Security Engineer meet these requirements?

- [ ] Create a cron job that runs a script to download the AWS IAM security credentials. We parse the file for account root user logins and email the Security team's distribution list.
- [x] Run AWS CloudTrail logs through Amazon CloudWatch Events to detect account roo4 user logins and trigger an AWS Lambda function to send an Amazon SNS notification to the Security team's distribution list.
- [ ] Save AWS CloudTrail logs to an Amazon S3 bucket in the Security team's account Process the CloudTrail logs with the Security Engineer's logging solution for account root user logins Send an Amazon SNS notification to the Security team upon encountering the account root user login events.
- [ ] Save VPC Plow Logs to an Amazon S3 bucket in the Security team's account and process the VPC Flow Logs with their logging solutions for account root user logins Send an Amazon SNS notification to the Security team upon encountering the account root user login events.

### A company has many member accounts in an organization in AWS Organizations. The company is concerned about the potential for misuse of the AWS account root user credentials for member accounts in the organization. To address this potential misuse, the company wants to ensure that even if the account root user credentials are compromised, the account is still protected. Which solution will meet this requirement?

- [x] Block service access by using SCPs for the root user.
- [ ] Remove the password for the root user.
- [ ] Delete access keys for the root user.
- [ ] Create an Amazon CloudWatch Events rule to detect any AWS account root user API events.

### A company's Chief Security Officer has requested that a Security Analyst review and improve the security posture of each company AWS account. The Security Analyst decides to do this by improving AWS account root user security. Which actions should the Security Analyst take to meet these requirements? (Choose three.)

- [x] Delete the access keys for the account root user in every account.
- [ ] Create an admin IAM user with administrative privileges and delete the account root user in every account.
- [x] Implement a strong password to help protect account-level access to the AWS Management Console by the account root user.
- [x] Enable multi-factor authentication (MFA) on every account root user in all accounts.
- [ ] Create a custom IAM policy to limit permissions to required actions for the account root user and attach the policy to the account root user.
- [ ] Attach an IAM role to the account root user to make use of the automated credential rotation in AWS STS.

### A security engineer needs to ensure their company's use of AWS meets AWS security best practices. As part of this, the AWS account root user must not be used for daily work. The root user must be monitored for use, and the security team must be alerted as quickly as possible if the root user is used. Which solution meets these requirements?

- [x] Set up an Amazon CloudWatch Events rule that triggers an Amazon SNS notification.
- [ ] Create root user access keys. Use an AWS Lambda function to parse AWS CloudTrail logs from Amazon S3 and generate notifications using Amazon SNS.
- [ ] Set up a rule in AWS Config to trigger root user events. Trigger an AWS Lambda function and generate notifications using Amazon SNS.
- [ ] Use Amazon Inspector to monitor the usage of the root user and generate notifications using Amazon SNS.

### A company has multiple AWS accounts that are part of AW5 Organizations. The company's Security team wants to ensure that even those Administrators with full access to the company's AWS accounts are unable to access the company's Amazon S3 buckets How should this be accomplished?

- [x] UseSCPs.
- [ ] Add a permissions boundary to deny access to Amazon S3 and attach it to all roles.
- [ ] Use an S3 bucket policy.
- [ ] Create a VPC endpoint for Amazon S3 and deny statements for access to Amazon S3.

### A company uses HTTP Live Streaming (HLS) to stream live video content to paying subscribers by using Amazon CloudFront. HLS splits the video content into chunks so that the user can request the right chunk based on different conditions Because the video events last for several hours, the total video is made up of thousands of chunks The origin URL is not disclosed and every user is forced to access the CloudFront URL The company has a web application that authenticates the paying users against an internal repository and a CloudFront key pair that is already issued. What is the simplest and MOST effective way to protect the content?

- [ ] Develop the application to use the CloudFront key pair to create signed URLs that users will use to access the content.
- [x] Develop the application to use the CloudFront key pair to set the signed cookies that users will use to access the content.
- [ ] Develop the application to issue a security token that Lambda@Edge will receive to authenticate and authorize access to the content.
- [ ] Keep the CloudFront URL encrypted inside the application, and use AWS KMS to resolve the URL on-the-fly after the user is authenticated.

### An organization policy states that all encryption keys must be automatically rotated every 12 months. Which AWS Key Management Service (KMS) key type should be used to meet this requirement?

- [x] AWS managed Customer Master Key (CMK)
- [ ] Customer managed CMK with AWS generated key material.
- [ ] Customer managed CMK with imported key material.
- [ ] AWS managed data key.

### A company has decided to use AWS Key Management Service (AWS KMS) for all of its encryption keys. The company plans to create all of its keys as customer managed CMKs and will not import any encryption keys. The company must rotate its encryption keys once every 12 months. Which solution will meet these requirements?

- [ ] Change the customer managed CMK key policy to enable automatic key rotation.
- [ ] Use AWS managed CMKs instead of customer managed CMKs so that AWS will rotate the keys automatically.
- [ ] Invoke an AWS Lambda function regularly to rotate the backing key of each customer managed CMK.
- [x] Enable automatic key rotation for each customer managed CMK after it has been created in AWS KMS.

### A company has a customer master key (CMK) with imported key materials. Company policy requires that all encryption keys must be rotated every year. What can be done to implement the above policy?

- [ ] Enable automatic key rotation annually for the CMK.
- [ ] Use AWS Command Line Interface to create an AWS Lambda function to rotate the existing CMK annually.
- [ ] Import new key material to the existing CMK and manually rotate the CMK.
- [x] Create a new CMK, import new key material to it, and point the key alias to the new CMK.

### A security engineer is responsible for providing secure access to AWS resources for thousands of developer in a company's corporate identity provider (idp). The developers access a set of AWS services from the corporate premises using IAM credential. Due to the velum of require for provisioning new IAM users, it is taking a long time to grant access permissions. The security engineer receives reports that developer are sharing their IAM credentials with others to avoid provisioning delays. The causes concern about overall security for the security engineer. Which actions will meet the program requirements that address security?

- [ ] Create an Amazon CloudWatch alarm for AWS CloudTrail Events. Create a metric filter to send a notification when me same set of IAM credentials is used by multiple developer.
- [x] Create a federation between AWS and the existing corporate IdP. Leverage IAM roles to provide federated access to AWS resources
- [ ] Create a VPN tunnel between the corporate premises and the VPC. Allow permissions to all AWS services only if it originates from corporate premises.
- [ ] Create multiple IAM rotes for each IAM user. Ensure that users who use the same IAM credentials cannot assume the same IAM role at the same time.

### A company requires that SSH commands used to access its AWS instance be traceable to the user who executed each command. How should a Security Engineer accomplish this?

- [ ] Allow inbound access on port 22 at the security group attached to the instance. Use AWS Systems Manager Session Manager for shell access to Amazon EC2 instances with the user tag defined. Enable Amazon CloudWatch togging for Systems Manager sessions.
- [ ] Use Amazon S3 to securely store one Privacy Enhanced Mail Certificate (PEM file) for each user. Allow Amazon EC2 to read from Amazon S3 and import every user that wants to use SSH to access EC2 instances. Allow inbound access on port 22 at the security group attached to the instance. Install the Amazon CloudWatch agent on the EC2 instance and configure it to ingest audit logs for the instance.
- [x] Deny inbound access on port 22 at the security group attached to the instance. Use AWS Systems Manager Session Manager for shell access to Amazon EC2 instances with the user tag defined. Enable Amazon CloudWatch togging for Systems Manager sessions.
- [ ] Use Amazon S3 to securely store one Privacy Enhanced Mall Certificate (PEM file) for each team or group. Allow Amazon EC2 to read from Amazon S3 and import every user that wants to use SSH to access EC2 instances. Allow inbound access on pod 22 at the security group attached to the instance. Install the Amazon CloudWatch agent on the EC2 instance and configure it to ingest audit logs for the instance.

### A company has a requirement that no Amazon EC2 security group can allow SSH access from the CIDR block 0.0.0.0/0. The company wants to monitor compliance with this requirement at all times and wants to receive a near-real-time notification if any security group is noncompliant. A security engineer has configured AWS Config and will use the restricted-ssh managed rule to monitor the security groups. What should the security engineer do next to meet these requirements?

- [ ] Configure AWS Config to send its configuration snapshots to an Amazon S3 bucket. Create an AWS Lambda function to run on a PutEvent to the S3 bucket. Configure the Lambda function to parse the snapshot for a compliance change to the restricted-ssh managed rule. Configure the Lambda function to send a notification to an Amazon Simple Notification Service (Amazon SNS) topic if a change is discovered.
- [x] Configure an Amazon EventBridge (Amazon CloudWatch Events) event rule that is invoked by a compliance change event from AWS Config for the restricted-ssh managed rule. Configure the event rule to target an Amazon Simple Notification Service (Amazon SNS) topic that will provide a notification.
- [ ] Configure AWS Config to push all its compliance notifications to Amazon CloudWatch Logs. Configure a CloudWatch Logs metric filter on the AWS Config log group to look for a compliance notification change on the restricted-ssh managed rule. Create an Amazon CloudWatch alarm on the metric filter to send a notification to an Amazon Simple Notification Service (Amazon SNS) topic if the alarm is in the ALARM state.
- [ ] Configure an Amazon CloudWatch alarm on the CloudWatch metric for the restricted-ssh managed rule. Configure the CloudWatch alarm to send a notification to an Amazon Simple Notification Service (Amazon SNS) topic if the alarm is in the ALARM state.

### A company's information security team wants to analyze Amazon EC2 performance and utilization data in the near-real time for anomalies. A Sec Engineer is responsible for log aggregation. The Engineer must collect logs from all of the company's AWS accounts in centralized location to perform the analysis. How should the Security Engineer do this? Log in to each account four te a day and filter the AWS CloudTrail log data, then copy and paste the logs in to the Amazon S3 bucket in the destination account.

- [x] Set up Amazon CloudWatch to stream data to an Amazon S3 bucket in each source account. Set up bucket replication for each source account into a centralized bucket owned by the security Engineer.
- [ ] Set up an AWS Config aggregator to collect AWS configuration data from multiple sources.
- [ ] Set up an AWS config aggregator to collect AWS configuration data from multiple sources.
- [ ] Set up Amazon CloudWatch cross-account log data sharing with subscriptions in each account. Send the logs to Amazon Kinesis Data Firehose in the Security Engineer's account.

### A Security Engineer is setting up an AWS CloudTrail trail for all regions in an AWS account. For added security, the logs are stored using server-side encryption with AWS KMS-managed keys (SSE-KMS) and have log integrity validation enabled. While testing the solution, the Security Engineer discovers that the digest files are readable, but the log files are not. What is the MOST likely cause?

- [ ] The log files fail integrity validation and automatically are marked as unavailable.
- [x] The KMS key policy does not grant the Security Engineer's IAM user or role permissions to decrypt with it.
- [ ] The bucket is set up to use server-side encryption with Amazon S3-managed keys (SSE-S3) as the default and does not allow SSE-KMS-encrypted files.
- [ ] An IAM policy applicable to the Security Engineer's IAM user or role denies access to the "CloudTrail/" prefix in the Amazon S3 bucket.

### A security engineer has created an Amazon Cognito user pool. The engineer needs to manually verify the ID and access token sent by the application for troubleshooting purposes. What is the MOST secure way to accomplish this?

- [x] Extract the subject (sub), audience (aud), and cognito:username from the ID token payload Manually check the subject and audience for the user name In the user pool.
- [ ] Search for the public key with a key ID that matches the key ID In the header of the token. Then use a JSON Web Token (JWT) library to validate the signature of the token and extract values, such as the expiry date.
- [ ] Verify that the token is not expired. Then use the token_use claim function In Amazon Cognito to validate the key IDs.
- [ ] Copy the JSON Web Token (JWT) as a JSON document Obtain the public JSON Web Key (JWK) and convert It to a pem file. Then use the file to validate the original JWT.

### A Security Engineer launches two Amazon EC2 instances in the same Amazon VPC but in separate Availability Zones. Each instance has a public IP address and is able to connect to external hosts on the internet. The two instances are able to communicate with each other by using their private IP addresses, but they are not able to communicate with each other when using their public IP addresses. Which action should the Security Engineer take to allow communication over the public IP addresses?

- [ ] Associate the instances to the same security groups.
- [ ] Add 0.0.0.0/0 to the egress rules of the instance security groups.
- [ ] Add the instance IDs to the ingress rules of the instance security groups.
- [x] Add the public IP addresses to the ingress rules of the instance security groups.

### A company uses multiple AWS accounts managed with AWS Organizations Security engineers have created a standard set of security groups for all these accounts. The security policy requires that these security groups be used for all applications and delegates modification authority to the security team only. A recent security audit found that the security groups are inconsistency implemented across accounts and that unauthorized changes have been made to the security groups. A security engineer needs to recommend a solution to improve consistency and to prevent unauthorized changes in the individual accounts in the future. Which solution should the security engineer recommend?

- [ ] Use AWS Resource Access Manager to create shared resources for each requited security group and apply an IAM policy that permits read-only access to the security groups only.
- [x] Create an AWS CloudFormation template that creates the required security groups Execute the template as part of configuring new accounts Enable Amazon Simple Notification Service (Amazon SNS) notifications when changes occur.
- [ ] Use AWS Firewall Manager to create a security group policy, enable the policy feature to identify and revert local changes, and enable automatic remediation.
- [ ] Use AWS Control Tower to edit the account factory template to enable the snare security groups option Apply an SCP to the OU or individual accounts that prohibits security group modifications from local account users.

### A company's security information events management (SIEM) tool receives new AWS CloudTrail logs from an Amazon S3 bucket that is configured to send all object created event notification to an Amazon SNS topic An Amazon SQS queue is subscribed to this SNS topic. The company's SEM tool then ports this SQS queue for new messages using an IAM role and fetches new log events from the S3 bucket based on the SQS messages. After a recent security review that resulted m restricted permissions, the SEM tool has stopped receiving new CloudTral logs. Which of the following are possible causes of this issue? (Select THREE)

- [x] The SOS queue does not allow the SQS SendMessage action from the SNS topic.
- [ ] The SNS topic does not allow the SNS Publish action from Amazon S3.
- [ ] The SNS topic is not delivering raw messages to the SQS queue.
- [x] The S3 bucket policy does not allow CloudTrail to perform the PutObject action.
- [ ] The IAM role used by the 5EM tool does not have permission to subscribe to the SNS topic.
- [x] The IAM role used by the SEM tool does not allow the SQS DeleteMessage action.

### A city is implementing an election results reporting website that will use Amazon GoudFront. The website runs on a fleet of Amazon EC2 instances behind an Application Load Balancer (ALB) in an Auto Scaling group. Election results are updated hourly and are stored as .pdf tiles in an Amazon S3 bucket. A Security Engineer needs to ensure that all external access to the website goes through CloudFront. Which solution meets these requirements?

- [ ] Create an IAM role that allows CloudFront to access the specific S3 bucket. Modify the S3 bucket policy to allow only the new IAM role to access its contents. Create an interface VPC endpoint for CloudFront to securely communicate with the ALB.
- [ ] Create an IAM role that allows CloudFront to access the specific S3 bucket. Modify the S3 bucket policy to allow only the new IAM role to access its contents. Associate the ALB with a security group that allows only incoming traffic from the CloudFront service to communicate with the ALB.
- [x] Create an origin access identity (OAI) in CloudFront. Modify the S3 bucket policy to allow only the new OAI to access the bucket contents. Create an interface VPC endpoint for CloudFront to securely communicate with the ALB.
- [ ] Create an origin access identity (OAI) in CloudFront. Modify the S3 bucket policy to allow only the new OAI to access the bucket contents. Associate the ALB with a security group that allows only incoming traffic from the CloudFront service to communicate with the ALB.

### An company is using AWS Secrets Manager to store secrets that are encrypted using a CMK and are stored in the security account 111122223333. One of the company's production accounts. 444455556666, must to retrieve the secret values from the security account 111122223333. A security engineer needs to apply a policy to the secret in the security account based on least privilege access so the production account can retrieve the secret value only. Which policy should the security engineer apply?

![Question 203 option A](images/question203_1.png)

![Question 203 option B](images/question203_2.png)

![Question 203 option C](images/question203_3.png)

- [x] Option A.
- [ ] Option B.
- [ ] Option C.
- [ ] Option D.

### A company has a forensic logging use case whereby several hundred applications running on Docker on EC2 need to send logs to a central location. The Security Engineer must create a logging solution that is able to perform real-time analytics on the log files, grants the ability to replay events, and persists data. Which AWS Services, together, can satisfy this use case? (Choose TWO)

- [x] Amazon Elasticsearch.
- [x] Amazon Kinesis.
- [ ] Amazon SQS.
- [ ] Amazon CloudWatch.
- [ ] Amazon Athena.

### A Security Engineer is troubleshooting a connectivity issue between a web server that is writing log files to the logging server in another VPC. The Engineer has confirmed that a peering relationship exists between the two VPCs. VPC flow logs show that requests sent from the Web server are accepted by the logging server, but the Web server never receives a reply. Which of the following actions could fix this issue?

- [ ] Add an inbound rule to the security group associated with the logging server that allows requests from the Web server.
- [ ] Add an outbound rule to the security group associated with the Web server that allows requests to the logging server.
- [x] Add a route to the route table associated with the subnet that hosts the logging server that targets the peering connection.
- [ ] Add a route to the route table associated with the subnet that hosts the Web server that targets the peering connection.

### A company's Security Engineer is copying all application logs to centralized Amazon S3 buckets. Currently, each of the company's application is in its own AWS account, and logs are pushed into S3 buckets associated with each account. The Engineer will deploy an AWS Lambda function into each account that copies the relevant log files to the centralized S3 bucket. The Security Engineer is unable to access the log files in the centralized S3 bucket. The Engineer's IAM user policy from the centralized account looks like this. The centralized S3 bucket policy looks like this. Why is the Security Engineer unable to access the log files?

![Question 246 part 1](images/question246_1.png)
![Question 246 part 2](images/question246_2.png)

- [ ] The S3 bucket policy does not explicitly allow the Security Engineer access to the objects in the bucket.
- [x] The object ACLs are not being updated to allow the users within the centralized account to access the objects.
- [ ] The Security Engineer's IAM policy does not grant permissions to read objects in the S3 bucket.
- [ ] The `s3:PutObject` and `s3:PutObjectAcl` permissions should be applied at the S3 bucket level.

### A Security Engineer has created an Amazon CloudWatch event that invokes an AWS Lambda function daily. The Lambda function runs an Amazon Athena query that checks AWS CloudTrail logs in Amazon S3 to detect whether any IAM user accounts or credentials have been created in the past 30 days. The results of the Athena query are created in the same S3 bucket. The Engineer runs a test execution of the Lambda function via the AWS Console, and the function runs successfully. After several minutes, the Engineer finds that his Athena query has failed with the error message: `Insufficient Permissions`. The IAM permissions of the Security Engineer and the Lambda function are shown below. Security Engineer. Lambda function execution role. What is causing the error?

![Question 247 part 1](images/question247_1.png)
![Question 247 part 2](images/question247_2.png)

- [ ] The Lambda function does not have permissions to start the Athena query execution.
- [ ] The Security Engineer does not have permissions to start the Athena query execution.
- [ ] The Athena service does not support invocation through Lambda.
- [x] The Lambda function does not have permissions to access the CloudTrail S3 bucket.

### A startup company hosts a fleet of Amazon EC2 instances in private subnets using the latest Amazon Linux 2 AMI. The company's engineers rely heavily on SSH access to the instances for troubleshooting. The company's existing architecture includes the following: A VPC with private and public subnets, and a NAT gateway. Site-to-Site VPN for connectivity with the on-premises environment. EC2 security groups with direct SSH access from the on-premises environment. The company needs to increase security controls around SSH access and provide auditing of commands run by the engineers. Which strategy should a solutions architect use?

- [ ] Install and configure EC2 Instance Connect on the fleet of EC2 instances. Remove all security group rules attached to EC2 instances that allow inbound TCP on port 22. Advise the engineers to remotely access the instances by using the EC2 Instance Connect CLI.
- [ ] Update the EC2 security groups to only allow inbound TCP on port 22 to the IP addresses of the engineer's devices. Install the Amazon CloudWatch agent on all EC2 instances and send operating system audit logs to CloudWatch Logs.
- [ ] Update the EC2 security groups to only allow inbound TCP on port 22 to the IP addresses of the engineer's devices. Enable AWS Config for EC2 security group resource changes. Enable AWS Firewall Manager and apply a security group policy that automatically remediates changes to rules.
- [x] Create an IAM role with the AmazonSSMManagedInstanceCore managed policy attached. Attach the IAM role to all the EC2 instances. Remove all security group rules attached to the EC2 instances that allow inbound TCP on port 22. Have the engineers install the AWS Systems Manager Session Manager plugin for their devices and remotely access the instances by using the start-session API call from Systems Manager.

### A company has an AWS Lambda function that needs read access to an Amazon S3 bucket that is located in the same AWS account. Which solution will meet these requirements in the MOST secure manner?

- [ ] Apply an S3 bucket policy that grants read access to the S3 bucket.
- [x] Apply an IAM role to the Lambda function. Apply an IAM policy to the role to grant read access to the S3 bucket.
- [ ] Embed an access key and a secret key in the Lambda function's code to grant the required IAM permissions for read access to the S3 bucket.
- [ ] Apply an IAM role to the Lambda function. Apply an IAM policy to the role to grant read access to all S3 buckets in the account.

### A security engineer needs to create an Amazon S3 bucket policy to grant least privilege read access to IAM user accounts that are named User1, User2 and User3. These IAM user accounts are members of the AuthorizedPeople IAM group. The security engineer drafts the following S3 bucket policy. When the security engineer tries to add the policy to the S3 bucket, the following message appears: `Missing required field Principal.` The security engineer is adding a Principal element to the policy. The addition must provide read access to only User1, User2 and User3. Which solution meets these requirements?

![Question 250](images/question250.jpg)

- [x] Option A.
![Question 250 option A](images/question250_A.png)
- [ ] Option B.
![Question 250 option B](images/question250_B.png)
- [ ] Option C.
![Question 250 option C](images/question250_C.png)
- [ ] Option D.
![Question 250 option D](images/question250_D.png)

### A company has decided to move its fleet of Linux-based web server instances to an Amazon EC2 Auto Scaling group. Currently, the instances are static and are launched manually. When an administrator needs to view log files, the administrator uses SSH to establish a connection to the instances and retrieves the logs manually. The company often needs to query the logs to produce results about application sessions and user issues. The company does not want its new automatically scaling architecture to result in the loss of any log files when instances are scaled in. Which combination of steps should a security engineer take to meet these requirements MOST cost-effectively? (Choose two.)

- [ ] Configure a cron job on the instances to forward the log files to Amazon S3 periodically.
- [ ] Configure AWS Glue and Amazon Athena to query the log files.
- [x] Configure the Amazon CloudWatch agent on the instances to forward the logs to Amazon CloudWatch Logs.
- [x] Configure Amazon CloudWatch Logs Insights to query the log files.
- [ ] Configure the instances to write the logs to an Amazon Elastic File System (Amazon EFS) volume.

### A company maintains sensitive data in an Amazon S3 bucket that must be protected using an AWS KMS CMK. The company requires that keys be rotated automatically every year. How should the bucket be configured?

- [ ] Select server-side encryption with Amazon S3-managed keys (SSE-S3) and select an AWS-managed CMK.
- [x] Select Amazon S3-AWS KMS managed encryption keys (S3-KMS) and select a customer-managed CMK with key rotation enabled.
- [ ] Select server-side encryption with Amazon S3-managed keys (SSE-S3) and select a customer-managed CMK that has imported key material.
- [ ] Select server-side encryption with AWS KMS-managed keys (SSE-KMS) and select an alias to an AWS-managed CMK.

### A company maintains an open-source application that is hosted on a public GitHub repository. While creating a new commit to the repository, an engineer uploaded their AWS access key and secret access keys. The engineer reported the mistake to a manager, and the manager immediately disabled the access key. The company needs to assess the impact of the exposed access key. A security engineer must recommend a solution that requires the least possible managerial overhead. Which solution meets these requirements?

- [ ] Analyze an AWS Identity and Access Management (IAM) use report from AWS Trusted Advisor to see. When the access key was last used.
- [ ] Analyze Amazon CloudWatch Logs for activity by searching for the access key.
- [ ] Analyze VPC flow logs for activity by searching for the access key.
- [x] Analyze a credential report in AWS Identity and Access Management (IAM) to see. When the access key was last used.

### A Solutions Architect is designing a web application that uses Amazon CloudFront, an Elastic Load Balancing Application Load Balancer, and an Auto Scaling group of Amazon EC2 instances. The load balancer and EC2 instances are in the US West (Oregon) region. It has been decided that encryption in transit is necessary by using a customer-branded domain name from the client to CloudFront and from CloudFront to the load balancer. Assuming that AWS Certificate Manager is used, how many certificates will need to be generated?

- [x] One in the US West (Oregon) region and one in the US East (Virginia) region.
- [ ] Two in the US West (Oregon) region and none in the US East (Virginia) region.
- [ ] One in the US West (Oregon) region and none in the US East (Virginia) region.
- [ ] Two in the US East (Virginia) region and none in the US West (Oregon) region.

### A large company has hundreds of AWS accounts. The company needs to provide its employees with access to these accounts. The solution must maximize scalability and operational efficiency. Which solution meets these requirements?

- [ ] With each AWS account, create dedicated IAM users that employees can assume through federation based upon group membership in their existing identity provider.
- [ ] Use a centralized account with IAM roles that employees can assume through federation with their existing identity provider. Create a custom authorizer by using AWS SDK to give federated users the ability to assume their target role in the resource accounts.
- [x] Implement AWS Control Tower for multi-account management by integrating AWS Single Sign-On with the company's existing identity provider. Create IAM roles for the identity provider to assume.
- [ ] Configure the IAM trust policies within each account's role to set up a trust back to the company's existing identity provider. Allow users to assume the role based on their SAML token.

### A company is running an Amazon RDS Multi-AZ DB instance inside a VPC. The DB instance is using two subnets that provide a default route to the internet through a NAT gateway. The company also has application servers that run on Amazon EC2 instances that use the RDS database. The company has deployed these EC2 instances into two other private subnets within the same VPC. These EC2 instances use a default route to access the internet through the same NAT gateway. Each subnet in the VPC uses its own unique route table. After a recent security audit, the company added a new security requirement. The DB instance must never be able to connect to the internet. A security engineer must make this change immediately without disrupting the application servers' network traffic. How can the security engineer meet these requirements?

- [ ] Remove the existing NAT gateway. Create a new NAT gateway that only the application server subnets can use.
- [ ] Configure the DB instance's inbound network ACL to deny traffic from the security group ID of the NAT gateway.
- [x] Modify the route tables of the DB instance subnets to remove the default route to the NAT gateway.
- [ ] Configure the route table of the NAT gateway to deny connections to the DB instance subnets.

### A company has a group of Amazon EC2 instances in a single private subnet of a VPC with no internet gateway attached. A security engineer has installed the Amazon CloudWatch agent on all instances in that subnet to capture logs from a specific application. To ensure that the logs flow securely, the company's networking team has created VPC endpoints for CloudWatch monitoring and CloudWatch logs. The networking team has attached the endpoints to the VPC. The application is generating logs. However, when the security engineer queries CloudWatch, the logs do not appear. Which combination of steps should the security engineer take to troubleshoot this issue? (Choose three.)

- [x] Ensure that the EC2 instance profile that is attached to the EC2 instances has permissions to create log streams and write logs.
- [ ] Create a metric filter on the logs so that they can be viewed in the AWS Management Console.
- [x] Check the CloudWatch agent configuration file on each EC2 instance to make sure that the CloudWatch agent is collecting the proper log files.
- [x] Check the VPC endpoint policies of both VPC endpoints to ensure that the EC2 instances have permissions to use them.
- [ ] Create a NAT gateway in the subnet so that the EC2 instances can communicate with CloudWatch.
- [ ] Ensure that the security groups allow all the EC2 instances to communicate with each other to aggregate logs before sending.

### A company is using Amazon Elastic Container Service (Amazon ECS) to run its container-based application on AWS. The company needs to ensure that the container images contain no severe vulnerabilities. The company also must ensure that only specific IAM roles and specific AWS accounts can access the container images. Which solution will meet these requirements with the LEAST management overhead?

- [ ] Pull images from the public container registry. Publish the images to Amazon Elastic Container Registry (Amazon ECR) repositories with scan on push configured in a centralized AWS account. Use a CI/CD pipeline to deploy the images to different AWS accounts. Use identity-based policies to restrict access to which IAM principals can access the images.
- [ ] Pull images from the public container registry. Publish the images to a private container registry that is hosted on Amazon EC2 instances in a centralized AWS account. Deploy host-based container scanning tools to EC2 instances that run Amazon ECS. Restrict access to the container images by using basic authentication over HTTPS.
- [x] Pull images from the public container registry. Publish the images to Amazon Elastic Container Registry (Amazon ECR) repositories with scan on push configured in a centralized AWS account. Use a CI/CD pipeline to deploy the images to different AWS accounts. Use repository policies and identity-based policies to restrict access to which IAM principals and accounts can access the images.
- [ ] Pull images from the public container registry. Publish the images to AWS CodeArtifact repositories in a centralized AWS account. Use a CI/CD pipeline to deploy the images to different AWS accounts. Use repository policies and identity-based policies to restrict access to which IAM principals and accounts can access the images.

### A company wants to establish separate AWS Key Management Service (AWS KMS) keys to use for different AWS services. The company's security engineer created the following key policy to allow the infrastructure deployment team to create encrypted Amazon Elastic Block Store (Amazon EBS) volumes by assuming the InfrastructueDeployment IAM role. The security engineer recently discovered that IAM roles other than the InfrastructureDeployment role used this key for other services. Which change to the policy should the security engineer make to resolve these issues?

![Question 256](images/question256.jpg)

- [ ] In the statement block that contains the Sid Allow use of the key, under the Condition block, change StringEquals to StringLike.
- [x] In the policy document, remove the statement block that contains the Sid Enable IAM User Permissions. Add key management policies to the KMS policy.
- [ ] In the statement block that contains the Sid Allow use of the key, under the Condition block, change the `kms:ViaService` value to ec2.`us-east-1`.amazonaws.com.
- [ ] In the policy document, add a new statement block that grants the `kms:Disable*` permission to the security engineer's IAM role.

### A company has enabled Amazon GuardDuty in all Regions as part of its security monitoring strategy. In one of the VPCs, the company hosts an Amazon EC2 instance working as an FTP server that is contacted by a high number of clients from multiple locations. This is identified by GuardDuty as a brute force attack due to the high number of connections that happen every hour. The finding has been flagged as a false positive. However, GuardDuty keeps raising the issue. A Security Engineer has been asked to improve the signal-to-noise ratio. The Engineer needs to ensure that changes do not compromise the visibility of potential anomalous behavior. How can the Security Engineer address the issue?

- [ ] Disable the FTP rule in GuardDuty in the Region where the FTP server is deployed.
- [ ] Add the FTP server to a trusted IP list and deploy it to GuardDuty to stop receiving the notifications.
- [x] Use GuardDuty filters with auto archiving enabled to close the findings.
- [ ] Create an AWS Lambda function that closes the finding whenever a new occurrence is reported.

### A company uses Amazon GuardDuty to detect threats and malicious activities in AWS accounts. The company has subscribed to a third-party threat intelligence list uploaded to an Amazon S3 bucket. How should the security engineer efficiently use the threat list across all company AWS accounts?

- [ ] Ensure the S3 bucket policy allows all company AWS accounts access to the threat list. Use an AWS Lambda function to automatically add the threat list to all company AWS accounts.
- [x] Ensure GuardDuty is in master-member configuration. Add the threat list to the master account referencing the S3 object that contains the threat list.
- [ ] Ensure all accounts are part of the same organization in AWS Organizations. Add the threat list to any company account within AWS Organizations.
- [ ] Ensure the threat list in the S3 bucket is publicly accessible. Use an Amazon CloudWatch Events event on GuardDuty findings to match IPs against the threat list.

### A company is hosting multiple applications within a single VPC in its AWS account. The applications are running behind an Application Load Balancer that is associated with an AWS WAF web ACL. The company's security team has identified that multiple port scans are originating from a specific range of IP addresses on the internet. A security engineer needs to deny access from the offending IP addresses. Which solution will meet these requirements?

- [x] Modify the AWS WAF web ACL with an IP set match rule statement to deny incoming requests from the IP address range.
- [ ] Add a rule to all security groups to deny the incoming requests from the IP address range.
- [ ] Modify the AWS WAF web ACL with a rate-based rule statement to deny incoming requests from the IP address range.
- [ ] Configure the AWS WAF web ACL with regex match conditions. Specify a pattern set to deny the incoming requests based on the match condition.

### A company has two software development teams that are creating applications that store sensitive data in Amazon S3. Each team's data must always be separate. The company's security team must design a data encryption strategy for both teams that provides the ability to audit key usage. The solution must also minimize operational overhead. What should the security team recommend?

- [ ] Tell the application teams to use two different S3 buckets with separate AWS Key Management Service (AWS KMS) AWS managed CMKs. Limit the key policies to allow encryption and decryption of the CMKs to their respective teams only. Force the teams to use encryption context to encrypt and decrypt.
- [ ] Tell the application teams to use two different S3 buckets with a single AWS Key Management Service (AWS KMS) AWS managed CMK. Limit the key policy to allow encryption and decryption of the CMK only. Do not allow the teams to use encryption context to encrypt and decrypt.
- [x] Tell the application teams to use two different S3 buckets with separate AWS Key Management Service (AWS KMS) customer managed CMKs. Limit the key policies to allow encryption and decryption of the CMKs to their respective teams only. Force the teams to use encryption context to encrypt and decrypt.
- [ ] Tell the application teams to use two different S3 buckets with a single AWS Key Management Service (AWS KMS) customer managed CMK. Limit the key policy to allow encryption and decryption of the CMK only. Do not allow the teams to use encryption context to encrypt and decrypt.

### An Amazon EC2 Auto Scaling group launches Amazon Linux EC2 instances and installs the Amazon CloudWatch agent to publish logs to Amazon CloudWatch Logs. The EC2 instances launch with an IAM role that has an IAM policy attached. The policy provides access to publish custom metrics to CloudWatch. The EC2 instances run in a private subnet inside a VPC The VPC provides access to the internet for private subnets through a NAT gateway. A security engineer notices that no logs are being published to CloudWatch Logs for the EC2 instances that the Auto Scaling group launches. The security engineer validates that the CloudWatch Logs agent is running and is configured properly on the EC2 instances. In addition, the security engineer validates that network communications are working properly to AWS services. What can the security engineer do to ensure that the logs are published to CloudWatch Logs?

- [x] Configure the IAM policy in use by the IAM role to have access to the required cloudwatch: API actions that will publish logs.
- [ ] Adjust the Amazon EC2 Auto Scaling service-linked role to have permissions to write to CloudWatch Logs.
- [ ] Configure the IAM policy in use by the IAM role to have access to the required AWS logs: API actions that will publish logs.
- [ ] Add an interface VPC endpoint to provide a route to CloudWatch Logs.

### A company has a web-based application that runs behind an Application Load Balancer (ALB). The application is experiencing a credential stuffing attack that is producing many failed login attempts. The attack is coming from many IP addresses. The login attempts are using a user agent string of a known mobile device emulator. A security engineer needs to implement a solution to mitigate the credential stuffing attack. The solution must still allow legitimate logins to the application. Which solution will meet these requirements?

- [ ] Create an Amazon CloudWatch alarm that reacts to login attempts that contain the specified user agent string Add an Amazon Simple Notification Service (Amazon SNS) topic to the alarm.
- [ ] Modify the inbound security group on the ALB to deny traffic from the IP addresses that are involved in the attack.
- [x] Create an AWS WAF web ACL for the ALB Create a custom rule that blocks requests that contain the user agent string of the device emulator.
- [ ] Create an AWS WAF web ACL for the ALB. Create a custom rule that allows requests from legitimate user agent strings.

### A DevOps team is planning to deploy a containerized application on Amazon Elastic Container Service (Amazon ECS). The team will use an Application Load Balancer (ALB) to distribute the incoming traffic for the ECS application. A security engineer needs to terminate the TLS traffic at the ALB to ensure security of data in transit. Which solutions can the security engineer use to create a certificate and deploy the certificate at the ALB to meet these requirements? (Choose two.)

- [x] Use TLS tools to create a certificate signing request (CSR). Get the CSR signed by a certificate authority (CA) to produce a certificate. Import the certificate into AWS Certificate Manager (ACM).
Specify the certificate for the TLS listener on the ALB.
- [x] Use AWS Certificate Manager (ACM) to request a certificate. Specify the certificate fort the TLS listener on the ALB.
- [ ] Use AWS Key Management Service (AWS KMS) tools to create a certificate signing request (CSR). Get the CSR signed by a certificate authority (CA) to produce a certificate. Import the certificate into AWS Certificate Manager (ACM). Specify the certificate for the TLS listener on the ALB.
- [ ] Configure automatic TLS support in the ECS cluster. Configure the ALB to pass the TLS connection to the containers in the cluster.
- [ ] Generate a certificate while creating the ECS cluster. Import the certificate into AWS Certificate Manager (ACM). Specify the certificate for the TLS listener on the ALB.

### A company is running an Amazon RDS for MySQL DB instance in a VPC. The VPC must not send or receive network traffic through the internet. A security engineer wants to use AWS Secrets Manager to rotate the DB instance credentials automatically. Because of a security policy, the security engineer cannot use the standard AWS Lambda function that Secrets Manager provides to rotate the credentials. The security engineer deploys a custom Lambda function in the VPC. The custom Lambda function will be responsible for rotating the secret in Secrets Manager. The security engineer edits the DB instance's security group to allow connections from this function. When the function is invoked, the function cannot communicate with Secrets Manager to rotate the secret properly. What should the security engineer do so that the function can rotate the secret?

- [ ] Add an egress-only internet gateway to the VPC. Allow only the Lambda function's subnet to route traffic through the egress-only internet gateway.
- [ ] Add a NAT gateway to the VPC. Configure only the Lambda function's subnet with a default route through the NAT gateway.
- [ ] Configure a VPC peering connection to the default VPC for Secrets Manager. Configure the Lambda function's subnet to use the peering connection for routes.
- [x] Configure a Secrets Manager interface VPC endpoint. Include the Lambda function's private subnet during the configuration process.

### A security engineer needs to build a solution to turn AWS CloudTrail back on in multiple AWS Regions in case it is ever turned off. What is the MOST efficient way to implement this solution?

- [x] Use AWS Config with a managed rule to initiate the AWS-EnableCloudTrail remediation.
- [ ] Create an Amazon EventBridge event with a cloudtrail.amazonaws.com event source and a StartLogging event name to invoke an AWS Lambda function to call the StartLogging
API.
- [ ] Create an Amazon CloudWatch alarm with a cloudtrail.amazonaws.com event source and a StopLoggmg event name to invoke an AWS Lambda function to call the StartLogging API.
- [ ] Monitor AWS Trusted Advisor to ensure CloudTrail logging is enabled.

### A public subnet contains two Amazon EC2 instances. The subnet has a custom network ACL. A security engineer is designing a solution to improve the subnet security. The solution must allow outbound traffic to an internet service that uses TLS through port 443. The solution also must deny inbound traffic that is destined for MySQL port 3306. Which network ACL rule set meets these requirements?

- [x] Use inbound rule 100 to allow traffic on TCP port 443. Use inbound rule 200 to deny traffic on TCP port 3306. Use outbound rule 100 to allow traffic on TCP port 443.
- [ ] Use inbound rule 100 to deny traffic on TCP port 3306. Use inbound rule 200 to allow traffic on TCP port range 1024-65535. Use outbound rule 100 to allow traffic on TCP port 443.
- [ ] Use inbound rule 100 to allow traffic on TCP port range 1024-65535. Use inbound rule 200 to deny traffic on TCP port 3306. Use outbound rule 100 to allow traffic on TCP port 443.
- [ ] Use inbound rule 100 to deny traffic on TCP port 3306. Use inbound rule 200 to allow traffic on TCP port 443. Use outbound rule 100 to allow traffic on TCP port 443.

### A security engineer is configuring a mechanism to send an alert when three or more failed sign-in attempts to the AWS Management Console occur during a 5-minute period. The security engineer creates a trail in AWS CloudTrail to assist in this work. Which solution will meet these requirements?

- [ ] In CloudTrail, turn on Insights events on the trail. Configure an alarm on the insight with eventName matching ConsoleLogin and errorMessage matching "Failed authentication''. Configure a threshold of 3 and a period of 5 minutes.
- [x] Configure CloudTrail to send events to Amazon CloudWatch Logs. Create a metric filter for the relevant log group. Create a filter pattern with eventName matching ConsoleLogin and errorMessage matching "Failed authentication". Create a CloudWatch alarm with a threshold of 3 and a period of 5 minutes.
- [ ] Create an Amazon Athena table from the CloudTrail events. Run a query for eventName matching ConsoleLogin and for errorMessage matching "Failed authentication". Create a notification action from the query to send an Amazon Simple Notification Service (Amazon SNS) notification when the count equals 3 within a period of 5 minutes.
- [ ] In AWS Identity and Access Management Access Analyzer, create a new analyzer. Configure the analyzer to send an Amazon Simple Notification Service (Amazon SNS) notification when a failed sign-in event occurs 3 times for any IAM user within a period of 5 minutes.

### A company's security engineer receives an abuse notification from AWS. The notification indicates that someone is hosting malware from the company's AWS account. After investigation, the security engineer finds a new Amazon S3 bucket that an IAM user created without authorization. Which combination of steps should the security engineer take to MINIMIZE the consequences of this compromise? (Choose three.)

- [ ] Encrypt all AWS CloudTrail logs.
- [ ] Turn on Amazon GuardDuty.
- [x] Change the password for all IAM users.
- [x] Rotate or delete all AWS access keys.
- [ ] Take snapshots of all Amazon Elastic Block Store (Amazon EBS) volumes.
- [x] Delete any resources that are unrecognized or unauthorized.

### A company has a web server in the AWS Cloud. The company will store the content for the web server in an Amazon S3 bucket. A security engineer must use an Amazon CloudFront distribution to speed up delivery of the content. None of the files can be publicly accessible from the S3 bucket directly. Which solution will meet these requirements?

- [ ] Configure the permissions on the individual files in the S3 bucket so that only the CloudFront distribution has access to them.
- [x] Create an origin access control (OAC). Associate the OAC with the CloudFront distribution. Configure the S3 bucket permissions so that only the OAC can access the files in the S3 bucket.
- [ ] Create an S3 role in AWS Identity and Access Management (IAM). Allow only the CloudFront distribution to assume the role to access the files in the S3 bucket.
- [ ] Create an S3 bucket policy that uses only the CloudFront distribution ID as the principal and the Amazon Resource Name (ARN) as the target.

### A company does not allow the permanent installation of SSH keys onto an Amazon Linux 2 EC2 instance. However, three employees who have IAM user accounts require access to the EC2 instance. The employees must use an SSH session to perform critical duties. How can a security engineer provide the appropriate access to the EC2 instance to meet these requirements?

- [ ] Use AWS Systems Manager Inventory to select the EC2 instance and connect. Provide the IAM user accounts with the permissions to use Systems Manager Inventory.
- [ ] Use AWS Systems Manager Run Command to open an SSH connection to the EC2 instance. Provide the IAM user accounts with the permissions to use Run Command.
- [x] Use AWS Systems Manager Session Manager. Provide the IAM user accounts with the permissions to use Systems Manager Session Manager.
- [ ] Connect to the EC2 instance as the ec2-user through the AWS Management Console's EC2 SSH client method. Provide the IAM user accounts with access to use the EC2 service in the AWS Management Console.

### A company wants to prevent SSH access through the use of SSH key pairs for any Amazon Linux 2 Amazon EC2 instances in its AWS account. However, a system administrator occasionally will need to access these EC2 instances through SSH in an emergency. For auditing purposes, the company needs to record any commands that a user runs in an EC2 instance. What should a security engineer do to configure access to these EC2 instances to meet these requirements?

- [ ] Use the EC2 serial console. Configure the EC2 serial console to save all commands that are entered to an Amazon S3 bucket. Provide the EC2 instances with an IAM role that allows the EC2 serial console to access Amazon S3. Configure an IAM account for the system administrator. Provide an IAM policy that allows the IAM account to use the EC2 serial console.
- [ ] Use EC2 Instance Connect. Configure EC2 Instance Connect to save all commands that are entered to Amazon CloudWatch Logs. Provide the EC2 instances with an IAM role that allows the EC2 Instances to access CloudWatch Logs. Configure an IAM account for the system administrator. Provide an IAM policy that allows the IAM account to use EC2 Instance Connect.
- [ ] Use an EC2 key pair with an EC2 instance that needs SSH access. Access the EC2 instance with this key pair by using SSH. Configure the EC2 instance to save all commands that are entered to Amazon CloudWatch Logs. Provide the EC2 instance with an IAM role that allows the EC2 instance to access Amazon S3 and CloudWatch Logs.
- [x] Use AWS Systems Manager Session Manager. Configure Session Manager to save all commands that are entered in a session to an Amazon S3 bucket. Provide the EC2 instances with an IAM role that allows Systems Manager to manage the EC2 instances. Configure an IAM account for the system administrator. Provide an IAM policy that allows the IAM account to use Session Manager.

### A company is using AWS Organizations to manage multiple AWS accounts. The company has an application that allows users to assume the AppUser IAM role to download files from an Amazon S3 bucket that is encrypted with an AWS KMS CMK. However, when users try to access the files in the S3 bucket, they get an access denied error. What should a security engineer do to troubleshoot this error? (Choose three.)

- [x] Ensure the KMS policy allows the AppUser role to have permission to decrypt for the CMK.
- [x] Ensure the S3 bucket policy allows the AppUser role to have permission to get objects for the S3 bucket.
- [ ] Ensure the CMK was created before the S3 bucket.
- [ ] Ensure the S3 block public access feature is enabled for the S3 bucket.
- [ ] Ensure that automatic key rotation is disabled for the CMK.
- [x] Ensure the SCPs within Organizations allow access to the S3 bucket.

### A company is building applications in containers. The company wants to migrate its on-premises development and operations services from its on-premises data center to AWS. Management states that production systems must be cloud agnostic and use the same configuration and administrator tools across production systems. A solutions architect needs to design a managed solution that will align open-source software. Which solution meets these requirements?

- [ ] Launch the containers on Amazon EC2 with EC2 instance worker nodes.
- [x] Launch the containers on Amazon Elastic Kubernetes Service (Amazon EKS) and EKS worker nodes.
- [ ] Launch the containers on Amazon Elastic Containers service (Amazon ECS) with AWS Fargate instances.
- [ ] Launch the containers on Amazon Elastic Container Service (Amazon ECS) with Amazon EC2 instance worker nodes.

### A company uses infrastructure as code (IaC) to create AWS infrastructure. The company writes the code as AWS CloudFormation templates to deploy the infrastructure. The company has an existing CI/CD pipeline that the company can use to deploy these templates. After a recent security audit, the company decides to adopt a policy-as-code approach to improve the company's security posture on AWS. The company must prevent the deployment of any infrastructure that would violate a security policy, such as an unencrypted Amazon Elastic Block Store (Amazon EBS) volume. Which solution will meet these requirements?

- [ ] Turn on AWS Trusted Advisor. Configure security notifications as webhooks in the preferences section of the CI/CD pipeline.
- [ ] Turn on AWS Config. Use the prebuilt rules or customized rules. Subscribe tile CI/CD pipeline to an Amazon Simple Notification Service (Amazon SNS) topic that receives notifications from AWS Config.
- [x] Create rule sets in AWS CloudFormation Guard. Run validation checks for CloudFormation templates as a phase of the CI/CD process.
- [ ] Create rule sets as SCPs. Integrate the SCPs as a part of validation control in a phase of the CI/CD process.

### A security engineer is setting up a new AWS account. The engineer has been asked to continuously monitor the company's AWS account using automated compliance checks based on AWS best practices and Center for Internet Security (CIS) AWS Foundations Benchmarks. How can the security engineer accomplish this using AWS services?

- [x] Enable AWS Config and set it to record all resources in all Regions and global resources. Then enable AWS Security Hub and confirm that the CIS AWS Foundations compliance standard is enabled.
- [ ] Enable Amazon Inspector and configure it to scan all Regions for the CIS AWS Foundations Benchmarks. Then enable AWS Security Hub and configure it to ingest the Amazon Inspector findings.
- [ ] Enable Amazon Inspector and configure it to scan all Regions for the CIS AWS Foundations Benchmarks. Then enable AWS Shield in all Regions to protect the account from DDoS attacks.
- [ ] Enable AWS Config and set it to record all resources in all Regions and global resources. Then enable Amazon Inspector and configure it to enforce CIS AWS Foundations Benchmarks using AWS Config rules.

### A company uses AWS Organizations to manage several AWs accounts. The company processes a large volume of sensitive data. The company uses a serverless approach to microservices. The company stores all the data in either Amazon S3 or Amazon DynamoDB. The company reads the data by using either AWS Lambda functions or container-based services that the company hosts on Amazon Elastic Kubernetes Service (Amazon EKS) on AWS Fargate. The company must implement a solution to encrypt all the data at rest and enforce least privilege data access controls. The company creates an AWS Key Management Service (AWS KMS) customer managed key. What should the company do next to meet these requirements?

- [ ] Create a key policy that allows the `kms:Decrypt` action only for Amazon S3 and DynamoDB. Create an SCP that denies the creation of S3 buckets and DynamoDB tables that are not encrypted with the key.
- [ ] Create an IAM policy that denies the `kms:Decrypt` action for the key. Create a Lambda function than runs on a schedule to attach the policy to any new roles. Create an AWS Config rule to send alerts for resources that are not encrypted with the key.
- [x] Create a key policy that allows the `kms:Decrypt` action only for Amazon S3, DynamoDB, Lambda, and Amazon EKS. Create an SCP that denies the creation of S3 buckets and DynamoDB tables that are not encrypted with the key.
- [ ] Create a key policy that allows the kms:Decrypt action only for Amazon S3, DynamoDB, Lambda, and Amazon EKS. Create an AWS Config rule to send alerts for resources that are not encrypted with the key.

### A security engineer is configuring AWS Config for an AWS account that uses a new IAM entity. When the security engineer tries to configure AWS Config rules and automatic remediation options, errors occur. In the AWS CloudTrail logs, the security engineer sees the following error message: `Insufficient delivery policy to s3 bucket: DOC-EXAMPLE-BUCKET, unable to write to bucket, provided s3 key prefix is 'null'.` Which combination of steps should the security engineer take to remediate this issue? (Choose two.)

- [x] Check the Amazon S3 bucket policy. Verify that the policy allows the config amazonaws,com service to write to the target bucket.
- [x] Verify that the IAM entity has the permissions necessary to perform the `s3:GetBucketAcl and s3:PutObject*` operations to write to the target bucket.
- [ ] Verify that the Amazon S3 bucket policy has the permissions necessary to perform the `s3:GetBucketAcl and s3:PutObject*` operations to write to the target bucket.
- [ ] Check the policy that is associated with the IAM entity. Verify that the policy allows the config.amazonaws.com service to write to the target bucket.
- [ ] Verify that the AWS Config service role has permissions to invoke the BatchGetResourceConfig action instead of the GetResourceConfigHistory action and `s3:PutObject*` operation.

### A company is running a legacy application on Amazon EC2 instances in multiple Availability Zones behind a software load balancer that runs on an active/standby set of EC2 instances. For disaster recovery, the company has created a warm standby version of the application environment that is deployed in another AWS Region. The domain for the application uses a hosted zone from Amazon Route 53. The company needs the application to use static IP addresses, even in the case of a failover event to the secondary Region. The company also requires the client's source IP address to be available for auditing purposes. Which solution meets these requirements with the LEAST amount of operational overhead?

- [x] Replace the software load balancer with an AWS Application Load Balancer. Create an AWS Global Accelerator accelerator. Add an endpoint group for each Region. Configure Route 53 health checks. Add an alias record that points to the accelerator.
- [ ] Replace the software load balancer with an AWS Network Load Balancer. Create an AWS Global Accelerator accelerator. Add an endpoint group for each Region. Configure Route 53 health checks. Add a CNAME record that points to the DNS name of the accelerator.
- [ ] Replace the software load balancer with an AWS Application Load Balancer. Use AWS Global Accelerator to create two separate accelerators. Add an endpoint group for each Region. Configure Route 53 health checks. Add a record set that is configured for active-passive DNS failover. Point the record set to the DNS names of the two accelerators.
- [ ] Replace the software load balancer with an AWS Network Load Balancer. Use AWS Global Accelerator to create two separate accelerators. Add an endpoint group for each Region. Configure Route 53 health checks. Add a record set that is configured for weighted round-robin DNS failover. Point the record set to the DNS names of the two accelerators.

### An online media company has an application that customers use to watch events around the world. The application is hosted on a fleet of Amazon EC2 instances that run Amazon Linux 2. The company uses AWS Systems Manager to manage the EC2 instances. The company applies patches and application updates by using the AWS-AmazonLinux2DefaultPatchBaseline patching baseline in Systems Manager Patch Manager. The company is concerned about potential attacks on the application during the week of an upcoming event. The company needs a solution that can immediately deploy patches to all the EC2 instances in response to a security incident or vulnerability. The solution also must provide centralized evidence that the patches were applied successfully. Which combination of steps will meet these requirements? (Choose two.)

- [x] Create a new patching baseline in Patch Manager. Specify Amazon Linux 2 as the product. Specify Security as the classification. Set the automatic approval for patches to 0 days. Ensure that the new patching baseline is the designated default for Amazon Linux 2.
- [x] Use the Patch Now option with the scan and install operation in the Patch Manager console to apply patches against the baseline to all nodes. Specify an Amazon S3 bucket as the patching log storage option.
- [ ] Use the Clone function of Patch Manager to create a copy of the AWS-AmazonLmux2DefaultPatchBaseline built-in baseline. Set the automatic approval for patches to 1 day.
- [ ] Create a patch policy that patches all managed nodes and sends a patch operation log output to an Amazon S3 bucket. Use a custom scan schedule to set Patch Manager to check every hour for new patches. Assign the baseline to the patch policy.
- [ ] Use Systems Manager Application Manager to inspect the package versions that were installed on the EC2 instances. Additionally use Application Manager to validate that the patches were correctly installed.

### A company's data lake uses Amazon S3 and Amazon Athena. The company's security engineer has been asked to design an encryption solution that meets the company's data protection requirements. The encryption solution must work with Amazon S3 and keys managed by the company. The encryption solution must be protected in a hardware security module that is validated to Federal Information Processing Standards (FIPS) 140-2 Level 3. Which solution meets these requirements?

- [ ] Use client-side encryption with an AWS KMS customer-managed key implemented with the AWS Encryption SDK.
- [ ] Use AWS CloudHSM to store the keys and perform cryptographic operations. Save the encrypted text in Amazon S3.
- [x] Use an AWS KMS customer-managed key that is backed by a custom key store using AWS CloudHSM.
- [ ] Use an AWS KMS customer-managed key with the bring your own key (BYOK) feature to import a key stored in AWS CloudHSM.

### A company has a serverless application that uses AWS Lambda functions and AWS Systems Manager parameters to store configuration data. The company moves the Lambda functions inside the VPC and into private subnets. The Lambda functions are now producing errors in their attempts to access Systems Manager parameters. Which solution will allow the Lambda functions to access Systems Manager parameters inside the VPC?

- [ ] Configure security groups to allow access to Systems Manager.
- [x] Create an interface VPC endpoint for Systems Manager.
- [ ] Use an Internet gateway from inside the VPC.
- [ ] Create a gateway VPC endpoint for Systems Manager.

### A company has an application on Amazon EC2 instances that store confidential customer data. The company must restrict access to customer data. A security engineer requires secure access to the instances that host the application. According to company policy, users must not open any inbound ports, maintain bastion hosts, or manage SSH keys for the EC2 instances. The security engineer wants to monitor, store, and access all session activity logs. The logs must be encrypted. Which solution will meet these requirements?

- [ ] Use AWS Control Tower to connect to the EC2 instances. Configure Amazon CloudWatch logging for the sessions. Select the upload session logs option and allow only encrypted CloudWatch Logs log groups.
- [ ] Use AWS Security Hub to connect to the EC2 instances. Configure Amazon CloudWatch logging for the sessions. Select the upload session logs option and allow only encrypted CloudWatch Logs log groups.
- [ ] Use AWS Systems Manager Session Manager to connect to the EC2 instances. Configure Amazon CloudWatch monitoring to record the sessions. Select the store session logs option for the desired CloudWatch Logs log groups.
- [x] Use AWS Systems Manager Session Manager to connect to the EC2 instances. Configure Amazon CloudWatch logging. Select the upload session logs option and allow only encrypted CloudWatch Logs log groups.

### A company's security policy requires that VPC Flow Logs are enabled on all VPCs. A Security Engineer is looking to automate the process of auditing the VPC resources for compliance. What combination of actions should the Engineer take? (Choose two.)

- [x] Create an AWS Lambda function that determines whether Flow Logs are enabled for a given VPC.
- [ ] Create an AWS Config configuration item for each VPC in the company AWS account.
- [ ] Create an AWS Config managed rule with a resource type of AWS:: Lambda:: Function.
- [ ] Create an Amazon CloudWatch Event rule that triggers on events emitted by AWS Config.
- [x] Create an AWS Config custom rule, and associate it with an AWS Lambda function that contains the evaluating logic.

### A security engineer is creating an AWS Lambda function. The Lambda function needs to use a role that is named LambdaAuditRole to assume a role that is named AcmeAuditFactoryRole in a different AWS account. When the code is processed, the following error message appears: `An error occurred (AccessDenied) when calling the AssumeRole operation.` Which combination of steps should the security engineer take to resolve this error? (Choose two.)

- [x] Ensure that LambdaAuditRole has the `sts:AssumeRole` permission for AcmeAuditFactoryRole.
- [ ] Ensure that LambdaAuditRole has the AWSLambdaBasicExecutionRole managed policy attached.
- [x] Ensure that the trust policy for AcmeAuditFactoryRole allows the `sts:AssumeRole` action from LambdaAuditRole.
- [ ] Ensure that the trust policy for LambdaAuditRole allows the `sts:AssumeRole` action from the lambda.amazonaws.com service.
- [ ] Ensure that the `sts:AssumeRole` API call is being issued to the us-east-1 Region endpoint.

### A company's application uses Amazon DynamoDB to store data. The company's security policy requires all data to be encrypted at rest. The security policy also requires the company to use an on-premises hardware security module (HSM) to generate and manage the company's encryption keys. A security engineer uses the on-premises HSM to generate an encryption key. What should the security engineer do next to meet these requirements?

- [x] Generate a new AWS Key Management Service (AWS KMS) customer managed key. Import the new key material. Grant DynamoDB access to use the key. Create a new DynamoDB table, and select the new key as the encryption key. Import the data into DynamoDB.
- [ ] Generate a new AWS Key Management Service (AWS KMS) customer managed key. Import the new key material. Create a new DynamoDB table, and select the new key as the encryption key. Disable the KMS key after table creation. Import the data into DynamoDB.
- [ ] Generate a new AWS Key Management Service (AWS KMS) AWS managed key. Import the new key material. Grant DynamoDB access to use the key. Create a new DynamoDB table, and select the new key as the encryption key. Import the data into DynamoDB.
- [ ] Generate a new AWS Key Management Service (AWS KMS) AWS managed key. Import the new key material. Use the AWS SDK integration with AWS KMS to encrypt the data locally by using the new KMS key. Create a new DynamoDB table, and select the new key as the encryption key. Disable the KMS key after table creation. Import the data into DynamoDB.

### A security engineer has noticed that VPC Flow Logs are getting a lot of REJECT traffic originating from a single Amazon EC2 instance in an Auto Scaling group. The security engineer is concerned that this EC2 instance may be compromised. What immediate action should the security engineer take?

- [x] Remove the instance from the Auto Scaling group. Close the security group with ingress only from a single forensic IP address to perform an analysis.
- [ ] Remove the instance from the Auto Scaling group. Change the network ACL rules to allow traffic only from a single forensic IP address to perform an analysis. Add a rule to deny all other traffic.
- [ ] Remove the instance from the Auto Scaling group. Enable Amazon GuardDuty in that AWS account. Install the Amazon Inspector agent on the suspicious EC2 instance to perform a scan.
- [ ] Take a snapshot of the suspicious EC2 instance. Create a new EC2 instance from the snapshot in a closed security group with ingress only from a single forensic IP address to perform an analysis.

### A company is running its workloads in a single AWS Region and uses AWS Organizations. A security engineer must implement a solution to prevent users from launching resources in other Regions. Which solution will meet these requirements with the LEAST operational overhead?

- [ ] Create an IAM policy that has an `aws:RequestedRegion` condition that allows actions only in the designated Region. Attach the policy to all users.
- [ ] Create an IAM policy that has an `aws:RequestedRegion` condition that denies actions that are not in the designated Region. Attach the policy to the AWS account in AWS Organizations.
- [ ] Create an IAM policy that has an `aws:RequestedRegion` condition that allows the desired actions. Attach the policy only to the users who are in the designated Region.
- [x] Create an SCP that has an `aws:RequestedRegion` condition that denies actions that are not in the designated Region. Attach the SCP to the AWS account in AWS Organizations.

### A security engineer is evaluating a company's use of AWS Key Management Service (AWS KMS). The security engineer must implement a hybrid solution with two sets of keys to meet the following requirements: Set 1: The company needs granular control over the keys so that the company can maintain a copy of the keys in the key management infrastructure and reimport the keys at any time. The company needs the ability to set the expiration period to 3 days for the keys. Set 2: No restrictions exist regarding immediate key deletion. A waiting period of 14 days is acceptable for keys to be marked deleted. Which solution will meet these requirements?

- [ ] Use imported keys for Set 1. Use AWS managed keys for Set 2. For Set 1, set an expiration period and manually delete the keys after the expiration period has elapsed.
- [x] Use imported keys for Set 1. Use AWS managed keys for Set 2. For Set 1, set an expiration period. AWS will automatically delete the keys after the expiration period has elapsed.
- [ ] Use AWS managed keys for Set 1. Use imported keys for Set 2. For Set 1, set an expiration period and manually delete the keys after the expiration period has elapsed.
- [ ] Use AWS managed keys for Set 1. Use imported keys for Set 2. For Set 1, set an expiration period. AWS will automatically delete the keys after the expiration period has elapsed.

### A company operates a web application that runs on Amazon EC2 instances. The application listens on port 80 and port 443. The company uses an Application Load Balancer (ALB) with AWS WAF to terminate SSL and to forward traffic to the application instances only on port 80. The ALB is in public subnets that are associated with a network ACL that is named NACL. The application instances are in dedicated private subnets that are associated with a network ACL that is named NACL2. An Amazon RDS for PostgreSQL DB instance that uses port 5432 is in a dedicated private subnet that is associated with a network ACL that is named NACL3. All the network ACLs currently allow all inbound and outbound traffic. Which set of network ACL changes will increase the security of the application while ensuring functionality?

- [ ] Make the following changes to NACL3: Add a rule that allows inbound traffic on port 5432 from NACL2. Add a rule that allows outbound traffic on ports 1024-65536 to NACL2. Remove the default rules that allow all inbound and outbound traffic.
- [x] Make the following changes to NACL3: Add a rule that allows inbound traffic on port 5432 from the CIDR blocks of the application instance subnets. Add a rule that allows outbound traffic on ports 1024-65536 to the application instance subnets. Remove the default rules that allow all inbound and outbound traffic.
- [ ] Make the following changes to NACL2: Add a rule that allows outbound traffic on port 5432 to the CIDR blocks of the RDS subnets. Remove the default rules that allow all inbound and outbound traffic.
- [ ] Make the following changes to NACL2: Add a rule that allows inbound traffic on port 5432 from the CIDR blocks of the RDS subnets. Add a rule that allows outbound traffic on port 5432 to the RDS subnets.

### The Security team believes that a former employee may have gained unauthorized access to AWS resources sometime in the past 3 months by using an identified access key. What approach would enable the Security team to find out what the former employee may have done within AWS?

![Question 290](images/question290.png)

- [x] Use the AWS CloudTrail console to search for user activity.
- [ ] Use the Amazon CloudWatch Logs console to filter CloudTrail data by user.
- [ ] Use AWS Config to see what actions were taken by the user.
- [ ] Use Amazon Athena to query CloudTrail logs stored in Amazon S3.

### A company is storing data in Amazon S3 Glacier. The security engineer implemented a new vault lock policy for 10TB of data and called initiate-vault-lock operation 12 hours ago. The audit team identified a typo in the policy that is allowing unintended access to the vault. What is the MOST cost-effective way to correct this?

- [x] Call the abort-vault-lock operation. Update the policy. Call the initiate-vault-lock operation again.
- [ ] Copy the vault data to a new S3 bucket. Delete the vault. Create a new vault with the data.
- [ ] Update the policy to keep the vault lock in place.
- [ ] Update the policy. Call initiate-vault-lock operation again to apply the new policy.

### A company wants to control access to its AWS resources by using identities and groups that are defined in its existing Microsoft Active Directory.What must the company create in its AWS account to map permissions for AWS services to Active Directory user attributes?

- [ ] AWS IAM groups.
- [ ] AWS IAM users.
- [x] AWS IAM roles.
- [ ] AWS IAM access keys.

### A company has contracted with a third party to audit several AWS accounts. To enable the audit, cross-account IAM roles have been created in each account targeted for audit. The Auditor is having trouble accessing some of the accounts. Which of the following may be causing this problem? (Choose three.).

- [ ] The external ID used by the Auditor is missing or incorrect.
- [ ] The Auditor is using the incorrect password.
- [x] The Auditor has not been granted sts:AssumeRole for the role in the destination account.
- [ ] The Amazon EC2 role used by the Auditor must be set to the destination account role.
- [x] The secret key used by the Auditor is missing or incorrect.
- [x] The role ARN used by the Auditor is missing or incorrect.

### Compliance requirements state that all communications between company on-premises hosts and EC2 instances be encrypted in transit. Hosts use custom proprietary protocols for their communication, and EC2 instances need to be fronted by a load balancer for increased availability. Which of the following solutions will meet these requirements?

- [ ] Offload SSL termination onto an SSL listener on a Classic Load Balancer, and use a TCP connection between the load balancer and the EC2 instances.
- [x] Route all traffic through a TCP listener on a Classic Load Balancer, and terminate the TLS connection on the EC2 instances.
- [ ] Create an HTTPS listener using an Application Load Balancer, and route all of the communication through that load balancer.
- [ ] Offload SSL termination onto an SSL listener using an Application Load Balancer, and re-spawn and SSL connection between the load balancer and the EC2 instances.

### A Security Administrator is restricting the capabilities of company root user accounts. The company uses AWS Organizations and has enabled it for all feature sets, including consolidated billing. The top-level account is used for billing and administrative purposes, not for operational AWS resource purposes. How can the Administrator restrict usage of member root user accounts across the organization?

- [ ] Disable the use of the root user account at the organizational root. Enable multi-factor authentication of the root user account for each organizational member account.
- [ ] Configure IAM user policies to restrict root account capabilities for each Organizations member account.
- [x] Create an organizational unit (OU) in Organizations with a service control policy that controls usage of the root user. Add all operational accounts to the new OU.
- [ ] Configure AWS CloudTrail to integrate with Amazon CloudWatch Logs and then create a metric filter for RootAccountUsage.

### A Systems Engineer has been tasked with configuring outbound mail through Simple Email Service (SES) and requires compliance with current TLS standards. The mail application should be configured to connect to which of the following endpoints and corresponding ports?

- [ ] email.us-east-1.amazonaws.com over port 8080.
- [ ] email-pop3.us-east-1.amazonaws.com over port 995.
- [x] email-smtp.us-east-1.amazonaws.com over port 587.
- [ ] email-imap.us-east-1.amazonaws.com over port 993.

### A threat assessment has identified a risk whereby an internal employee could exfiltrate sensitive data from production host running inside AWS (Account 1). The threat was documented as follows: Threat description: A malicious actor could upload sensitive data from Server X by configuring credentials for an AWS account (Account 2) they control and uploading data to an Amazon S3 bucket within their control. Server X has outbound internet access configured via a proxy server. Legitimate access to S3 is required so that the application can upload encrypted files to an S3 bucket. Server X is currently using an IAM instance role. The proxy server is not able to inspect any of the server communication due to TLS encryption. Which of the following options will mitigate the threat? (Choose two.)

- [x] Bypass the proxy and use an S3 VPC endpoint with a policy that whitelists only certain S3 buckets within Account 1.
- [ ] Block outbound access to public S3 endpoints on the proxy server.
- [x] Configure Network ACLs on Server X to deny access to S3 endpoints.
- [ ] Modify the S3 bucket policy for the legitimate bucket to allow access only from the public IP addresses associated with the application server.
- [ ] Remove the IAM instance role from the application server and save API access keys in a trusted and encrypted application config file.

### A company will store sensitive documents in three Amazon S3 buckets based on a data classification scheme of `Sensitive,` `Confidential,` and `Restricted.` The security solution must meet all of the following requirements:  Each object must be encrypted using a unique key. Items that are stored in the `Restricted` bucket require two-factor authentication for decryption. AWS KMS must automatically rotate encryption keys annually. Which of the following meets these requirements?

- [x] Create a Customer Master Key (CMK) for each data classification type, and enable the rotation of it annually. For the "Restricted" CMK, define the MFA policy within the key policy. Use S3 SSE-KMS to encrypt the objects.
- [ ]  Create a CMK grant for each data classification type with EnableKeyRotation and MultiFactorAuthPresent set to `true`. S3 can then use the grants to encrypt each object with a unique CMK.
- [ ] Create a CMK for each data classification type, and within the CMK policy, enable rotation of it annually, and define the MFA policy. S3 can then create DEK grants to uniquely encrypt each object within the S3 bucket.
- [ ] Create a CMK with unique imported key material for each data classification type, and rotate them annually. For the "Restricted" key material, define the MFA policy in the key policy. Use S3 SSE-KMS to encrypt the objects.

### An organization wants to deploy a three-tier web application whereby the application servers run on Amazon EC2 instances. These EC2 instances need access to credentials that they will use to authenticate their SQL connections to an Amazon RDS DB instance. Also, AWS Lambda functions must issue queries to the RDS database by using the same database credentials. The credentials must be stored so that the EC2 instances and the Lambda functions can access them. No other access is allowed. The access logs must record when the credentials were accessed and by whom. What should the Security Engineer do to meet these requirements?

- [ ]  Store the database credentials in AWS Key Management Service (AWS KMS). Create an IAM role with access to AWS KMS by using the EC2 and Lambda service principals in the role's trust policy. Add the role to an EC2 instance profile. Attach the instance profile to the EC2 instances. Set up Lambda to use the new role for execution.
- [ ] Store the database credentials in AWS KMS. Create an IAM role with access to KMS by using the EC2 and Lambda service principals in the role's trust policy. Add the role to an EC2 instance profile. Attach the instance profile to the EC2 instances and the Lambda function.
- [ ] Store the database credentials in AWS Secrets Manager. Create an IAM role with access to Secrets Manager by using the EC2 and Lambda service principals in the role's trust policy. Add the role to an EC2 instance profile. Attach the instance profile to the EC2 instances and the Lambda function.
- [x]  Store the database credentials in AWS Secrets Manager. Create an IAM role with access to Secrets Manager by using the EC2 and Lambda service principals in the role's trust policy. Add the role to an EC2 instance profile. Attach the instance profile to the EC2 instances. Set up Lambda to use the new role for execution.

### A water utility company uses a number of Amazon EC2 instances to manage updates to a fleet of 2,000 Internet of Things (IoT) field devices that monitor water quality. These devices each have unique access credentials. An operational safety policy requires that access to specific credentials is independently auditable. What is the MOST cost-effective way to manage the storage of credentials?

- [x] Use AWS Systems Manager to store the credentials as Secure Strings Parameters. Secure by using an AWS KMS key.
- [ ] Use AWS Key Management System to store a master key, which is used to encrypt the credentials. The encrypted credentials are stored in an Amazon RDS instance.
- [ ] Use AWS Secrets Manager to store the credentials.
- [ ] Store the credentials in a JSON file on Amazon S3 with server-side encryption.

### An organization is using Amazon CloudWatch Logs with agents deployed on its Linux Amazon EC2 instances. The agent configuration files have been checked and the application log files to be pushed are configured correctly. A review has identified that logging from specific instances is missing. Which steps should be taken to troubleshoot the issue? (Choose two.)

- [ ] Use an EC2 run command to confirm that the "awslogs" service is running on all instances.
- [x] Verify that the permissions used by the agent allow creation of log groups/streams and to put log events.
- [x] Check whether any application log entries were rejected because of invalid time stamps by reviewing /var/cwlogs/rejects.log.
- [ ] Check that the trust relationship grants the service "cwlogs.amazonaws.com" permission to write objects to the Amazon S3 staging bucket.
- [ ] Verify that the time zone on the application servers is in UTC.

### A Security Engineer must design a solution that enables the incident Response team to audit for changes to a user's IAM permissions in the case of a security incident. How can this be accomplished?

- [x] Use AWS Config to review the IAM policy assigned to users before and after the incident.
- [ ] Run the GenerateCredentialReport via the AWS CLI, and copy the output to Amazon S3 daily for auditing purposes.
- [ ] Copy AWS CloudFormation templates to S3, and audit for changes from the template.
- [ ] Use Amazon EC2 Systems Manager to deploy images, and review AWS CloudTrail logs for changes.

### A company has complex connectivity rules governing ingress, egress, and communications between Amazon EC2 instances. The rules are so complex that they cannot be implemented within the limits of the maximum number of security groups and network access control lists (network ACLs). What mechanism will allow the company to implement all required network rules without incurring additional cost?

- [ ] Configure AWS WAF rules to implement the required rules.
- [x] Use the operating system built-in, host-based firewall to implement the required rules.
- [ ] Use a NAT gateway to control ingress and egress according to the requirements.
- [ ] Launch an EC2-based firewall product from the AWS Marketplace, and implement the required rules in that product.

### An IAM user with fill EC2 permissions could bot start an Amazon EC2 instance after it was stopped for a maintenance task. Upon starting the instance, the instance state would change to `Pending`, but after a few seconds, it would switch back to `Stopped`. An inspection revealed that the instance has attached Amazon EBS volumes that were encrypted by using a Customer Master Key (CMK). When these encrypted volumes were detached, the IAM user was able to start the EC2 instances. The IAM user policy is as follows: What additional items need to be added to the IAM user policy? (Choose two.)

- [ ] kms:GenerateDataKey.
- [ ] kms:Decrypt.
- [x] kms:CreateGrant.
- [ ] "Condition": { "Bool": { "kms:ViaService": "ec2.us-west-2.amazonaws.com" } }.
- [x] "Condition": { "Bool": { "kms:GrantIsForAWSResource": true } }.

### A Security Administrator has a website hosted in Amazon S3. The Administrator has been given the following requirements: Users may access the website by using an Amazon CloudFront distribution. Users may not access the website directly by using an Amazon S3 URL. Which configurations will support these requirements? (Choose two.)

- [x] Associate an origin access identity with the CloudFront distribution.
- [ ] Implement a "Principal": "cloudfront.amazonaws.com" condition in the S3 bucket policy.
- [x] Modify the S3 bucket permissions so that only the origin access identity can access the bucket contents.
- [ ] Implement security groups so that the S3 bucket can be accessed only by using the intended CloudFront distribution.
- [ ] Configure the S3 bucket policy so that it is accessible only through VPC endpoints, and place the CloudFront distribution into the specified VPC.

### A company requires that IP packet data be inspected for invalid or malicious content. Which of the following approaches achieve this requirement? (Choose two.)

- [ ] Configure a proxy solution on Amazon EC2 and route all outbound VPC traffic through it. Perform inspection within proxy software on the EC2 instance.
- [ ] Configure the host-based agent on each EC2 instance within the VPC. Perform inspection within the host-based agent.
- [ ] Enable VPC Flow Logs for all subnets in the VPC. Perform inspection from the Flow Log data within Amazon CloudWatch Logs.
- [ ] Configure Elastic Load Balancing (ELB) access logs. Perform inspection from the log data within the ELB access log files.
- [x]  Configure the CloudWatch Logs agent on each EC2 instance within the VPC. Perform inspection from the log data within CloudWatch Logs.

### An organization has a system in AWS that allows a large number of remote workers to submit data files. File sizes vary from a few kilobytes to several megabytes. A recent audit highlighted a concern that data files are not encrypted while in transit over untrusted networks. Which solution would remediate the audit finding while minimizing the effort required?

- [ ] Upload an SSL certificate to IAM, and configure Amazon CloudFront with the passphrase for the private key.
- [ ] Call KMS.Encrypt() in the client, passing in the data file contents, and call KMS.Decrypt() server-side.
- [x] Use AWS Certificate Manager to provision a certificate on an Elastic Load Balancing in front of the web service's servers.
- [ ] Create a new VPC with an Amazon VPC VPN endpoint, and update the web service's DNS record.

### Which option for the use of the AWS Key Management Service (KMS) supports key management best practices that focus on minimizing the potential scope of data exposed by a possible future key compromise?

- [x] Use KMS automatic key rotation to replace the master key, and use this new master key for future encryption operations without re-encrypting previously encrypted data.
- [ ] Generate a new Customer Master Key (CMK), re-encrypt all existing data with the new CMK, and use it for all future encryption operations.
- [ ] Change the CMK alias every 90 days, and update key-calling applications with the new key alias.
- [ ] Change the CMK permissions to ensure that individuals who can provision keys are not the same individuals who can use the keys.

### A Security Engineer must enforce the use of only Amazon EC2, Amazon S3, Amazon RDS, Amazon DynamoDB, and AWS STS in specific accounts. What is a scalable and efficient approach to meet this requirement?

![Question 309](images/question309_1.png)
![Question 309](images/question309_2.png)
![Question 309](images/question309_3.png)
![Question 309](images/question309_4.png)

- [x] Set up an AWS Organizations hierarchy, and replace the FullAWSAccess policy with the following Service Control Policy for the governed organization units:
- [ ] Create multiple IAM users for the regulated accounts, and attach the following policy statement to restrict services as required:
- [ ] Set up all users in the Active Directory for federated access to all accounts in the company. Associate Active Directory groups with IAM groups, and attach the
- [ ]  Set up all users in the Active Directory for federated access to all accounts in the company. Associate Active Directory groups with IAM groups, and attach the following policy statement to restrict services as required:

### A company's database developer has just migrated an Amazon RDS database credential to be stored and managed by AWS Secrets Manager. The developer has also enabled rotation of the credential within the Secrets Manager console and set the rotation to change every 30 days. After a short period of time, a number of existing applications have failed with authentication errors. What is the MOST likely cause of the authentication errors?

- [x] Migrating the credential to RDS requires that all access come through requests to the Secrets Manager.
- [ ] Enabling rotation in Secrets Manager causes the secret to rotate immediately, and the applications are using the earlier credential.
- [ ] The Secrets Manager IAM policy does not allow access to the RDS database.
- [ ] The Secrets Manager IAM policy does not allow access for the applications.

### The Security Engineer is managing a web application that processes highly sensitive personal information. The application runs on Amazon EC2. The application has strict compliance requirements, which instruct that all incoming traffic to the application is protected from common web exploits and that all outgoing traffic from the EC2 instances is restricted to specific whitelisted URLs. Which architecture should the Security Engineer use to meet these requirements?

- [ ] Use AWS Shield to scan inbound traffic for web exploits. Use VPC Flow Logs and AWS Lambda to restrict egress traffic to specific whitelisted URLs.
- [ ] Use AWS Shield to scan inbound traffic for web exploits. Use a third-party AWS Marketplace solution to restrict egress traffic to specific whitelisted URLs.
- [ ] Use AWS WAF to scan inbound traffic for web exploits. Use VPC Flow Logs and AWS Lambda to restrict egress traffic to specific whitelisted URLs.
- [x] Use AWS WAF to scan inbound traffic for web exploits. Use a third-party AWS Marketplace solution to restrict egress traffic to specific whitelisted URLs.

### A company recently experienced a DDoS attack that prevented its web server from serving content. The website is static and hosts only HTML, CSS, and PDF files that users download. Based on the architecture shown in the image, what is the BEST way to protect the site against future attacks while minimizing the ongoing operational overhead?

![Question 312](images/question312.jpg)

- [x] Move all the files to an Amazon S3 bucket. Have the web server serve the files from the S3 bucket.
- [ ] Launch a second Amazon EC2 instance in a new subnet. Launch an Application Load Balancer in front of both instances.
- [ ] Launch an Application Load Balancer in front of the EC2 instance. Create an Amazon CloudFront distribution in front of the Application Load Balancer.
- [ ] Move all the files to an S3 bucket. Create a CloudFront distribution in front of the bucket and terminate the web server.

### The Information Technology department has stopped using Classic Load Balancers and switched to Application Load Balancers to save costs. After the switch, some users on older devices are no longer able to connect to the website. What is causing this situation?

- [ ] Application Load Balancers do not support older web browsers.
- [ ] The Perfect Forward Secrecy settings are not configured correctly.
- [ ] The intermediate certificate is installed within the Application Load Balancer.
- [x] The cipher suites on the Application Load Balancers are blocking connections.

### A security team is responsible for reviewing AWS API call activity in the cloud environment for security violations. These events must be recorded and retained in a centralized location for both current and future AWS regions. What is the SIMPLEST way to meet these requirements?

- [ ] Enable AWS Trusted Advisor security checks in the AWS Console, and report all security incidents for all regions.
- [x] Enable AWS CloudTrail by creating individual trails for each region, and specify a single Amazon S3 bucket to receive log files for later analysis.
- [ ] Enable AWS CloudTrail by creating a new trail and applying the trail to all regions. Specify a single Amazon S3 bucket as the storage location.
- [ ] Enable Amazon CloudWatch logging for all AWS services across all regions, and aggregate them to a single Amazon S3 bucket for later analysis.

### A Security Administrator is performing a log analysis as a result of a suspected AWS account compromise. The Administrator wants to analyze suspicious AWS CloudTrail log files but is overwhelmed by the volume of audit logs being generated. What approach enables the Administrator to search through the logs MOST efficiently?

- [ ] Implement a "write-only" CloudTrail event filter to detect any modifications to the AWS account resources.
- [ ] Configure Amazon Macie to classify and discover sensitive data in the Amazon S3 bucket that contains the CloudTrail audit logs.
- [x] Configure Amazon Athena to read from the CloudTrail S3 bucket and query the logs to examine account activities.
- [ ] Enable Amazon S3 event notifications to trigger an AWS Lambda function that sends an email alarm when there are new CloudTrail API entries.

### During a recent security audit, it was discovered that multiple teams in a large organization have placed restricted data in multiple Amazon S3 buckets, and the data may have been exposed. The auditor has requested that the organization identify all possible objects that contain personally identifiable information (PII) and then determine whether this information has been accessed. What solution will allow the Security team to complete this request?

- [ ] Using Amazon Athena, query the impacted S3 buckets by using the PII query identifier function. Then, create a new Amazon CloudWatch metric for Amazon S3 object access to alert when the objects are accessed.
- [x] Enable Amazon Macie on the S3 buckets that were impacted, then perform data classification. For identified objects that contain PII, use the research function for auditing AWS CloudTrail logs and S3 bucket logs for GET operations.
- [ ] Enable Amazon GuardDuty and enable the PII rule set on the S3 buckets that were impacted, then perform data classification. Using the PII findings report from GuardDuty, query the S3 bucket logs by using Athena for GET operations.
- [ ] Enable Amazon Inspector on the S3 buckets that were impacted, then perform data classification. For identified objects that contain PII, query the S3 bucket logs by using Athena for GET operations.

### During a recent internal investigation, it was discovered that all API logging was disabled in a production account, and the root user had created new API keys that appear to have been used several times. What could have been done to detect and automatically remediate the incident?

- [ ] Using Amazon Inspector, review all of the API calls and configure the inspector agent to leverage SNS topics to notify security of the change to AWS CloudTrail, and revoke the new API keys for the root user.
- [ ] Using AWS Config, create a config rule that detects when AWS CloudTrail is disabled, as well as any calls to the root user create-api-key. Then use a Lambda function to re-enable CloudTrail logs and deactivate the root API keys.
- [x] Using Amazon CloudWatch, create a CloudWatch event that detects AWS CloudTrail deactivation and a separate Amazon Trusted Advisor check to automatically detect the creation of root API keys. Then use a Lambda function to enable AWS CloudTrail and deactivate the root API keys.
- [ ] Using Amazon CloudTrail, create a new CloudTrail event that detects the deactivation of CloudTrail logs, and a separate CloudTrail event that detects the creation of root API keys. Then use a Lambda function to enable CloudTrail and deactivate the root API keys.

### An application has a requirement to be resilient across not only Availability Zones within the application's primary region but also be available within another region altogether. Which of the following supports this requirement for AWS resources that are encrypted by AWS KMS?

- [ ] Copy the application's AWS KMS CMK from the source region to the target region so that it can be used to decrypt the resource after it is copied to the target region.
- [ ] Configure AWS KMS to automatically synchronize the CMK between regions so that it can be used to decrypt the resource in the target region.
- [x] Use AWS services that replicate data across regions, and re-wrap the data encryption key created in the source region by using the CMK in the target region so that the target region's CMK can decrypt the database encryption key.
- [ ] Configure the target region's AWS service to communicate with the source region's AWS KMS so that it can decrypt the resource in the target region.

### A Security Administrator is configuring an Amazon S3 bucket and must meet the following security requirements: Encryption in transit Encryption at rest Logging of all object retrievals in AWS CloudTrail Which of the following meet these security requirements? (Choose three.)

- [x] Specify "aws:SecureTransport": "true" within a condition in the S3 bucket policy.
- [ ] Enable a security group for the S3 bucket that allows port 443, but not port 80.
- [x] Set up default encryption for the S3 bucket.
- [ ] Enable Amazon CloudWatch Logs for the AWS account.
- [x] Enable API logging of data events for all S3 objects.
- [ ] Enable S3 object versioning for the S3 bucket.

### What is the function of the following AWS Key Management Service (KMS) key policy attached to a customer master key (CMK)?

![Question 322](images/question322.png)

- [ ] The Amazon WorkMail and Amazon SES services have delegated KMS encrypt and decrypt permissions to the ExampleUser principal in the 111122223333 account.
- [ ] The ExampleUser principal can transparently encrypt and decrypt email exchanges specifically between ExampleUser and AWS.
- [x] The CMK is to be used for encrypting and decrypting only when the principal is ExampleUser and the request comes from WorkMail or SES in the specified region.
- [ ] The key policy allows WorkMail or SES to encrypt or decrypt on behalf of the user for any CMK in the account.

### A Security Engineer who was reviewing AWS Key Management Service (AWS KMS) key policies found this statement in each key policy in the company AWS account. What does the statement allow?

![Question 323](images/question323.png)

- [ ] All principals from all AWS accounts to use the key.
- [ ] Only the root user from account 111122223333 to use the key.
- [ ] All principals from account 111122223333 to use the key but only on Amazon S3.
- [x] Only principals from account 111122223333 that have an IAM policy applied that grants access to this key to use the key.

### A Software Engineer wrote a customized reporting service that will run on a fleet of Amazon EC2 instances. The company security policy states that application logs for the reporting service must be centrally collected. What is the MOST efficient way to meet these requirements?

- [ ] Write an AWS Lambda function that logs into the EC2 instance to pull the application logs from the EC2 instance and persists them into an Amazon S3 bucket.
- [ ] . Enable AWS CloudTrail logging for the AWS account, create a new Amazon S3 bucket, and then configure Amazon CloudWatch Logs to receive the application logs from CloudTrail.
- [ ] Create a simple cron job on the EC2 instances that synchronizes the application logs to an Amazon S3 bucket by using rsync.
- [x] Install the Amazon CloudWatch Logs Agent on the EC2 instances, and configure it to send the application logs to CloudWatch Logs.

### A Security Engineer is trying to determine whether the encryption keys used in an AWS service are in compliance with certain regulatory standards. Which of the following actions should the Engineer perform to get further guidance?

- [ ] Read the AWS Customer Agreement.
- [x] Use AWS Artifact to access AWS compliance reports.
- [ ] Post the question on the AWS Discussion Forums.
- [ ] Run AWS Config and evaluate the configuration outputs.

### The Development team receives an error message each time the team members attempt to encrypt or decrypt a Secure String parameter from the SSM Parameter Store by using an AWS KMS customer managed key (CMK). Which CMK-related issues could be responsible? (Choose two.)

- [x] The CMK specified in the application does not exist.
- [ ] The CMK specified in the application is currently in use.
- [ ] The CMK specified in the application is using the CMK KeyID instead of CMK Amazon Resource Name.
- [x] The CMK specified in the application is not enabled.
- [ ] The CMK specified in the application is using an alias.

### An application has been written that publishes custom metrics to Amazon CloudWatch. Recently, IAM changes have been made on the account and the metrics are no longer being reported. Which of the following is the LEAST permissive solution that will allow the metrics to be delivered?

- [ ] Add a statement to the IAM policy used by the application to allow logs:putLogEvents and logs:createLogStream.
- [ ] Modify the IAM role used by the application by adding the CloudWatchFullAccess managed policy.
- [x] Add a statement to the IAM policy used by the application to allow cloudwatch:putMetricData.
- [ ] Add a trust relationship to the IAM role used by the application for cloudwatch.amazonaws.com.

### A Developer's laptop was stolen. The laptop was not encrypted, and it contained the SSH key used to access multiple Amazon EC2 instances. A SecurityEngineer has verified that the key has not been used, and has blocked port 22 to all EC2 instances while developing a response plan. How can the Security Engineer further protect currently running instances?

- [ ] Delete the key-pair key from the EC2 console, then create a new key pair.
- [ ] Use the modify-instance-attribute API to change the key on any EC2 instance that is using the key.
- [x] Use the EC2 RunCommand to modify the authorized_keys file on any EC2 instance that is using the key.
- [ ] Update the key pair in any AMI used to launch the EC2 instances, then restart the EC2 instances.

### An organization has tens of applications deployed on thousands of Amazon EC2 instances. During testing, the Application team needs information to let them know whether the network access control lists (network ACLs) and security groups are working as expected. How can the Application team's requirements be met?

- [x] Turn on VPC Flow Logs, send the logs to Amazon S3, and use Amazon Athena to query the logs.
- [ ] Install an Amazon Inspector agent on each EC2 instance, send the logs to Amazon S3, and use Amazon EMR to query the logs.
- [ ] Create an AWS Config rule for each network ACL and security group configuration, send the logs to Amazon S3, and use Amazon Athena to query the logs.
- [ ] Turn on AWS CloudTrail, send the trails to Amazon S3, and use AWS Lambda to query the trails.

### An application outputs logs to a text file. The logs must be continuously monitored for security incidents. Which design will meet the requirements with MINIMUM effort?

- [x] Create a scheduled process to copy the component's logs into Amazon S3. Use S3 events to trigger a Lambda function that updates Amazon CloudWatch metrics with the log data. Set up CloudWatch alerts based on the metrics.
- [ ] Install and configure the Amazon CloudWatch Logs agent on the application's EC2 instance. Create a CloudWatch metric filter to monitor the application logs. Set up CloudWatch alerts based on the metrics.
- [ ]  Create a scheduled process to copy the application log files to AWS CloudTrail. Use S3 events to trigger Lambda functions that update CloudWatch metrics with the log data. Set up CloudWatch alerts based on the metrics.
- [ ] Create a file watcher that copies data to Amazon Kinesis when the application writes to the log file. Have Kinesis trigger a Lambda function to update Amazon CloudWatch metrics with the log data. Set up CloudWatch alerts based on the metrics.

### The Security Engineer for a mobile game has to implement a method to authenticate users so that they can save their progress. Because most of the users are part of the same OpenID-Connect compatible social media website, the Security Engineer would like to use that as the identity provider. Which solution is the SIMPLEST way to allow the authentication of users using their social media identities?

- [x] Amazon Cognito.
- [ ] AssumeRoleWithWebIdentity API.
- [ ] Amazon Cloud Directory.
- [ ] Active Directory (AD) Connector.

### A Software Engineer is trying to figure out why network connectivity to an Amazon EC2 instance does not appear to be working correctly. Its security group allows inbound HTTP traffic from 0.0.0.0/0, and the outbound rules have not been modified from the default. A custom network ACL associated with its subnet allows inbound HTTP traffic from 0.0.0.0/0 and has no outbound rules. What would resolve the connectivity issue?

- [ ] The outbound rules on the security group do not allow the response to be sent to the client on the ephemeral port range.
- [ ] The outbound rules on the security group do not allow the response to be sent to the client on the HTTP port.
- [x] An outbound rule must be added to the network ACL to allow the response to be sent to the client on the ephemeral port range.
- [ ] An outbound rule must be added to the network ACL to allow the response to be sent to the client on the HTTP port.

### A Security Engineer has been asked to create an automated process to disable IAM user access keys that are more than three months old. Which of the following options should the Security Engineer use?

- [x] In the AWS Console, choose the IAM service and select "Users". Review the "Access Key Age" column.
- [ ] Define an IAM policy that denies access if the key age is more than three months and apply to all users.
- [ ] Write a script that uses the GenerateCredentialReport, GetCredentialReport, and UpdateAccessKey APIs.
- [ ] Create an Amazon CloudWatch alarm to detect aged access keys and use an AWS Lambda function to disable the keys older than 90 days.

### The InfoSec team has mandated that in the future only approved Amazon Machine Images (AMIs) can be used. How can the InfoSec team ensure compliance with this mandate?

- [ ] Terminate all Amazon EC2 instances and relaunch them with approved AMIs.
- [ ] Patch all running instances by using AWS Systems Manager.
- [x] Deploy AWS Config rules and check all running instances for compliance.
- [ ] Define a metric filter in Amazon CloudWatch Logs to verify compliance.

### A pharmaceutical company has digitized versions of historical prescriptions stored on premises. The company would like to move these prescriptions to AWS and perform analytics on the data in them. Any operation with this data requires that the data be encrypted in transit and at rest. Which application flow would meet the data protection requirements on AWS?

- [x] Digitized files -> Amazon Kinesis Data Analytics.
- [ ] Digitized files -> Amazon Kinesis Data Firehose -> Amazon S3 -> Amazon Athena.
- [ ] Digitized files -> Amazon Kinesis Data Streams -> Kinesis Client Library consumer -> Amazon S3 -> Athena.
- [ ] Digitized files -> Amazon Kinesis Data Firehose -> Amazon Elasticsearch.

### The Security Engineer created a new AWS Key Management Service (AWS KMS) key with the following key policy: What are the effects of the key policy? (Choose two.)

![Question 337](images/question337.png)

- [x] The policy allows access for the AWS account 111122223333 to manage key access though IAM policies.
- [x] The policy allows all IAM users in account 111122223333 to have full access to the KMS key.
- [ ] The policy allows the root user in account 111122223333 to have full access to the KMS key.
- [ ] The policy allows the KMS service-linked role in account 111122223333 to have full access to the KMS key.
- [ ] The policy allows all IAM roles in account 111122223333 to have full access to the KMS key.

### A company uses AWS Organization to manage 50 AWS accounts. The finance staff members log in as AWS IAM users in the FinanceDept AWS account. The staff members need to read the consolidated billing information in the MasterPayer AWS account. They should not be able to view any other resources in the MasterPayer AWS account. IAM access to billing has been enabled in the MasterPayer account. Which of the following approaches grants the finance staff the permissions they require without granting any unnecessary permissions

- [ ] Create an IAM group for the finance users in the FinanceDept account, then attach the AWS managed ReadOnlyAccess IAM policy to the group.
- [ ] Create an IAM group for the finance users in the MasterPayer account, then attach the AWS managed ReadOnlyAccess IAM policy to the group.
- [ ]  Create an AWS IAM role in the FinanceDept account with the ViewBilling permission, then grant the finance users in the MasterPayer account the permission to assume that role.
- [x] Create an AWS IAM role in the MasterPayer account with the ViewBilling permission, then grant the finance users in the FinanceDept account the permission to assume that role.

### A Security Engineer has been asked to troubleshoot inbound connectivity to a web server. This single web server is not receiving inbound connections from the internet, whereas all other web servers are functioning properly. The architecture includes network ACLs, security groups, and a virtual security appliance. In addition, the Development team has implemented Application Load Balancers (ALBs) to distribute the load across all web servers. It is a requirement that traffic between the web servers and the internet flow through the virtual security appliance. The Security Engineer has verified the following: 1. The rule set in the Security Groups is correct 2. The rule set in the network ACLs is correct 3. The rule set in the virtual appliance is correct Which of the following are other valid items to troubleshoot in this scenario? (Choose two.)

- [ ] Verify that the 0.0.0.0/0 route in the route table for the web server subnet points to a NAT gateway.
- [x] Verify which Security Group is applied to the particular web server's elastic network interface (ENI).
- [ ] Verify that the 0.0.0.0/0 route in the route table for the web server subnet points to the virtual security appliance.
- [x] Verify the registered targets in the ALB.
- [ ] Verify that the 0.0.0.0/0 route in the public subnet points to a NAT gateway.

### A company has multiple production AWS accounts. Each account has AWS CloudTrail configured to log to a single Amazon S3 bucket in a central account. Two of the production accounts have trails that are not logging anything to the S3 bucket. Which steps should be taken to troubleshoot the issue? (Choose three.)

- [x] Verify that the log file prefix is set to the name of the S3 bucket where the logs should go.
- [x] Verify that the S3 bucket policy allows access for CloudTrail from the production AWS account IDs.
- [ ] Create a new CloudTrail configuration in the account, and configure it to log to the account's S3 bucket.
- [ ] Open the global CloudTrail configuration in the master account, and verify that the storage location is set to the correct S3 bucket.
- [x] Confirm in the CloudTrail Console that the S3 bucket name is set correctly.

### Amazon CloudWatch Logs agent is successfully delivering logs to the CloudWatch Logs service. However, logs stop being delivered after the associated log stream has been active for a specific number of hours. What steps are necessary to identify the cause of this phenomenon? (Choose two.)

- [ ] Ensure that file permissions for monitored files that allow the CloudWatch Logs agent to read the file have not been modified.
- [x] Verify that the OS Log rotation rules are compatible with the configuration requirements for agent streaming.
- [ ] Configure an Amazon Kinesis producer to first put the logs into Amazon Kinesis Streams.
- [ ] Create a CloudWatch Logs metric to isolate a value that changes at least once during the period before logging stops.
- [x] Use AWS CloudFormation to dynamically create and maintain the configuration file for the CloudWatch Logs agent.

### A company has deployed a custom DNS server in AWS. The Security Engineer wants to ensure that Amazon EC2 instances cannot use the Amazon-provided DNS. How can the Security Engineer block access to the Amazon-provided DNS in the VPC?

- [ ] Deny access to the Amazon DNS IP within all security groups.
- [ ] Add a rule to all network access control lists that deny access to the Amazon DNS IP.
- [ ] Add a route to all route tables that black holes traffic to the Amazon DNS IP.
- [x] Disable DNS resolution within the VPC configuration.

### Which of the following minimizes the potential attack surface for applications?

- [ ] Use security groups to provide stateful firewalls for Amazon EC2 instances at the hypervisor level.
- [x] Use network ACLs to provide stateful firewalls at the VPC level to prevent access to any specific AWS resource.
- [ ] Use AWS Direct Connect for secure trusted connections between EC2 instances within private subnets.
- [ ] Design network security in a single layer within the perimeter network (also known as DMZ, demilitarized zone, and screened subnet) to facilitate quicker responses to threats.

### A distributed web application is installed across several EC2 instances in public subnets residing in two Availability Zones. Apache logs show several intermittent brute-force attacks from hundreds of IP addresses at the layer 7 level over the past six months. What would be the BEST way to reduce the potential impact of these attacks in the future?

- [ ] Use custom route tables to prevent malicious traffic from routing to the instances.
- [ ] Update security groups to deny traffic from the originating source IP addresses.
- [x] Use network ACLs.
- [ ] Install intrusion prevention software (IPS) on each instance.

### A company plans to move most of its IT infrastructure to AWS. They want to leverage their existing on-premises Active Directory as an identity provider for AWS. Which combination of steps should a Security Engineer take to federate the company's on-premises Active Directory with AWS? (Choose two.)

- [x] Create IAM roles with permissions corresponding to each Active Directory group.
- [ ] Create IAM groups with permissions corresponding to each Active Directory group.
- [x] Configure Amazon Cloud Directory to support a SAML provider.
- [ ] Configure Amazon Cognito to add relying party trust between Active Directory and AWS.

### A security alert has been raised for an Amazon EC2 instance in a customer account that is exhibiting strange behavior. The Security Engineer must first isolate the EC2 instance and then use tools for further investigation. What should the Security Engineer use to isolate and research this event? (Choose three.)

- [x] AWS CloudTrail.
- [ ] Amazon Athena.
- [ ] AWS Key Management Service (AWS KMS).
- [x] VPC Flow Logs.
- [ ] AWS Firewall Manager.
- [x] Security groups.

### A financial institution has the following security requirements: Cloud-based users must be contained in a separate authentication domain. Cloud-based users cannot access on-premises systems. As part of standing up a cloud environment, the financial institution is creating a number of Amazon managed databases and Amazon EC2 instances. An Active Directory service exists on-premises that has all the administrator accounts, and these must be able to access the databases and instances. How would the organization manage its resources in the MOST secure manner? (Choose two.)

- [ ] Configure an AWS Managed Microsoft AD to manage the cloud resources.
- [x] Configure an additional on-premises Active Directory service to manage the cloud resources.
- [x] Establish a one-way trust relationship from the existing Active Directory to the new Active Directory service.
- [ ] Establish a one-way trust relationship from the new Active Directory to the existing Active Directory service.
- [ ] Establish a two-way trust between the new and existing Active Directory services.

### An organization wants to be alerted when an unauthorized Amazon EC2 instance in its VPC performs a network port scan against other instances in the VPC. When the Security team performs its own internal tests in a separate account by using pre-approved third-party scanners from the AWS Marketplace, the Security team also then receives multiple Amazon GuardDuty events from Amazon CloudWatch alerting on its test activities. How can the Security team suppress alerts about authorized security tests while still receiving alerts about the unauthorized activity?

- [ ] Use a filter in AWS CloudTrail to exclude the IP addresses of the Security team's EC2 instances.
- [ ] Add the Elastic IP addresses of the Security team's EC2 instances to a trusted IP list in Amazon GuardDuty.
- [x] Install the Amazon Inspector agent on the EC2 instances that the Security team uses.
- [ ] Grant the Security team's EC2 instances a role with permissions to call Amazon GuardDuty API operations.

### An organization is moving non-business-critical applications to AWS while maintaining a mission-critical application in an on-premises data center. An on-premises application must share limited confidential information with the applications in AWS. The internet performance is unpredictable. Which configuration will ensure continued connectivity between sites MOST securely?

- [ ] VPN and a cached storage gateway.
- [ ] AWS Snowball Edge.
- [x] VPN Gateway over AWS Direct Connect.
- [ ] AWS Direct Connect.

### An application has been built with Amazon EC2 instances that retrieve messages from Amazon SQS. Recently, IAM changes were made and the instances can no longer retrieve messages. What actions should be taken to troubleshoot the issue while maintaining least privilege? (Choose two.)

- [ ] Configure and assign an MFA device to the role used by the instances.
- [x] Verify that the SQS resource policy does not explicitly deny access to the role used by the instances.
- [ ] Verify that the access key attached to the role used by the instances is active.
- [ ] Attach the AmazonSQSFullAccess managed policy to the role used by the instances.
- [x] Verify that the role attached to the instances contains policies that allow access to the queue.

### A company has a forensic logging use case whereby several hundred applications running on Docker on EC2 need to send logs to a central location. The Security Engineer must create a logging solution that is able to perform real-time analytics on the log files, grants the ability to replay events, and persists data. Which AWS Services, together, can satisfy this use case? (Choose two.)

- [ ] Amazon Elasticsearch.
- [x] Amazon Kinesis.
- [ ] Amazon SQS.
- [x] Amazon CloudWatch.
- [ ] Amazon Athena.

### Which of the following is the most efficient way to automate the encryption of AWS CloudTrail logs using a Customer Master Key (CMK) in AWS KMS?

- [ ] Use the KMS direct encrypt function on the log data every time a CloudTrail log is generated.
- [ ] Use the default Amazon S3 server-side encryption with S3-managed keys to encrypt and decrypt the CloudTrail logs.
- [x] Configure CloudTrail to use server-side encryption using KMS-managed keys to encrypt and decrypt CloudTrail logs.
- [ ] Use encrypted API endpoints so that all AWS API calls generate encrypted CloudTrail log entries using the TLS certificate from the encrypted API call.

### An organization is using AWS CloudTrail, Amazon CloudWatch Logs, and Amazon CloudWatch to send alerts when new access keys are created. However, the alerts are no longer appearing in the Security Operations mail box. Which of the following actions would resolve this issue?

- [ ] In CloudTrail, verify that the trail logging bucket has a log prefix configured.
- [ ] In Amazon SNS, determine whether the "Account spend limit" has been reached for this alert.
- [ ] In SNS, ensure that the subscription used by these alerts has not been deleted.
- [x] In CloudWatch, verify that the alarm threshold "consecutive periods" value is equal to, or greater than 1.

### A Security Engineer must add additional protection to a legacy web application by adding the following HTTP security headers: -Content Security-Policy -X-Frame-Options -X-XSS-Protection The Engineer does not have access to the source code of the legacy web application. Which of the following approaches would meet this requirement?

- [ ] Configure an Amazon Route 53 routing policy to send all web traffic that does not include the required headers to a black hole.
- [x] Implement an AWS Lambda@Edge origin response function that inserts the required headers.
- [ ] Migrate the legacy application to an Amazon S3 static website and front it with an Amazon CloudFront distribution.
- [ ] Construct an AWS WAF rule to replace existing HTTP headers with the required security headers by using regular expressions.

### During a security event, it is discovered that some Amazon EC2 instances have not been sending Amazon CloudWatch logs. Which steps can the Security Engineer take to troubleshoot this issue? (Choose two.)

- [x] Connect to the EC2 instances that are not sending the appropriate logs and verify that the CloudWatch Logs agent is running.
- [x] Log in to the AWS account and select CloudWatch Logs. Check for any monitored EC2 instances that are in the "Alerting" state and restart them using the EC2 console.
- [ ] Verify that the EC2 instances have a route to the public AWS API endpoints.
- [ ] Connect to the EC2 instances that are not sending logs. Use the command prompt to verify that the right permissions have been set for the Amazon SNS topic.
- [ ] Verify that the network access control lists and security groups of the EC2 instances have the access to send logs over SNMP.

### A Security Engineer discovers that developers have been adding rules to security groups that allow SSH and RDP traffic from 0.0.0.0/0 instead of the organization firewall IP. What is the most efficient way to remediate the risk of this activity?

- [ ] Delete the internet gateway associated with the VPC.
- [x] Use network access control lists to block source IP addresses matching 0.0.0.0/0.
- [ ] Use a host-based firewall to prevent access from all but the organization's firewall IP.
- [ ] Use AWS Config rules to detect 0.0.0.0/0 and invoke an AWS Lambda function to update the security group with the organization's firewall IP.

### In response to the past DDoS attack experiences, a Security Engineer has set up an Amazon CloudFront distribution for an Amazon S3 bucket. There is concern that some users may bypass the CloudFront distribution and access the S3 bucket directly. What must be done to prevent users from accessing the S3 objects directly by using URLs?

- [ ] Change the S3 bucket/object permission so that only the bucket owner has access.
- [x] Set up a CloudFront origin access identity (OAI), and change the S3 bucket/object permission so that only the OAI has access.
- [ ] Create IAM roles for CloudFront, and change the S3 bucket/object permission so that only the IAM role has access.
- [ ] Redirect S3 bucket access to the corresponding CloudFront distribution.

### A company plans to move most of its IT infrastructure to AWS. The company wants to leverage its existing on-premises Active Directory as an identity provider for AWS. Which steps should be taken to authenticate to AWS services using the company's on-premises Active Directory? (Choose three.)

- [x] Create IAM roles with permissions corresponding to each Active Directory group.
- [ ] Create IAM groups with permissions corresponding to each Active Directory group.
- [x] Create a SAML provider with IAM.
- [ ] Create a SAML provider with Amazon Cloud Directory.
- [x] Configure AWS as a trusted relying party for the Active Directory
- [ ] Configure IAM as a trusted relying party for Amazon Cloud Directory.

### Example.com hosts its internal document repository on Amazon EC2 instances. The application runs on EC2 instances and previously stored the documents on encrypted Amazon EBS volumes. To optimize the application for scale, example.com has moved the files to Amazon S3. The security team has mandated that all the files are securely deleted from the EBS volume, and it must certify that the data is unreadable before releasing the underlying disks. Which of the following methods will ensure that the data is unreadable by anyone else?

- [ ] Change the volume encryption on the EBS volume to use a different encryption mechanism. Then, release the EBS volumes back to AWS.
- [ ] Release the volumes back to AWS. AWS immediately wipes the disk after it is deprovisioned.
- [ ] Delete the encryption key used to encrypt the EBS volume. Then, release the EBS volumes back to AWS.
- [x] Delete the data by using the operating system delete commands. Run Quick Format on the drive and then release the EBS volumes back to AWS.

### A Systems Administrator has written the following Amazon S3 bucket policy designed to allow access to an S3 bucket for only an authorized AWS IAM user from the IP address range 10.10.10.0/24: When trying to download an object from the S3 bucket from 10.10.10.40, the IAM user receives an access denied message. What does the Administrator need to change to grant access to the user?

![Question 360](images/question360.png)

- [x] Change the "Resource" from "arn: aws:s3:::Bucket" to "arn:aws:s3:::Bucket/*".
- [ ] Change the "Principal" from "*" to {AWS:"arn:aws:iam: : account-number: user/username"}.
- [ ] Change the "Version" from "2012-10-17" to the last revised date of the policy.
- [ ] Change the "Action" from ["s3:*"] to ["s3:GetObject", "s3:ListBucket"].

### The Security Engineer has discovered that a new application that deals with highly sensitive data is storing Amazon S3 objects with the following key pattern, which itself contains highly sensitive data. Pattern: "randomID_datestamp_PII.csv" Example: "1234567_12302017_000-00-0000 csv" The bucket where these objects are being stored is using server-side encryption (SSE). Which solution is the most secure and cost-effective option to protect the sensitive data?

- [ ] Remove the sensitive data from the object name, and store the sensitive data using S3 user-defined metadata.
- [x] Add an S3 bucket policy that denies the action s3:GetObject.
- [ ] Use a random and unique S3 object key, and create an S3 metadata index in Amazon DynamoDB using client-side encrypted attributes.
- [ ] Store all sensitive objects in Binary Large Objects (BLOBS) in an encrypted Amazon RDS instance.

### AWS CloudTrail is being used to monitor API calls in an organization. An audit revealed that CloudTrail is failing to deliver events to Amazon S3 as expected. What initial actions should be taken to allow delivery of CloudTrail events to S3? (Choose two.)

- [ ] Verify that the S3 bucket policy allow CloudTrail to write objects.
- [ ] Verify that the IAM role used by CloudTrail has access to write to Amazon CloudWatch Logs.
- [ ] Remove any lifecycle policies on the S3 bucket that are archiving objects to Amazon Glacier.
- [x] Verify that the S3 bucket defined in CloudTrail exists.
- [x] Verify that the log file prefix defined in CloudTrail exists in the S3 bucket.

### Due to new compliance requirements, a Security Engineer must enable encryption with customer-provided keys on corporate data that is stored in DynamoDB. The company wants to retain full control of the encryption keys. Which DynamoDB feature should the Engineer use to achieve compliance'?

- [ ] Use AWS Certificate Manager to request a certificate. Use that certificate to encrypt data prior to uploading it to DynamoDB.
- [ ] Enable S3 server-side encryption with the customer-provided keys. Upload the data to Amazon S3, and then use S3Copy to move all data to DynamoDB
- [ ] Create a KMS master key. Generate per-record data keys and use them to encrypt data prior to uploading it to DynamoDS. Dispose of the cleartext and encrypted data keys after encryption without storing.
- [X] Use the DynamoDB Java encryption client to encrypt data prior to uploading it to DynamoDB.

### A Security Engineer must design a system that can detect whether a file on an Amazon EC2 host has been modified. The system must then alert the Security Engineer of the modification. What is the MOST efficient way to meet these requirements?

- [ ] Install antivirus software and ensure that signatures are up-to-date. Configure Amazon CloudWatch alarms to send alerts for security events.
- [ ] Install host-based IDS software to check for file integrity. Export the logs to Amazon CloudWatch Logs for monitoring and alerting.
- [ ] Export system log files to Amazon S3. Parse the log files using an AWS Lambda function that will send alerts of any unauthorized system login attempts through Amazon SNS.
- [X] Use Amazon CloudWatch Logs to detect file system changes. If a change is detected, automatically terminate and recreate the instance from the most recent AMI. Use Amazon SNS to send notification of the event.

### A company has multiple VPCs in their account that are peered, as shown in the diagram. A Security Engineer wants to perform penetration tests of the Amazon EC2 instances in all three VPCs. How can this be accomplished? (Choose two.)

![Question 365](images/question365.png)

- [ ] Deploy a pre-authorized scanning engine from the AWS Marketplace into VPC B, and use it to scan instances in all three VPCs. Do not complete the penetration test request form.
- [ ] Deploy a pre-authorized scanning engine from the Marketplace into each VPC, and scan instances in each VPC from the scanning engine in that VPC. Do not complete the penetration test request form.
- [x] Create a VPN connection from the data center to VPC A. Use an on-premises scanning engine to scan the instances in all three VPCs. Complete the penetration test request form for all three VPCs.
- [ ] Create a VPN connection from the data center to each of the three VPCs. Use an on-premises scanning engine to scan the instances in each VPC. Do not complete the penetration test request form.
- [x] Create a VPN connection from the data center to each of the three VPCs. Use an on-premises scanning engine to scan the instances in each VPC. Complete the penetration test request form for all three VPCs.

### For compliance reasons, an organization limits the use of resources to three specific AWS regions. It wants to be alerted when any resources are launched in unapproved regions. Which of the following approaches will provide alerts on any resources launched in an unapproved region?

- [x] Develop an alerting mechanism based on processing AWS CloudTrail logs.
- [ ] Monitor Amazon S3 Event Notifications for objects stored in buckets in unapproved regions.
- [ ] Analyze Amazon CloudWatch Logs for activities in unapproved regions.
- [ ] Use AWS Trusted Advisor to alert on all resources being created.

### A company runs an application on AWS that needs to be accessed only by employees. Most employees work from the office, but others work remotely or travel. How can the Security Engineer protect this workload so that only employees can access it?

- [ ] Add each employee's home IP address to the security group for the application so that only those users can access the workload.
- [x] Create a virtual gateway for VPN connectivity for each employee, and restrict access to the workload from within the VPC.
- [ ] Use a VPN appliance from the AWS Marketplace for users to connect to, and restrict workload access to traffic from that appliance.
- [ ] Route all traffic to the workload through AWS WAF. Add each employee's home IP address into an AWS WAF rule, and block all other traffic.

### A Systems Engineer is troubleshooting the connectivity of a test environment that includes a virtual security appliance deployed inline. In addition to using the virtual security appliance, the Development team wants to use security groups and network ACLs to accomplish various security requirements in the environment. What configuration is necessary to allow the virtual security appliance to route the traffic?

- [ ] Disable network ACLs.
- [ ] Configure the security appliance's elastic network interface for promiscuous mode.
- [ ] Disable the Network Source/Destination check on the security appliance's elastic network interface.
- [x] Place the security appliance in the public subnet with the internet gateway.

### A Security Architect is evaluating managed solutions for storage of encryption keys. The requirements are: -Storage is accessible by using only VPCs. -Service has tamper-evident controls. -Access logging is enabled. -Storage has high availability. Which of the following services meets these requirements?

- [ ] Amazon S3 with default encryption.
- [x] AWS CloudHSM.
- [ ] Amazon DynamoDB with server-side encryption.
- [ ] AWS Systems Manager Parameter Store.

### An AWS account includes two S3 buckets: bucket1 and bucket2. The bucket2 does not have a policy defined, but bucket1 has the following bucket policy: In addition, the same account has an IAM User named `alice`, with the following IAM policy. Which buckets can user `alice` access?

![Question 370](images/question370_1.png)
![Question 370](images/question370_2.png)

- [ ] Bucket1 only.
- [ ] Bucket2 only.
- [x] Both bucket1 and bucket2.
- [ ] Neither bucket1 nor bucket2.

### An organization has three applications running on AWS, each accessing the same data on Amazon S3. The data on Amazon S3 is server-side encrypted by using an AWS KMS Customer Master Key (CMK). What is the recommended method to ensure that each application has its own programmatic access control permissions on the KMS CMK?

- [ ] Change the key policy permissions associated with the KMS CMK for each application when it must access the data in Amazon S3.
- [ ] Have each application assume an IAM role that provides permissions to use the AWS Certificate Manager CMK.
- [ ] Have each application use a grant on the KMS CMK to add or remove specific access controls on the KMS CMK.
- [x] Have each application use an IAM policy in a user context to have specific access permissions on the KMS CMK.

### The Security Engineer is given the following requirements for an application that is running on Amazon EC2 and managed by using AWS CloudFormation templates with EC2 Auto Scaling groups: -Have the EC2 instances bootstrapped to connect to a backend database. -Ensure that the database credentials are handled securely. -Ensure that retrievals of database credentials are logged. Which of the following is the MOST efficient way to meet these requirements?

- [ ] Pass databases credentials to EC2 by using CloudFormation stack parameters with the property set to true. Ensure that the instance is configured to log to Amazon CloudWatch Logs.
- [x] Store database passwords in AWS Systems Manager Parameter Store by using SecureString parameters. Set the IAM role for the EC2 instance profile to allow access to the parameters.
- [ ]  Create an AWS Lambda that ingests the database password and persists it to Amazon S3 with server-side encryption. Have the EC2 instances retrieve the S3 object on startup, and log all script invocations to syslog.
- [ ] Write a script that is passed in as UserData so that it is executed upon launch of the EC2 instance. Ensure that the instance is configured to log to Amazon CloudWatch Logs.

### A company has two AWS accounts, each containing one VPC. The first VPC has a VPN connection with its corporate network. The second VPC, without a VPN, hosts an Amazon Aurora database cluster in private subnets. Developers manage the Aurora database from a bastion host in a public subnet as shown in the image. A security review has flagged this architecture as vulnerable, and a Security Engineer has been asked to make this design more secure. The company has a short deadline and a second VPN connection to the Aurora account is not possible. How can the Security Engineer securely set up the bastion host?

![Question 373](images/question373.jpg)

- [ ] Move the bastion host to the VPC with VPN connectivity. Create a VPC peering relationship between the bastion host VPC and Aurora VPC.
- [x] Create an SSH port forwarding tunnel on the Developer's workstation to the bastion host to ensure that only authorized SSH clients can access the bastion host.
- [ ] Move the bastion host to the VPC with VPN connectivity. Create a cross-account trust relationship between the bastion VPC and Aurora VPC, and update the Aurora security group for the relationship.
- [ ]  Create an AWS Direct Connect connection between the corporate network and the Aurora account, and adjust the Aurora security group for this connection.

### An organization operates a web application that serves users globally. The application runs on Amazon EC2 instances behind an Application Load Balancer. There is an Amazon CloudFront distribution in front of the load balancer, and the organization uses AWS WAF. The application is currently experiencing a volumetric attack whereby the attacker is exploiting a bug in a popular mobile game. The application is being flooded with HTTP requests from all over the world with the User-Agent set to the following string: Mozilla/5.0 (compatible; ExampleCorp; ExampleGame/1.22; Mobile/1.0) What mitigation can be applied to block attacks resulting from this bug while continuing to service legitimate requests?

- [ ] Create a rule in AWS WAF rules with conditions that block requests based on the presence of ExampleGame/1.22 in the User-Agent header.
- [ ] Create a geographic restriction on the CloudFront distribution to prevent access to the application from most geographic regions.
- [x] Create a rate-based rule in AWS WAF to limit the total number of requests that the web application services.
- [ ] Create an IP-based blacklist in AWS WAF to block the IP addresses that are originating from requests that contain ExampleGame/1.22 in the User-Agent header.

### Some highly sensitive analytics workloads are to be moved to Amazon EC2 hosts. Threat modeling has found that a risk exists where a subnet could be maliciously or accidentally exposed to the internet. Which of the following mitigations should be recommended?

- [ ] Use AWS Config to detect whether an Internet Gateway is added and use an AWS Lambda function to provide auto-remediation.
- [x] Within the Amazon VPC configuration, mark the VPC as private and disable Elastic IP addresses.
- [ ] Use IPv6 addressing exclusively on the EC2 hosts, as this prevents the hosts from being accessed from the internet.
- [ ] Move the workload to a Dedicated Host, as this provides additional network security controls and monitoring.

### A Developer who is following AWS best practices for secure code development requires an application to encrypt sensitive data to be stored at rest, locally in the application, using AWS KMS. What is the simplest and MOST secure way to decrypt this data when required?

- [ ] Request KMS to provide the stored unencrypted data key and then use the retrieved data key to decrypt the data.
- [ ] Keep the plaintext data key stored in Amazon DynamoDB protected with IAM policies. Query DynamoDB to retrieve the data key to decrypt the data.
- [ ] Use the Encrypt API to store an encrypted version of the data key with another customer managed key. Decrypt the data key and use it to decrypt the data when required.
- [ ] Store the encrypted data key alongside the encrypted data. Use the Decrypt API to retrieve the data key to decrypt the data when required.

### An organization receives an alert that indicates that an EC2 instance behind an ELB Classic Load Balancer has been compromised. What techniques will limit lateral movement and allow evidence gathering?

- [ ] Remove the instance from the load balancer and terminate it.
- [x] Remove the instance from the load balancer, and shut down access to the instance by tightening the security group.
- [ ] Reboot the instance and check for any Amazon CloudWatch alarms.
- [ ] Stop the instance and make a snapshot of the root EBS volume.

### A Development team has asked for help configuring the IAM roles and policies in a new AWS account. The team using the account expects to have hundreds of master keys and therefore does not want to manage access control for customer master keys (CMKs). Which of the following will allow the team to manage AWS KMS permissions in IAM without the complexity of editing individual key policies?

- [ ] The account's CMK key policy must allow the account's IAM roles to perform KMS EnableKey.
- [ ] Newly created CMKs must have a key policy that allows the root principal to perform all actions.
- [ ] Newly created CMKs must allow the root principal to perform the kms CreateGrant API operation.
- [x] Newly created CMKs must mirror the IAM policy of the KMS key administrator.

### An Amazon EC2 instance is part of an EC2 Auto Scaling group that is behind an Application Load Balancer (ALB). It is suspected that the EC2 instance has been compromised. Which steps should be taken to investigate the suspected compromise? (Choose three.)

- [x] Detach the elastic network interface from the EC2 instance.
- [ ] Initiate an Amazon Elastic Block Store volume snapshot of all volumes on the EC2 instance.
- [ ] Disable any Amazon Route 53 health checks associated with the EC2 instance.
- [ ] De-register the EC2 instance from the ALB and detach it from the Auto Scaling group.
- [x] Attach a security group that has restrictive ingress and egress rules to the EC2 instance.
- [x] Add a rule to an AWS WAF to block access to the EC2 instance.

### A Security Engineer is implementing a solution to allow users to seamlessly encrypt Amazon S3 objects without having to touch the keys directly. The solution must be highly scalable without requiring continual management. Additionally, the organization must be able to immediately delete the encryption keys. Which solution meets these requirements?

- [ ] Use AWS KMS with AWS managed keys and the ScheduleKeyDeletion API with a PendingWindowInDays set to 0 to remove the keys if necessary.
- [x] Use KMS with AWS imported key material and then use the DeletelmportedKeyMaterial API to remove the key material if necessary.
- [ ] Use AWS CloudHSM to store the keys and then use the CloudHSM API or the PKCS11 library to delete the keys if necessary.
- [ ] Use the Systems Manager Parameter Store to store the keys and then use the service API operations to delete the key if necessary.

### An application uses Amazon Cognito to manage end users' permissions when directly accessing AWS resources, including Amazon DynamoDB. A new feature request reads as follows: Provide a mechanism to mark customers as suspended pending investigation or suspended permanently. Customers should still be able to log in when suspended, but should not be able to make changes. The priorities are to reduce complexity and avoid potential for future security issues. Which approach will meet these requirements and priorities?

- [x] Create a new database field "suspended_status" and modify the application logic to validate that field when processing requests.
- [ ] Add suspended customers to second Cognito user pool and update the application login flow to check both user pools.
- [ ] Use Amazon Cognito Sync to push out a "suspension_status" parameter and split the IAM policy into normal users and suspended users.
- [ ] Move suspended customers to a second Cognito group and define an appropriate IAM access policy for the group.

### A company stores data on an Amazon EBS volume attached to an Amazon EC2 instance. The data is asynchronously replicated to an Amazon S3 bucket. Both the EBS volume and the S3 bucket are encrypted with the same AWS KMS Customer Master Key (CMK). A former employee scheduled a deletion of that CMK before leaving the company. The company's Developer Operations department learns about this only after the CMK has been deleted. Which steps must be taken to address this situation?

- [x] Copy the data directly from the EBS encrypted volume before the volume is detached from the EC2 instance.
- [ ] Recover the data from the EBS encrypted volume using an earlier version of the KMS backing key.
- [ ] Make a request to AWS Support to recover the S3 encrypted data.
- [ ] Make a request to AWS Support to restore the deleted CMK, and use it to recover the data.

### An AWS Lambda function was misused to alter data, and a Security Engineer must identify who invoked the function and what output was produced. The Engineer cannot find any logs created by the Lambda function in Amazon CloudWatch Logs. Which of the following explains why the logs are not available?

- [x] The execution role for the Lambda function did not grant permissions to write log data to CloudWatch Logs.
- [ ] The Lambda function was executed by using Amazon API Gateway, so the logs are not stored in CloudWatch Logs.
- [ ] The execution role for the Lambda function did not grant permissions to write to the Amazon S3 bucket where CloudWatch Logs stores the logs.
- [ ] The version of the Lambda function that was executed was not current.

### A company has Windows Amazon EC2 instances in a VPC that are joined to on-premises Active Directory servers for domain services. The security team has enabled Amazon GuardDuty on the AWS account to alert on issues with the instances. During a weekly audit of network traffic, the Security Engineer notices that one of the EC2 instances is attempting to communicate with a known command-and- control server but failing. This alert does not show up in GuardDuty. Why did GuardDuty fail to alert to this behavior?

- [ ] GuardDuty did not have the appropriate alerts activated.
- [ ] GuardDuty does not see these DNS requests.
- [x] GuardDuty only monitors active network traffic flow for command-and-control activity.
- [ ] GuardDuty does not report on command-and-control activity.

### The AWS Systems Manager Parameter Store is being used to store database passwords used by an AWS Lambda function. Because this is sensitive data, the parameters are stored as type SecureString and protected by an AWS KMS key that allows access through IAM. When the function executes, this parameter cannot be retrieved as the result of an access denied error. Which of the following actions will resolve the access denied error?

- [x] Update the ssm.amazonaws.com principal in the KMS key policy to allow kms: Decrypt.
- [ ] Update the Lambda configuration to launch the function in a VPC.
- [ ] Add a policy to the role that the Lambda function uses, allowing kms: Decrypt for the KMS key.
- [ ] Add lambda.amazonaws.com as a trusted entity on the IAM role that the Lambda function uses.

### A company's security policy requires that VPC Flow Logs are enabled on all VPCs. A Security Engineer is looking to automate the process of auditing the VPC resources for compliance. What combination of actions should the Engineer take? (Choose two.)

- [ ] Create an AWS Lambda function that determines whether Flow Logs are enabled for a given VPC.
- [x] Create an AWS Config configuration item for each VPC in the company AWS account.
- [ ] Create an AWS Config managed rule with a resource type of AWS:: Lambda:: Function.
- [x] Create an Amazon CloudWatch Event rule that triggers on events emitted by AWS Config.
- [ ] Create an AWS Config custom rule, and associate it with an AWS Lambda function that contains the evaluating logic.

### A Security Engineer is looking for a way to control access to data that is being encrypted under a CMK. The Engineer is also looking to use additional authenticated data (AAD) to prevent tampering with ciphertext. Which action would provide the required functionality?

- [ ] Pass the key alias to AWS KMS when calling Encrypt and Decrypt API actions.
- [ ] Use IAM policies to restrict access to Encrypt and Decrypt API actions.
- [ ] Use kms:EncryptionContext as a condition when defining IAM policies for the CMK.
- [x] Use key policies to restrict access to the appropriate IAM groups.

### An application makes calls to AWS services using the AWS SDK. The application runs on Amazon EC2 instances with an associated IAM role. When the application attempts to access an object within an Amazon S3 bucket; the Administrator receives the following error message: HTTP 403: Access Denied.Which combination of steps should the Administrator take to troubleshoot this issue? (Choose three.)

- [ ] Confirm that the EC2 instance's security group authorizes S3 access.
- [x] Verify that the KMS key policy allows decrypt access for the KMS key for this IAM principle.
- [x] Check the S3 bucket policy for statements that deny access to objects.
- [ ] Confirm that the EC2 instance is using the correct key pair.
- [x] Confirm that the IAM role associated with the EC2 instance has the proper privileges.
- [ ] Confirm that the instance and the S3 bucket are in the same Region.

### A Security Engineer must implement mutually authenticated TLS connections between containers that communicate inside a VPC. Which solution would be MOST secure and easy to maintain?

- [ ] Use AWS Certificate Manager to generate certificates from a public certificate authority and deploy them to all the containers.
- [ ] Create a self-signed certificate in one container and use AWS Secrets Manager to distribute the certificate to the other containers to establish trust.
- [ ] Use AWS Certificate Manager Private Certificate Authority (ACM PCA) to create a subordinate certificate authority, then create the private keys in the containers and sign them using the ACM PCA API.
- [x] Use AWS Certificate Manager Private Certificate Authority (ACM PCA) to create a subordinate certificate authority, then use AWS Certificate Manager to generate the private certificates and deploy them to all the containers.

### The Accounting department at Example Corp. has made a decision to hire a third-party firm, AnyCompany, to monitor Example Corp.'s AWS account to help optimize costs. The Security Engineer for Example Corp. has been tasked with providing AnyCompany with access to the required Example Corp. AWS resources. The Engineer has created an IAM role and granted permission to AnyCompany's AWS account to assume this role. When customers contact AnyCompany, they provide their role ARN for validation. The Engineer is concerned that one of AnyCompany's other customers might deduce Example Corp.'s role ARN and potentially compromise the company's account. What steps should the Engineer perform to prevent this outcome?

- [ ] Create an IAM user and generate a set of long-term credentials. Provide the credentials to AnyCompany. Monitor access in IAM access advisor and plan to rotate credentials on a recurring basis.
- [x] Request an external ID from AnyCompany and add a condition with sts:Externald to the role's trust policy.
- [ ] Require two-factor authentication by adding a condition to the role's trust policy with aws:MultiFactorAuthPresent.
- [ ] Request an IP range from AnyCompany and add a condition with aws:SourceIp to the role's trust policy.

### An Amazon S3 bucket is encrypted using an AWS KMS CMK. An IAM user is unable to download objects from the S3 bucket using the AWS Management Console; however, other users can download objects from the S3 bucket. Which policies should the Security Engineer review and modify to resolve this issue? (Choose three.)

- [x] The CMK policy.
- [ ] The VPC endpoint policy.
- [x] The S3 bucket policy.
- [ ] The S3 ACL.
- [x] The IAM policy.

### While analyzing a company's security solution, a Security Engineer wants to secure the AWS account root user. What should the Security Engineer do to provide the highest level of security for the account?

- [ ] Create a new IAM user that has administrator permissions in the AWS account. Delete the password for the AWS account root user.
- [ ] Create a new IAM user that has administrator permissions in the AWS account. Modify the permissions for the existing IAM users.
- [ ] Replace the access key for the AWS account root user. Delete the password for the AWS account root user.
- [x] Create a new IAM user that has administrator permissions in the AWS account. Enable multi-factor authentication for the AWS account root user.

### A Security Engineer is working with a Product team building a web application on AWS. The application uses Amazon S3 to host the static content, Amazon API Gateway to provide RESTful services; and Amazon DynamoDB as the backend data store. The users already exist in a directory that is exposed through a SAML identity provider. Which combination of the following actions should the Engineer take to enable users to be authenticated into the web application and call APIs? (Choose three.)

- [ ] Create a custom authorization service using AWS Lambda.
- [x] Configure a SAML identity provider in Amazon Cognito to map attributes to the Amazon Cognito user pool attributes.
- [x] Configure the SAML identity provider to add the Amazon Cognito user pool as a relying party.
- [ ] Configure an Amazon Cognito identity pool to integrate with social login providers.
- [ ] Update DynamoDB to store the user email addresses and passwords.
- [x] Update API Gateway to use a COGNITO_USER_POOLS authorizer.

### While securing the connection between a company's VPC and its on-premises data center, a Security Engineer sent a ping command from an on-premises host (IP address 203.0.113.12) to an Amazon EC2 instance (IP address 172.31.16.139). The ping command did not return a response. The flow log in the VPC showed the following: 2 123456789010 eni-1235b8ca 203.0.113.12 172.31.16.139 0 0 1 4 336 1432917027 1432917142 ACCEPT OK 2 123456789010 eni-1235b8ca 172.31.16.139 203.0.113.12 0 0 1 4 336 1432917094 1432917142 REJECT OK What action should be performed to allow the ping to work?

- [ ] In the security group of the EC2 instance, allow inbound ICMP traffic.
- [ ] In the security group of the EC2 instance, allow outbound ICMP traffic.
- [ ] In the VPC's NACL, allow inbound ICMP traffic.
- [x] In the VPC's NACL, allow outbound ICMP traffic.

### A Security Engineer is building a Java application that is running on Amazon EC2. The application communicates with an Amazon RDS instance and authenticates with a user name and password. Which combination of steps can the Engineer take to protect the credentials and minimize downtime when the credentials are rotated? (Choose two.)

- [ ] Have a Database Administrator encrypt the credentials and store the ciphertext in Amazon S3. Grant permission to the instance role associated with the EC2 instance to read the object and decrypt the ciphertext.
- [ ] Configure a scheduled job that updates the credential in AWS Systems Manager Parameter Store and notifies the Engineer that the application needs to be restarted.
- [x] Configure automatic rotation of credentials in AWS Secrets Manager.
- [ ] Store the credential in an encrypted string parameter in AWS Systems Manager Parameter Store. Grant permission to the instance role associated with the EC2 instance to access the parameter and the AWS KMS key that is used to encrypt it.
- [x] Configure the Java application to catch a connection failure and make a call to AWS Secrets Manager to retrieve updated credentials when the password is rotated. Grant permission to the instance role associated with the EC2 instance to access Secrets Manager.

### A company plans to migrate a sensitive dataset to Amazon S3. A Security Engineer must ensure that the data is encrypted at rest. The encryption solution must enable the company to generate its own keys without needing to manage key storage or the encryption process. What should the Security Engineer use to accomplish this?

- [ ] Server-side encryption with Amazon S3-managed keys (SSE-S3)
- [x] Server-side encryption with AWS KMS-managed keys (SSE-KMS)
- [ ] Server-side encryption with customer-provided keys (SSE-C)
- [ ] Client-side encryption with an AWS KMS-managed CMK

### A Security Engineer is defining the logging solution for a newly developed product. Systems Administrators and Developers need to have appropriate access to event log files in AWS CloudTrail to support and troubleshoot the product. Which combination of controls should be used to protect against tampering with and unauthorized access to log files? (Choose two.)

- [x] Ensure that the log file integrity validation mechanism is enabled.
- [ ] Ensure that all log files are written to at least two separate Amazon S3 buckets in the same account.
- [ ] Ensure that Systems Administrators and Developers can edit log files, but prevent any other access.
- [x] Ensure that Systems Administrators and Developers with job-related need-to-know requirements only are capable of viewing - but not modifying - the log files.
- [ ] Ensure that all log files are stored on Amazon EC2 instances that allow SSH access from the internal corporate network only.
