# Shortcut to Size TMA

Telegram Mini App -muotoinen, yhden ruudun treeniloki. Ohjelman harjoitusliikkeiden perusrakenne pohjautuu repoosi [vili-pet/shortcut-to-size](https://github.com/vili-pet/shortcut-to-size). Käyttöliittymässä voi valita päivän treenin, katsoa aiemman painoehdotuksen, syöttää painon ja kuitata sarjan yhdellä napilla. Kirjaukset tallentuvat selaimen localStorageen.

## Kehitys

```sh
npm install
npm run dev
npm run build
```

## Telegram-asennus

Aseta HTTPS-hostattu Mini App URL Telegram BotFatherissa botin Mini App / Web App -asetukseksi ja avaa se botin valikosta tai Mini App -linkillä. Sovellus lataa virallisen `telegram-web-app.js`-skriptin ja kutsuu `Telegram.WebApp.ready()` sekä `expand()`; tavallinen selain toimii ilman Telegram-ympäristöä. Värit noudattavat Telegramin teemaa.

Tämä asiakas ei varmista Telegram-käyttäjän identiteettiä. Älä luota selaimesta tulevaan `initData`-arvoon käyttäjän todentamisessa; validoi initData palvelinpuolella ennen kuin lisäät käyttäjäkohtaisia tai arkaluonteisia backend-toimintoja.

Huom: nykyinen valikkovalinta tarjoaa neljä ohjelman harjoituspäivää ja tämän päivän kierrot. Lokit ovat laitekohtaisia; ei pilvisynkronointia.