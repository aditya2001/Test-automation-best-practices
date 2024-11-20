## Test Automation Framework Best Practices --

### 1.Why do we need automation frameworks?
1. Reusability -> Automation test can be run again and again with same inputs and expected outputs.
2. Reduced human error -> Automated test reduces possibility of human errors because of less human intervention.
3. Continuous integration -> Automation test can be integrated with pipelines which can identify issues.
4. Efficiency -> Automated tests can be run faster and more frequently than manual tests which can save lots of time and resources.

### 2. What changes utilities have you added to the framework?
1. Driver Manager class to initialize the web driver based on the browser parameter.
2. Property utils class to read env specific config files and initialize the static variables. URL, id, password
3. Custom Exception classes like PropertyFileException extending RuntimeException.
4. Json Reader - used private static JSONParser parser = new JSONParser(); to read json files.
5. Response Handler - Response handler to deserialize the json into java object.

   used Jackon's object mapper class 

   ObjectMapper mapper = new ObjectMapper();


### 3. What is Test automation framework?
Test automation framework is a set libraries and guidelines that help us to design and execute test cases without any manual intervention.
It consists of several components where each component is responsible for specific tasks.

Best practices and tools include -
1. Test data handling methods 
2. Page object classes
3. Config reader class
4. Report generation api's

### 4. Why is Java popular among test automation frameworks?
Java is platform independent, object-oriented, has extensive library support, large community makes it suitable for integration with test automation frameworks like Selenium, TestNG.
Java works with object-oriented principles, error handling mechanism, allowing us to create reusable and maintainable tests.

1. Comprehensive libraries to support IO operations, file handling.
2. Strong typing to catch issues at compile time.
3. Easy integration with test frameworks like TestNG or Junit.

### 4. What is the role of exception handling in test automation?
Exception handling deals with unexpected events like missing elements or timeouts. we need to handle them without halting entire test execution.
We need to gracefully handle the errors.

try {
 WebElement element = driver.findElement(By.xpath("//input[@id=123]"));
 element.click();
} catch ( NoSuchElementException e) {
  System.out.println("Element not found");
  System.out.println("Handle thru java script executor)
  //
}

### 5. File handling in test automation ?
File handling allows to read data from and write results to file supporting data driven testing.
The commonly used classes are FileReader, Buffered Reader for reading and FileWriter and BufferedWriter for writing.

### 5. Why are TestNG and Junit so popular among testing frameworks?

JUnit and TestNG are Java testing frameworks, for unit, integration and end-to-end testing.
TestNG has advanced features like parametrized test and parallel execution.



### 6. Page object design pattern?
1. In page object design pattern we create a separate page class for each page, This helps in test maintenance by separating
page classes from test classes. Enhances test maintenance.
2. Reusability by defining page methods which can be used in other classes as well.
Reduces code duplication

Advantages of POM-
1. Reusability.
2. Better code maintenance.
3. Separation of test logic from page structure.
4. Less code duplication.
5. If the functionality changes you only need to update relevant page class.

### 7. How is POM different from Page Factory?
1. POM is a design pattern while Page Factory is a class in selenium that provides easier way to initialize the web elements.
2. Page Factory uses @FindBy annotation to locate elements.

### 8. Role of constructor in POM?
1. Constructors in POM are used to initialize the WebDriver instance variable and initializing page elements using page factory.
2. PageFactory.initElements(driver, this)

### 9 Disadvantages of POM?
1. POM can lead to creation of too many classes for large applications.
2. Increased complexity.


### 10. How can we use multiple drivers in POM?
Yes, We need to ensure each page class has its own driver instance to avoid conflicts.




