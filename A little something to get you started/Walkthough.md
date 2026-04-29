# Trival - A little something to get you started

**Difficulty:** Trival  
**Category:** Web Security  
**Flags:** 1/1  
**Platform:** Hacker101 CTF

---


# 📣  General Overview 

A little something to get you started is where you first start your introduction to web security based CTF.

---


# 📜  Reconnaissance
The website is only showing a text " Welcome to level 0. Enjoy your stay."
maybe we can inspect element for checking the suspicious HTML code

---


# 🚩  FLAG 1 : Inspect Element.

**This website it looks like normally but there was hidding the code.**
try looking at it using inspect element in the browser.

1. Inspect Element (F12)

2. look the code at <style> there is something suspicious code background image


```html
<html>
    <head>
        <style>
            body {
                background-image: url("background.png");
            }
        </style>
    </head>
    <body>
        <p>Welcome to level 0.  Enjoy your stay.</p>
    </body>
</html>
```

3. Let's open the link by adding .../background.png at the end.

4. And boom, the website showing the hidden code 

```html
<html>
    <head>
    </head>
      <body>
        ^FLAG^1a364e396c92ba4ba033237ec46e16d05ac70e7f2c6adcd1d8a03b081ebd9cdb$FLAG$
      </body>
</html>
```


Analyst : The code Flag is hidden in background.png from style 



### 🏁 Now were get the flag and submit finish!!
