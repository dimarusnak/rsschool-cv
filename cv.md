## [rsschool-cv](https://app.rs.school/) ##
# Dmitry Rusnak #


## Contact information: ##

### Phone: [+7(952)345-28-20](tel:+79523452820) ###

### E-mail: creatorviewer@gmail.com ###

### Telegram: [@Demetrius_user](https://t.me/Demetrius_user) ###

### Discord: [Dmitry(@DemetriusUser)](https://discord.com/users/830367835175125052) ###

### GitHub: [dimarusnak](https://github.com/dimarusnak) ###

## Summary ##

My name is Dmitry. All I want  - it's learning and create something, that
can help to other people. Now my goal is to become a good frontend-developer.
I have nothing more to say. I'm a learner, soon I will update this page.

## Skills ##

* HTML, CSS
* JavaScript Basics 
* Git, GitHub
* Figma
* VS Code

## Code Examples ##


```
const enterButton = document.getElementById('enterButton');
const againButton = document.getElementById('againButton');
const output = document.getElementById('outputText');

const randomNumber = Math.floor(Math.random() * 100) + 1;

function checkNumber () {
    const input = document.getElementById("userInput").value;
    if (input == randomNumber) {
        output.innerHTML = `You guessed right, it was ${randomNumber}`;
        output.style.color = "yellow";
    }
    else if (input > randomNumber && input <= 100) {
        output.innerHTML = `You guessed too high`;
    }

    else if (input < randomNumber && input >= 1) {
        output.innerHTML = `You guessed too low`;
    }
    else if (input < 1) {
        output.innerHTML = `Higher, it has to be between 1 and 100`;
    } 
    else if (isNaN(input)) {
        output.innerHTML = `That's not a number`;
    }
    else {
        output.innerHTML = `Lower, it has to be between 1 and 100`;
    }
};

enterButton.addEventListener('click', checkNumber);
againButton.addEventListener('click', function() {
    location.reload();
});
```