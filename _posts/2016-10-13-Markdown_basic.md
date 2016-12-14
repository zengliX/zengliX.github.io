---
title:  "Markdown Basics"
date:   2016-10-25
layout: single
author_profile: true
comments: true
tags: [markdown, latex]
---



_**Markdown**_ is not as fancy as _Latex_, doesn't have many typesetting features as the latter does, but it's very useful in daily non-serious publications: such as online articles, lecture notes or research notes.

_Latex_ is better suited for serious academic writing and requires a lot of time in writing the code and compiling, while _Markdown_ only provides the most essential typesetting features in daily writing and the syntax is easy to pickup.

## Typeface
Italic : `_an italic phrase_` _an italic phrase_  
 Bold: `**a bold phrase**`  **a bold phrase**  

And they can be embedded as well: **_both italic and bold_**

## Header
You can use a series of \# signs to start headers. The more \# sign you use, the smaller the headers are.   
Example inputs:    

```md
### medium header
#### small header
##### smaller header
###### smallest header
```

Outputs:      
### medium header   
#### small header   
##### smaller header   
###### smallest header   

You can use up to 6 \# signs.

## Links   

### link to website   

You can incorporate links in sentences with the syntax: `\[text\](link address)`.  

Example: here is the link to [Github](https://github.com/), generated from code `[Github](https://github.com/)`  

We can also do it this way: `[Github][label1]` -> [also a link to Github][label1], and define `[label1]` later in  file:  
`[label1]:https://github.com/`
[label1]:https://github.com/

### link to online images
Could also use the same syntax to include images, just add `!` exclamation mark in the front:  

```
![My first picture](https://www.coursebuffet.com/course_images/coursera/introstats.png)
```
![My first picture](https://www.coursebuffet.com/course_images/coursera/introstats.png)

### link to local images
```
![local](/assets/batman.png)
```
![local](/pics/batman.png)

### link to text on local page (named anchor)
This is extremely useful if you write a long page, which makes it a headache if you have to scroll down  and down to reach certain text. 

The way **named anchor** works is that, you can leave an anchor at the target text, and then create a link to it where you need.

```md
//create anchor at target text
//let's take Blockquotes section as example
<a name="blockquotes"> Blockquotes </a>

// then refer to it wherever needed
// syntax is similar to other links
[link text](#blockquotes)
```

So here is the link to [blockquotes](#blockquotes). 

The linked text will appear in other color. If you don't want this effect, simply write `</a>` right after `<a name="***">`. This is basically  _html_ language. The front `< >` opens a tag, while the latter `< >` closes a tag.

## <a name="blockquotes"> Blockquotes </a>
Use the "greater than" sign `>` to quote a line:  

```md
> "let me do _a_  **quote** "
```

> "let me do _a_  **quote**"

Obviously, you can include all kinds of Markdown effects as well.

## Listing
Code to make a list:

```
- For unordered list:
 * Asterisk listing (\*)
 - Hyphen listing (\-)
 * Use indent and (\* or \- or number) to add more depth to the list
   * a level 2 here (\*)
     * level 3
      level 3 line 2
   - another sub level (\-)


- For ordered list:
 1. point 1
 2. point 2

- Task Lists: (would appear on some websites as check boxes)
  - [x]  some job done
  - [ ] some job undone
```

- For unordered list:
 * Asterisk listing (\*)
 - Hyphen listing (\-)
 * Use indent and (\* or \- or number) to add more depth to the list
   * a level 2 here (\*)
     * level 3
      level 3 line 2
   - another sub level (\-)


- For ordered list:
 1. point 1
 2. point 2

- Task Lists: (would appear on some websites as check boxes)
  - [x]  some job done
  - [ ] some job undone


## Insert Code
- Inline code: you can just use \` your code here \`:   
`int *fun(int x, int y)`

- Include syntax highlighting:

```c
int x=1, y=2;
return x+y;
```

This looks very similar to an _Rmarkdown_ chunk.

## Insert Tables
```
Table column 1 | Table column 2
---------------|-------------
cell 11 | cell 12
cell 21 | cell 22
```
And you get:

Table column 1 | Table column 2
---------------|-------------
cell 11 | cell 12
cell 21 | cell 22

## Markdown $\LaTeX$ and Math
### Math

- use double dollar sign `$$ contents $$` to center math equations:

```
$$y_{ij}= \sum_{k=1}^N a_{ik}b_{kj} \exp(c_k)$$
```
	
$$y_{ij}= \sum_{k=1}^N a_{ik}b_{kj} \exp(c_k)$$

- use single dollar sign `$ content $` to include inline math equation:

```
I get $cos(x)y$ from $\frac{\partial sin(x)y}{\partial x}$
```

I get $cos(x)y$ from $\frac{\partial sin(x)y}{\partial x}$.
	
Rules are the same as in _Latex_.


## Others

### make new lines
By default, Markdown only jump one line after your 'enter'. But when sometimes you want a bit more space between lines, and your Markdown compiler supports _html_, you can write one line with `<br><br>`, and that line would appear blank.

This is _html_ language way for starting a new line, and `br` stands for _break_.


### Markdown comments
Syntax: `[//]: comments here`