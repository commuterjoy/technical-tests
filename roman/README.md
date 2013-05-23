BBC Web Developer Role: Practical Assessment
--------------------------------------------

This short task should give you the opportunity to demonstrate your PHP and Zend Framework experience. It should take around 2 hours, once you have finished the task please package all the files in a .tar or .zip archive and send them back to us at the BBC.

Roman numerals
--------------

This is a simple Zend Framework application consisting of a single page with an HTML form. The application is for converting roman numerals to decimals and back again, it should be able to handle numbers up to 3999. The HTML form allows users to submit a number in either decimal or Roman numerals and converts it to the opposite format, presenting the result to the user.  

The application has been created by following the Zend Framework quick-start guide:

http://framework.zend.com/manual/en/learning.quickstart.create-project.html

Unfortunately the developer has failed to grasp the concept of controllers, separation of concerns and a whole other heap of patterns and practices we expect from a modern PHP application. All of the code the developer has added so far to the project exists in the view template:

	application/views/scripts/index/index.phtml
	
It is your task to recreate this application using your expert knowledge of the framework and PHP development. Choose the correct components from Zend and where necessary create utility classes within the library folder.

Please remember what we try to strive for here at the BBC:

* Appropriate use of framework components
* Security - validation and filtering of user input
* Correct handling of user input errors
* Creation of reusable components and library code
* Unit testing of any new code with PHPUnit
* Well commented code
* Follow coding standards, e.g. Zend Coding Standards
* Valid and modern XHTML

Whilst CSS, javascript and an excellent UX are a major part of our day to day work here you will not primarily be assessed on these features in this task.

Good luck!
