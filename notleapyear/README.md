
The following takes a date in the format DD/MM/YYYY, extracts the year and works out if it
is a leap year. The code is poorly written.

What improvements would you make to this code to pass it fit for deployment?

<?

 1.    function notLeapYear ($var)
 2.		{
 3.        $var = substr($var, 6, 4);
 4.        if (!($var %400 )&& $var % 100) {
 5.            return 1;
 6.       }
 7.        return $var % 4;
 8.    }
 9.
10.    $testDates = array('03/12/2000', '01/04/2001', '28/01/2004', '29/11/2200');

?>

The expected result is:-

    * 03/12/2000 falls in a leap year
    * 01/04/2001 does not fall in a leap year
    * 28/01/2004 falls in a leap year
    * 29/11/2200 does not fall in a leap year

Answers (there might be more) :-

 - More common place name would be, function isLeapYear(){}.
 - $var is a bad name for a variable, it also gets redeclared on the first line, which might confuse people.
 - Should be OO'd by extending an existing base object, Date.prototype.isLeapYear = function(){} or Zend_Date() etc. - only worth it if it's reused or part of some lib/util
 - Returns 'true' or 'a number'. Going by the function name it should return a boolean.
 - It invents it's own date parsing code (substr) when most languages handle dates natively - so you could cast the $var to a Date() and do getYear() for robustness
	- ... likewise it could handle more date formats if you did this.
 - Lack of comments, especially around the logic of line #4 - Eg. i'd link to wikipedia or something that explains leap year logic
 - Line #4 has crappy/confusing formatting
 - Brace styles differ on function & if, likewise one side of the conditional is ()'d and the other isn't	
 - Could be rewritten a one-liner - Eg, var isLeapYear = new Date(theYear,1,29).getDate() == 29;
 - Could add some validation around the function input, Eg. handle bad input by specifying an argument data type.
 - Needs phpdoc/jsdoc.
 - Probably doesn't handle every edge case leap year (functional requirement rather than bug I'd say)
 - Test cases (in the $testDates array) are weak

