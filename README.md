# deploy_qualys_SSM
**deploy Qualys Cloud Agent via Run command to AWS managed instances using SSM Documents**

# License
_**THIS SCRIPT IS PROVIDED TO YOU "AS IS."  TO THE EXTENT PERMITTED BY LAW, QUALYS HEREBY DISCLAIMS ALL WARRANTIES AND LIABILITY FOR THE PROVISION OR USE OF THIS SCRIPT.  IN NO EVENT SHALL THESE SCRIPTS BE DEEMED TO BE CLOUD SERVICES AS PROVIDED BY QUALYS**_

# Usage:
Follow the steps mentioned below to utilize the document to install Qualys Cloud agent.

1.	Open the AWS Systems Manager console. 

2.	In the navigation pane under Systems Manager Services, choose Run Command.

3.	For Command document, search with Owner : Equal : Public and then choose the document QualysCloudAgent-Install with search string Document name prefix : Equal : QualysCloudAgent-Install.

![qca](/images/qca.png?raw=true "QCA")

4.	This document will open a form which you need to fill for installing the cloud agent.
There are two required options which you must input. They are ActivationID: An ID to authenticate agents so that they could be grouped and bind to your account and CustomerID: An ID to identify your account.

![parameters](/images/parameters.png?raw=true "Parameters")

**Note: The same document can be used to install Qualys CA on Windows and Debian or RPM based Linux instances.**

5.	Specify your EC2 instances either by choosing the Specifying a Tag option or by Manually Selecting Instances and then selecting Select instances.

![results](/images/results.png?raw=true "results")

6.	Provide your choices for the rest of the available options using the instructions in Executing Commands from the EC2 Console, and then select Run.

The SSM Document is tested on following Operating systems:

*	Amazon Linux 2

* CentOS Linux 7.5.1804 (Core) 

*	Red Hat Enterprise Linux Server 7.5 

*	Ubuntu Linux 14.04.5 

*	Microsoft Windows Server 2012 and their service packs

**Note:To utilize this option, make sure that your EC2 instance has the SSM Agent installed and has an IAM role that allows Run Command. For more information, refer the below links:**

[Installing and Configuring SSM Agent](http://docs.aws.amazon.com/systems-manager/latest/userguide/ssm-agent.html)

[Configuring Security Roles for System Manager](http://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-access.html)
