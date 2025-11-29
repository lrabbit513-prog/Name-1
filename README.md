<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Print Name Characters</title>
</head>
<body>

<h2>พิมพ์ตัวอักษรตามด้วย !</h2>

<input type="text" id="username" placeholder="กรอกชื่อ">
<button onclick="printWhile()">แสดงผล (while)</button>
<button onclick="printDoWhile()">แสดงผล (do-while)</button>

<p id="result"></p>

<script>
    function printWhile() {
        const name = document.getElementById("username").value;
        let result = "";
        let i = 0;

        while (i < name.length) {
            result += name[i].toUpperCase() + "!<br>";
            i++;
        }

        document.getElementById("result").innerHTML = result;
    }

    function printDoWhile() {
        const name = document.getElementById("username").value;
        let result = "";
        let i = 0;

        if (name.length > 0) {
            do {
                result += name[i].toUpperCase() + "!<br>";
                i++;
            } while (i < name.length);
        }

        document.getElementById("result").innerHTML = result;
    }
</script>

</body>
</html>
