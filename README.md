# 💖💖💖 FARDAUSH BOT 💖💖💖
# 🔥🔥 FREE FIRE AUTOMATION BOT 🔥🔥

<p align="center">
  <img src="https://img.shields.io/badge/FARDAUSH-BOT-ff69b4?style=for-the-badge">
  <img src="https://img.shields.io/badge/FREE-FIRE-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/VERSION-1.0-blue?style=for-the-badge">
</p>

---

# 🌸 Welcome To FARDAUSH BOT 🌸

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
rm -rf $HOME/.fardaush
rm -f $PREFIX/bin/fardaush

# Clone fresh copy
git clone https://github.com/fhhayato-source/fhfardaush

# Install requirements
pip install --upgrade pip
pip install -r $HOME/.fardaush/requirements.txt

# Create permanent command
cat << 'EOF' > $PREFIX/bin/fardaush
#!/data/data/com.termux/files/usr/bin/bash
if [ ! -d "$HOME/.fardaush" ]; then
    git clone https://github.com/fhhayato-source/fhfardaush
fi

cd $HOME/.fardaush
git pull > /dev/null 2>&1

if [ -f "requirements.txt" ]; then
    pip install -r requirements.txt > /dev/null 2>&1
fi

python FARDAUSH.py
EOF

chmod +x $PREFIX/bin/fardaush
