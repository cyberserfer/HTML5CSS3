# styles.css

```
*  
{
    padding:0px;
    margin: 0px;
}

body
{
    background-color:#cccccc;
}

.menu
{
    list-style: none;
    text-align:center;
}

.menu li:hover
{
    background-color: #cc9999;
}

.menu li
{
    display:inline-block;
    width: 150px;    
    text-align:center;
    padding: 3px 0 0 10px;
    border-bottom: 3px solid #000000;           
    background-color: #cccc99;
}

.menu li a
{
    text-decoration:none;
    color: #000000;
}
```

# page.html

```
<!DOCTYPE html>
<html>
<head>
    <title>Links</title>    
    <link rel="stylesheet" href="styles.css" type="text/css" />    
    
</head>
<body>
    <ul class="menu">
        <li>
            <a href="http://www.w3.org/Style/CSS/">CSS Specifications</a>        
        </li>
        <li>
            <a href="http://www.csszengarden.com/">CSS Zen Garden</a>
        </li>   
        <li>
            <a href="http://www.blueprintcss.org/">Blueprint</a>
        </li> 
        <li>
            <a href="http://developer.yahoo.com/yui/">YUI</a>
        </li>
    </ul>    
</body>
</html>
```
