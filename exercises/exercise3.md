# Part 3
1. When computer is playing with you on the computer, we should also be able to input our choice on the computer too. Therefore, let us add 3 buttons for us to select our choice. Then the computer will select its choice. 

```html
<h3>Choose one: </h3>
<button type="button">Rock</button>
<button type="button">Paper</button>
<button type="button">Scissors</button>
```

2. Again as the computer does not know what to do when we press this button, let us add "onclick" to explain to the computer what to do. So, add an attribute onclick="userPlay('rock')", onclick="userPlay('paper')", onclick="userPlay('scissors')" to the button. 

Notice how we added same name userPlay but with three different words, 'rock', 'paper' and 'scissors'. What does this mean? These are the different arguments for the same method. Like in the cake recipe example. 

3. Now, we will tell the computer what to do with these three arguments. Make a section for displaying the users choice - Rock or Paper or Scissors. Then make another empty section for showing the users selected choice image. So when the user clicks rock, we want to ask the computer to display the image of the rock in the user selected choice and so on. Refer to how we are displaying the images for the computers choice. It should be done in the similar manner.

4. Now, when you click rock or paper of scissor, we want the computer to display your choice and also display the computer's choice. So call the computerPlay() function after we display the users choice and delete the play button. 

5. By now, you can see that we have three buttons, when we press any one of the buttons, we can see what we chose and then we can see what did computer choose. You can see who is the winner, right?

In the next section, we will make the computer smarter and make it print out who is the winner. 
