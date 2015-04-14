# cURL

## curl_exec($ch)
contoh
```
// inisialisasi cURL 1
$ch = curl_init();
curl_setopt($ch, CURLOPT_USERAGENT, "Mozilla/5.0 (X11; Fedora; Linux x86_64; rv:36.0) Gecko/20100101 Firefox/36.0");
curl_setopt($ch, CURLOPT_URL, $url );
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch,CURLOPT_RETURNTRANSFER,1);
curl_setopt($ch, CURLOPT_FOLLOWLOCATION, 1);
curl_setopt($ch, CURLOPT_POSTFIELDS, 'vc=&userid='.$userid.'&pass='.$password.'&submit=');
curl_setopt($ch, CURLOPT_COOKIEJAR, 'cookies');
curl_setopt($ch, CURLOPT_COOKIEFILE, 'cookies');

// ambil KPJ dan NOHP
curl_setopt($ch, CURLOPT_COOKIEJAR, 'cookies');
curl_setopt($ch, CURLOPT_COOKIEFILE, 'cookies');
curl_setopt($ch,CURLOPT_RETURNTRANSFER,1);
curl_setopt($ch, CURLOPT_FOLLOWLOCATION, 1);
curl_setopt($ch, CURLOPT_URL, 'https://es.bpjsketenagakerjaan.go.id/sso/profil.bpjs');
curl_setopt($ch, CURLOPT_REFERER, 'https://es.bpjsketenagakerjaan.go.id/sso/dashboard.bpjs');

```

kesalahen si usur bas script sidatas e, emekap la inget ngeksekusi scriptna sope lanjutken ku teruhna. fungsi si arusna i pake emekap
```
curl_exec($ch);
```
e makana lanjutken ku script cURL siteruhna, adina lahang asa metua doni enda labo dat datana.

## outputna ndarat
bas piga-piga kasus la ateta si pedarat hasil eksekusi script cURL-ta, tapina lalap ia idah e enggo man tambaren alu
```
curl_setopt($ch,CURLOPT_RETURNTRANSFER,1);
```
fungsi sidatas e lit hubungenna ras curl_exec si bas datas. Arah dokumentasi PHP nari
```
CURLOPT_RETURNTRANSFER 	TRUE to return the transfer as a string of the return value of curl_exec() instead of outputting it out directly.
```

