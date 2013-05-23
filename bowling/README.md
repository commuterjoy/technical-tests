The Bowling Game Kata
---------------------

We’d like you to create a php or javascript object that will keep accurate score in a ten-pin bowling match for a single player, with software tests in place to prove the accuracy of your scoring mechanism.

Ten-pin bowling scoring rules: http://en.wikipedia.org/wiki/Ten-pin_bowling#Scoring 

This test is designed to allow us to see your thought processes during the development cycle, and the techniques and design patterns you may use.

Please leave comments in your code to explain your thinking also – comments in the code leave an additional permanent record of your thinking.

Feel free to use any documentation you may require. (We’d appreciate it if you didn’t search for ‘Bowling Game Kata Solutions’ or anything like that.)

Please try to use the time to show your approach to finding a solution for a programming problem, using all the tools at your disposal. It is more important that you approach this in a professional manner, than that you complete the task. We’d rather see half the problem solved in an elegant manner using industry-standard tools and techniques, than a complete solution that has been hacked.

If you’re going to email script files back then it would probably be a good idea to zip the files up or put them in a public location on Dropbox and point us to that. This will reduce the chance that email software blocks them on the way through. 

Scoring in Bowling
------------------

The game consists of 10 frames. In each frame the player has two opportunities to knock down 10 pins. The score for the frame is the total number of pins knocked down, plus bonuses for strikes and spares.

A spare is when the player knocks down all 10 pins in two tries. The bonus for that frame is the number of pins knocked down by the next roll. So in frame 3 above, the score is 10 (the total number knocked down) plus a bonus of 5 (the number of pins knocked down on the next roll.)

A strike is when the player knocks down all 10 pins on his first try. The bonus for that frame is the value of the next two balls rolled.

In the tenth frame a player who rolls a spare or strike is allowed to roll the extra balls to complete the frame. However no more than three balls can be rolled in tenth frame.

Bowling vocabulary 
 
 * Pins 
 * Ball, Roll 
 * Lane 
 * Gutter 

A bowling game consists of: 

 * 10 frames (rounds) 
 * Strike - All ten pins knocked down with the first ball (i.e. in one roll)
 * The score for a strike is 10 + the next two rolls
 * Spare - All ten pins knocked down with two balls 
 * The score for a spare is 10 + the next roll
 * Perfect game, 300 points 
 * Gutter game, 0 points
 * Open frame, less than 10 points in a frame

Also see: http://en.wikipedia.org/wiki/Ten-pin_bowling

