# 📱 Modified Baileys WhatsApp Library

Library ini adalah hasil modifikasi dari [Baileys](https://github.com/WhiskeySockets/Baileys), sebuah Web API untuk WhatsApp.  
Modifikasi ini difokuskan agar lebih **stabil**, **ringan**, dan **mendukung fitur terbaru WhatsApp Business**.

---

## ✨ Fitur Utama
- 🔑 **Custom Pairing Code** – Mendukung koneksi dengan kode pairing yang bisa dikustomisasi.  
- 🔗 **Koneksi Stabil** – Optimasi agar koneksi tidak mudah terputus.  
- 💬 **Support Interactive Message** – Sudah mendukung `interactiveMessage` untuk WhatsApp Business.  
- ⚡ **Ringan & Efisien** – Lebih hemat resource sehingga cocok untuk proyek skala kecil maupun besar.  

--- 

## Usage
```json
"depencies": {
  "@whiskeysockets/baileys": "github:TeddyHost-WaBaileys"
}
```
## Import
```javascript
const {
  default:makeWASocket,
  // Other Options 
} = require('@whiskeysockets/baileys');
```

---
# How To Connect To Whatsapp
## With QR Code
```javascript
const {
  default: makeWASocket
} = require('@whiskeysockets/baileys');

const client = makeWASocket({
  browser: ['Ubuntu', 'Chrome', '20.00.1'],
  printQRInTerminal: true
})
```

## Connect With Number
```javascript
const {
  default: makeWASocket
} = require('@whiskeysockets/baileys');

const client = makeWASocket({
  browser: ['Ubuntu', 'Chrome', '20.00.1'],
  printQRInTerminal: true,
  // Other options
});

const number = "628XXXXX";
const code = await client.requestPairingCode(number.trim) /* Use : (number, "YYYYYYYY") for custom-pairing */

console.log("Ur pairing code : " + code)
```
