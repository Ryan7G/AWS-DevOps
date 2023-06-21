# AWS Global Infrastructure
For our employee directory application, we'll be using photos of each of our employees.

If we have only one copy of those photos and don't want to lose them, we have to store them somewhere safe. 

Currently, the only copy of these photos are saved on my laptop. But if my laptop breaks, what happens? No more photos. 

I want to make sure this doesn't happen, so I'm going to upload the photos to AWS to ensure that the copies exist even if my laptop is destroyed. 

This also allows me to access my photos from anywhere, my home, my phone, a plane, on a train, everywhere. 

When I store these photos in an AWS service, I'm storing it in a data center somewhere, on servers inside that data center. 

But if a natural disaster happens, such as an alien coming down from space and destroying a data center, then what do we do? Luckily, AWS has planned for
this event and many others, including natural disasters and other unavoidable alien accidents. 

The way they plan for it is through redundancy. AWS has clusters of data centers around the world. 

So here AWS would have a second data center connected to the first through redundant high speed and low latency links. That way, if the first
data center goes down, the second data center is still up and running. 

This cluster of data centers is called an availability zone or AZ. An AZ consists of one or more data centers with redundant power,
networking, and connectivity. Unfortunately, sometimes natural disasters like hurricanes or other disasters might also extend to
impacting an entire AZ, but AWS has planned for that, too, again, using redundancy. 

Like data centers, AWS also clusters AZs together and also connects them with redundant high speed and low latency links. A cluster of AZs is
simply called a region. 

In AWS, you get to choose the location of your resources by not only picking an AZ, but also choosing a region. 

Regions are generally named by location so you can easily tell where they are. 

For example, I could put our employee photos in a region in Northern Virginia called the Northern Virginia Region. 

So knowing there are many AWS regions around the world, how do you choose an AWS region? As a basic rule, there are four aspects you need to consider when
deciding which AWS region to use, compliance, latency, price, and service availability. 

Let's start with compliance. Before any other factors, you must first look at your compliance requirements. You might find that your application, company, or country that you live in requires you to handle
your data and IT resources in a certain way. 

Do you have a requirement that your data must live in the UK boundaries? Then you should choose the London Region, full stop. 

None of the rest of the factors matter. 

Or if you operate in Canada, then you may be required to run inside the Canada Central Region. 

But if you don't have a compliance or regulatory control dictating your region, then you can look at other factors. 

For example, our employee photos are not restricted by regulations, so I can continue looking at the next factor, which is latency. 

Latency is all about how close your IT resources are to your user base. 

If I want every employee around the world to be able to view the employee photos quickly, then I should place the infrastructure that hosts those photos
close to my employees. 

We are all bound by the speed of light. Applied to your business, that means that if your users live in Oregon, then it makes sense to run your application in the Oregon Region. You could run it in the Brazil Region, but the latency from Oregon to Brazil might impact your users and create a slower load time. But maybe I really want
to run my application or store my employee photos in Brazil. 

One problem I might run into is the pricing, which is the next factor we'll talk about. 

The pricing can vary from region to region, so it may be that some regions, like the Sao Paulo Region, are more expensive than others due to different tax structures. 

So even if I wanted to store my employee photos in Brazil, it might not make sense from the latency perspective or the pricing perspective. 

And then finally, the fourth factor you'll want to consider is the services you want to use. 

Often when we create new services or features in AWS, we don't roll those services to every region we have right away. 

Meaning, if you want to begin using a new service on day one after it launches, then you'll want to make sure it operates in the region that you're looking at running
your infrastructure in. 

To recap, regions, availability zones, and data centers exist in a redundant, nested sort of way. 

There are data centers inside of availability zones and availability zones inside of regions. And how do you choose a region? By looking at compliance, latency, pricing, and service availability. Those are the basics, but it
isn't the end of the story when it comes to AWS global infrastructure. 

We also have the Global Edge Network, which consists of Edge locations and regional Edge caches. 

Edge locations and regional Edge caches are used to cache content closer to end users, thus reducing latency. 

Consider this scenario. You are a company hosting a website to your users all over the world. 

Even though your website is being downloaded from all over, it's hosted out of an AWS region in North America, say Ohio. 

Without caching, every user would need to send a request to the Ohio region where
the data is downloaded, and then the data would be returned to the user and rendered in their browser. 

If the user is located in the USA or nearby country, there may not be much latency in this process. 

However, if a user is coming from a place that is located far from the Ohio region, then latency will be greater. 

Latency is a big hurdle for many use cases, including web applications. So to reduce this latency, you could use the Edge locations to cache frequently accessed content. 

When you cache content at an Edge location, a copy is hosted across the Edge locations around the world. 

That way, when a user goes to retrieve that information, it will come from the closest Edge location, which will greatly reduce
the latency for that user. 

You can use services like Amazon CloudFront to cache content using the Edge locations.
