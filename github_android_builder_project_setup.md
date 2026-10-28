# Aether Study Hub - GitHub Actions APK Builder Setup Guide

මේ Zip ෆයිල් එක ඇතුළේ GitHub Actions හරහා Android APK එකක් සෑදීමට අවශ්‍ය සියලුම Scripts සහ Android Configuration ෆයිල් තියෙනවා.

---

### Zip File එකේ අඩංගු ෆෝල්ඩර් පද්ධතිය (File Structure):

```text
aether-study-hub-android/
├── .github/
│   └── workflows/
│       └── build-apk.yml       <-- GitHub එකේ automatic APK build කරන script එක
├── www/
│   └── index.html              <-- ඔබේ ප්‍රධාන Web App Code එක
├── android/                    <-- Capacitor Android Project එක
├── package.json                <-- Web App Configuration
└── capacitor.config.json       <-- App ID, App Name විස්තර
```

---

### GitHub එකට Upload කර APK එක සාදාගන්නා ආකාරය (Step-by-Step Guide):

1. **Zip ෆයිල් එක Extract කරගන්න:**
   - පහත ලබාදී ඇති Zip ෆයිල් එක ඔබේ පරිගණකයට හෝ දුරකථනයට Download කර Extract (Unzip) කරගන්න.

2. **GitHub එකට Upload කරන්න (New Repository):**
   - ඔබේ GitHub Account එකට ගොස් **New Repository** එකක් සාදන්න.
   - Extract කරගත් ෆෝල්ඩර් එක ඇතුළේ ඇති සියලුම ෆයිල් (ලපිට තියෙන `.github` ෆෝල්ඩර් එකත් එක්කම) Repository එකට Upload කර **Commit Changes** ලබාදෙන්න.

3. **APK එක Download කරගන්න:**
   - Upload වූ පසු ඔබේ Repository එකේ **"Actions"** ටැබ් එකට යන්න.
   - එතන **"Build Android APK"** නමින් Automatic Job එකක් Run වෙනවා බලාගත හැක (මිනිත්තු 2-4 අතර කාලයක් යයි).
   - එය සාර්ථක වූ පසු (Green Tick එක ආ පසු), එම Job එක මත Click කර පහළට Scroll කළ විට **`app-release-unsigned`** කියන Artifact එක යටතේ ඔබේ **APK** එක Download කරගත හැක.
