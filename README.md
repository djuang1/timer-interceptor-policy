# Timer Interceptor Policy

With the introduction of Mule 4.x, the interceptor-stack in Mule 3.x has been removed ( [link](https://docs.mulesoft.com/mule-runtime/4.1/migration-core) ) and the recommended approach is to use custom policies.

This project provides a Mule 4.x custom policy that can be published to your Anypoint Exchange and applied to your APIs to provide visibility into the time it takes to process a transaction in milliseconds.

# Setup

1. Modify the pom.xml file and change the `groupId` to your Anypoint Platform Organization ID
2. Package the custom policy by running the following command below. Additional info can be found at this [link](https://docs.mulesoft.com/api-manager/2.x/custom-policy-packaging-policy)
```
mvn clean install
```
3. Upload the custom policy to Exchange by running the following command below. Additional info can be found at this [link](https://docs.mulesoft.com/api-manager/2.x/custom-policy-uploading-to-exchange)
```
mvn deploy
```
4. In Anypoint API Manager, apply the policy to your APIs running on Mule 4.x
