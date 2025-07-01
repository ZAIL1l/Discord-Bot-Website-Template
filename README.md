# Discord Bot Website Template

Website template for your Discord bot.  
Includes **WidgetBot** for real-time live chat from your support server.

---

## 🌐 Live Demo

👉 [View Live Preview](https://discord-bot-website-template.netlify.app)  

---

## Footer Credit
You are free to remove the "Website Designed By..." line from the footer. However, keeping it is highly appreciated as a form of support for this work.

---

## Preview

![img](/images/preview.png)

---

## 🚀 Tech Stack

* **HTML**
* **CSS**
* **JavaScript**
* **Font Awesome** (icons)
* **WidgetBot** (Discord live chat)

---

### 📦 Clone the Repository

Open your terminal:

```bash
git clone https://github.com/AdityaLF/Discord-Bot-Website-Template.git
cd Discord-Bot-Website-Template
```

## ⚙️ Setup Instructions

### **Update Bot Invite Link**

To ensure the "Invite Bot" buttons work correctly, you need to update the invite link.

1. Open `main.js` file.
2. Find the inviteBot() function:

    ```bash
    // Invite bot
    function inviteBot() {
        // Replace with your actual Discord bot invite link
        const inviteUrl = 'https://discord.com/api/oauth2/authorize?client_id=YOUR_BOT_ID&permissions=8&scope=bot%20applications.commands';
        window.open(inviteUrl, '_blank');
    }
    ```

3. In the `inviteUrl` line, replace with your actual Discord bot invite link.

---

### **Update WidgetBot Configuration**

To connect the live chat widget to your Discord server, you need to invite WidgetBot to your Discord server and then provide your Server and Channel IDs.

1. Invite the WidgetBot to Your Server
   * [Invite WidgetBot](https://discord.com/oauth2/authorize?client_id=543225764036870167&scope=bot+applications.commands&permissions=537218112)

3. In the `main.js` file, find the `initializeWidgetBot()` function:

    ```bash
    // Function to load and initialize the WidgetBot
    function initializeWidgetBot() {
        const crateScript = document.createElement('script');
        crateScript.src = 'https://cdn.jsdelivr.net/npm/@widgetbot/crate@3';
        crateScript.async = true;
        crateScript.defer = true;

        crateScript.onload = () => {
            console.log("WidgetBot Crate loaded, initializing...");
            new Crate({
                server: '1227468427132928110', // Your Discord Server ID
                channel: '1231573078845292644' // Your Discord Channel ID
            });
        };
        
        document.body.appendChild(crateScript);
    }
    ```

4. Inside the `new Crate({...})` object, replace the placeholder values:.

    - **server:** Replace `'1227468427132928110'` with your **Discord Server ID**.
    - **channel:** Replace `'1231573078845292644'` with your **Discord Channel ID**.

Once you have updated the server and channel IDs, WidgetBot will be connected to your Discord server and will allow real-time interactions on your website.

---

## 👤 Author

* **GitHub**: [@AdityaLF](https://github.com/AdityaLF)
* **Discord**: [@05.07am](https://discordapp.com/users/786163564205047839)
* **Support Me**: [ko-fi.com/adityaf](https://ko-fi.com/adityaf)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
