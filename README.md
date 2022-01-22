# Web Page for Paint Application

## AIM:

To design a static website for Paint Application using HTML5 canvas.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML,CSS and canvas.

### Step 3:

Write javascript to capture move events.

### Step 4:

Perform the drawing operation based on the user input.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
~~~
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Canvas Application</title>
    <style>
        .maincontainer {
            text-align: center;
            background-color: transparent;
            grid-gap: 50px;
            width: 1080px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .fbox {
            display: block;
            width: 100%;
            background-color: whitesmoke;
            opacity: 60%;
            min-height: 100px;
            margin-top: 0px;
            margin-bottom: 0px;
            box-shadow: inset 0 0 15px black;
            backdrop-filter: blur(9px);
            border-radius: 10px;
            border: 1px solid whitesmoke;
        }
        
        .fbox2 {
            display: block;
            width: 100%;
            background-color: whitesmoke;
            opacity: 60%;
            min-height: 35px;
            margin-top: 0px;
            margin-bottom: 0px;
            box-shadow: inset 0 0 15px black;
            backdrop-filter: blur(9px);
            border-radius: 10px;
            border: 1px solid whitesmoke;
        }
        
        body {
            background-color: #084f79;
            background-image: linear-gradient(315deg, #ff4e00 0%, #ec9f05 74%);
            background-image: url("img/1.jpg");
            background-repeat: no-repeat;
            background-attachment: fixed;
            position: sticky;
            background-size: cover;
        }
        
        input {
            background-color: rgba(98, 136, 9, 0.603);
            border: 2px solid grey;
            border-radius: 25px;
            color: white;
            padding: 15px 32px;
            text-align: center;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
        }
        
        canvas {
            background-color: white;
            backface-visibility: initial;
        }
        
        .footer {
            background: linear-gradient(to right, #daf10c, #e94057, #8a2387);
            color: transparent;
            -webkit-background-clip: text;
            background-clip: text;
            text-decoration: none;
            margin: 0;
            line-height: 26px;
            font-size: 20px;
            color: #990099;
            text-align: center;
        }
    </style>

    <script type="text/javascript">
        var shape;
        var color;

        function myClickEvent(e) {
            var ctx = c.getContext("2d");
            ctx.beginPath();
            if (color == 1) {
                ctx.strokeStyle = 'red';
            } else if (color == 2) {
                ctx.strokeStyle = 'yellow';
            } else if (color == 3) {
                ctx.strokeStyle = 'blue';
            }
            if (shape == 0) {
                ctx.arc(e.offsetX, e.offsetY, 45, 0, 2 * Math.PI);
                ctx.stroke();

            } else if (shape == 1) {
                ctx.moveTo(150, 100);
                ctx.lineTo(200, 150);
                ctx.lineTo(200, 50);
                ctx.closePath();
                ctx.stroke();

            } else if (shape == 2) {
                ctx.rect(e.offsetX, e.offsetY, 250, 200);
                ctx.stroke();


            } else if (shape == 3) {
                ctx.rect(e.offsetX, e.offsetY, 100, 100);
                ctx.stroke();
            }
        }

        function circleClicked() {
            shape = 0;
        }

        function triangleClicked() {
            shape = 1;
        }

        function rectangleClicked() {
            shape = 2;
        }

        function squareClicked() {
            shape = 3;
        }

        function redClicked() {
            color = 1;
        }

        function blueClicked() {
            color = 3;
        }

        function yellowClicked() {
            color = 2;
        }
    </script>
</head>

<body>
    <div class="maincontainer">
        <div>
            <h1><b>Canvas Drawing Application</b></h1>
        </div>
        <div class="fbox">
            <br><br><br>
            <canvas id="myCanvas" width="1000" height="505" style="border:1px solid #000000"></canvas>
            <div>
                <input type="button" id="circle" value="Circle">
                <input type="button" id="line" value="Triangle">
                <input type="button" id="rectangle" value="Rectangle">
                <input type="button" id="square" value="Square">

            </div>
            <div>
                <input type="button" id="red" value="Red">
                <input type="button" id="blue" value="Blue">
                <input type="button" id="yellow" value="Yellow">
            </div>
            <script type="text/javascript">
                var c = document.getElementById("myCanvas");
                c.addEventListener("click", myClickEvent);
                document.getElementById("circle").addEventListener("click", circleClicked);
                document.getElementById("line").addEventListener("click", triangleClicked);
                document.getElementById("rectangle").addEventListener("click", rectangleClicked);
                document.getElementById("square").addEventListener("click", squareClicked);
                document.getElementById("red").addEventListener("click", redClicked);
                document.getElementById("blue").addEventListener("click", blueClicked);
                document.getElementById("yellow").addEventListener("click", yellowClicked);
            </script>
        </div>
        <br>
        <div class="fbox2">
            <div class="footer">
                Developed by Ragul M (21500303).
            </div>
        </div>
</body>

</html>
~~~

## OUTPUT:



## Result:

Thus a website is designed and validated for paint application using HTML5 canvas.
