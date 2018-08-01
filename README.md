# seisan-2
 <html lang="ja">
 <head>
 <meta charset="UTF-8">
 <title>まほろば_2017</title>

<style type="text/css">
 p {
color: #0d0015;
font-size: 1.5em;
 }

body { background-color: #6699ff; }


</style>
<link rel="stylesheet" href="../style.css/" type="text/css">

</head>


<body>



  <section>
 <h2>簡易表計算-JavaScriptバージョンアップ版_2</h2>
  <script>
    var selects = prompt('参加人数を入力！');

    var name = [];

    for (var i=0; i<selects; i++){

      name[i] = prompt("名前を入力");

    }   

    var menu = [];    

    for (var i=0; i<selects; i++){

      menu[i] = prompt("支払金額を入力");

    } 

     document.write("支払金額は<br>")

    for (var i=0; i<menu.length; i++){

      document.write(name[i] + "さん：" + menu[i] + "円 <br>")

    }

//各自の会計額を計算

    var kasan = [];

      kasan[0] = menu[0];

    for (var i=0; i<selects-1; i++){

kasan[i+1] = Math.round (Number(kasan[i]) + Number(menu[i+1]));

      }

//各自の分担分を計算

var buntan = Math.round (Number(kasan[selects-1])/Number(selects))

//各自の割り勘分を計算

    var wari = [];

    for (var i=0; i<selects; i++){

    wari[i] = Math.round (Number(buntan) - Number(menu[i]));

      }

document.write("<br>支払金の総額：" + kasan[selects-1] + "円<br>")

document.write("一人当たりの分担：" + buntan + "円<br>")

document.write("<br>清算金額は<br>")

    for (var i=0; i<menu.length; i++){

      document.write(name[i] + "さん：" + wari[i] + "円 <br>")

    }

</script>
 </section>

</body>
</html>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<!-- フッタ -->
 <footer>
 Copyright 2018/08/01 S.Hada
 </footer>
