# Part 2 
1. Let us now play Rock Paper Scissors against the computer.
2. Find one image for rock, one for paper and one for scissors. 
3. We will add these to our web page. 
4. Can you google search how to add images to your webpage? 
5. Save your project and make sure that you can see the images through your webpage. 
6. Now let us edit the images size and make them appear in the center using css.
7. Add a `<button>` to our webpage so that when we click the button, we can make the computer choose which image (Rock, Paper or Scissors?) does it want. 
		`<button type="button">Play!</button>`
8. Save the page and notice that you can see the button but when you click it, nothing happens. This is because we have not added any logic for the computer to choose the image. For that we need `<script>`.  
9. Add onClick attribute to the button so that it knows what to do when we click the button. Edit your button tag like this:
		`<button type="button" onClick="console.log('Hi, I am your computer!');">Play!</button>`
10. Save the file and click the play button. What happens? Where does the "Hi, I am your computer!" message go?
11. Let us try to debug this. Press `Ctrl+Shift+I` on your internet browser (Developer tools option) and look for console tab. Can you see your message there? If not, reach out to any of the volunteers for help. 
12. Now we want the onClick attribute to generate computer's response. For that let us create a method. Method is a like a procedure that we need to do to generate output. Like in science experiments, you have some methods to generate water from hydrogen and oxygen. 
13. Replace the line after onClick by 
		`computerPlay()`
14. Now add `<script>` tag after your `<button>` and add the following:
		`function computerPlay(){
			console.log('Hi, I am your computer!');
		}`
15. Save your file and see that the computer does the exact same thing as before but now we have a method (function) to do that instead of in the button tag. 
16. Now let us break down the task we need to work on. 
	- We have 3 images - rock, paper and scissors. 
	- We need the computer to choose one of the images randomly when we click the play button.  
17. So, first what we need to do is, we need to create a way to get random image. You can use this method called Math.random() that can help you get a random value between 0 to 1. 
18. Notice the use of method. Once you create a method, it can be called or used again anywhere else, depending on the people who created the method. This `Math.random()` method is created by someone and now we can use it. 
19. Let us print out the random number generated using this function. Remember when we created a name variable in the last exercise. Now we need to create a variable called random to save the random number generated from the `Math.random()` function. Therefore, add the following line to save the random number. And then console.log the random number the same way we printed our name out in the previous exercise.
		`var random = Math.random()`
20. Hit the play button multiple times and you should be able to see that the number is different everytime. 
21. Now instead of printing this number out in the console log, let us use this number to get computers choice. There are 3 different possiblities for the choice, therefore, we can divide the number this method can generate into 3 portions like 0.00-0.33, 0.34-0.66 and 0.67-1.00.
When the number is in 0.00-0.33, we will choose rock. When the number is between 0.34-0.66, we will choose paper. And at last, we will choose scissors. 
22. Remember the if-else logic we did in scratch? We will use similar concept to select the computer's choice here. 
		`let computerChoice = "rock";

	    if (randomNumber < 0.34) {
	      computerChoice = "rock";
	    } else if(randomNumber <= 0.67) {
	      computerChoice = "paper";
	    } else {
	      computerChoice = "scissors";
	    }
	    `
23. Now we will print the computersChoice variable in the console log and see if the computer is cheating or it is sending random answer everything you hit play. 
24. We do not want to always go to console log to print the result. Let us use the way we printed out our name in last exercise to print out computers choice. 
		`document.getElementById("computer-choice").innerHTML = "Computer chose " + computerChoice + "!";`
25. Hit save and see if you can see the computers choice on your webpage when you click play. Notice, that you cannot see it yet. Let us find out why. 
26. Remember that the tag in the last exercise had an ID. Currently, we do not have any id which is called "computer-choice". Therefore, let us go to the `<body>` and add a section for the computer to display its choice.
		`<h3 id="computer-choice"></h3>`
27. Now hit save and notice it will show the right answer on the screen.
28. Now, the last part of this exercise is to show image result of what is computers resposnse.
29. Add a section to display computers choice image. 
		`<div id="computer-choice-image"></div>`
30. Now add the following to display the image according to the choice of the computer.
		`let computerChoiceImage = '<img src="images/rock.jpeg" width="500px"/>';

	    if(computerChoice === "paper") {
	      computerChoiceImage = '<img src="images/paper.jpeg" width="500px"/>';
	    }
	    else if(computerChoice === "scissors") {
	      computerChoiceImage = '<img src="images/scissors.jpeg" width="500px"/>';
	    }

	    document.getElementById("computer-choice-image").innerHTML =
	      computerChoiceImage;
	      `
31. Hit save and play with the computer!
