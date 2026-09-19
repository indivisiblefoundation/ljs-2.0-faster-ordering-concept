# ljs-2.0-faster-ordering-concept
This is a my version of ljs which is entirely faster than the real ljs and this is only for submission to the company in order to sell my version to them.  In full when downloaded extracted and run correctly just  follow directions and all you have to do is open a browser and go to the site it tells you to in order to play on the faster app 

On Linux Mint 
git clone https://github.com/YOUR_USERNAME/ljs-mint.git
cd ljs-mint

# if you downloaded LJS_MINT_FIXED.zip
unzip ~/Downloads/LJS_MINT_FIXED.zip -o -d /tmp/ljs-fixed
cp -r /tmp/ljs-fixed/*/* ./ 2>/dev/null || cp -r /tmp/ljs-fixed/* ./

# install & run
npm install
npm run dev
# → http://localhost:5173

Build APK 
npm run build
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap init "LJS 2.0 Concept" com.tomas.ljs2 --web-dir=dist
npx cap add android
npx cap open android
# In Android Studio: wait for Gradle Sync → Run (green triangle)
# APK: android/app/build/outputs/apk/debug/app-debug.apk

# Or build without Android Studio UI:
cd android && ./gradlew assembleDebug

Real Phone
sudo tee /etc/udev/rules.d/51-android.rules > /dev/null <<'EOF'
SUBSYSTEM=="usb", MODE="0666", GROUP="plugdev"
EOF
sudo usermod -aG plugdev $USER
sudo udevadm control --reload-rules
adb devices

Project Structure

ljs-mint/
├── src/
│   ├── App.tsx          # Main app - Home/Menu/Rewards/Stores
│   ├── main.tsx
│   ├── index.css        # Tailwind
│   └── assets/
│       ├── fish_basket_meal.webp
│       ├── chicken_tenders_fries_basket.webp
│       └── seafood_platter_topdown.webp
├── public/
├── LJS_SIMPLE_NO_INSTALL.html  # No-install single file demo
├── index.html
├── vite.config.ts
├── tailwind.config.js


Disclaimer
This is a speculative, unpaid concept project. Long John Silver's®, Seacret Society®, and all menu names are trademarks of Long John Silver's LLC. This repo is not affiliated with, endorsed by, or connected to Long John Silver's LLC or Four Oaks Partners. No logos or copyrighted menu photos are distributed — demo food photos are generated placeholders.

If you are Long John Silver's and want this taken down or want to talk about a real v2, open an issue or contact me.


└── README.md
