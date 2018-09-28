# Exercise 4

1. As you know when you follow the cake recipe, the end product is a cake. Therefore, we want our method recipe to give out an end product too. So add this in your computerPlay() method `return computerChoice;`. Now in our `userPlay(choice)`, we want to be able to get this end product and store it in a variable. Therefore, add `var computerChoice = computerPlay()`.

2. Now it is time to decide who wins! The computer or you.
There are 3 possible choices for both you and the computer. Based on that there are only these possible outcoumes -

| You      | Computer | Outcome  |
|----------|----------|----------|
| Rock     | Rock     | Draw     |
| Rock     | Paper    | You lose |
| Rock     | Scissors | You win  |
| Paper    | Rock     | You win  |
| Paper    | Paper    | Draw     |
| Paper    | Scissors | You lose |
| Scissors | Rock     | You lose |
| Scissors | Paper    | You win  |
| Scissors | Scissors | Draw     |

3. After the computer chooses, we need to decide who wins. You know the `userChoice` and the `computerChoice`. It is time to compare them both and decide what the result will be! You can convert the table to javaScript code like so -

```javascript
var result;
if(userChoice == 'rock') {
    if(computerChoice == 'rock') {
        result = 'Draw!';
    }

    else if(computerChoice == 'paper') {
        result = 'You lose!';
    }

    else if(computerChoice == 'scissors') {
        result = 'You win!';
    }
}
// ...
// Similarly for paper and scissors...
```

4. As you've done before, display the result on the webpage by doing `document.getElementById('result').innerHTML = result;`. Save your file, and start playing on the browser! 
5. Wait, why is it not working? Remember, you have not created <div> with an ID 'result'. Add that in order for the computer to identify where to display the result. 
6. Now, you have completed your game. Hurray!
