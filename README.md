
![screen or GIF of your app](https://via.placeholder.com/1000x300)

# Project Name

This project is a simple calculator built with plain JavaScript.  
The application allows the user to perform basic mathematical operations in the browser using `prompt()`, and it also stores the history of all calculations.

**Main features**:
- basic mathematical operations: addition, subtraction, multiplication and division
- exponentiation implemented using a loop instead of `Math.pow()`
- storing and displaying calculation history
- validation of allowed operators
- protection against division by zero
- interactive user input using `prompt()`
 

&nbsp;
 
## 💡 Technologies
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)


&nbsp;
 
## 🔗 See also
Are you interested in JavaScript and Frontend Development? See my other project **React Kanban Board**.

&nbsp;
 
## 💿 Installation

The project uses HTML, CSS and JavaScript only, so no additional packages are required.
1. Download or clone the repository
2. Open the project folder
3. Run the `index.html` file in your browser

&nbsp;
 
## 🤔 Solutions provided in the project

- Calculator constructor

The calculator is created using a constructor function that stores available actions and calculation history.

```javascript
function Calculator() {
    this.actions = ['+', '-', '*', '/', '^'];
    this.history = [];
}
```
 &nbsp;

- Validation of available operations

The isCorrectAction() method checks if the user entered a valid operator.

```javascript
Calculator.prototype.isCorrectAction = function (action) {
    return this.actions.includes(action);
}
```

Each operation result is stored in an array and later displayed to the user.

```javascript
Calculator.prototype.getHistoryAsString = function () {
    return this.history.join('\n');
}
```

Exponentiation implemented with a loop:

```javascript
Calculator.prototype.pow = function (num1, num2) {
    let result = 1;

    if (num2 !== 0) {
        for (let i = 0; i < num2; i++) {
            result *= num1;
        }
    }

    this.history.push(num1 + '^' + num2 + '=' + result);
}
```
 &nbsp;

| Issue                                   | Solution                                            |     |
| --------------------------------------- | --------------------------------------------------- | --- |
| checking valid operators                | `used includes() on the actions array`              |     |
| displaying previous calculations        | `sused join('\n') to show history as text`          |     |
| exponentiation without built-in function| `used for loop instead of Math.pow()`               |     |

 &nbsp;
 
- four - some shortcut <kbd>Ctrl</kbd> + <kbd>C</kbd>

 &nbsp;
 
- five - example with a screenshot
<img alt='what it is' src="https://via.placeholder.com/500x200" />


&nbsp;

## 💭 Conclusions for future projects

This project helped me better understand how constructor functions and prototype methods work in JavaScript.  
I also practiced working with loops, conditions and handling user input.

In future projects I would like to improve:

- creating a graphical user interface instead of using `prompt()`
- improving input validation
- refactoring repeated `if` statements into a cleaner structure
- displaying results directly on the webpage
- organizing the code into smaller reusable functions


#### This is the first issue:
Handling division by zero.
```javascript
Calculator.prototype.division = function (num1, num2) {
    if (num2 !== 0) {
        const result = num1 / num2;
        this.history.push(num1 + '/' + num2 + '=' + result);
    } else {
        this.history.push(num1 + '/' + num2 + ' => division by zero is not allowed');
    }
};
```

#### This is the second issue:
Implementing exponentiation without using Math.pow().

``` javascript
Calculator.prototype.pow = function (num1, num2) {
    let result = 1;

    for (let i = 0; i < num2; i++) {
        result *= num1;
    }

    this.history.push(num1 + '^' + num2 + '=' + result);
};
```

&nbsp;

## 🙋‍♂️ Feel free to contact me
If you like the project or have suggestions – feel free to reach out via [GitHub](https://github.com/satoshi300) or [LinkedIn](https://www.linkedin.com/in/michal-wasiak-457a5331/).


&nbsp;

## 👏 Thanks / Special thanks / Credits
Thanks to my [Mentor - devmentor.pl](https://devmentor.pl/) – for providing me with this task and for code review.
