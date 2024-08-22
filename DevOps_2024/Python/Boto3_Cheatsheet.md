### Setup and Configuration
Install Boto3 :Setup and Configuration


```
pip install boto3
```
- Import and Initialize Boto3
```
import boto3

# Initialize a session using Amazon S3
s3 = boto3.client('s3')

# Initialize a session using Amazon EC2
ec2 = boto3.resource('ec2')
```

**AWS Credentials and Configuration**

Boto3 automatically looks for credentials in the following order:

- Environment variables (AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY)
- AWS credentials file (~/.aws/credentials)
- AWS config file (~/.aws/config)
- IAM roles assigned to the instance

### Amazon S3 Operations

- Create an S3 Bucket
```
s3.create_bucket(Bucket='my-new-bucket')
```
- List All Buckets
```
response = s3.list_buckets()
for bucket in response['Buckets']:
    print(bucket['Name'])
```
- Upload a File to S3
```
s3.upload_file('local_file.txt', 'my-new-bucket', 'file_in_s3.txt')
```

- Download a File from S3
```
s3.download_file('my-new-bucket', 'file_in_s3.txt', 'local_file.txt')
```

- List Files in a Bucket
```

response = s3.list_objects_v2(Bucket='my-new-bucket')
for obj in response.get('Contents', []):
    print(obj['Key'])
```

- Delete an S3 Object
```

s3.delete_object(Bucket='my-new-bucket', Key='file_in_s3.txt')
```

### Amazon EC2 Operations
- Launch a New EC2 Instance
```
ec2.create_instances(
    ImageId='ami-0abcdef1234567890',
    MinCount=1,
    MaxCount=1,
    InstanceType='t2.micro',
    KeyName='my-key-pair'
)
```

- List Running EC2 Instances
```

for instance in ec2.instances.filter(Filters=[{'Name': 'instance-state-name', 'Values': ['running']}]):
    print(instance.id, instance.instance_type)
```
- Stop an EC2 Instance
```

ec2.instances.filter(InstanceIds=['i-0123456789abcdef0']).stop()
```
- Start an EC2 Instance
```
ec2.instances.filter(InstanceIds=['i-0123456789abcdef0']).start()
```
- Terminate an EC2 Instance
```
ec2.instances.filter(InstanceIds=['i-0123456789abcdef0']).terminate()
```

###Amazon DynamoDB Operations
- Initialize DynamoDB Resource
```
dynamodb = boto3.resource('dynamodb')

- Create a DynamoDB Table
```

table = dynamodb.create_table(
    TableName='my-table',
    KeySchema=[
        {
            'AttributeName': 'id',
            'KeyType': 'HASH'  # Partition key
        }
    ],
    AttributeDefinitions=[
        {
            'AttributeName': 'id',
            'AttributeType': 'S'  # String
        }
    ],
    ProvisionedThroughput={
        'ReadCapacityUnits': 5,
        'WriteCapacityUnits': 5
    }
)
```

- List All DynamoDB Tables
```
tables = list(dynamodb.tables.all())
for table in tables:
    print(table.name)
```

- Put an Item into DynamoDB
```
table = dynamodb.Table('my-table')
table.put_item(
   Item={
        'id': '123',
        'name': 'John Doe',
        'age': 30
    }
)
```
- Get an Item from DynamoDB
```
response = table.get_item(
    Key={
        'id': '123'
    }
)
item = response['Item']
print(item)
```

- Update an Item in DynamoDB
```
table.update_item(
    Key={
        'id': '123'
    },
    UpdateExpression='SET age = :val1',
    ExpressionAttributeValues={
        ':val1': 31
    }
)
```

- Delete an Item from DynamoDB
```
table.delete_item(
    Key={
        'id': '123'
    }
)

```
### Amazon SNS (Simple Notification Service) Operations
- Initialize SNS Client
```
sns = boto3.client('sns')
```

- Create a Topic
```

response = sns.create_topic(Name='my-topic')
topic_arn = response['TopicArn']
```

- List All Topics
```
response = sns.list_topics()
for topic in response['Topics']:
    print(topic['TopicArn'])
```

- Subscribe to a Topic
```
sns.subscribe(
    TopicArn=topic_arn,
    Protocol='email',
    Endpoint='example@example.com'
)
```
- Publish a Message to a Topic
```
sns.publish(
    TopicArn=topic_arn,
    Message='Hello World!',
    Subject='Test Message'
)
```

- Delete a Topic
```
sns.delete_topic(TopicArn=topic_arn)
```
### Amazon SQS (Simple Queue Service) Operations
- Initialize SQS Client
```
sqs = boto3.client('sqs')
```

- Create a Queue
```
response = sqs.create_queue(QueueName='my-queue')
queue_url = response['QueueUrl']
```

- List All Queues
```
response = sqs.list_queues()
for queue in response.get('QueueUrls', []):
    print(queue)
```

- Send a Message to SQS Queue
```
sqs.send_message(QueueUrl=queue_url, MessageBody='Hello World!')
```

- Receive Messages from SQS Queue
```
response = sqs.receive_message(QueueUrl=queue_url)
for message in response.get('Messages', []):
    print(message['Body'])
    sqs.delete_message(QueueUrl=queue_url, ReceiptHandle=message['ReceiptHandle'])
```

- Delete an SQS Queue
```
sqs.delete_queue(QueueUrl=queue_url)
```
### AWS Lambda Operations
- Initialize Lambda Client
```

lambda_client = boto3.client('lambda')
```
- Create a Lambda Function
```
with open('lambda_function.zip', 'rb') as f:
    zipped_code = f.read()

response = lambda_client.create_function(
    FunctionName='my-function',
    Runtime='python3.8',
    Role='arn:aws:iam::123456789012:role/execution_role',
    Handler='lambda_function.lambda_handler',
    Code=dict(ZipFile=zipped_code)
)
```

- Invoke a Lambda Function
```
response = lambda_client.invoke(
    FunctionName='my-function',
    InvocationType='RequestResponse',
    Payload=json.dumps({"key": "value"})
)
response_payload = json.load(response['Payload'])
print(response_payload)
```

- List Lambda Functions
```
response = lambda_client.list_functions()
for function in response['Functions']:
    print(function['FunctionName'])
```

- Delete a Lambda Function
```
lambda_client.delete_function(FunctionName='my-function')
```
