## Creating a Lambda function with Quarkus!

To execute the following steps it's necessary to have the following tools:

- Java 11
- GraalVM
- Maven or Gradle
- Docker (If you are not using Linux)
- Configure the following environment variable with a role that can access a lambda function:
    `LAMBDA_ROLE_ARN="arn:aws:iam::1234567890:role/lambda-role"`
    
To create the lambda role, you can do it on the AWS UI:



## Install a native image function for Mac or Windows
mvn clean install -Dnative -Dquarkus.native.container-build=true

## Create a normal function
target/manage.sh create

## Invoke a normal function
target/manage.sh invoke

## Delete a normal function
target/manage.sh delete

## Create a native function
target/manage.sh native create

## Invoke a native function
target/manage.sh native invoke

## Delete a native function
target/manage.sh native delete

## Extra information - To generate a Quarkus application, use the following command

```
mvn archetype:generate \
       -DarchetypeGroupId=io.quarkus \
       -DarchetypeArtifactId=quarkus-amazon-lambda-archetype \
       -DarchetypeVersion=1.8.3.Final
```

