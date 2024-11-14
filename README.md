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
Test automation framework is a set tools and guidelines that help us to design and execute test cases.
It consists of several components where each component is responsible for specific tasks.

Best practices and tools include -
1. Test data handling methods 
2. Page object classes
3. Config reader class
4. Report generation api's


### 4. Report structure in your framework?
I have used mostly Extent reports.


