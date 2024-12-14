# Christmas-tree
Make a Christmas tree using basic HTML 

    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beautiful Christmas Tree</title>
    <style>
        body {
            background: linear-gradient(to bottom, #00111a, #004466);
            color: white;
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .tree-container {
            position: relative;
            margin: 50px auto;
            width: 200px;
        }
        .tree-layer {
            position: relative;
            width: 0;
            height: 0;
            border-left: 100px solid transparent;
            border-right: 100px solid transparent;
            border-bottom: 100px solid green;
            margin: -30px auto;
        }
        .tree-layer:nth-child(1) {
            border-bottom-color: #2ecc71;
        }
        .tree-layer:nth-child(2) {
            border-bottom-color: #27ae60;
            border-bottom-width: 120px;
        }
        .tree-layer:nth-child(3) {
            border-bottom-color: #1e8449;
            border-bottom-width: 140px;
        }
        .star {
            position: absolute;
            top: -50px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 40px;
            color: gold;
            animation: sparkle 1s infinite;
        }
        .trunk {
            position: relative;
            margin: 0 auto;
            background-color: #8b5a2b;
            width: 40px;
            height: 60px;
        }
        .lights {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 1;
            pointer-events: none;
        }
        .light {
            position: absolute;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background-color: red;
            animation: blink 2s infinite;
        }
        .light:nth-child(odd) {
            animation-delay: 1s;
        }
        @keyframes sparkle {
            0%, 100% {
                transform: translateX(-50%) scale(1);
                opacity: 1;
            }
            50% {
                transform: translateX(-50%) scale(1.2);
                opacity: 0.7;
            }
        }
        @keyframes blink {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.3;
            }
        }
    </style>
</head>
<body>
    <div class="tree-container">
        <div class="star">★</div>
        <div class="tree-layer"></div>
        <div class="tree-layer"></div>
        <div class="tree-layer"></div>
        <div class="trunk"></div>
        <div class="lights">
            <div class="light" style="top: 20%; left: 45%;"></div>
            <div class="light" style="top: 30%; left: 60%;"></div>
            <div class="light" style="top: 40%; left: 40%;"></div>
            <div class="light" style="top: 50%; left: 50%;"></div>
            <div class="light" style="top: 60%; left: 70%;"></div>
            <div class="light" style="top: 70%; left: 30%;"></div>
        </div>
    </div>
    <h1>Merry Christmas!</h1>
</body>
</html>
       
