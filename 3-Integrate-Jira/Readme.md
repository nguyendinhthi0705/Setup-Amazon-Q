#  Integration Amazon Q with Jira
Amazon Q allow integrate with Jira, Saleforce, ServiceNow to create a ticket by summary the chat content.
 - Prerequisite: 
    <ul>
     <li> Register a free/paid Jira Account </li>
      <li> Create some projects such as Software Development, Customer Service ..etc </li>
    </ul>

## Create API token in Jira Account
1. Login into Jira and Go to "Manage Account" and Security tab, Click API tokens

    ![](/3-Integrate-Jira/images/img1.jpeg)

2. Create an API token "MyAssistant"

    ![](/3-Integrate-Jira/images/img2.jpeg)
    - Copy your Jira API Token
    - Copy your jira Url
    - Copy your Jira Username (It is usually your login email)

## Create Jira Plugin in Amazon Q
1. Login into AWS Console and go to your Amazon Q Application

    ![](/3-Integrate-Jira/images/img3.jpeg)

2. Click Add Plugin and Select Jira 

    ![](/3-Integrate-Jira/images/img4.jpeg)

4. Input your Url and Authentication
    Input your Url

    ![](/3-Integrate-Jira/images/img4.jpeg)

    Create and Add new Secret with Jira Username and API Token

    ![](/3-Integrate-Jira/images/img5.jpeg)

## Test your Jira plugin with Amazon Q
- Login your Amazon Q
- Upload a file for ticket content and input text "What content in the txt file ?"

     ![](/3-Integrate-Jira/images/img6.jpeg)

- Input "Please create a jira ticket to track meeting minutes" and select a project, a new ticket then will be created
     ![](/3-Integrate-Jira/images/img7.jpeg)
- You can view your new ticket on Jira by click on the link
      ![](/3-Integrate-Jira/images/img8.jpeg)



