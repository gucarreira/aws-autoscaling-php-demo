## AWS AutoScaling PHP App Demo

The purpose of this demo is show how to use some AWS services to create a scalable architecture. We are going to create a web app architecture and do a load test.

![demo](architecture/scaling.jpg)

The architecture above shows a VPC separating the subnets in public and private subnets, a high scalable application layer utilizing AutoScaling and a high scalable data layer with managed cache service **(Amazon ElastiCache)** to store sessions and managed relational database service **(Amazon RDS)** with replicas to scale reads. Also, we are storing static assets in a bucket **(Amazon S3)** and utilizing a CDN **(Amazon CloudFront)** to deliver the static assets and minimize latency to deliver dynamic content.

![test](architecture/locust.jpg)

To test the application architecture we are utilizing the tool **Locust**, an open source load testing tool, to simulate users acessing our workload.

To get started you will need an IAM user with the following access:

* CloudFormation
* EC2
* CloudFront
* ElastiCache
* RDS
* S3
* VPC
* CloudWatch
* Route53
* IAM

__Note: Tested in the N. Virginia region (us-east-1).__

## App CloudFormation

## AutoScaling

## Load CloudFormation

## Testing

## Next Steps

## Clean up
1. Delete the resources that you created (Route53, CloudFront, AutoScaling)
2. Open the CloudFormation console at https://console.aws.amazon.com/cloudformation
3. Select the CloudFormation stack and click on Delete button

## Reference links
* Scaling up to your first 10 million users: https://www.youtube.com/watch?v=Ma3xWDXTxRg
* Getting started AutoScaling: https://docs.aws.amazon.com/autoscaling/ec2/userguide/GettingStartedTutorial.html
* Locust: https://docs.locust.io/en/stable/
* Getting started with CloudFront: https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/GettingStarted.html
* Getting started with Route53: https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/getting-started.html

## License summary
This sample code is made available under the MIT-0 license. See the LICENSE file.