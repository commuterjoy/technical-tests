# Odds and Evens

This short test is suitable for doing as part of interviews, it could be done in any language (even pseudo-code) and could either be done on pen and paper or text editor. It is aimed at trainee-mid level applicants.

Completion of the exercise should give you confidence in the applicants basic abilities to program, the use of functions, arrays, loops, etc. You could also use it to identify stronger applicants by those who abstract there solutions further, or identify more advanced ways of completing the task.

## Spec

Write a function called oddsAndEvens that expects an array of integers and returns two arrays, the first containing the odd numbers, the second containing the evens.

  oddsAndEvens([1,2,3,4,5,6,7,8,9,10]) # => [[1,3,5,7,9], [2,4,6,8,10]]

## Hints

* How would you loop the array? (basic)
* How do you determine if a number is odd and even? (basic)
* How would you best document that? (intermediate)
* Can you add a method to the Array object? (advanced)
* Can you not use an if statement - ternary? (advanced)
* Is there a common pattern that can be abstracted? (advanced)
* Can you rewrite it without using a for loop? (advanced)

## Example responses

## Poor answer

  * Can't complete exercise
  * Major errors in code
  * Can't easily determine parity of number

## Cheating

Some languages have built-in partition functions, although using this does show good knowledge of the target language (providing it's real!) - perhaps identifies a stronger developer but ask them to write a partition function to be sure.

  [1,2,3,4,5,6,7,8,9,10].partition {|x| x % 2 == 0} # Ruby


## Good answer

  /**
   * Takes an array of integers and returns an array containing
   * odd numbers as the first element and evens as the second
   */
  function oddsAndEvens(arr) {
    var odds = [], evens  = [];
    for (var i = 0, len = arr.length; i < len; i++) {
      if (arr[i] % 2 == 0) {
        evens.push(arr[i]);
      } else {
        odds.push(arr[i]);
      }
    }
    return [odds,evens];
  };

## More advanced answer (abstracts common pattern, uses high order paradigm)

  /**
   * Partitions an array into two based on the callback function.
   * If callback return true elements are put into the first array,
   * otherwise they are put into the second
   */
  function partition(arr, func) {
    return arr.reduce(function(prev, cur) {
      if (func(cur) == true) {
        prev[0].push(cur);
      } else {
        prev[1].push(cur);
      }
      return prev;
    }, [[],[]]);
  }

  /**
   * Takes an array of integers and returns an array containing
   * odd numbers as the first element and evens as the second
   */
  function oddsAndEvens(arr) {
    return partition(arr, function(item) {
      return item % 2 != 0;
    });
  }

## And more advanced again, using prototypes + ternary

  Array.prototype.partition = function(func) {
    return this.reduce(function(prev, cur) {
      prev[((func(cur) == true) ? 1 : 0)].push(cur);
      return prev;
    }, [[],[]]);
  };

  [1,2,23,4,5,67,7,8].partition(function(item) {
     return item % 2 != 0;
  });



