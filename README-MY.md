# Charging Voice Myanmar

Android app:
- Charger connected → “အားသွင်းနေပါပြီ”
- Charger disconnected → “အားသွင်းမထားတော့ပါ”

## Android Studio ဖြင့် Build လုပ်နည်း

1. Android Studio ကို install လုပ်ပါ။
2. ZIP ကို Extract လုပ်ပါ။
3. Android Studio → **Open** → `ChargingVoiceMyanmar` folder ကိုရွေးပါ။
4. Gradle Sync ပြီးအောင်စောင့်ပါ။
5. ဖုန်းတွင် Developer options + USB debugging ဖွင့်ပြီး USB ဖြင့်ချိတ်ပါ။
6. Android Studio → Build → **Build APK(s)** ကိုနှိပ်ပါ။
7. APK ကို:
   `app/build/outputs/apk/debug/app-debug.apk`
   တွင်ရပါမည်။

## မြန်မာမိန်းကလေးအသံ

App က Android ရဲ့ Text-to-Speech (TTS) engine ကိုသုံးပါတယ်။
ဖုန်းတိုင်းမှာ မြန်မာဘာသာ female voice မရှိနိုင်ပါ။

မပြောပါက:
Settings → Accessibility / Language & input → Text-to-speech output
(ဖုန်းအမျိုးအစားအလိုက် menu အမည်ကွာနိုင်သည်)
ထဲမှာ Google Speech Services / TTS voice data ကို စစ်ပါ။

Female voice ရှိလျှင် TTS engine ထဲက available Myanmar female voice ကို app က
ဦးစားပေးရွေးပါမယ်။

## မှတ်ချက်

Android ရဲ့ power-connected / power-disconnected broadcast ကို အသုံးပြုထားပါတယ်။
Battery optimization သို့မဟုတ် manufacturer power-saving policy အချို့က background
လုပ်ဆောင်မှုကို ကန့်သတ်နိုင်ပါတယ်။ ထိုသို့ဖြစ်ပါက app ကို Battery → Unrestricted
အဖြစ်ထားပေးပါ။
