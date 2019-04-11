# JCML
Write web-pages in JSON, compile them into HTML

## Why is it called JCML?
JCML stands for JSON Markup language. The C is for my last name, because things on the internet already were JSONML, JML, etc...

## Why do I need this?
I'm going to figure that out as I go, it seems good in theory: write a web-page with JSON like this:
```json
{
    "html":{
        "//":"the head section",
        "head":{
            "title":{
                "text": "Customers"
            },
            "link":{
                "rel":"stylesheet",
                "href":"main.css"
            }
        },
        "//": "The body section",
        "body":{
            "header":{

            },
            "main":{
                "h1":{
                    "align":"center",
                    "text":"Admin Pages"
                },
                "p":"This is a paragraph with nothing put the p-tag wrapped around this text"
            },
            "footer":{
                
            }
        }
    }
}
```
instead of HTML that is this:
```html
<html>
<!-- the head section -->

<head>
    <title>Customers</title>
    <link rel="stylesheet" href="main.css">
</head>

<!-- the body section -->

<body>
    <header></header>
    <main>
        <h1 align="center">Admin Pages</h1>
        <p>This is a paragraph with nothing put the p-tag wrapped around this text</p>
        
    </main>
    <footer></footer>
</body>

</html>
```

It should save you a lot of typing, and make things feel more Object Oriented. Granted, this may have a higher learning curve, since it's not as intuitive to know when things really end...

I'm going to start with a parser, get it to convert some basic JSON into HTML. Once that is complete, I want to see if I can introduce some way to also convert CSS (and tie in's with node? maybe some node.js to build the JSON? A node.js API? We'll see).

I plan on writing this in node.js because that makes the most sense. I need to look into babel and see if that would be helpful to me for parsing JavaScript.

Please open issues if you have any ideas, or if you think this is silly :-) I want to hear your thoughts.
