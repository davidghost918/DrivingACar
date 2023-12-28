
# DrivingACar




<html>
<head>
    <meta charset="utf-8">
    <title>Car animation</title>
    <style>
        @keyframes car {
            from {
                left: 0;
                top: 0;
            }
            to {
                left: calc(100% - 250px);
                top: 0;
            }
        }

        .car {
            position: relative;
            width: 200px;
            animation: car 10s 1;
            animation-fill-mode: forwards;
        }

        .car-front {
            position: absolute;
            top: 0;
            right: 0;
            background: red;
            width: 60px;
            height: 50px;
            border-radius: 0 55px 0 0;
        }

        .car-back {
            width: 150px;
            height: 50px;
            background: red;
            position: relative;
            border-radius: 10px 0 0 0;
        }

        .window {
            position: absolute;
            background: white;
            width: 30px;
            height: 12px;
            border-radius: 0 20px 0 0;
            padding-bottom: 10px;
            top: 4px;
            left: 12px;
        }

        .b-tyres, .f-tyres {
            width: 30px;
            height: 30px;
            background: black;
            border-radius: 30px;
            position: absolute;
            border: 2px solid #ccc;
            bottom: -12px;
            z-index: 1;
        }

        .b-tyres {
            left: 10px;
        }

        .f-tyres {
            right: 10px;
        }

        .b-tyres::after,
        .f-tyres::after {
            content: "";
            background: lightgray;
            width: 20px;
            height: 20px;
            border-radius: 10px;
            top: 5px;
            left: 5px;
            position: absolute;
        }

        html, body {
            margin: 0;
            padding: 0;
            background-color: lightgreen;
        }

        .road {
            padding-top: 20px;
            width: 100%;
            position: absolute;
            top: 40%;
            bottom: auto;
            background-color: lightslategray;
            height: 76px;
        }

        .tree {
            margin-left: 20px;
            position: absolute;
            height: 40%;
        }

        .tree-part-1 {
            top: 20px;
            border-width: 0 100px 60px 100px;
        }

        .tree-part-2 {
            top: 10px;
            border-width: 0 150px 80px 150px;
        }

        .tree-part-3 {
            border-width: 0 200px 100px 200px;
            top: -20px;
        }

        .tree-common {
            width: 0;
            height: 0;
            position: relative;
            margin-left: auto;
            margin-right: auto;
            border-style: solid;
            border-color: transparent transparent #004511 transparent;
            border-radius: 50%;
            z-index: 2;
        }

        .trunk {
            position: relative;
            width: 30px;
            height: 50px;
            margin-left: 184px;
            top: -25px;
            background-color: #53350a;
            z-index: 1;
        }

        .sun {
            margin-top: 20px;
            margin-left: calc(100% - 250px);
            display: inline-block;
            border-radius: 50%;
            height: 100px;
            width: 100px;
            background: orange;
            box-shadow: 0 0 10px orange,
            0 0 60px orange,
            0 0 200px yellow,
            inset 0 0 80px yellow;
            z-index: 99;
        }

        .sky {
            top: 0;
            position: absolute;
            background-color: lightblue;
            height: 20%;
            width: 100%;
        }

    </style>
</head>

<body>
<div class="sky">
    <div class="sun"></div>
</div>
<div class="tree">
    <div class="tree-part-1 tree-common"></div>
    <div class="tree-part-2 tree-common"></div>
    <div class="tree-part-3 tree-common"></div>
    <div class="trunk"></div>
</div>

<div class="road">
    <div class="car">
        <div class="car-back"></div>
        <div class="car-front">
            <div class="window"></div>
        </div>
        <div class="b-tyres"></div>
        <div class="f-tyres"></div>
    </div>
</div>
</body>
</html>
