How to host a static website on AWS S3 and CloudFront

1. In your AWS account, search for S3 bucket and create
![](./Images/1.JPG)

2. Pick a unique bucket name![](./Images/2.JPG)

3. Disable ACL and uncheck public access![](./Images/3.JPG)

4. Acknowledge![](./Images/4.JPG)

5. Click on create bucket
![](./Images/5.JPG)

6. Click on the bucket name
![](./Images/6.JPG)

7. Under the 'objects' tab, click to upload files. You will upload the files needed to host your static website. (html file, css and the images).
![](./Images/7.JPG)

8. Add the files. ![](./Images/8.JPG)

9. Upload![](./Images/9.JPG)

10. Upload successful. You should get this notification status. If you have errors, check your network connection.![](./Images/10.JPG)

11. Go to your bucket properties![](./Images/11.JPG)

12. Scroll down to enable static website hosting![](./Images/12.JPG)

13. Enable static website hosting and type 'index.html' in the index document. ![](./Images/13.JPG)

14. Save your changes and reload your page. It will automatically display your website url![](./Images/14.JPG)

15. Copy the url and paste on your browser. Notice the website url bearing your bucket name. This error pae will pop up. It shows your website has been hosted but you're unable to view its content because you have not added the necessary permissions.![](./Images/15.JPG)

16. To add the necessary permissions for public access, you need to attach a bucket policy. Go to the permissions tab.![](./Images/16.JPG)

17. Scroll down to bucket policy and edit.![](./Images/17.JPG)

18. Write your policy and save changes. This policy will grant public access.![](./Images/18.JPG)

19. Go back to your browser and reload the page. The content of your website is now visible.![](./Images/19.JPG)

20. The next step is connecting your website to cloudfront. This is done for low latency and high transfer speed in accessing the website. In your management console, search for cloudfront and create.![](./Images/20.JPG)

21. Click on origin name and select your newly created bucket. ![](./Images/21.JPG)

22. Scroll down the page and enable firewall.![](./Images/22.JPG)

23. Go down to the defaukt root and write 'index.html'. Create your distribution. ![](./Images/23.JPG)

24. Allow the deployment process to be completed. Copy and paste the domain name on your browser. ![](./Images/24.JPG)

25. Your website now has '.cloudfront.net' extension. ![](./Images/25.JPG)

If you're just practicing and not using this for production,, kindly remember to delete and terminate all the resources you created. Delete the s3 bucket and the cloudfront distribution to avoid billings.