# What's New for Me

## Stages Finisheed

* [Role Playing Game](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures-v8/#learn-basic-javascript-by-building-a-role-playing-game)

## JS HTML Methods 

* ```document.querySelector('')``` [link](https://doka.guide/js/query-selector/) 
  + Позволяет найти элемент по CSS-селектору среди дочерних. 
  + Если элементов несколько, то вернётся первый подходящий. 
  + Если подходящих элементов нет, то вернёт null.

```
const button1 = document.querySelector('#button1');
const monsterHealthText = document.querySelector('#monsterHealth');
```

## JS HTML Properties

* ```.innerText``` [link](https://doka.guide/js/element-innertext/)

  * позволяет считывать или задавать текстовое содержимое элемента. 
  * gри считывании текста с элемента будет возвращена строка с текстовым содержимым всех вложенных дочерних элементов. 
  * не будет считываться только содержимое скрытых с помощью CSS элементов, а так же содержимое тегов \<script> и \<style>.

  ! Аналогичной функциональностью обладает свойство textContent, но он возвращает содержимое всех дочерних элементов

```
const text = document.querySelector('#text');
text.innerText = "You do not have enough gold to buy health.";
```
## JS Objects
[LearnJS](https://learn.javascript.ru/object)

### how to Create

```
let user = new Object(); // синтаксис "конструктор объекта"
let user = {}; // literal notation
``` 

#### Some Examples

```
const weapons = [
  { name: 'stick', power: 5 },
  { name: 'dagger', power: 30 },
  { name: 'claw hammer', power: 50 },
  { name: 'sword', power: 100 }
];
```

```
const locations = [
  {
    name: "town square",
    "button text": ["Go to store", "Go to cave", "Fight dragon"],
    "button functions": [goStore, goCave, fightDragon],
    text: "You are in the town square. You see a sign that says \"Store\"."
  }, 
  ...]
```

If we have a string containing > 1 word as a key, we need to use quotes. - 'my key'

```
{
    name: "store",
    "button text": ["Buy 10 health (10 gold)", "Buy weapon (30 gold)", "Go to town square"],
    "button functions": [buyHealth, buyWeapon, goTown],
    text: "You enter the store."
  },
```
Calling long keys.value

```
// use:
// object['key name']
button1.innerText = location['button text']; 
```