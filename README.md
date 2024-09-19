# loding-page
<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
    </head>
    <body>
        
        <!--  Coded by: Aashush raaz-->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css">
<style>
@import url(https://fonts.googleapis.com/css?family=Roboto:400,900italic,900,700italic,700,500italic,500,400italic,300italic,300,100italic,100);
* {
  box-sizing: border-box;
  margin: 0;
}

h1, p, h2, h3, h4, ul, li, div {
  margin: 0;
  padding: 0;
}

body {
  padding: 0;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  display: -webkit-box;
  display: flex;
  font-family: Roboto;
}

.loading-page {
  background: #0d0d0d;
  width: 100vw;
  height: 100vh;
  display: -webkit-box;
  display: flex;
  -webkit-box-pack: center;
          justify-content: center;
  -webkit-box-align: center;
          align-items: center;
}
.loading-page .counter {
  text-align: center;
}
.loading-page .counter p {
  font-size: 40px;
  font-weight: 100;
  color: #f60d54;
}
.loading-page .counter h1 {
  color: white;
  font-size: 60px;
  margin-top: -10px;
}
.loading-page .counter hr {
  background: #f60d54;
  border: none;
  height: 1px;
}
.loading-page .counter {
  position: relative;
  width: 200px;
}
.loading-page .counter h1.abs {
  position: absolute;
  top: 0;
  width: 100%;
}
.loading-page .counter .color {
  width: 0px;
  overflow: hidden;
  color: #f60d54;
}
</style>
<div class="loading-page">
<div class="counter">
<p>loading</p>
<h1>0%

</h1>
<hr />
</div>
</div>
<script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.2/jquery.min.js'></script>
<script>
$(document).ready(function () {

  var counter = 0;
  var c = 0;
  var i = setInterval(function () {
    $(".loading-page .counter h1").html(c + "%");
    $(".loading-page .counter hr").css("width", c + "%");
    //$(".loading-page .counter").css("background", "linear-gradient(to right, #f60d54 "+ c + "%,#0d0d0d "+ c + "%)");

    /*
    $(".loading-page .counter h1.color").css("width", c + "%");
    */
    counter++;
    c++;

    if (counter == 101) {
      clearInterval(i);
    }
  }, 50);
});
</script>
    </body>
</html>
