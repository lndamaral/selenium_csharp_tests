## Selenium CSharp Tests

### Setup

This is a automation architecture for C# language.

 1. Cloning the repository:

    ```shell
    git clone https://github.com/lndamaral/selenium_csharp_tests.git
    ```


### Architecture

    /Framework:

        Base/                           # Super classes for Elements, Pages and Tests.
            BaseElement.cs          
            BasePage.cs             
            BaseTest.cs

        Driver/                         # Used to manage drivers.
            Chrome.cs            
            Firefox.cs              

        Helper/                         # Used to keep useful methods for common Selenium operations
            DatabaseFactory.cs            
            DriverFactory.cs
            General.cs
            WaitUntil.cs
            
    /Test.UI.[System Name]:             # Project tha references the system is being automated.
        
        Page/                           # Folder where classes that implement pages mapping according to PageObjects.
            [PageName]Page.cs
            [PageName]Page.cs
            [PageName]Page.cs

        Test/                            # Folder where test cases are kept.
            [TestName]Test.py
            [TestName]Test.py
            [TestName]Test.py

        app.config                       # File where all variables needed to run the tests are kept.
        AssemblyInfo.cs                  # File where the level of parallelism is set.

### Test Execution

 1. Local Execution
 
    Set `False` at `<add key="Remote" value="[here]" />`
    
 2. Remote Execution
 3. parallel Execution
 
### Docker Compose

