# 2024 AP Computer Science Principles Free-Response Questions: Set 1

## AP® Computer Science Principles Written Response Prompts

### Instructions:
- **Time:** 1 hour
- **Questions:** 2
- Read each question carefully and completely.
- Write your response in the space provided for each question in the Written Response booklet.
- You may plan your answers in this orange booklet, but no credit will be given for anything written in this booklet. You will only earn credit for what you write in the separate Written Response booklet.

---
### Pre-FRQ Practice

## Identify the Algorithm present in the JavaScript Files. 
### Aspects of Algorithm
Sequencing
Selection 
Iteration

Gabe.js:

~~~Javascript
function final(array){
        let a = 0
        let b = 0
        for (let i = 0; i < array.length; i++){
         if (array[i].includes("Correct")) {a++}
         if (array[i].includes("Incorrect")) {b++}}
         clear()
         const correct = a * 100/DOMSelectors.input.value
         const incorrect = b * 100/DOMSelectors.input.value
         DOMSelectors.question.insertAdjacentHTML("beforeend", `<h1>You got ${correct}% of them right and ${incorrect}% of them wrong!</h1>`)
        }
~~~

Sequencing: displays steps in a logical order, first creating the variables, the going through the for loop, then returning values.
Selection: the if statements show selection. In this function, the selection is based on if the specific item in the array is correct or incorrect. Based on that, it decides whether variables a or b are increased by one.
Iteration: this for loop in the function shows iteration. In this function, the for loop iterates through an array, performing selection on each item in the array.

Evan.js:

~~~Javascript
function removeToDo() {
    const specificCard = this.parentElement;
    const specificCardText =
      specificCard.querySelector(".to-do-card").textContent;

    for (let i = 0; i < ToDoItems.length; i++) {
      if (ToDoItems[i] === specificCardText) {
        ToDoItems.splice(i, 1);
        break;
      }
    }
    
    specificCard.remove();
  }
~~~

Sequencing: sets variables and retrievs text content before running its remove function.
Selection: the if statement checks each item in the list and decides whether to remove it or keep it.
Iteration: the function's for loop iterates through the ToDo list to check each item.

### Question 1
Programs accept input to achieve their intended functionality. **Describe at least one valid input to your program and what your program does with that input.**

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

Evan.js : 

~~~Javascript
function addToDo(event) {
  DOMSelectors.toDoList.innerHTML = "";
  const inputtedToDo = DOMSelectors.userInput.value;
  event.preventDefault();
  ToDoItems.push(inputtedToDo);
  displayToDoList(ToDoItems);
  DOMSelectors.userInput.value = "";
}

DOMSelectors.submitButton.addEventListener("click", addToDo);
~~~

In this program, when the use presses the submit button, the program will take the user's input and push it into an array. The program will then use that array and display it on screen.

Gabe.js:

~~~Javascript
function game(qa) {
     let i = 0
     const used = []
     
     DOMSelectors.form.addEventListener('submit', function(event) {
         event.preventDefault()
         const input = DOMSelectors.input.value;
         displayQuestion(input)
     });
 
     function displayQuestion(input) {
         if (i < input) {
             let q = qa[i]
             console.log(q)
             clear()
             DOMSelectors.question.insertAdjacentHTML("beforeend", `<h1>${q.question}</h1>`)
         }
         
     }
}
~~~

In this program, the function takes the user input and sets its value as a variable "input". Based on this input which would seem to be a number, it gives the user questions up to the amount the user desired based on their input.
---

### Question 2
Refer to your Personalized Project Reference when answering this question.

#### Part (a):
Consider the first iteration statement included in the Procedure section of your Personalized Project Reference. **Describe what is being accomplished by the code in the body of the iteration statement.**

#### Part (b):
Consider the procedure identified in part (i) of the Procedure section of your Personalized Project Reference.
- Write two calls to your procedure that each cause a different code segment in the procedure to execute.
- Describe the expected behavior of each call. If it is not possible for two calls to your procedure to cause different code segments to execute, explain why this is the case for your procedure.

#### Part (c):
Suppose another programmer provides you with a procedure called `checkValidity(value)` that:
- Returns `true` if a value passed as an argument is considered valid by the other programmer.
- Returns `false` otherwise.

Using the list identified in the List section of your Personalized Project Reference, **explain in detailed steps an algorithm that uses `checkValidity` to check whether all elements in your list are considered valid by the other programmer.** Your explanation must be detailed enough for someone else to write the program code for the algorithm that uses `checkValidity`.

- Write your responses to this question only on the designated pages in the separate Written Response booklet.
- If there are multiple parts to this question, write the part letter with your response.

---

### End of Exam

