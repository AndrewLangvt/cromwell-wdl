# Setting up Cromwell on AWS
#### Additional information about Cromwell [here](https://docs.opendata.aws/genomics-workflows/)

To run cromwell, you will need several components
 1) Virtual Private Cloud (VPC)- optional
 2) AWS Batch compute infrastructure
 3) AWS Batch Job Queues
 4) IAM Roles
 5) S3 Bucket
 6) EC2 Launch Templates

While these can be created individually by following the instructions [here](https://docs.opendata.aws/genomics-workflows/quick-start/), it is significantly easier to simply to a `full stack deployment` found [here](https://docs.opendata.aws/genomics-workflows/orchestration/cromwell/cromwell-overview/)

### Full Stack Deployment
1) Begin deployment (2 methods)
  - click the orange arrow on [this page](https://docs.opendata.aws/genomics-workflows/orchestration/cromwell/cromwell-overview/) to deploy Cromwell All-in-one 
  - manually input template
    - On AWS, navigate to "CloudFormation" and click `create stack` (select "with new resources" if you are doing a build from scratch)
    - Upload your `yaml` file to serve as the template for the build. Can be found [here](https://github.com/aws-samples/aws-genomics-workflows/blob/master/src/templates/cromwell/cromwell-aio.template.yaml)
2) enter stack name
3) select Ec2 key pair
4) name your S3 bucket (select `true` in following line if it already existst) NOTE: must be all lowercase, and globally unique
5) choose your instance type
6) click next
7) specify tags, if desired (for tracking of resource usage purposes)
8) click next
9) review stack and select BOTH "I acknowledge" boxes at the bottom of the page
10) launch your stack
