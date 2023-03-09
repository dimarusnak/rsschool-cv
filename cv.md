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

### Guess a Number game ###
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

### My old homeworks ###

```
// Замыкание. Пример 1
console.log('Результаты примера 1:');
let a = 10;

function counter() {
    let a = 0; /* Есть область видимости, где используется переменная из функции, а не из глобальной области видимости */
    return function () {  /* Анонимная функция, так как её область видимости замкнута внутри другой функции */
        a++;
        console.log(`Счётчик равен: ${a}`);
    };
}

let b = counter(); /* Каждая переменная создаёт отдельный блок области видимости */
let c = counter();
b();
b();
c();
b();

// Замыкание. Пример 2. Для этого создал ещё один JS файл.
(function () { /* Делаем анонимную функцию, чтобы не засорять названиями глобальную область видимости */
    let p = 24;
    let a = document.querySelector('.button-1');
    a.onclick = () => {
        p *= 3;
        console.log(`P из первой кнопки равен: ${p}`);
    }
})();

// Замыкание. Пример 3.

function randomInteger (min, max) {
    let rand = min - 0.5 + Math.random() * (max - min + 1);
    return Math.round(rand);
}


function someFun () {
 let someNumber = 10; /* Замыкание заключается в том, что внутри функции находится переменная, как и в первом примере  */
  return function randomSum () {
    someNumber += randomInteger(0, 100); /* randomInteger не определена, нужно прописать для неё функцию*/
    console.log(`Результат рандомной суммы: ${someNumber}`);
    if (someNumber > 320) return;
    randomSum ();
 }
};

let k = someFun();
k();
k();
k();
k();
k();
k();
/* -------------------------------------------------------------------------- 
Примеры использования методов массивов: map, filter, reduce */

/* Map */
let userNumber = +prompt('Введите число',0);

let intoArray = String(userNumber).split('').map((userNumber) => {
    return Number(userNumber);
})

console.log(`Держите ваш массив: ${intoArray}`)

/* Filter */

let filterResult = intoArray.filter(x => x > 5);

console.log(`Числа больше пяти: ${filterResult}`);

/* Reduce */

let total = intoArray.reduce(function (a,b) {
    return a + b;
});

console.log (`Сумма всех значений в массиве: ${total}`);

/* ----------------------------------------------------------------------------------
Вывести все ключи Объекта в виде массива */

let someGuy = {
    name: 'Alex',
    age: 27,
    sex: 'male',
    profession: 'cop',
}

let propertyNames = Object.keys(someGuy);
console.log(propertyNames);
/* ------------------------------------------------------------------------------------
Сделать функцию и использовать параметры по умолчанию */

function Human (name, age, sex, profession) {
    this.name = name;
    this.age = age;
    this.sex = sex;
    this.profession = profession;
}

let Michael = new Human ('Micheal',32,'male','doctor')
console.log(Michael);

let Andrew = new Human ('Andrew', 22, 'male', 'student');
console.log(Andrew);

let Kate = new Human ('Kate', 28, 'female', 'cooker');
console.log(Kate);
/* ------------------------------------------------------------------------------------------
Создать  экземпляры каждого класса и превратить в JSON */
let MichealString = JSON.stringify(Michael);
console.log(MichealString);
let AndrewString = JSON.stringify(Andrew);
console.log(AndrewString);
let KateString = JSON.stringify(Kate);
console.log(KateString);
```