# **Kirill Kalashnikov**
### **junior** javascript developer
* * *
## **Contact information**:
### Phone: +37062387681
### E-mail: kirillrik1994@gmail.com
### [Telegramm](https://t.me/s1ran0)
### [LinkedIn](https://www.linkedin.com/in/kirill-kalashnikov/)
### [GitHub](https://github.com/KalashnikovKV)
* * *
## **Skills and Proficiency**
* **HTML/CSS**;
* **Javascript**;
* **Java Core**;
* **Node JS**;
* **Express JS**;
* **Docker**;
* **Git, GitHub**;
* **VS Code, IntelliJ IDEA**;

* * *
## **Code example**
### ***Task***: 
### Write an algorithm for finding a way out of the maze. The maze is a 2-dimensional array in which:
### 0 - start position + - way # - wall
### The solution should be an array of strings with a sequence of necessary actions to exit the maze.

### _Example of input data_:
### [ ['#','#','#','#','#','#','#','#','#'],
### ['#','+','+','+','#','+','+','+','#'],
### ['#','+','#','+','#','+','#','+','#'],
### ['+','+','#','+','0','+','#','+','#'],
### ['#','#','#','+','#','#','#','#','#'],
### ['#','#','+','+','#','#','#','#','#'],
### ['#','#','+','#','#','#','#','#','#'],
### ['#','#','#','#','#','#','#','#','#'], ]

### _Example of answer_:
['left', 'top','top','left','left','bottom','bottom','left']`

### ***Code***:
```
let maze = [
    ["#", "#", "#", "#", "#", "#", "#", "#", "#"],
  
    ["#", "+", "+", "+", "#", "+", "+", "+", "#"],
  
    ["#", "+", "#", "+", "#", "+", "#", "+", "#"],
  
    ["+", "+", "#", "+", "0", "+", "#", "+", "#"],
  
    ["#", "#", "#", "+", "#", "#", "#", "#", "#"],
  
    ["#", "#", "+", "+", "#", "#", "#", "#", "#"],
  
    ["#", "#", "+", "#", "#", "#", "#", "#", "#"],
  
    ["#", "#", "#", "#", "#", "#", "#", "#", "#"],
];
  
console.log(maze);

let arrayWay = [];
let cordStart = {};
let cordEnd = {};

searchStartEndCords(maze);

console.log(searchPath(cordStart, cordEnd).reverse())

function searchStartEndCords(array) {
    for (let i = 0; i < array.length; i++) {
        for (let j = 0; j < array[i].length; j++) {
                if (array[i][j] == "+" && (
                    i == array.length - array.length || 
                    j == array[i].length - array[i].length || 
                    i == array.length - 1 || 
                    j == array[i].length - 1 )
                ) {
                    cordEnd.x = j;
                    cordEnd.y = i;
                } else {
                    if (array[i][j] == "0") {
                        cordStart.x = j;
                        cordStart.y = i;
                    }
                }
            }
        }
    return cordStart, cordEnd;
};

function searchPath(start, end) {
    maze[start.y][start.x] = 'x' ;     
    let siblings = getValidSib(start);
    if(siblings.length > 0) {
        for(let i=0; i < siblings.length; i++){
            let current = siblings[i];

            let isSolved = current.x === end.x && current.y === end.y;
            let notVisited = maze[current.y][current.x] !== 'x';

            if (isSolved || (notVisited && searchPath(current,end))) {
                arrayWay.push(current.side);
                return arrayWay;                
            }
        }
    }
    return false;
}

function getValidSib(cord) {
    const { x, y } = cord;  
    let cords = [];
  
    if (maze[y - 1] !== undefined) {
      cords.push({ x: x, y: y - 1, val: maze[y - 1][x], side: "top" });
    }
    if (maze[y + 1] !== undefined) {
      cords.push({ x: x, y: y + 1, val: maze[y + 1][x], side: "bottom" });
    }
    if (maze[y][x - 1] !== undefined) {
      cords.push({ x: x - 1, y: y, val: maze[y][x - 1], side: "left" });
    }
    if (maze[y][x + 1] !== undefined) {
      cords.push({ x: x + 1, y: y, val: maze[y][x + 1], side: "right" });
    }
    return cords.filter((el) => el.val === "+");
}
```
* * *
## **Experience**
* Internship in **[ITRex Group](https://itrexgroup.com/)** (2 months)
* * *
## **Courses**
* [IT Academy](https://www.linkedin.com/school/it-academy/) Java fundamentals (88 academic hours)
* JavaScript on [learnjavascript.ru](https://learn.javascript.ru/)
* Some courses on [https://www.linkedin.com/learning](https://www.linkedin.com/learning)
* [RS Schools](https://rs.school/) , [Course «JavaScript/Front-end. Stage 0»](https://rs.school/js-stage0/) (in progress)
* * *
## **Languages**
* ***English*** - A2+
* ***Russian*** - Native