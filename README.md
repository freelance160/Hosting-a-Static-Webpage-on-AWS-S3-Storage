# Hosting-a-Static-Webpage-on-AWS-S3-Storage

I always assumed the AWS S3 object storage was solely for storing data. I recently discovered it is a great option for hosting static websites. 

These are the steps I took in hosting my first webpage using an AWS S3 bucket. 

I logged into my AWS account and navigated to the S3 section via the search bar in the AWS console. 


I then created a new storage bucket and appropriately named it for this exercise. 
<img width="1464" alt="Screenshot 2025-02-24 at 19 52 33" src="https://github.com/user-attachments/assets/923bf1c4-05fd-4e08-87e7-f51d98edeff0" />


￼
A simple but key step after creating the bucket is to access the bucket settings and set it to static website. I then defined my index document and error document names.
<img width="1470" alt="Screenshot 2025-02-24 at 19 56 41" src="https://github.com/user-attachments/assets/a3477228-38e5-4ef5-9d4e-37528cdb66b9" />

￼

Next, I made changes to the bucket permissions. The first change was to allow public access to the bucket. Then, I added a JSON policy that would allow requests for objects in the storage bucket. 

A helpful tip is to use a policy generator to create the policy. This will make the bucket contents visible when accessed via the endpoint link.
<img width="1470" alt="Screenshot 2025-02-24 at 22 44 03" src="https://github.com/user-attachments/assets/d1ad4269-180d-4ceb-86bb-17256ba2b183" />

￼
Now it is time to upload a few files. I created a simple HTML page and named it “index.html”. I then uploaded the html file and my photo into the bucket. 

<img width="1470" alt="Screenshot 2025-02-24 at 22 41 33" src="https://github.com/user-attachments/assets/e47b7b2d-69fa-43eb-872b-9c97ab31d1d0" />


Accessing the webpage is done using the bucket website endpoint. 

<img width="1470" alt="Screenshot 2025-02-24 at 22 41 54" src="https://github.com/user-attachments/assets/c5e069a2-6f5f-4762-b926-a98944857f93" />


My result: A fully working webpage hosted on an AWS S3 bucket. 

<img width="1377" alt="Screenshot 2025-02-24 at 22 43 04" src="https://github.com/user-attachments/assets/c8d591d3-fb1e-4025-b82b-6c032979f3a6" />

￼
Next steps to improve the webpage:
Add an SSL certificate and a user friendly domain name using AWS’s Route 53.
