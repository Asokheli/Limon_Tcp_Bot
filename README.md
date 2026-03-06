# 💖💖💖 LIMON BOT 💖💖💖
# 🔥🔥 FREE FIRE AUTOMATION BOT 🔥🔥

<p align="center">
  <img src="https://img.shields.io/badge/LIMON-BOT-ff69b4?style=for-the-badge">
  <img src="https://img.shields.io/badge/FREE-FIRE-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/VERSION-1.0-blue?style=for-the-badge">
</p>

---

# 🌸 Welcome To LIMON BOT 🌸

> 💎 Cute Design  
> ⚡ Super Fast  
> 🔥 Powerful Performance  
> 💖 Made With Love  

---

# ✨ FEATURES ✨

🌺 Auto Room Join  
🌺 Auto Invite  
🌺 Auto Emote  
🌺 Custom Room Name  
🌺 Auto Restart System  
🌺 Smooth & Secure  

---

# 📥 INSTALLATION (TERMUX)

```
pkg update -y
pkg install git python -y

# Remove old installation if exists
rm -rf $HOME/.limon
rm -f $PREFIX/bin/limon

# Clone fresh copy
git clone https://github.com/Ariyan20267/Ariyan_bot.git $HOME/.limon

# Install requirements
pip install --upgrade pip
pip install -r $HOME/.limon/requirements.txt

# Create permanent command
cat << 'EOF' > $PREFIX/bin/limon
#!/data/data/com.termux/files/usr/bin/bash
if [ ! -d "$HOME/.limon" ]; then
    git clone https://github.com/Ariyan20267/Ariyan_bot.git $HOME/.limon
fi

cd $HOME/.limon
git pull > /dev/null 2>&1

if [ -f "requirements.txt" ]; then
    pip install -r requirements.txt > /dev/null 2>&1
fi

python LIMON.py
EOF

chmod +x $PREFIX/bin/limon
