# 🤘 YouTube Likes Cleaner

**DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE**

A one-liner script to automatically remove **all liked videos** from your YouTube playlist using the browser console.

Однострочный скрипт для автоматического удаления **всех понравившихся видео** на YouTube через консоль браузера.

---

## 🌐 Page / Страница

**Use only on / Использовать только на:**
```
https://www.youtube.com/playlist?list=LL
```

---

## 🚀 How to Use / Как использовать

1. **Open your Liked Videos playlist**  
   **Открой плейлист "Понравившиеся"**

2. **Press F12 or Ctrl+Shift+I** to open Developer Tools  
   **Нажми F12 или Ctrl+Shift+I** для открытия инструментов разработчика

3. **Go to the Console tab**  
   **Перейди на вкладку Console**

4. **Paste the script below** (1st then 2nd after loading videos) and press Enter  
   **Вставь скрипт ниже** (1й, после загрузки видео 2й) и нажми Enter

---

## 📜 One-liner Script / Скрипт в одну строку

### 1️⃣ Load up to 500 videos / Загрузить по 500 видео
```javascript
(async()=>{let h=0;while(h!==document.documentElement.scrollHeight){h=document.documentElement.scrollHeight;window.scrollTo(0,h);await new Promise(r=>setTimeout(r,500));}console.log('✅ Готово');})();
```

### 2️⃣ Delete all likes / Удалить все лайки
```javascript
(async()=>{let v=document.querySelectorAll('ytd-playlist-video-renderer'),t=v.length,r=0,s=Date.now();for(let i=0;i<t;i++){try{v[i].querySelector('button[aria-label="Меню действий"]')?.click();await new Promise(r=>setTimeout(r,5));document.querySelectorAll('ytd-menu-service-item-renderer').forEach(n=>{if(n.innerText.includes('удалить')||n.innerText.includes('понравившихся')){n.click();r++;if(r%50===0)console.log(`🔥 ${r}/${t} (${Math.round(r/t*100)}%)`);}});}catch(e){}}console.log(`✅ Готово! Удалено ${r}/${t} за ${((Date.now()-s)/1e3).toFixed(0)}с`);})();
```
---

## ⚡ Performance / Производительность

| Videos / Видео | Time / Время |
|----------------|--------------|
| 1,000 | ~8-10 seconds |
| 5,000 | ~45-50 seconds |
| 10,000 | ~1.5 minutes |

---

## ⚠️ Notes / Примечания

- Script works **only** on `youtube.com/playlist?list=LL`
- Disable ad blockers and download extensions for best performance
- You can stop anytime by refreshing the page (F5)
- Tested in Chrome, Firefox, Edge, Opera

- Скрипт работает **только** на `youtube.com/playlist?list=LL`
- Отключите блокировщики рекламы и расширения на скачку видео - они вызывают ошибки кода
- Остановить скрипт обновлением страницы (F5)
- Протестировано на Chrome, Firefox, Edge, Opera

---

## 🏴‍☠️ License - WTFPL

## ⭐ Support / Поддержка

If this script helped you, give it a ⭐ on GitHub!  
Если скрипт помог, поставь ⭐ на GitHub!

---

**Made with 🤘 by someone who had Over9000 liked videos**
