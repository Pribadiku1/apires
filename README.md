
<h1 align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&duration=4000&pause=1000&center=true&vCenter=true&width=435&lines=🚀+Private+API+Result+v1;💎+Powered+by+YanzHost+%E2%9A%A1" alt="Typing SVG" />
</h1>

<p align="center">
  <i>Versi privat, ringan, dan aman untuk menampilkan result berbasis PHP</i><br>
  <b>Status: 🔒 Private Access Only</b>
</p>

---

## 🔐 Tentang Project

**Private API Result v1** adalah sistem backend berbasis **PHP** yang dirancang secara eksklusif untuk:

- ⚙️ Autores / Auto-Responder Script
- 💎 Tools Premium / VIP Access Only
- 🧾 Menampilkan result akun secara real-time
- 🔍 Menampilkan data **100% real look / asli**

📦 API ini membaca data langsung dari file PHP (`file1.php`, `file2.php`) dan bisa diintegrasikan ke berbagai **bot, tools, atau panel web internal** — tanpa database.

---

## ⚙️ Cara Kerja

> Tanpa database, tanpa ribet.  
> **Edit file PHP, upload, dan tampilkan!**

### 📂 File Utama

- 📄 **Data Akun (Raw)**  
  ```
  https://raw.githubusercontent.com/Pribadiku1/apires/main/file1.php
  ```

- 👥 **Data Operator (Raw)**  
  ```
  https://raw.githubusercontent.com/Pribadiku1/apires/main/file2.php
  ```

---

## 🧪 Contoh Penggunaan (PHP + cURL)

```php
function ambilIsiFileViaCurl($url) {
    if (!filter_var($url, FILTER_VALIDATE_URL)) {
        return "❌ URL tidak valid: $url";
    }

    $ch = curl_init($url);
    curl_setopt_array($ch, [
        CURLOPT_RETURNTRANSFER => true,
        CURLOPT_FOLLOWLOCATION => true,
        CURLOPT_TIMEOUT => 10,
        CURLOPT_CONNECTTIMEOUT => 5,
        CURLOPT_SSL_VERIFYPEER => false,
        CURLOPT_USERAGENT => 'Mozilla/5.0 (Curl Request by Yanzxz)'
    ]);

    $response = curl_exec($ch);
    $httpCode = curl_getinfo($ch, CURLINFO_HTTP_CODE);

    if (curl_errno($ch)) {
        $error = curl_error($ch);
        curl_close($ch);
        return "❌ cURL error: $error";
    }

    curl_close($ch);

    if ($httpCode !== 200) {
        return "❌ Gagal mengambil file. HTTP Status: $httpCode";
    }

    return $response;
}

// Contoh penggunaan:
$isiAkun = ambilIsiFileViaCurl('https://raw.githubusercontent.com/Pribadiku1/apires/main/file1.php');
$isiOperator = ambilIsiFileViaCurl('https://raw.githubusercontent.com/Pribadiku1/apires/main/file2.php');
```


---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:6A5ACD,100:00BFFF&height=200&section=footer&text=Thanks%20for%20Using%20Private%20API%20🚀&fontSize=22&fontAlign=50&fontColor=ffffff" alt="footer animation"/>
</p>

<p align="center" style="font-family: 'Fira Code', monospace; font-size: 16px;">
  🔐 Built with precision by <strong>Yanz Host</strong> — <em>Stay elite, stay encrypted.</em><br>
  <img src="https://img.shields.io/badge/API-PRIVATE-blueviolet?style=flat-square&logo=php" alt="Private API Badge"/>
  <img src="https://img.shields.io/badge/Status-LOCKED-red?style=flat-square&logo=protonmail" alt="Locked Badge"/>
  <img src="https://img.shields.io/badge/Maintainer-Pribadiku1-blue?style=flat-square&logo=github" alt="Maintainer Badge"/>
</p>
