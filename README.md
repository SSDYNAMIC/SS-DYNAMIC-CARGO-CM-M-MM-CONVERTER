# SS-DYNAMIC-CARGO-CM-M-MM-CONVERTER
SS DYNAMIC CARGO = CM, M, MM CONVERTER
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SS DYNAMIC CARGO - Dimension Converter</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:linear-gradient(rgba(0,0,0,.85),rgba(0,0,0,.85)),
url('https://images.unsplash.com/photo-1566438480900-0609be27a4be');
background-size:cover;
background-position:center;
color:#fff;
min-height:100vh;
}

header{
background:#111;
padding:30px;
text-align:center;
border-bottom:3px solid red;
}

header h1{
color:red;
font-size:42px;
}

header h2{
margin-top:10px;
font-size:22px;
}

.container{
max-width:1200px;
margin:auto;
padding:30px;
}

.card{
background:#111;
padding:25px;
border-radius:15px;
margin-bottom:25px;
border:1px solid #333;
}

.card h3{
color:red;
margin-bottom:20px;
}

label{
display:block;
margin-top:15px;
margin-bottom:5px;
font-weight:bold;
}

input,select{
width:100%;
padding:12px;
border:none;
border-radius:8px;
background:#222;
color:white;
}

button{
width:100%;
padding:15px;
background:red;
color:white;
font-size:18px;
font-weight:bold;
border:none;
border-radius:8px;
cursor:pointer;
margin-top:20px;
}

button:hover{
background:#cc0000;
}

.result{
margin-top:20px;
background:#000;
padding:20px;
border-radius:10px;
font-size:18px;
line-height:1.8;
border:1px solid red;
}

.flags{
font-size:45px;
margin-bottom:10px;
text-align:center;
}

footer{
background:#111;
padding:20px;
text-align:center;
margin-top:30px;
}

</style>
</head>

<body>

<header>

<div class="flags">
🇨🇳 CHINA ➜ 🇲🇾 MALAYSIA
</div>

<h1>SS DYNAMIC CARGO</h1>

<h2>LOGISTICS FORWARDER CARGO CHINA TO MALAYSIA</h2>

</header>

<div class="container">

<div class="card">

<h3>CM • M • MM CONVERTER</h3>

<label>Length (CM)</label>
<input type="number" id="length" placeholder="Enter Length">

<label>Width (CM)</label>
<input type="number" id="width" placeholder="Enter Width">

<label>Height (CM)</label>
<input type="number" id="height" placeholder="Enter Height">

<label>Weight (KG)</label>
<input type="number" id="weight" placeholder="Enter Weight">

<button onclick="convertDimensions()">
CALCULATE DIMENSIONS
</button>

<div class="result" id="result">

Waiting for calculation...

</div>

</div>

</div>

<footer>

<h3>SS DYNAMIC CARGO</h3>

<p>Forwarder Logistics Cargo China To Malaysia</p>

<p>🇨🇳 Warehouse China | 🇲🇾 Delivery Malaysia</p>

</footer>

<script>

function convertDimensions(){

let l = parseFloat(document.getElementById("length").value) || 0;
let w = parseFloat(document.getElementById("width").value) || 0;
let h = parseFloat(document.getElementById("height").value) || 0;
let kg = parseFloat(document.getElementById("weight").value) || 0;

let lengthM = l / 100;
let widthM = w / 100;
let heightM = h / 100;

let lengthMM = l * 10;
let widthMM = w * 10;
let heightMM = h * 10;

let cbm = (l * w * h) / 1000000;

document.getElementById("result").innerHTML =

"<b>DIMENSION RESULTS</b><br><br>" +

"Length: " + l.toFixed(2) + " CM | " +
lengthM.toFixed(3) + " M | " +
lengthMM.toFixed(0) + " MM<br><br>" +

"Width: " + w.toFixed(2) + " CM | " +
widthM.toFixed(3) + " M | " +
widthMM.toFixed(0) + " MM<br><br>" +

"Height: " + h.toFixed(2) + " CM | " +
heightM.toFixed(3) + " M | " +
heightMM.toFixed(0) + " MM<br><br>" +

"Weight: " + kg.toFixed(2) + " KG<br><br>" +

"CBM: " + cbm.toFixed(3) + " m³";

}

</script>

</body>
