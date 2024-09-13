This is a game website created using html css and javascript
Basic Rule of the game is: The player having dice with highest number will be the winner. 

Process of cretaing the website:
step 1:First created the index.html file and then javascript file name index.js and linked it with index.html file

step 2:Add dice images:add the images of dice6.png as the source to both of the <img> elements.

  Reference image:
  ![image](https://github.com/user-attachments/assets/50658ccf-b4f3-49d2-9735-408aff3e1b76)
  
step 3:Inside index.js, create a new variable called randomNumber1 then set the value of this variable to a random number between 1 and 6.

step 4:Use the random number you created in the last step to pick out a random dice image between dice1.png to dice 6.png then place this image inside the left <img> element.(Using the DOM Concept and setAttribute() method.)

  Reference image:
  ![image](https://github.com/user-attachments/assets/b11531f2-1abc-4c8c-a8ca-a2f2d71c2ee8)
  
step 5: Change both <img> elements:

  Reference image:
  ![image](https://github.com/user-attachments/assets/08b4b948-6083-4d2b-b174-3ebde86dd38a)
  
step 6:Change the title to display a Winner:Change the text in the h1, (which currently says Refresh Me) to show which user won or if there was a draw depending on the dice values of player 1 (left) and player 2 (right).

  Reference image:
  ![image](https://github.com/user-attachments/assets/4834e273-eae5-485e-b9eb-1c18df9b99bd)

Website URL : http://127.0.0.1:3000/DOM/Dicee+Challenge+-+Starting+Files/dicee.html
