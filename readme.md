# Quiz Week 9

## Instructions

1. Fork this repo
2. Clone your fork
3. Fill in your answers by writing in the appropriate area, or placing an 'x' in
the square brackets (for multiple-choice questions).
4. Add/Commit/Push your changes to Github.
5. Open a pull request.

## AJAX

### Question #1

Using jQuery, write code that makes an AJAX get request to "http://kittengifs.com/gifs". Output to the console the total number of results you get back. (Assume the server responds with a JSON array of objects representing gifs.)

Your Answer:
```js
$(document).ready(function(){
  $(".load-kitten-gifs-button").on("click", function(){
    var url = "http://kittengifs.com/gifs"
    $.ajax({
      url: url,
      type: "get",
      dataType: "json"
    }).done(function(response){
      console.log("Purrrrr... " + response.length + " kitten gifs loaded.")
    }).fail(function(){
      console.log("MRRRREEEOOOOWWW! Could not load kitten gifs!!")
    })
  })
})
```

### Question #2

Describe at a high level how we use jQuery to submit a form via AJAX.

Your Answer:
```text

```


## Mongo / Mongoose

### Question #3

Describe the differences between a SQL and NoSQL DB, and when you might use each.

Your Answer:
```text
A SQL database is a database structured as a table or spreadsheet, while a NoSQL database is a collection of objects with no such inherent structure to it. A SQL database would be a better choice for storing data that mostly have similar attributes, because its structure allows values to be retrieved faster. But if the values have dissimilar attributes, a SQL database will expand the 'table' to include lots of unnecessary empty 'cells', so to speak, so a NoSQL database is a better choice in this instance.
```


### Question #4

What's wrong with this mongoose code and how might we fix it?
(Hint: Assuming there is a document with a name of "Bob", why is results not an author model on the second line?)

```js
var results = AuthorModel.find({name: "Bob"});
console.log(results);
```

Your Answer:
```text

```

## Front-end OOJS

### Question #5

Describe the purpose of views and models in FE JS.

Your Answer:
```text
Front-end JS does not necessarily require dedicated views or models, since the concatenation of .js files on the client-side means they are all sewn together into one. So an entire front-end *can* be built in one big file. However, it's good practice for purposes of separation of concerns and future readability and extensibility to abstract distinct functions out into their own .js files, and since the model-view-controller structure is the preferred pattern for most web development,
```

### Question #6

Given the following front-end JS model, add an instance method for all pandas called `eat_bamboo`. Calling this method should increase that panda's value for `num_bamboo_eaten` by 1.

```js
var Panda = function(name, age) {
  this.name = name;
  this.age = age;
  this.num_bamboo_eaten = 0;
}
```

Your Answer:
```text

```


## OAuth

### Question #7

How is the concept of OAuth related to a valet key?

Your Answer:
```text

```


## RWD

### Question #8

Write some basic CSS that demonstrates changing a CSS property when the device width drops below 40rem.

```css
body {
  background-color: lemonchiffon;
}

@media (max-width: 40rem) {
  body {
    background-color: chucknorris;
  }
}
```

## Git

### Question #9

How is rebase different than a merge?

Your Answer:
```text
A merge rejoins two branches at a new commit point. A rebase merges the entire commit history of a branch into the commit history of another branch, erasing them as distinct branches and rewriting them with a new shared history. Rebases allow for cleaner commit histories in the sense that the tangle of branches can be reduced, but they are dangerous because they result in the erasure of old, saved code.
```

### Question #10

Describe some of the common git workflows for teams (fork and pull request, etc).

```text

```
