# Brick-Breaker
 
Here is another game. Brick Breaker is a Breakout clone which the player must smash a wall of bricks by deflecting a bouncing ball with a paddle.

In this game the paddle can move only in horizontal axis. When the ball hits on the brick points added to player . When the player miss the ball life of the player minuses and the x-axis position of the paddle reset to the center and the ball position is reset to the vector2.Zero .

In this game I use 5 colors of bricks and each brick have different life. For that I use an array to store the different states of the brick . and access that array to represent the life of brick.

In this game I use some calculations to get the bouncing angle to the ball when the ball hit the paddle for that I take the position of the peddle then I take first contact point that ball collide with the paddle and by getting these two I calculates the offset by minuting the x-axis value of contact point from x-axis value of paddle position . I get the Half length of the paddle by taking the size of x-axis from the bounds in other collider method and divided it by 2 . also I get the current angle by signed angle in vector2 . I set a maximum bouncing angle as 75 degree to regulate the angle of bouncing back of the ball from the paddle. I calculated the bouncing angle by dividing the half length of the paddle by the offset and multiply by the maximum bouncing angle . And to get the new bouncing angle I added the current angle by bouncing angle and check the set the maximum value is +75 and minimum value is -75. After that by using Quaternion I rotate the ball by new angle get from the above with same velocity

To minus the life I use a script for the wall at the down weather the ball collide the wall by on collision enter 2d function to detect the collision

by using same method on the brick I use the same function to add the points to the player when the ball hit the brick
