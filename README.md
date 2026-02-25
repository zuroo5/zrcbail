<!-- BANNER VIDEO THUMBNAIL --><p align="center">
  <a href="https://files.catbox.moe/6hx5xc.mp4">
    <img src="https://files.catbox.moe/cyxu94.jpg" width="600" alt="Watch Video"/>
  </a>
</p><p align="center">
  <a href="https://files.catbox.moe/6hx5xc.mp4">
    <img src="https://img.shields.io/badge/Watch-Video-red?style=for-the-badge&logo=video"/>
  </a>
</p>---

WhatsApp Baileys Enhanced

<p align="center">
  Professional WhatsApp automation library with full interactive message, video support, and native flow integration.
</p><p align="center"><img src="https://img.shields.io/badge/Node.js-18+-green?style=flat-square&logo=node.js"/>
<img src="https://img.shields.io/badge/Baileys-Latest-blue?style=flat-square"/>
<img src="https://img.shields.io/badge/MultiDevice-Supported-success?style=flat-square"/>
<img src="https://img.shields.io/badge/License-MIT-orange?style=flat-square"/></p>---

Live Preview

Click banner above or link below:

https://files.catbox.moe/6hx5xc.mp4

---

GIF Preview (Recommended for GitHub)

<p align="center">
  <img src="https://yourdomain.com/preview.gif" width="600"/>
</p>Replace with your GIF file:

preview.gif

Put inside repo root.

Example:

repo/
 ├ preview.gif
 └ README.md

---

Features

- Interactive Message Support
- Video Interactive Header
- Native Flow Message
- Multi-Device Support
- Fast & Lightweight
- Stable Connection
- Full Media Support
- Professional Bot Ready

---

Installation
npm install @zuroo5/zrcbail

---

Send Video Example

await sock.sendMessage(jid, {
    video: {
        url: "https://files.catbox.moe/6hx5xc.mp4"
    },
    caption: "Baileys Video Preview"
})

---

Interactive Video Example

const { prepareWAMessageMedia } = require("@whiskeysockets/baileys")

const video = await prepareWAMessageMedia(
{
video: { url: "https://files.catbox.moe/6hx5xc.mp4" }
},
{
upload: sock.waUploadToServer
}
)

await sock.sendMessage(jid, {

interactiveMessage: {

header: {
videoMessage: video.videoMessage,
hasMediaAttachment: true
},

title: "Baileys Interactive Video",
body: "Professional WhatsApp Bot",
footer: "Baileys Library",

nativeFlowMessage: {
buttons: [
{
name: "cta_url",
buttonParamsJson: JSON.stringify({
display_text: "Watch Video",
url: "https://files.catbox.moe/6hx5xc.mp4"
})
}
]
}

}

})

---

Supported

Feature| Status
Text| ✅
Image| ✅
Video| ✅
Audio| ✅
Document| ✅
Interactive| ✅
Native Flow| ✅
Product Message| ✅
Event Message| ✅

---

Advantages

- High Performance
- Stable Pairing
- Professional Use Ready
- Full Control
- Modern WhatsApp Features

---

Support

If you like this project:

Give a Star 

---

License

MIT License
