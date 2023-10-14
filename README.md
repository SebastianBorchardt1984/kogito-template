# kogito-template

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application, packaged as an _über-jar_, is now runnable using `java -jar target/*-runner.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Dnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Dnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/kogito-template-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.

## Related Guides

- Kogito Add-On Events Decisions ([guide](https://quarkus.io/version/2.13/guides/kogito-dmn)): Kogito Add-On for processing events on Decisions (DMN) based projects
- Kogito Add-On User Tasks e-mail ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On for e-mail support on Human Tasks.
- Kogito Add-On Events MongoDB ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On for storing Kogito events log on MongoDB for later pushing via Debezium, allowing Outbox pattern implementation.
- Kogito Add-On Monitoring Elasticsearch ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On for Elasticsearch Monitoring
- Kogito Add-On Knative Eventing ([guide](https://quarkus.io/version/2.13/guides/kogito)): Adds support for CloudEvents on top of HTTP and Knative env vars configuration.
- Kogito Addons Quarkus Data Index MongoDB ([guide](https://quarkus.io/guides/kogito)): Kogito Data Index MongoDB Add-On
- Kogito - Decisions (DMN) ([guide](https://quarkus.io/version/2.13/guides/kogito-dmn)): Add Kogito decision (DMN) capabilities - Include Drools DMN engine
- SmallRye GraphQL ([guide](https://quarkus.io/guides/microprofile-graphql)): Create GraphQL Endpoints using the code-first approach from MicroProfile GraphQL
- Kogito Add-On Process Messaging ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Events handling for BPMN messages Add-On
- Kogito Add-On Process Management ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Process Management REST API
- Kogito ([guide](https://quarkus.io/version/2.13/guides/kogito)): Add business automation capabilities - processes and rules with Kogito (a toolkit that originates from projects Drools and jBPM)
- Kogito Runtime Tools ([guide](https://quarkus.io/guides/kogito)): Runtime development tools for Kogito projects
- SmallRye OpenAPI ([guide](https://quarkus.io/guides/openapi-swaggerui)): Document your REST APIs with OpenAPI - comes with Swagger UI
- Kogito - Rules (DRL) ([guide](https://quarkus.io/version/2.13/guides/kogito-drl)): Add Kogito rules (DRL) capabilities - Include Drools engine
- Kogito Add-On Monitoring Prometheus ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On for Prometheus Monitoring
- SmallRye Reactive Messaging - Kafka Connector ([guide](https://quarkus.io/guides/kafka-reactive-getting-started)): Connect to Kafka with Reactive Messaging
- SmallRye GraphQL Client ([guide](https://quarkus.io/guides/smallrye-graphql-client)): Create GraphQL Clients
- Kogito Add-On Jobs Service ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On to interact with Kogito Jobs Service
- Kogito Add-On Task Management ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On Task Management REST API
- Kogito - Predictions (PMML) ([guide](https://quarkus.io/version/2.13/guides/kogito-pmml)): Add Kogito predictions (PMML) capabilities - Include Drools PMML engine
- REST Client Reactive ([guide](https://quarkus.io/guides/rest-client-reactive)): Call REST services reactively
- Kogito Add-On Tracing Decision ([guide](https://quarkus.io/version/2.13/guides/kogito-dmn)): Kogito Add-On to enable tracing decisions projects
- Kogito Add-On Events Rules ([guide](https://quarkus.io/version/2.13/guides/kogito-drl)): Kogito Add-On for processing events on Rules (DRL) based projects
- Kogito - Process (jBPM) ([guide](https://quarkus.io/version/2.13/guides/kogito)): Add Kogito Processes capabilities - Includes Process (jBPM) Engine
- Kogito Add-On Events Process ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On for Processes Events
- RESTEasy Reactive ([guide](https://quarkus.io/guides/resteasy-reactive)): A JAX-RS implementation utilizing build time processing and Vert.x. This extension is not compatible with the quarkus-resteasy extension, or any of the extensions that depend on it.
- Kogito Add-On Jobs Service Messaging ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On to interact with the Kogito Jobs Service using events via the reactive messaging api
- SmallRye Health ([guide](https://quarkus.io/guides/microprofile-health)): Monitor service health
- Kogito Add-On Process SVG ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On for SVG process generation
- Kogito Add-On Task Notification ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On to handle tasks notifications
- SmallRye Reactive Messaging ([guide](https://quarkus.io/guides/reactive-messaging)): Produce and consume messages and implement event driven and data streaming applications
- Kogito Add-On Persistence MongoDB ([guide](https://quarkus.io/version/2.13/guides/kogito)): Kogito Add-On support for persistence on MongoDB

## Provided Code

### Kogito DMN codestart

This is an example Kogito DMN Quarkus codestart, it contains a sample DMN model for REST code generation based on the model definition.

[Related guide section...](https://quarkus.io/version/2.13/guides/kogito-dmn)

This Kogito DMN Quarkus codestart contains a sample DMN model as described in the [Quarkus Kogito DMN guide](https://quarkus.io/version/2.13/guides/kogito-dmn).
The goal is to showcase automatic REST endpoint codegen, based on the content of the model.
The `pricing.dmn` DMN model calculates a base price quotation based on some criteria provided as input.

You can reference the [full guide on the Quarkus website](https://quarkus.io/version/2.13/guides/kogito-dmn).

### Reactive Messaging codestart

Use SmallRye Reactive Messaging

[Related Apache Kafka guide section...](https://quarkus.io/guides/kafka-reactive-getting-started)


### RESTEasy Reactive

Easily start your Reactive RESTful Web Services

[Related guide section...](https://quarkus.io/guides/getting-started-reactive#reactive-jax-rs-resources)

### SmallRye GraphQL

Start coding with this Hello GraphQL Query

[Related guide section...](https://quarkus.io/guides/smallrye-graphql)

### SmallRye Health

Monitor your application's health using SmallRye Health

[Related guide section...](https://quarkus.io/guides/smallrye-health)
