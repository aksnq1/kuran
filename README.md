# kuran
Kur’an-ı Kerim Türkçe mealli bilgilendirici web sitesi
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Kur’an-ı Kerim</title>
</head>
<body>
<h1>Kur’an-ı Kerim</h1>
<h2>Örnek Ayetler</h2>
<p>1. Rahmân ve Rahîm olan Allah’ın adıyla.</p>
<p>2. Hamd, âlemlerin Rabbi Allah’a mahsustur.</p>
<p>3. O, Rahmân ve Rahîm’dir, din gününün sahibidir.</p>
<p>4. Yalnız sana ibadet eder ve yalnız senden yardım dileriz.</p>
<p>5. Bizi doğru yola ilet, nimet verdiğin kimselerin yoluna.</p>
</body>
</html>
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Kur’an-ı Kerim</title>
</head>
<body>
<h1>Kur’an-ı Kerim</h1>

<p><b>Fâtiha Suresi</b></p>
<p>1. Rahmân ve Rahîm olan Allah’ın adıyla.</p>
<p>2. Hamd âlemlerin Rabbi Allah’a mahsustur.</p>
<p>3. O, Rahmân ve Rahîm’dir.</p>
<p>4. Din gününün sahibidir.</p>
<p>5. Yalnız Sana ibadet eder, yalnız Senden yardım dileriz.</p>
<p>6. Bizi doğru yola ilet.</p>
<p>7. Nimet verdiklerinin yoluna; gazaba uğrayanların ve sapmışların yoluna değil.</p>

</body>
</html>
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Kur’an-ı Kerim</title>
</head>
<body>
<h1>Kur’an-ı Kerim</h1>

<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Kur’an-ı Kerim</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  font-family: Arial, sans-serif;
  background: #f9f9f9;
  margin: 0;
  padding: 0;
}
header {
  background: #0b5345;
  color: white;
  padding: 15px;
  text-align: center;
}
select {
  width: 90%;
  padding: 10px;
  margin: 15px auto;
  display: block;
  font-size: 16px;
}
.ayet {
  background: white;
  margin: 10px 15px;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.footer {
  text-align: center;
  padding: 10px;
  background: #0b5345;
  color: white;
  font-size: 14px;
}
</style>
</head>
<body>

<header>
  <h2>Kur’an-ı Kerim</h2>
  <p>Sure seçin ve ayetleri görün</p>
</header>

<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<title>Kur’an-ı Kerim</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body {
  font-family: Arial, sans-serif;
  background: #f9f9f9;
  margin: 0;
  padding: 0;
}
header {
  background: #0b5345;
  color: white;
  padding: 15px;
  text-align: center;
}
select {
  width: 90%;
  padding: 10px;
  margin: 15px auto;
  display: block;
  font-size: 16px;
}
.ayet {
  background: white;
  margin: 10px 15px;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.footer {
  text-align: center;
  padding: 10px;
  background: #0b5345;
  color: white;
  font-size: 14px;
}
</style>
</head>
<body>

<header>
  <h2>Kur’an-ı Kerim</h2>
  <p>Sure seçin ve ayetleri görün</p>
</header>

<select id="sureler">
  <option value="">Sure seç...</option>
</select>

<div id="icerik"></div>

<div class="footer">© 2026 | Kur’an-ı Kerim</div>

<script>
// Sure listesini çek
fetch("https://api.alquran.cloud/v1/surah")
.then(res => res.json())
.then(data => {
  let select = document.getElementById("sureler");
  data.data.forEach(sure => {
    let option = document.createElement("option");
    option.value = sure.number;
    option.textContent = sure.number + ". " + sure.englishName + " (" + sure.name + ")";
    select.appendChild(option);
  });
});

// Sure seçilince ayetleri göster
document.getElementById("sureler").addEventListener("change", function() {
  let sureNo = this.value;
  let div = document.getElementById("icerik");
  div.innerHTML = "";

  if (!sureNo) return;

  fetch("https://api.alquran.cloud/v1/surah/" + sureNo + "/tr.diyanet")
  .then(res => res.json())
  .then(data => {
    data.data.ayahs.forEach(a => {
      let ayetDiv = document.createElement("div");
      ayetDiv.className = "ayet";
      ayetDiv.innerHTML =
        "<strong>" + a.numberInSurah + ".</strong> " + a.text;
      div.appendChild(ayetDiv);
    });
  });
});
</script>

</body>
</html> id="sureler">
  <option value="">Sure seç...</option>
</select>

<div id="icerik"></div>

<div class="footer">© 2026 | Kur’an-ı Kerim</div>

<script>
// Sure listesini çek
fetch("https://api.alquran.cloud/v1/surah")
.then(res => res.json())
.then(data => {
  let select = document.getElementById("sureler");
  data.data.forEach(sure => {
    let option = document.createElement("option");
    option.value = sure.number;
    option.textContent = sure.number + ". " + sure.englishName + " (" + sure.name + ")";
    select.appendChild(option);
  });
});

// Sure seçilince ayetleri göster
document.getElementById("sureler").addEventListener("change", function() {
  let sureNo = this.value;
  let div = document.getElementById("icerik");
  div.innerHTML = "";

  if (!sureNo) return;

  fetch("https://api.alquran.cloud/v1/surah/" + sureNo + "/tr.diyanet")
  .then(res => res.json())
  .then(data => {
    data.data.ayahs.forEach(a => {
      let ayetDiv = document.createElement("div");
      ayetDiv.className = "ayet";
      ayetDiv.innerHTML =
        "<strong>" + a.numberInSurah + ".</strong> " +
