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

```javascript
await sock.newsletterId(url)
```

### Check banned number
You can see the status of blocked numbers here 

```javascript
await sock.checkWhatsApp(jid)
```

---

## SendMessage Documentation

### Status Group Message V2
Send group status with version 2 

```javascript
await sock.sendMessage(jid, {
     groupStatusMessage: {
          text: "Hello World"
     }
});
```

### Album Message (Multiple Images)
Send multiple images in a single album message:

```javascript
await sock.sendMessage(jid, { 
    albumMessage: [
        { image: cihuy, caption: "Foto pertama" },
        { image: { url: "URL IMAGE" }, caption: "Foto kedua" }
    ] 
}, { quoted: m });
```

### Event Message
Create and send WhatsApp event invitations:

```javascript
await sock.sendMessage(jid, { 
    eventMessage: { 
        isCanceled: false, 
        name: "Hello World", 
        description: "Vld_TheKingsZuro", 
        location: { 
            degreesLatitude: 0, 
            degreesLongitude: 0, 
            name: "rowrrrr" 
        }, 
        joinLink: "https://call.whatsapp.com/video/yumevtc", 
        startTime: "1763019000", 
        endTime: "1763026200", 
        extraGuestsAllowed: false 
    } 
}, { quoted: m });
```

### Poll Result Message
Display poll results with vote counts:

```javascript
await sock.sendMessage(jid, { 
    pollResultMessage: { 
        name: "Hello World", 
        pollVotes: [
            {
                optionName: "TEST 1",
                optionVoteCount: "112233"
            },
            {
                optionName: "TEST 2",
                optionVoteCount: "1"
            }
        ] 
    } 
}, { quoted: m });
```

### Simple Interactive Message
Send basic interactive messages with copy button functionality:

```javascript
await sock.sendMessage(jid, {
    interactiveMessage: {
        header: "Hello World",
        title: "Hello World",
        footer: "telegram: @Vld_TheKingsZuro ",
        buttons: [
            {
                name: "cta_copy",
                buttonParamsJson: JSON.stringify({
                    display_text: "copy code",
                    id: "123456789",              
                    copy_code: "ABC123XYZ"
                })
            }
        ]
    }
}, { quoted: m });
```

### Interactive Message with Native Flow
Send interactive messages with buttons, copy actions, and native flow features:

```javascript
await sock.sendMessage(jid, {    
    interactiveMessage: {      
        header: "Hello World",
        title: "Hello World",      
        footer: "telegram: @Vld_TheKingsZuro",      
        image: { url: "https://files.catbox.moe/cyxu94.jpg" },      
        nativeFlowMessage: {        
            messageParamsJson: JSON.stringify({          
                limited_time_offer: {            
                    text: "idk hummmm?",            
                    url: "https://t.me/Vld_TheKingsZuro",            
                    copy_code: "RΞGΔL",            
                    expiration_time: Date.now() * 999          
                },          
                bottom_sheet: {            
                    in_thread_buttons_limit: 2,            
                    divider_indices: [1, 2, 3, 4, 5, 999],            
                    list_title: "RΞGΔL ΞMPIRE",            
                    button_title: "RΞGΔL ΞMPIRE"          
                },          
                tap_target_configuration: {            
                    title: " X ",            
                    description: "bomboclard",            
                    canonical_url: "https://t.me/Vld_TheKingsZuro",            
                    domain: "shop.example.com",            
                    button_index: 0          
                }        
            }),        
            buttons: [          
                {            
                    name: "single_select",            
                    buttonParamsJson: JSON.stringify({              
                        has_multiple_buttons: true            
                    })          
                },          
                {            
                    name: "call_permission_request",            
                    buttonParamsJson: JSON.stringify({              
                        has_multiple_buttons: true            
                    })          
                },          
                {            
                    name: "single_select",            
                    buttonParamsJson: JSON.stringify({              
                        title: "Hello World",              
                        sections: [                
                            {                  
                                title: "APALAH KIMAK",                  
                                highlight_label: "label",                  
                                rows: [                    
                                    {                      
                                        title: "@Vld_TheKingsZuro",                      
                                        description: "love you",                      
                                        id: "row_2"                    
                                    }                  
                                ]                
                            }              
                        ],              
                        has_multiple_buttons: true            
                    })          
                },          
                {            
                    name: "cta_copy",            
                    buttonParamsJson: JSON.stringify({              
                        display_text: "copy code",              
                        id: "123456789",              
                        copy_code: "ABC123XYZ"            
                    })          
                }        
            ]      
        }    
    }  
}, { quoted: m });
```

