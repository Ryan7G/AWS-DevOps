Hey there. I hope you're excited to learn about cloud computing on AWS. I'm excited to get started too. So let's hop in.

To kick things off, we are going to cover some of the foundational concepts you'll need to know about when working with AWS. Working with AWS's part theory, part technical knowledge, part vocabulary and lots of practice and experimentation. These first few lessons are going to help you establish a little bit from each of those categories.

You will learn the theory behind cloud computing and the benefits of the cloud. This will help you make informed decisions about the cloud from a high level, and give you some of the reasoning around why and when to use the cloud.

Then we will dive into the AWS global infrastructure, covering regions and availability zones, followed by lessons on how to interact with AWS services. This lesson is going to give you the technical knowledge and vocabulary you need to create and discuss AWS architectures, and properly understand AWS documentation and examples.

A lot of what AWS offers can relate back to concepts used in traditional on-premises computing. And getting started with AWS means comparing these concepts to AWS concepts.

After that, we will begin to discuss security, and identity and access management. This is important to understand when you're getting started because as soon as you create an AWS account, you'll have some actionable knowledge on how to secure that account right from the start. Starting off secure is a good place to be.

Throughout all the topics, in these next few sections and over the duration of the entire course, we'll be using a sample employee directory web application to demonstrate how AWS services are used. Let's go ahead and take a look at the Employee Directory app.

You can see I'm in the browser, and I want to show you the functionality. This is a basic CRUD app or create read, update, delete. This app keeps track of employees within a company. So the first thing I'm going to do is create a new employee.

To create an employee, we'll give the employee a name, and I'm going to add myself. So I'll add my name. My location is USA. And then my job title, I'll enter in Cloud Technologist. And then we can add some badges for each employee. This is like an employee's flare, so I'm gonna select Mac User for myself and Photographer, and then I will click Save. Now, I'm back on the homepage, and I actually forgot to add a photo for this employee, so let's go ahead and edit it and add the employee photo.

You can also see this app gives me the ability to delete employees from the directory. So, those are the features of the app from a user's perspective. Time to review how we will build this app using AWS services.

This application will be built in a private network using Amazon Virtual Private Cloud or VPC. We will host the application's backend code on Amazon Elastic Compute Cloud, or EC2, which is a service that essentially offers virtual machines on AWS. So let's go ahead and add those servers to our diagram.

The employee data will be stored in a database, which will also live inside this network and will be hosted using a service called Amazon Relational Database Service or RDS. So I'll go ahead and add that to the diagram as well.

The images for the employees will be stored using the object storage service, Amazon Simple Storage Service or S3, which allows the unlimited storage of any type of file, like images in our example. These are the basic building blocks of our application.

We will use Amazon CloudWatch for monitoring this solution, and we will also want to ensure that our application is scalable and fault tolerant. So I'm going to go ahead and add Amazon Elastic Load Balancing and Amazon EC2 Auto Scaling to this diagram.

For security and identity, we will be using Amazon Identity and Access Management or IAM, so let's add that. There's a lot of pieces on this diagram, but don't worry, we will build this app step by step using the AWS Management Console. We will add to this diagram, reference it, and change it throughout the course to meet our needs and let it evolve as new ideas and techniques enter our world.

One more thing to note about this course before I let you go. If you hear this noise, (notification dings) it means that you are gonna be seeing one of our informational popups on the screen, which convey extra information like word definitions, AWS best practices, tips, tricks, or general commentary written for you by our lively, furry sidekicks, Meowzy and Fluffy. They know all the tips and are very helpful little friends to have around during this course.

That's it for now, see you soon.
