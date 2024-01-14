# Step by step to setup Amazon Q

## Setup Amazon Q
1. Access Amazon Q by Search "Amazon Q" or Access this <a href='https://us-east-1.console.aws.amazon.com/amazonq/home?region=us-east-1#welcome'>link </a> 
![Amazon Q Home](/1-Setup-AmazonQ/images/img1.jpeg)
2. Click “Get Started”
3. Click Create Application and input application name such as “my-assistant”
![Amazon Q Home](/1-Setup-AmazonQ/images/img2.jpeg)
4. Input the number of Indexes, default as 1 for 10K document
![Amazon Q Home](/1-Setup-AmazonQ/images/img3.jpeg)
## Setup Amazon Q data source:
1. Select S3 as data source and name as “knowledge-base”:
2. Select S3 bucket for your data-source
3. For Sync on Schedule, just choose “Run on Demand”.
![Amazon Q Home](/1-Setup-AmazonQ/images/img4.jpeg)
4. Click Create Data Source and wait a couple minutes to success create. 
5. Click Create application.
## Upload data to knowledge base and Sync the data
Open your application and open data source and click “Detail tab” you will see S3 bucket
![Amazon Q Home](/1-Setup-AmazonQ/images/img5.jpeg)

Open S3 bucket and upload your documents:
    * Sample documents 
        * Amazon annual report https://www.annualreports.com/HostedData/AnnualReports/PDF/NASDAQ_AMZN_2022.pdf
        * Apple annual report https://www.annualreports.com/HostedData/AnnualReports/PDF/NASDAQ_AAPL_2022.pdf

    * Upload document to your S3 bucket:
        * Open S3 and Select Upload button

![Amazon Q Home](/1-Setup-AmazonQ/images/img6.jpeg)
Select file and click Upload button to upload the file
![Amazon Q Home](/1-Setup-AmazonQ/images/img7.jpeg)
![Amazon Q Home](/1-Setup-AmazonQ/images/img8.jpeg)
Back to your Q application and tick your data source to check Sync status. If it is not Sync, just click “Sync now“
![Amazon Q Home](/1-Setup-AmazonQ/images/img9.jpeg)

Wait for a couple minutes when you see The Last Sync status is completed 
![Amazon Q Home](/1-Setup-AmazonQ/images/img10.jpeg)

## Test your application
Click “Preview Web Experience” to test your application
Try some testing like “Summary Amazon revenue 2022” or “Summary Apple revenue 2022”
![Amazon Q Home](/1-Setup-AmazonQ/images/img11.jpeg)    
Click “ New Conversation” and create a new file with sample content as below
![Amazon Q Home](/1-Setup-AmazonQ/images/img12.jpeg)
Click Upload file and ask “What content in the file” to see content summary
![Amazon Q Home](/1-Setup-AmazonQ/images/img13.jpeg)

