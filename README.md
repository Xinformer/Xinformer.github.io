# Xinformer.github.io
🧠 "Your digital companion for better writing—clarify your words and organize your thoughts instantly!
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SmartWrite - Smart Writing Assistant</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}

body{
    background:linear-gradient(135deg,#eef3f8,#dfeeff);
    display:flex;
    justify-content:center;
    align-items:center;
    min-height:100vh;
    padding:20px;
}

.container{
    width:100%;
    max-width:900px;
    background:#fff;
    border-radius:18px;
    padding:35px;
    box-shadow:0 15px 40px rgba(0,0,0,0.08);
    text-align:center;
}

h1{
    color:#2f4f6f;
    font-size:2.5rem;
    margin-bottom:10px;
    letter-spacing:1px;
}

.subtitle{
    color:#6b7d90;
    margin-bottom:30px;
    font-size:1.05rem;
}

textarea{
    width:100%;
    min-height:320px;
    padding:20px;
    border:2px solid #d7e5f3;
    border-radius:14px;
    resize:vertical;
    outline:none;
    font-size:1rem;
    line-height:1.7;
    color:#333;
    background:#fbfdff;
    transition:0.3s;
}

textarea:focus{
    border-color:#6da8ff;
    box-shadow:0 0 10px rgba(109,168,255,0.25);
}

.buttons{
    display:flex;
    justify-content:center;
    gap:15px;
    margin-top:25px;
    flex-wrap:wrap;
}

button{
    padding:14px 28px;
    border:none;
    border-radius:10px;
    cursor:pointer;
    font-size:1rem;
    font-weight:600;
    transition:0.3s;
}

.clear-btn{
    background:#eef2f7;
    color:#44576b;
}

.clear-btn:hover{
    background:#dde6ef;
}

.copy-btn{
    background:#5d9df7;
    color:#fff;
}

.copy-btn:hover{
    background:#4b8dea;
}

.footer{
    margin-top:25px;
    color:#8896a5;
    font-size:0.9rem;
}

@media(max-width:600px){

.container{
    padding:22px;
}

h1{
    font-size:2rem;
}

.subtitle{
    font-size:0.95rem;
}

textarea{
    min-height:250px;
}

button{
    width:100%;
}
}
</style>

</head>
<body>

<div class="container">

<h1>SmartWrite</h1>

<p class="subtitle">
Write freely, stay focused, and manage your text effortlessly with a clean writing experience.
</p>

<textarea id="editor" placeholder="Start writing here..."></textarea>

<div class="buttons">
    <button class="clear-btn" onclick="clearText()">Clear Text</button>
    <button class="copy-btn" onclick="copyText()">Copy to Clipboard</button>
</div>

<p class="footer">
Designed for distraction-free writing.
</p>

</div>

<script>
function clearText(){
    document.getElementById("editor").value = "";
}

function copyText(){
    const textArea = document.getElementById("editor");
    textArea.select();
    textArea.setSelectionRange(0,99999);

    navigator.clipboard.writeText(textArea.value)
    .then(()=>{
        alert("Text copied to clipboard!");
    })
    .catch(()=>{
        alert("Unable to copy text.");
    });
}
</script>

</body>
</html>
