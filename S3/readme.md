# Learning
What is S3

What is Object 

How to use versioning

How to retrieve deleted data by using versioning


What is Bucket , Object , Naming rules of bucket

# S3 (Amazon Simple Storage Service)

In this we can store our data , we can also host our website bu ysing S3

if we are using S3 AWS will charge for( that storage , no. of peoples dowloaded that data , no of requests for that particular data)

In S3 we have to create one folder and it is known as BUCKET in AWS , name of that bucket is always unique from AWS buckets , we create bucket in specific region not globally

**(our AMIs or snapshots also store in S3 of AWS itself)


Data in our bucket is known as object

Bucket Name must not contain Uppercase character , bucket name (3-63) character long , bucket name will always start with small letter or number only

In S3 bucket we can upload a file or can create one folder & we can also create a folder inside one folder

When we upload only file in bucket and see its key it is index.html

But when we create one folder name aman4399 & upload file namely index.html then its key will be (aman4399/index.html) , here aman4399 is called as prefix 

If you upload a file of same name again in folder AWS will replace it with older one 


# Objects

when you go ina ibject you can see tis properties like it iwner , region in which my object is created , last modeifrid date , ARN , file syntax etc .

There is one metadata which is of two types (user defined & system defined)

Key is a object name 

# Preventing a object from deletion using Versioning

Problem statement - Lets suppose you create a file nd then edit it after 2 days amd you save it then the old file is replace , after some time you again edit the file & update it then 2nd one file will be replaced .

But your client ask the file wchich was updated 1st time , how will you give that because files is replaced in this case preventing helps us using versioning 


So for this ,

Go to your bucket

Go on Bucket properties , then edit bucket versioning and set it set as enabled .

Once you enable versioning and go inside a folder you will see one new option (Show versions )

Now if you upload the updated file with same name AWS will replace it , but when you toggle on the show versions you will see sub files with last updted date .


**(if we delete our latest updted file then updated file is delete but when you enable show versions you can see your files again)

**(if you delete your file by mistakely you can again retreive it this o=is the good part of versioning )

(so to do this go on show versions , select on delete marker & then delete it , after that when you refresh it you will see your file will appear again)


if after some time we disbale our bucket versioning then also we can see our files in version toggle which was uploaded before diabling 

