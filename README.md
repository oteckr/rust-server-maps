# ЇРЖА — карти Rust

Публічне сховище посилань на карти сервера ЇРЖА. GitHub-власник: **oteckr**, проєкт MED.
Кожна карта має розмір світу **5000**. Файли розміщені у вкладеннях релізу, а не в Git/LFS.

## Перші три тижні

Реліз: [first-3-weeks-v1](https://github.com/oteckr/rust-server-maps/releases/tag/first-3-weeks-v1).

| Тиждень | Дата | Карта | Завантаження | Байтів |
|---|---|---|---|---:|
| 1 | 2026-11-02 | Atlas | [irzha-atlas-5000-v1.map](https://github.com/oteckr/rust-server-maps/releases/download/first-3-weeks-v1/irzha-atlas-5000-v1.map) | 60675325 |
| 2 | 2026-11-09 | Vital | [irzha-vital-5000-v1.map](https://github.com/oteckr/rust-server-maps/releases/download/first-3-weeks-v1/irzha-vital-5000-v1.map) | 64640420 |
| 3 | 2026-11-16 | Mirage | [irzha-mirage-5000-v1.map](https://github.com/oteckr/rust-server-maps/releases/download/first-3-weeks-v1/irzha-mirage-5000-v1.map) | 63839583 |

## Контрольні суми SHA256

[SHA256SUMS.txt](https://github.com/oteckr/rust-server-maps/releases/download/first-3-weeks-v1/SHA256SUMS.txt).

```text
a17cc2b9e68ac50226f9ac3e627f99fb7ab6095963fef7f3dd3873fa7a4632d6  irzha-atlas-5000-v1.map
ccf4a7f2c038001303a7f4c94acf258d921997860e025add9667bdc6d7a79bef  irzha-vital-5000-v1.map
f40d40cbed157bcebda8a20aefcf46137a6845fcd88305bd3f86f0dcf2e3852b  irzha-mirage-5000-v1.map
```

## Джерела та авторство

- **Atlas**: [https://maps.rustmaps.com/289/1d8fb71b372a448eab84a99363e9a6b9/3Ge-fVDDi0eP9YkAG09QHg/AtlasEu2xLargeReWipe22102026V2V_SY1Ci.map](https://maps.rustmaps.com/289/1d8fb71b372a448eab84a99363e9a6b9/3Ge-fVDDi0eP9YkAG09QHg/AtlasEu2xLargeReWipe22102026V2V_SY1Ci.map)
- **Vital**: [https://maps.vgn.gg/maps/2c705066/20261029T033005Z-ccf4a7f2-vitalrust.2x.monthly.eu.w55.v1.map](https://maps.vgn.gg/maps/2c705066/20261029T033005Z-ccf4a7f2-vitalrust.2x.monthly.eu.w55.v1.map)
- **Mirage**: [https://maps.rustmaps.com/289/bba7a33ce1ce4b5e8973797c96dcfb06/oZMfm71RqU6udGzJqdjUXA/procedural__5000_A6_qzsfp_06nIk4IOiRKmQ.spot.map](https://maps.rustmaps.com/289/bba7a33ce1ce4b5e8973797c96dcfb06/oZMfm71RqU6udGzJqdjUXA/procedural__5000_A6_qzsfp_06nIk4IOiRKmQ.spot.map)

Авторство карт належить їхнім відповідним творцям. MED та власник цього
репозиторію не заявляють авторства цих карт. Файли скопійовано без редагування;
змінено лише назви. Права на карти залишаються у їхніх творців.

## Порядок використання

1. На тиждень від 2 листопада 2026 року використовуйте Atlas, від 9 листопада — Vital,
   від 16 листопада — Mirage. Усі дати наведені за календарем Києва.
2. Візьміть пряму HTTPS-адресу відповідного `.map` із таблиці.
3. Вкажіть одну вибрану адресу в параметрі запуску Rust `+server.levelurl "URL"`.
   Параметри генерації процедурної карти `+server.seed` і `+server.worldsize`
   для такого запуску потрібно прибрати. Сервер та гравці завантажують карту
   за публічною адресою. Див. [офіційну інструкцію Facepunch](https://wiki.facepunch.com/rust/Hosting_a_custom_map).
4. Для ручного завантаження гравцями використовуйте ті самі посилання.
5. Перевірте розмір і SHA256 за таблицею та `SHA256SUMS.txt`, наприклад у PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath '.\irzha-atlas-5000-v1.map'
(Get-Item -LiteralPath '.\irzha-atlas-5000-v1.map').Length
```

## Незмінність посилань

Для цього набору використовується фіксований тег `first-3-weeks-v1`; URL не містять
токенів або параметрів запиту. Після публікації вміст цих файлів під цими адресами
не замінюється. Інші редакції слід публікувати під новими тегами та назвами.

Цей репозиторій стосується лише зберігання та розповсюдження файлів.
Публікація не змінює налаштувань серверів Rust.