### Interactive Message with Thumbnail
Send interactive messages with thumbnail image and copy button:

```javascript
await sock.sendMessage(jid, {
    interactiveMessage: {
        header: "Hello World",
        title: "Hello World",
        footer: "telegram: @Vld_TheKingsZuro",
        image: { url: "https://example.com/image.jpg" },
        buttons: [
            {
                name: "cta_copy",
                buttonParamsJson: JSON.stringify({
                    display_text: "copy code",
                    id: "123456789",
                    copy_code: "ABC123XYZ"
                })
            }
        ]
    }
}, { quoted: m });
```

### Product Message
Send product catalog messages with buttons and merchant information:

```javascript
await sock.sendMessage(jid, {
    productMessage: {
        title: "Produk Contoh",
        description: "Ini adalah deskripsi produk",
        thumbnail: { url: "https://example.com/image.jpg" },
        productId: "PROD001",
        retailerId: "RETAIL001",
        url: "https://example.com/product",
        body: "Detail produk",
        footer: "Harga spesial",
        priceAmount1000: 50000,
        currencyCode: "USD",
        buttons: [
            {
                name: "cta_url",
                buttonParamsJson: JSON.stringify({
                    display_text: "Beli Sekarang",
                    url: "https://example.com/buy"
                })
            }
        ]
    }
}, { quoted: m });
```

### Interactive Message with Document Buffer
Send interactive messages with document from buffer (file system) - **Note: Documents only support buffer**:

```javascript
await sock.sendMessage(jid, {
    interactiveMessage: {
        header: "Hello World",
        title: "Hello World",
        footer: "telegram: @Vld_TheKingsZuro",
        document: fs.readFileSync("./package.json"),
        mimetype: "application/pdf",
        fileName: "RΞGΔL.pdf",
        jpegThumbnail: fs.readFileSync("./document.jpeg"),
        contextInfo: {
            mentionedJid: [jid],
            forwardingScore: 777,
            isForwarded: false
        },
        externalAdReply: {
            title: "RΞGΔL ΞMPIRE BOT",
            body: "anu team",
            mediaType: 3,
            thumbnailUrl: "https://example.com/image.jpg",
            mediaUrl: " X ",
            sourceUrl: "https://t.me/Vld_TheKingsZuro",
            showAdAttribution: true,
            renderLargerThumbnail: false         
        },
        buttons: [
            {
                name: "cta_url",
                buttonParamsJson: JSON.stringify({
                    display_text: "Telegram",
                    url: "https://t.me/Vld_TheKingsZuro",
                    merchant_url: "https://t.me/yumevtc"
                })
            }
        ]
    }
}, { quoted: m });
```

### Interactive Message with Document Buffer (Simple)
Send interactive messages with document from buffer (file system) without contextInfo and externalAdReply - **Note: Documents only support buffer**:

```javascript
await sock.sendMessage(jid, {
    interactiveMessage: {
        header: "Hello World",
        title: "Hello World",
        footer: "telegram: @Vld_TheKingsZuro",
        document: fs.readFileSync("./package.json"),
        mimetype: "application/pdf",
        fileName: "RΞGΔL.pdf",
        jpegThumbnail: fs.readFileSync("./document.jpeg"),
        buttons: [
            {
                name: "cta_url",
                buttonParamsJson: JSON.stringify({
                    display_text: "Telegram",
                    url: "https://t.me/Vld_TheKingsZuro",
                    merchant_url: "https://t.me/Vld_TheKingsZuro"
                })
            }
        ]
    }
}, { quoted: m });
```

### Request Payment Message
Send payment request messages with custom background and sticker:

```javascript
let quotedType = m.quoted?.mtype || '';
let quotedContent = JSON.stringify({ [quotedType]: m.quoted }, null, 2);

await sock.sendMessage(jid, {
    requestPaymentMessage: {
        currency: "IDR",
        amount: 10000000,
        from: m.sender,
        sticker: JSON.parse(quotedContent),
        background: {
            id: "100",
            fileLength: "0",
            width: 1000,
            height: 1000,
            mimetype: "image/webp",
            placeholderArgb: 0xFF00FFFF,
            textArgb: 0xFFFFFFFF,     
            subtextArgb: 0xFFAA00FF   
        }
    }
}, { quoted: m });
```


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
