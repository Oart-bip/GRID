<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout com Grid e Pseudo-elementos</title>

    <style>
        body {
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: thistle;
        }
      
        .container{
            display: grid;
            grid-template-columns: repeat(3,1fr); 
            padding: 20px;
            max-width: 900px;
            margin: auto; 
        }

      
        .item{
            background-color: aqua;
            padding: 20px;
            text-align: center;
            border-radius: 8px; 
            box-shadow: 0 4px 6px black;
                
            position: relative;
        }

        .item:hover{
            background-color: yellowgreen;
            transform: scale(1.05);
            transition: 0.3s;
        }

        .item:nth-child(2){
            background-color:red;
        }

       
        .item::before{
            content: " + ";
            font-size: 20px;
        }

        .item::after{
            content: " + ";
            font-size: 20px;
        }
    </style>
</head>
<body>
    
    <div class="container">
        <div class="item">Item 1</div>
        <div class="item">Item 2</div>
        <div class="item">Item 3</div>
        <div class="item">Item 4</div>
        <div class="item">Item 5</div>
        <div class="item">Item 6</div>
    </div>


</body>
</html>
