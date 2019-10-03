# HTML
```
https://www.w3schools.com/
https://www.w3school.com.cn/

```

## html_1.html
```
https://www.w3schools.com/html/html_colors.asp
```
```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
	<title>我的第一份HTML5文件</title>
  </head>	
  <body>
    <h1> Hello! HTML5! </h1>
    <h2>Hello! Mydear!</h2>
    <h3>Hello! Teacher!</h3>
  </body>
</html>
```
```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
	<title> 龍大大的第一份HTML5文件</title>
  </head>	
  <body>
	<h1 style="background-color:Tomato;">Hello! 龍大大! </h1>
    <h2>Hello! Mydear!</h2>
    <h3>Hello! Teacher!</h3>
  </body>
</html>
```

標籤及其屬性:In HTML, a color can be specified by using a color name

## 超連結 html_2.html
```
https://www.w3schools.com/html/html_links.asp
```
```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
	<title> 龍大大的第一份HTML5文件</title>
  </head>	
  <body>
	<h1 style="background-color:Tomato;">Hello! 龍大大! </h1>
    <h2>Hello! Mydear!</h2>
    <h3>Hello! Teacher!</h3>
	
	<h2>HTML Links</h2>
<p><a href="https://www.w3schools.com/html/">造訪 HTML tutorial</a></p>
<p><a href="https://www.google.com">來去 Google</a></p>
  </body>
</html>
```
```
HTML標籤+屬性
<p>
<a>
```


## 鑲入圖片===>使用<img>標籤

```
https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_trulli
```

~~~
<!DOCTYPE html>
<html>
<body>

<h2>HTML Image</h2>
<img src="pic_trulli.jpg" alt="Trulli" width="500" height="333">

</body>
</html>

~~~
# 加分題:設計個人網頁
```
參考資料:https://www.balsnctf.com/index.html#tw

```

```

<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset='utf-8'>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="assets/css/style.css">
	  <link rel="icon" type="image/x-icon" sizes="16x16 24x24 32x32 48x48 64x64 96x96 128x128 256x256" href="assets/images/favicon.ico">
    <script src="assets/js/jquery-3.4.1.min.js"></script>
    <script src="assets/js/jquery.countdownTimer.js"></script>
    <title>Balsn | a CTF team from Network Security Lab of National Taiwan University</title>
  </head>
  <body>
    <header>
      <div class="container">
        <div class="btns">
          <h1>Balsn CTF 2019</h1>
          <section id="downloads">
              <a href="#en" class="btn" onclick="$('#main_content_tw').hide();$('#main_content_en').show();">English</a>
              <a href="#tw" class="btn" onfocus="$('#main_content_tw').show();$('#main_content_en').hide();">繁體中文</a>
          </section>
        </div>
      </div>
    </header>

    <div class="container">
      <section id="main_content">
        <section id="main_content_en">
<p><a href="https://balsn.tw/">Balsn</a> will hold our first CTF event <strong>Balsn CTF</strong> in October 2019.</p>

<p>The champions will pre-qualify directly for HITCON CTF Finals in December (Onsite in Taipei, Taiwan).</p>

<p>Registration will be available on 9/28, (UTC+8) 2019.</p>

<ul>
  <li>Date: 10/5 10:00 a.m. (UTC+8) ~ 10/7 10:00 a.m. (UTC+8)</li>
  <li>Format: Online Jeopardy</li>
  <li><a href="https://ctftime.org/event/811">CTFtime link</a></li>
  <li>Prize:
    <ul>
      <li>1st place: $25,000 TWD + pre-qualify for HITCON CTF Finals</li>
      <li>2nd place: $15,000 TWD</li>
      <li>3rd place: $10,000 TWD</li>
      <li>Balsn CTF Taiwan Star (1st domestic team): $ 10,000 TWD</li>
    </ul>
  </li>
</ul>
<p>The prize will be proceed in BTC or ETH.</p>
        </section>
        <section id="main_content_tw">
<p>Hi ! 我們是目前 CTFtime 排名世界第一的 <a href="https://balsn.tw/">Balsn</a> 戰隊，我們將會在 10 月初<br>
舉辦 Balsn CTF 搶旗競賽，本場比賽的冠軍，將可直接獲得 HITCON CTF 決賽資格。<br>
<br>
我們誠摯歡迎各位一起來參加這場比賽！比賽將於 9/28 (六) 之後開放註冊。</br>
</p>
<ul>
  <li>時間: 10/5 早上 10:00 (UTC+8) ~ 10/7 早上 10:00 (UTC+8)</li>
  <li>比賽型態：線上解題</li>
  <li>CTFtime 連結: <a href="https://ctftime.org/event/811">Link</a></li>
  <li>獎金:
    <ul>
      <li>冠軍：$25,000 新台幣 + 保送 HITCON CTF 決賽</li>
      <li>亞軍：$15,000 新台幣</li>
      <li>季軍: $10,000 TWD</li>
      <li>Balsn CTF 台灣之星(國內第一名)：$ 10,000 新台幣</li>
    </ul>
  </li>
</ul>
<p> 獎金將會使用比特幣或以太幣的方式發送。<br>
</p>
        </section>
      </section>
    </div>
    <div id="countdown">
      <p>CTF will start in </p>
      <div id="countdowntimer">
        <span class="future_date"></span>  
      </div>
    </div>
  </body>
  <script>
  $('.future_date').countdowntimer({
    dateAndTime : new Date("2019/10/05 10:00:00 GMT+0800"),
  });
  let lang = window.location.hash.substring(1);
  let showEn = () => {
    $('#main_content_tw').hide();
    $('#main_content_en').show();
  };
  let showTw = () => {
    $('#main_content_en').hide();
    $('#main_content_tw').show();
  };
  if (lang === 'en') {
    showEn();
  } else if (lang === 'tw') {
    showTw();
  } else {
    if (navigator.language.toLowerCase().includes('zh'))
      showTw();
    else
      showEn();
  }
  </script>
</html>


```
