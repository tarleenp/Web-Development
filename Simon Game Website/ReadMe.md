This is a game website. To know how to play this game click the link given below:
https://londonappbrewery.github.io/Simon-Game

Languages used: Html,css,javascript and jquery library.

Process to create website:

Step 1 - Add Javascript and jQuery:

Our game logic will be created inside an external Javascript file.
Create a new file called index.js
Link this new external JS file to your index.html
Add an alert to index.js and test that the alert gets triggered when you load up index.html in Chrome.
![image](https://github.com/user-attachments/assets/5c64ae8a-49d5-4f02-96af-fd536fa76cd8)
Once, you've confirmed that game.js is correctly linked, you can delete or comment out the alert.
Add jQuery to your website and test that it's successfully loaded by opening Chrome developer tools and typing $("h1").
If successful, you should get something like this printed:
![image](https://github.com/user-attachments/assets/433c3090-e0a7-415e-a1c6-7c44c41a52ff)
If jQuery is not added, you will get this instead:
![image](https://github.com/user-attachments/assets/576c6a34-d005-4976-8f2b-ea6bd62a99d4)

Step 2 - Create A New Pattern:

Inside index.js create a new function called nextSequence()
Inside the new function generate a new random number between 0 and 3, and store it in a variable called randomNumber
You can use the Chrome console to verify that your code creates random numbers between the correct range.
At the top of the index.js file, create a new array called buttonColours and set it to hold the sequence "red", "blue", "green", "yellow" .
Create a new variable called randomChosenColour and use the randomNumber from step 2 to select a random colour from the buttonColours array.
At the top of the index.js file, create a new empty array called gamePattern.
Add the new randomChosenColour generated in step 4 to the end of the gamePattern.

Step 3 - Show the Sequence to the User with Animations and Sounds:

Use jQuery to select the button with the same id as the randomChosenColour
You should end up with an effect like this:

![]https://img-b.udemycdn.com/redactor/raw/2018-11-22_10-50-30-ca62b559c6bd348f347ab370e5f009b4.gif

Use Javascript to play the sound for the button colour selected in step 1.

Use jQuery to detect when any of the buttons are clicked and trigger a handler function.
Inside the handler, create a new variable called userChosenColour to store the id of the button that got clicked.

--> So if the Green button was clicked, userChosenColour will equal its id which is "green".

At the top of the game.js file, create a new empty array with the name userClickedPattern.
Add the contents of the variable userChosenColour created in step 2 to the end of this new userClickedPattern
At this stage, if you log the userClickedPattern you should be able to build up an array in the console by clicking on different buttons.

![image](https://github.com/user-attachments/assets/771c3d8c-2942-4570-a7c9-589be2e8a78f)

In the same way we played sound in nextSequence() , when a user clicks on a button, the corresponding sound should be played. e.g if the Green button is clicked, then green.mp3 should be played.
Create a new function called playSound() that takes a single input parameter called name.
Take the code we used to play sound in the nextSequence() function and move it to playSound().
Refactor the code in playSound() so that it will work for both playing sound in nextSequence() and when the user clicks a button.

Create a new function called animatePress(), it should take a single input parameter called currentColour.
Take a look inside the styles.css file, you can see there is a class called "pressed", it will add a box shadow and changes the background colour to grey.

Use jQuery to add this pressed class to the button that gets clicked inside animatePress().
Use Javascript to remove the pressed class after a 100 milliseconds.
Once complete, you will get this effect when you click on any button.

![image](https://github.com/user-attachments/assets/b3578af0-9bee-4cb1-9282-8c405181756b)

Use jQuery to detect when a keyboard key has been pressed, when that happens for the first time, call nextSequence().

You'll need a way to keep track of whether if the game has started or not, so you only call nextSequence() on the first keypress.
Create a new variable called level and start at level 0.
The h1 title starts out saying "Press A Key to Start", when the game has started, change this to say "Level 0".
Inside nextSequence(), increase the level by 1 every time nextSequence() is called.
Inside nextSequence(), update the h1 with this change in the value of level.

All going well, this is what you should see when you refresh the website:

![image](https://github.com/user-attachments/assets/2e90509c-d9b6-41a5-a6d2-e9aa39fcdb5e)

Firstly, the game shows the first colour in the sequence (blue). The user clicks on the blue button.
Next, the game shows the next colour (red), the user has to remember the sequence is blue, red and so on and so forth.
If the user messes up the sequence, then the game ends.

![image](https://github.com/user-attachments/assets/910ee270-598f-469d-841a-7a80756c22d9)

In the sounds folder, there is a sound called wrong.mp3, play this sound if the user got one of the answers wrong.
In the styles.css file, there is a class called "game-over", apply this class to the body of the website when the user gets one of the answers wrong and then remove it after 200 milliseconds.

All going well, you should end up with this flash effect:
![image](https://github.com/user-attachments/assets/76fa463a-0321-4cb5-89ee-03270eee6969)

Change the h1 title to say "Game Over, Press Any Key to Restart" if the user got the answer wrong.
