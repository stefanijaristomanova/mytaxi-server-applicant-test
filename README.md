mytaxi backend Applicant Test Service

# Task Description
You should be able to start the example application by executing com.mytaxi.MytaxiServerApplicantTestApplication, which starts a webserver on port 8080 (http://localhost:8080) and serves SwaggerUI where can inspect and try existing endpoints.

The project is based on a small web service which uses the following technologies:

* Java 1.8
* Spring MVC with Spring Boot
* Database H2 (In-Memory)
* Maven

You should be aware of the following conventions while you are working on this exercise:

 * All new entities should have an ID with type of Long and a date_created with type of ZonedDateTime.
 * The architecture of the web service is built with the following components:
 	* DataTransferObjects: Objects which are used for outside communication via the API
   * Controller: Implements the processing logic of the web service, parsing of parameters and validation of in- and outputs.
   * Service: Implements the business logic and handles the access to the DataAccessObjects.
   * DataAccessObjects: Interface for the database. Inserts, updates, deletes and reads objects from the database.
   * DomainObjects: Functional Objects which might be persisted in the database.
 * TestDrivenDevelopment is a good choice, but it's up to you how you are testing your code.

You should commit into your local git repository and include the commit history into the final result.

## Task 2
First come first serve: A car can be selected by exactly one ONLINE Driver. If a second driver tries to select a already used car you should throw a CarAlreadyInUseException.

## Task 3
Make use of the filter pattern to implement an endpoint in the DriverController to get a list of drivers with specific characteristics. Use the characteristics of Driver and Car.
