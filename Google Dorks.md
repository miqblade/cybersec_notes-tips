Google Dorks

usefull resource - https://www.exploit-db.com/google-hacking-database

# Basic operators

| Оператор |                 example  | Призначення (EN / UA)                  |
| -------- | -----------------------: | -------------------------------------- |
| `""`     |          `"admin login"` | Exact phrase / Точна фраза             |  
| `OR` / ` |                        ` | `login OR signin`                      | 
| `-`      | `site:example.com -blog` | Exclude term / Виключити слово         | 
| `*`      |      `"file * download"` | Wildcard (any word) / Знак підстановки |


# Site, URL, title

| Оператор      |                      example | Purpose (EN / UA)                                 |
| ------------- | ---------------------------: | ------------------------------------------------- |
| `site:`       |                `site:gov.uk` | Search only that domain / Шукати тільки на домені |
| `inurl:`      |                `inurl:admin` | Word in URL / Слово в URL                         |
| `allinurl:`   |         `allinurl:login php` | All words in URL / Усі слова в URL                |
| `intitle:`    |         `intitle:"index of"` | Word in page title / Слово в заголовку сторінки   |
| `allintitle:` | `allintitle:dashboard login` | All words in title / Усі слова в заголовку        |


# File search

| Оператор     |                       example | Purpose (EN / UA)                           |
| ------------ | ----------------------------: | ------------------------------------------- |
| `filetype:`  |  `filetype:pdf cybersecurity` | Find file types / Шукома розширення файлу   |
| `ext:`       |           `ext:docx password` | Same as filetype / Те ж, що filetype        |
| `intext:`    |       `intext:"confidential"` | Word in page text / Слово в тексті сторінки |
| `allintext:` | `allintext:"vpn credentials"` | All words in text / Усі слова в тексті      |
