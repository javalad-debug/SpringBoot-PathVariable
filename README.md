# Create Spring Boot REST API with Path Variable

- Create a REST API to handle a path variable in a requests, so basically SpringBoot provides @pathvariable annotation to handle Path Variables in a request.
- Write the springBoot REST API that handles the Path Variable in a request URL
- Create a method and make that method like a REST API



### Ref Path/ Code:

```diff
springboot-rest-api\springboot-rest-api\src\main\java\net\javaguides\springboot\controller\StudentController.java
```

```bash
 public Student studentPathVariable(int id){
      }
```
- In order to bind the value of the URL template variable to the method argument, (id), we use the @PathVariable annotation

```bash
    public Student studentPathVariable(@PathVariable int id){
      }
```

- Use this if the URL template variable name is different from method argument (studentId)

```bash 
 // Example, if URL template variable name is, id
   public Student studentPathVariable(@PathVariable("id") int id){
      }
```
- To use multiple PATH VARIABLE in a URL

```bash
     // SpringBoot REST API with PATH VARIABLE
    // This {id} is called, URL template variable
    // http://localhost:8080/students/1/John/Doe
    @GetMapping("students/{id}/{first-name}/{last-name}")
    public Student studentPathVariable(@PathVariable("id") int studentId,
        @PathVariable("first-name") String firstName,
        @PathVariable("last-name") String lastName){
        return new Student(lastName, firstName, studentId);
    }

```
## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update `tests` as appropriate.

## License

***
