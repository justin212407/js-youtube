# Projects related to DOM

## Project link:
[Click here](https://stackblitz.com/edit/dom-project-chaiaurcode-bcjpgp?file=1-colorChanger%2Fchaiaurcode.js,1-colorChanger%2Findex.html)

# Solution Code
## Project 1

```javascript

const buttons = document.querySelectorAll('.button');
console.log(buttons);
const body = document.querySelector('body');

buttons.forEach(function (button) {
  console.log(button);
  button.addEventListener('click', function (e) {
    console.log(e);
    console.log(e.target);
    if (e.target.id === 'grey') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id === 'yellow') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id === 'white') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id === 'blue') {
      body.style.backgroundColor = e.target.id;
    }
  });
});

```

## Project 2 Solution

```javascript

const form = document.querySelector('form');

//const height = parseInt(document.querySelector('#height').value)
//This use case will give you empty value

form.addEventListener('submit', function (e) {
  e.preventDefault();
  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');

  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = `Please give a valid height ${height}`;
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = `Please give a valid weight${weight}`;
  } else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);
    // Show the result
    results.innerHTML = `<span>${bmi}</span>`;
  }
  const bmi = (weight / ((height * height) / 10000)).toFixed(2);
  const weightg = document.querySelector('#weight-guide')
  if(bmi < 18.6){
    weightg.innerHTML = "Under Weight";
  } else if (bmi >= 18.6 && bmi <=24.9){
    weightg.innerHTML = "Normal Range";
  }else {
    weightg.innerHTML = "Overweight"
  }
});

```
## Project 3

```javascript
document.getElementById('clock')
//document.querySelector('#clock')

setInterval(function(){
  let date = new Date()
  //console.log(date.toLocaleTimeString());
  clock.innerHTML = date.toLocaleTimeString();
}, 1000);

```
## Project 4

```javascript



```
