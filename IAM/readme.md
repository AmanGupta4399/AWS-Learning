# Learnig 

What is IAM

To create user with or without any permission

What is Policies 

To create User , User groups

To add user in a user groups 

To access any user by CLI

What is User Groups
# IAM 
Identify & Access Managment 

It is a AWS service which help us to control access , permission to our AWS resources (like for instance , S3, VPC etc)

like we want that person who have right to create new instance , can't access my bucket for that we use IAM Service 

IAM Service is global, not in any particluar zone 

Ther eis 5 default roles in IAM

# User
we create user in AWS which contains its user group, permissions etc 

# Creating user without any permission

When we giver user to access AWS console we have to set one password for that particular user and can set whether user  have to chnage  its password or not after 1st login

We have to give permission to that particular user that what he can access or not , we can also create user without any permission , after we created user AWS gives it URL for that user by which he can login and that URL contains its IAM id .

We dont give any permission to that user so when he login to cosnole & try to acees any service he get one mesaage (API Error in dashboard)

# Creating user with permission 

When I create user & add a policy to that user which is (Amzon EC2 full Access) by this when user sign in he can Access EC2 but rest of all services is disable for that user beacuse we inly give EC2 permission


**(if we create one user , and copy its permission from existing user then new user will also have same permission as existing user as well as that new user will also add in that user group in which existing user is define)

# Policies 

policy is generally a permission which we give to user 

By default there is 1441 policies in AWS , we can also create a custom policy

# USer Groups

It is a collection of several users which have same permissions , means instaed of giving permission to different different user we will add our user in that user group 

After adding our user in that user group he will also have the same permissions which we give to that user group

** (Single user can be a part of Multiple Groups) 

# Account Settings

In this we can edit our password poicy (there is a default password policy by IAM but you can custom it 

Maximum pssword expiration days is ( 1 day to 3 years)

We can also use prevent password reuse (means we will enter number like 5 which means that we cant use last 5 passwords )

# To access user by CLI

Create one user 

Go to that user 

Go to Security Credentials , under it create access key , select CLI because you need to connect it via CLI

After creating Acess key copy access key and secret access key 

If doing first time downnload  AWS CLI v2

then go to cmd

type aws configure , then paste access key and secret acces key on cli and you will be connect to your AWS by CLI
