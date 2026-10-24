## Exercise A
- ``` <p>Hi <strong>there</strong><br>friend<img src="a.png" alt="A cat"></p> ```
- It has 8 tags and 5 elements
- Tags are the individual markup labels used to construct code while elements are complete componenet including openeing tag, content and closing tag

## Exercise B
- The browser will ignore the extra spaces and tabs parsing the HTML code
- The white-space: pre style will preserve the extra spaces and tabs

## Exercise C
- the mistakes in `recovery.html` was rendered by browser as below
```
<p> this is a paragraph </p>
<h2> this is a heading </h2>
<p></p>
<div>div tag inside p tag</div>
<p></p>
<strong><em>wrong syntax</em></strong>
```
- error for closing p tag was resolved 
- div tag which was inside p was moved out by creating new closing tag p and opening tag p
- strong and em tag closing order was corrected

## Exercise D
- Tab comes up only to button element 
- the role for div is generic and it has name ""
- the role for button is button with name "Save"
