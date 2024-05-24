# Getting Started

### Reference Documentation

For further reference, please consider the following sections:

* [Official Gradle documentation](https://docs.gradle.org)
* [Spring Boot Gradle Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/3.2.5/gradle-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/3.2.5/gradle-plugin/reference/html/#build-image)
* [Spring Web](https://docs.spring.io/spring-boot/docs/3.2.5/reference/htmlsingle/index.html#web)

### Guides

The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)

### Additional Links

These additional references should also help you:

* [Gradle Build Scans – insights for your project's build](https://scans.gradle.com#gradle)

# Cash Card Application

The chart below has more details about Cash Card RESTful CRUD operations.

| Operation | API Endpoint    | HTTP Method | Response Status |
|-----------|-----------------|-------------|-----------------|
| Create    | /cashcards      | POST        | 201 (CREATED)   |
| Read      | /cashcards/{id} | GET         | 200 (OK)        |
| Update    | /cashcards/{id} | PUT         | 204 (NO DATA)   |
| Delete    | /cashcards/{id} | DELETE      | 204 (NO DATA)   |

The sections above can be summarised using the following table:

| HTTP Method | Operation | Definition of Resource URI           | What does it do?                                                                      | Response Status Code | Response Body        |
|-------------|-----------|--------------------------------------|---------------------------------------------------------------------------------------|----------------------|----------------------|
| POST        | Create    | Server generates and returns the URI | Creates a sub-resource ("under" or "within" the passed URI)                           | 201 CREATED          | The created resource |
| PUT         | Create    | Client supplies the URI              | Creates a resource (at the Request URI)                                               | 201 CREATED          | The created resource |
| PUT         | Update    | Client supplies the URI              | Replaces the resource: The entire record is replaced by the object in the Request     | 204 NO CONTENT       | (empty)              |
| PATCH       | Update    | Client supplies the URI              | URI	Partial Update: modify only fields included in the request on the existing record | 200 OK               | The updated resource |

### TDD -> Unit Tests -> Integration Tests -> E2E Tests

1. Red:Write a failing test for the desired functionality.
2. Green:Implement the simplest thing that can work to make the test pass.
3. Refactor:Look for opportunities to simplify, reduce duplication, or otherwise improve the code without changing any
   behavior—to refactor.
4. Repeat!

The three integration points in our application are the API "front door", the database, and security.

once downloaded <code>chmod +x ./gradlew</code> to run command line <code>./gradlew test</code>

Other popular data formats include YAML (Yet Another Markup Language) and XML (Extensible Markup Language). When
compared to XML, JSON reads and writes quicker, is easier to use, and takes up less space. You can use JSON with most
modern programming languages and on all major platforms. It also works seamlessly with Javascript-based applications.

* You’ve delved into REST and the lore of HTTP verbs: not just GET, but also PUT, PATCH, and POST.
* You've used HTTP response status codes as designed: not just 200 OK, but 204 NO CONTENT and 201 CREATED as well.
* By using Spring Boot, you’ve now got a solid understanding of Spring. You learned about its Inversion of Control
  container, how to use annotations, and how to employ auto-configuration to free you from configuration tasks.
* You built the API using a layered architecture. You understand how Spring Security sits at the “front” of the API,
  Spring Web enables HTTP communications between the API and its clients, and Spring Data handles reading and writing
  to/from the relational data store.
* You used a test-first approach to provide confidence that your application works as designed while driving out your
  app's functionality.
* You drove your implementation using a Steel Thread - exercising all the integration points and validating your
  architecture early on to de-risk your functionality.
* You used the Red, Green, Refactor process to improve your code (and tests!) throughout the application development.