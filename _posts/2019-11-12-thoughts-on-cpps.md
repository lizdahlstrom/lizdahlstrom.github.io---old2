---
layout: post
title:  "Thoughts on CSS preprocessors"
date:   2019-11-12 16:08:27
comments: true
categories: web frontend css
---

CSS preprocessors (CPP's) have been a part of web development for years. They have a bunch of features developed to make writing stylesheets easier.

<!--more-->

Making this website has not been my first experience with CPP's, although it has been a few years since my last little dabble. Back in those days CSS could be a headache to deal with (in my opinion), and familiarizing myself with Sass turned out to be a real pain reliever. 

So, what is so great about taking the extra steps of implementing a CPP? In the following article I will compare native CSS with some of the main features of Sass.

### 1. Variables
Writing CSS can get messy, fast. The number one reason why my head instantly felt lighter when I did start using SASS for the first time, was the ability to use variables. The ability to, for example, change color or font by changing the value of one single variable should have been a given thing. That being said, nowadays CSS does have support for variables, which is great.

### 2. Nesting
Another reason why CSS tends to look messy to the eye is that the hierarchy of selectors is not apparent. Yes, they are called Cascading Style Sheets for a reason! That is, that "cascading" is partly referring to the actual hierarchy system of CSS. However, nested code is easier to understand and is thus cleaner. Or at least, that is what I think. Nesting is available with Sass, and will most likely be supported in CSS in the future. [CSSWG Nesting draft](https://drafts.csswg.org/css-nesting/)

### 3. Conditionals, loops and functions
Sass allows you to perform complex operations with the support of conditionals, loops and functions. In comparison, CSS has some built in functions, for example ```calc()``` (used for calculations on property values) and ```attr()``` (gets the value of an attribute). Not nearly as powerful.


### 4. Inheritance
Sass offers a way for selectors to inherit from eachother. I like the idea of this feature as it, just like variables and functions, opens up to reuse of code.

An example:

```
.a-class {
  color: $some-color;
}

.another-class {
  @extend .a-class;
  font-size: $some-font-size;
}
```
### 5. Mixins
Again another feature which helps reduce the amount of repeated code. Mixins allow you to define reusable styles, with or without arguments. Native CSS does have something similar -  ```@apply```. However, using ```@apply``` does not allow you to use arguments.

## On this site
When building this site the main Sass features I made use of are variables and nesting. As the base theme Minima includes Sass files out of the box, all I had to do was add/edit the existing files. 

## Conclusion
There are many features of CPP's that are not only now available in CSS out of the box, but are on the list of things to come. Some of the features that native CSS offers are variables, imports (so you can split files into partials) and simple calculations.

For smaller projects building static web sites, using CSS out of the box might suffice. However, I think that it is slightly easier to organize and structure projects with the use of CPP's. Not to mention it has a better support for implementing DRY, organizing and making the code more readable and as such - more maintainable. Between basic CSS and using a CPP, I think the latter might be the better choice, especially when collaborating.
