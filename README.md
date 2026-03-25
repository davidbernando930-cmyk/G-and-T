# G-and-T
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Gubuk Togel</title>
    <style>
        body {
            font-family: monospace;
            background: black;
            color: #00ff00;
            text-align: center;
        }
        h1 {
            color: gold;
        }
        .container {
            margin-top: 50px;
        }
        button {
            padding: 12px 20px;
            margin: 10px;
            font-size: 14px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            background: #111;
            color: #0f0;
            border: 1px solid #0f0;
        }
        input {
            padding: 10px;
            margin-top: 20px;
            border-radius: 5px;
            border: none;
        }
        #formArea {
            display: none;
        }
        #loadingScreen {
            display: none;
            margin-top: 20px;
            text-align: left;
            width: 80%;
            margin-left: auto;
            margin-right: auto;
            border: 1px solid #0f0;
            padding: 15px;
            height: 200px;
            overflow-y: auto;
        }
    </style>
</head>
<body>

<h1>GUBUK TOGEL</h1>

<div class="container">
    <p>Pilih MOD:</p>

    <button onclick="pilihMod('Free Spin')">Free Spin</button>
    <button onclick="pilihMod('Auto Win')">Auto Win</button>
    <button onclick="pilihMod('*500 Bet')">*500 Bet</button>

    <div id="formArea">
        <p id="selectedMod"></p>
        <input type="text" id="username" placeholder="Masukkan Username">
        <br>
        <button onclick="startHack()">START</button>
    </div>

    <div id="loadingScreen"></div>
</div>

<script>
let modDipilih = "";

function pilihMod(mod) {
    modDipilih = mod;
    document.getElementById("formArea").style.display = "block";
    document.getElementById("selectedMod").innerText = "MOD: " + mod;
}

function startHack() {
    let user = document.getElementById("username").value;

    if(user === "") {
        alert("Masukkan username!");
        return;
    }

    document.getElementById("formArea").style.display = "none";
    let screen = document.getElementById("loadingScreen");
    screen.style.display = "block";

    let logs = [
        "Menghubungkan ke server...",
        "Mencari database akun...",
        "Bypass keamanan...",
        "Inject script " + modDipilih + "...",
        "Memverifikasi username: " + user,
        "Mengakses sistem...",
        "Menjalankan exploit...",
        "Sukses! Sedang menyelesaikan..."
    ];

    let i = 0;

    function ketik() {
        if(i < logs.length) {
            screen.innerHTML += logs[i] + "<br>";
            screen.scrollTop = screen.scrollHeight;
            i++;
            setTimeout(ketik, 1000);
        } else {
            screen.innerHTML += "<br>✔ SELESAI! MOD AKTIF!";
        }
    }

    ketik();
}
</script>

</body>
</html>
