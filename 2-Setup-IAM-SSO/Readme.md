# Step by step to setup SSO with Amazon Q
 - Configuare your IAM Identity Center 
 This document will guide your to setup Identity Provider for Amazon Q via IAM Identity Center. To confign IAM Identity Center, please try this <a href="https://docs.aws.amazon.com/singlesignon/latest/userguide/what-is.html">link</a>
## Setup Application SSO
1. Go to "IAM Identity Center" and choose Applications tab
2. Click Add Application

    ![](/2-Setup-IAM-SSO/images/img1.png)

3. Choose "I have an application I want to set up" and Application type as "SAML 2.0" and Click Next
    
    ![](/2-Setup-IAM-SSO/images/img2.png)

4. Download IAM Identity Center SAML metadata file and certificate

    ![](/2-Setup-IAM-SSO/images/img3.png)

5. Open a new tab and navigate to your Amazon Q Application
    Choose Web Experience Settings tab and Click Edit.
    ![](/2-Setup-IAM-SSO/images/img4.png)

    Copy the "Application consumer service (ACS) URL" and "Audience URI (SP Entity ID)"
![](/2-Setup-IAM-SSO/images/img5.png)

6. Back to "IAM Identity Center" and Application Tab to Config Application meta data:
    - Application ACS URL
    - Application SAML Audidence

    ![](/2-Setup-IAM-SSO/images/img6.png)
7. Click Submit to create Application
8. In Permission Set tab choose create Permission Set
    ![](/2-Setup-IAM-SSO/images/img13.jpeg)

-  Choose Customer Permission Set and Create the following IAM Policies if your account doesn't have
    > {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowAmazonQFullAccess",
            "Effect": "Allow",
            "Action": [
                "q:*"
            ],
            "Resource": "*"
        }
    ]
}

- Assign user/group to your application
    Choose AWS Account tab then click Assign users or groups 
    Choose user or group and then assign above permission set

    ![](/2-Setup-IAM-SSO/images/img11.jpeg)


9. Choose Action and Edit Attribute mappings:
    ![](/2-Setup-IAM-SSO/images/img7.jpeg)

    - Config ${user:email} as Subject Attribute
    - Config ${user:email} as Email Attribute

    ![](/2-Setup-IAM-SSO/images/img8.jpeg)
    
    Save Change

10. Back to your Amazon Q Application tab:
     Import Certificate from previous steps 
     Input "Email" as "Email attribute of SAML assertion"

    ![](/2-Setup-IAM-SSO/images/img10.jpeg)

     Click Deploy 

## Test Amazon Q Application
1. Access IAM Identity Center and Click AWS Access Portal URL
    
    ![](/2-Setup-IAM-SSO/images/img12.jpeg)
2. Login into Identity Center

    ![](/2-Setup-IAM-SSO/images/img14.jpeg)
3. Click My Assistant App, the system will navigate you to Amazon Q application

    ![](/2-Setup-IAM-SSO/images/img15.jpeg)

## Troubleshoot:

Troubleshoot link:
https://docs.aws.amazon.com/amazonq/latest/business-use-dg/idp-troubleshooting.html  

Identity Center attributes:
https://docs.aws.amazon.com/singlesignon/latest/userguide/attributemappingsconcept.html#supportedssoattributes



