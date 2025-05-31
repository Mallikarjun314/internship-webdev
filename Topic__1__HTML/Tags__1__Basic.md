# `<!DOCTYPE html>`

- Proper Structuring
- To tell the browser how to parse the document
- Applying Strict rules specific to HTML version 5

<br/>
<br/>
<br/>
<br/>

# Basic Html Elements
| Description           |        Tags        |
| --------------------- | :----------------: |
| Top Level tag         |      `<html>`      |
| Head Section          |      `<head>`      |
| Document / Page Title |     `<title>`      |
| Body Section          |      `<body>`      |
| Comments              | `<!--   ...   -->` |

#### Example:
```html
<!DOCTYPE html>
<html>
    
    <head>
        <title>Page title</title>
    </head>

    <body>
        <!--   This is some comment   -->
        ...
    </body>

</html>
```

<br/>
<br/>
<br/>
<br/>

# Basic Formating Tags

1. Headings : `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`

2. Bold : `<b> ... </b>` 
3. Italic : `<i> ... </i>` 
4. Underline : `<u> ... </u>`
5. Subscript : `<sub> ... </sub>`
6. Superscript : `<sup> ... </sup>`
7. Del : `<del> ... </del>`
8. Keyboard : `<kbd> ... </kbd>`
9. Link / Anchor Tag : `<a href="..." >  .....  </a>`
10. Paragraph Tag : `<p>  ...  </p>`
11. **Self closing tag**
    1.  Break Tag : `<br/>` 
    2.  Image : `<img   src="..."  alt="..."  />` (Self closing tag)
    3.  Horizontal line : `<hr/>`

<br/>
<br/>
<br/>

#### Example :

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Page title</title>
    </head>
    <body>
        <h1> This is a Heading </h1>

        <p> This is a <u>paragraph</u>. <br/> <del>Hello</del> how are <b>you</b> </p>

        <hr/>

        <p>Quadratic equation: <i>Y = 2 X<sup>2</sup> + 3 X + 7</i> </p>

        <hr/>

        <p>Shortcut for copy: <kbd>ctrl + c</kbd> </p>
    </body>
</html>
```


