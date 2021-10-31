Important Points:
1. All test data required is placed in "conduitData.xlsx" file which is available in src/main/resources/resources.
2. Path for browser is handled by webdriverManager api.
3. Please execute this program from testng.xml


************************************About project and Structure********************************************************
1.src/main/java : contains all main functions
	
com.conduit.qa.base : Contains two methods "init" and start appliaction.

        init() : init method checks for the browser and initilises driver.
        StartApplication() : Start application get the url from properties file initialises driver and returns
                             an object of homepage class. 

com.conduit.qa.config : contains a property file where all cofigurations are mentioned.

com.conduit.qa.pages : This package cotains all the page classes.

        HomePage Class :  home page class contains page factory and methodes to test the home page elements.

        SignInPage Class : Sign In class contains page factory and methodes to test the Sign In elements.
        
        SignUpPage Class :  SignUP page class contains page factory and methodes to test the SignUp page elements.

        

com.conduit.qa.utils : This package contains commonUtils class which contains some common methods to be used.
              
          getProperty() : get property method initilises a property object and reads data from the config.property file.
          
          getDataFromExcel() : get data from excel is utility used to read excel file the retun the data as object.

          waitForElement() : wait for element method waits for the elements until it is present using the explicite wait.


2. src/test/java : contains all the test cases

com.conduit.qa.tests : this package contains all the test classes.
      
       HomePageTests : home page test contains all the tests relate to home page.
        
       SignInPageTests : Sign In Page Tests contains all the tests relate to SignIn page.
 
       SignUpPageTests : Sign Up Page Tests contains all the tests relate to SignUp page.

3. src/main/resources : contains all the resources used to run the tests.
         
          constants class : constants class contains all the constansts are static and final variables.

          conduitData : This is an excel file used to store data for running test for exaple : user log in data.
