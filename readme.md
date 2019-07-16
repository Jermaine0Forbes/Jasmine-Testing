# Jasmine

- [how to install jasmine][inst-jasmine]
- [what does the describe function do][describe]
- [what does the "it" function do][it]

## Expectations
- [toBe][tobe]

[it]:#what-does-the-it-function-do
[describe]:#what-does-the-describe-function-do
[tobe]:#toBe
[home]:#jasmine
[inst-jasmine]:#how-to-install-jasmine


### what does the it function do

<details>
<summary>
View Content
</summary>

:link: **Reference**
- [jasmine global](https://jasmine.github.io/api/edge/global.html#it)
---
:question: **Syntax**

`it(description, testFunctionopt, timeoutopt)`

---
:blue_book: **Summary:** Define a single spec. A spec should contain one or more
 expectations that test the state of the code. A spec whose expectations all succeed
will be passing and a spec with any failures will fail.

```js
// The it functions purpose it to hold one or more expections
it("is actually a cat", function(){
      expect(cat.isCat).toBe(true);// checks if isCat returns true

      expect(cat.weight).toEqual("2kg"); // checks if weight is equivalent to 2kg
});
```

</details>

[go back :house:][home]


### what does the describe function do

<details>
<summary>
View Content
</summary>

:link: **Reference**
- [Your first suite](https://jasmine.github.io/tutorials/your_first_suite.html)
---

:question: **Syntax**

`describe(description, specDefinitions)`

---

:blue_book: **Summary:** The describe function is for grouping related specs, typically each test file has one at the top level. The string parameter is for naming the collection of specs, and will be concatenated with specs to make a spec's full name.

```js

// The describe function holds a group of related specs to be ran, and describes what it is about
describe("Cat", function(){
  const Cat = require("../../lib/jasmine_examples/Cat");// assigns the cat class to Cat
  let cat;

  beforeEach(function(){ // before a spec runs, Cat is instantiated into cat
    cat = new Cat();

  })

  // this spec, runs an assertion that the isCat property  is to return true
  it("is actually a cat", function(){
        expect(cat.isCat).toBe(true);
  });
});
```

</details>


### toBe

<details>
<summary>
View Content
</summary>

:link: **reference**
- [matchers](https://jasmine.github.io/api/edge/matchers.html)

:question: **syntax**

`expect(thing).toBe(realThing);`

**In js file**
```js
class Cat{

  constructor(){
    this.isCat = true;//this is the property we are going to test
   console.log("cat is created");
  }
}

module.exports = Cat;
```


**In spec file**
```js
it("is actually a cat", function(){
      expect(cat.isCat).toBe(true); //
});
```

</details>

[go back :house:][home]



### how to install jasmine

<details>
<summary>
View Content
</summary>

:link:**reference**
- [jasmine](https://jasmine.github.io/setup/nodejs.html)

1. In your terminal, install jasmine with these commands. Make sure you have npm
installed

```
npm install jasmine

npm install -g jasmine
```

2. In order to initialize a jasmine project just type this

```
jasmine init
```

3. To generate an example project type this

```
jasmine examples
```

4. To run all jasmine tests

```
jasmine
```

5. Hopefully, everything passes

</details>

[go back :house:][home]
