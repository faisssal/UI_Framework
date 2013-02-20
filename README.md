UI_Framework webdriver

This Package Includes:



1.   Config - Keeps all the configuration files such as property files

2.   InputTestData  - Has files containing input data for application

3.   OutputData  - Contains downloaded docs/images, fetched data in excel

4.   TestReports  - Contains ANT generated reports

5.  Util - Utility package contains all generic functions & business functions such as email configuration setting and all other utilities

6.   TestLogs - Contains log file corresponding to tests

7.   DAO - Classes for accessing persistent storage, such as to a database

8.   Pages - Page classes for particular pages

Test Function Using Page Object Model:
=====================================

 
In testValidLogin() function, firstly we tried to click on any tab by giving its name

Create an instance of Homepage, which extends BasePage

In BasePage create an instance of Tabs class

Call the clickElement() function by giving the name of tab to be clicked from Tabs class which implements BaseNavigation interface
Now create an instance of Clicked page i.e. DomesticFlightsPage

Verify that bottom navigation is present on this page by calling isNavPresent() function from Tabs class

Call the clickElement() function from Tabs class by giving the name of link to be clicked from bottom navigation

Login to the site by creating an object of Booking Summary page displayed after login and making same as return type of validLogin() function
Verify various things are displayed correctly on this page such as welcome message and email

Logout from site and login again with another user

=============================================================================

1.  Methods performing an action that results into other page should return the page object to user. Assert and wait to load the page completely with all elements of the page.
Example: Clicking a button on page A redirects the user to page B, then returns the object of page A

2.    Naming of variables and methods:

a. Standard JAVA naming conventions should be utilized
b. If a method performs an action that clicks on any element on the page, the name of the method should start with click 
c. If a method retrieves any value or entity, or a list of values or entities, the method name should start with get
d. If a method assigns a value to a web element, the method name should start with set e. If a method interacts with radio or check-boxes it should start with enable or disable
f.  Instance variables should be named using an underscore as a leading character. Example: _login, _pageName

3.    Encapsulation should be used as follow:

a. All methods intended for the implementation of tests for the automation of the web project, should be public 
b. All methods not intended for the implementation of tests should be private
c. All variables, with the exception of enums, should be private
 
4.   Common methods for similar web elements:

a. Lists (HTML tables): getAll* or getAll*ByName, find*ByName, click*_ByName b. List-boxes: getAll*Options or getAll*Options_ByText, click*Option
5.   All assertions and verifications should be within the tests using JUnit framework asserts


========================================================================
Ssome great features, which will making testing not only faster but easier as well. Key new features include:

1.   Generating Logs:
This usability function will provide user a log file placed in “TestLogs” folder along with an html file displaying logs in a beautiful format with all information.

2.   Comparing  PDF:
PDF documents can be challenging and time consuming to test. We made it easy with one of our usability functions. Just follow the below steps and you’ll be able to compare PDF content in significantly less time.
a. Add sample PDF content to ‘Sample_File.txt’ in ‘InputTestData’ folder of the Project b. Add url of the pdf in the code e.g. http://www.abc.com/pdf_file_name.pdf
c. Run the test “PdfTextComparison.java” and check the comparison results in the log files

3.   Taking Screenshot:
This usability helps you to take full size screenshots of website pages and save them in ‘OutputData’ folder of the Project. Screenshots images can be output in the JPG, GIF, PNG, or BMP formats.

4.   Upload/Download Functionality:
Websites under test require uploading and downloading of files. Take help of our usability for uploading/downloading files. Add files to upload in ‘InputTestData’ folder and you’ll get the downloaded ones in ‘OutputData’ folder.

5.   Read & Write Excel files: (.xls as well as .xlsx extension)
In our first release we have provided usability function which reads an Excel file having .xls extension i.e. 2003 format using
JXL. Now we have provided support for .xlsx extension files i.e. 2007-2010 format, using Apache POI.




