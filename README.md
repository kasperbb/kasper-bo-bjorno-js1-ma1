# Files for JavaScript 1 Module Asssignment 1

## Contents of [script.js](https://github.com/kasperbb/kasper-bo-bjorno-js1-ma1/blob/main/js/script.js)
```javascript
const cats = [
    {
        name: "Blob",
        age: 10
    },
    {
        name: "Harold",
    },
    {
        name: "Blurt",
        age: 21
    }
];

// Question 1
const cat = {
        complain: () => console.log("Meow!")
};

// Question 2
const heading = document.querySelector("h3");

heading.innerHTML = "Updated heading";

// Question 3
heading.style.fontSize = "2rem";

// Question 4
heading.classList.add("subheading");

// Question 5
const paragraphs = document.querySelectorAll("p");

paragraphs.forEach(p => p.style.color = "red");

// Question 6
const resultContainer = document.querySelector(".results");

resultContainer.innerHTML = "<p>New paragraph</p>";
resultContainer.style.backgroundColor = "yellow";

// Question 7
const listNames = (list) => {
    list.forEach(listItem => console.log(listItem.name));
}

listNames(cats);

// Question 8
const createCats = (cats) => {
    let html = "";
    cats.forEach(cat => {
        html += `
            <div>
                <h5>${cat.name}</h5>
                <p>${(cat.age) ? cat.age : "Age unknown"}</p>
            </div>
        `;
    })
    return html;
}

const catContainer = document.querySelector(".cat-container");

catContainer.innerHTML = createCats(cats);

```