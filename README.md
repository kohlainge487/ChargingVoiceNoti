# 🔋 Charging Voice Myanmar

Android app that speaks Burmese automatically:

- Charger connected → **“အားသွင်းနေပါပြီ”**
- Charger disconnected → **“အားသွင်းမထားတော့ပါ”**

It uses Android Text-to-Speech (TTS) and the power connected/disconnected broadcast.

## GitHub မှာတင်ပြီး APK Build လုပ်နည်း

### 1. GitHub Repository တည်ဆောက်ပါ

GitHub → **New repository** ကိုနှိပ်ပါ။  
Repository name ကို `ChargingVoiceMyanmar` လို့ပေးနိုင်ပါတယ်။

Public/Private ကြိုက်ရာရွေးနိုင်ပါတယ်။ GitHub ရဲ့ official guide အတိုင်း repository အသစ်တည်ဆောက်နိုင်ပါတယ်။

### 2. Project files တင်ပါ

ဒီ project folder ထဲက files/folders အားလုံးကို repository root ထဲတင်ပါ။

အရေးကြီးတာက `.github/workflows/build-apk.yml` ကိုပါ တင်ရပါမယ်။

### 3. GitHub Actions က APK build လုပ်ပါမယ်

Repository ထဲမှာ:

**Actions → Build Android APK → Run workflow**

ကိုနှိပ်ပါ။

ပြီးသွားရင် workflow run ကိုဖွင့်ပြီး **Artifacts** အောက်က:

`ChargingVoiceMyanmar-debug`

ကို Download လုပ်ပါ။

အဲဒီ ZIP ထဲမှာ `app-debug.apk` ပါပါမယ်။

## Android Studio မှာ Build လုပ်နည်း

Project folder ကို Android Studio → **Open** လုပ်ပါ။

ပြီးရင်:

**Build → Build APK(s)**

ကိုနှိပ်ပါ။

APK:

`app/build/outputs/apk/debug/app-debug.apk`

မှာရပါမယ်။

## မြန်မာ Female Voice

App က device ရဲ့ Android TTS engine ကိုအသုံးပြုပါတယ်။

ဖုန်းထဲမှာ Myanmar female voice မရှိရင် app က female voice ကို အတင်းမဖန်တီးနိုင်ပါ။ TTS engine/voice data ထဲမှာ ရရှိတဲ့ Myanmar voice ကို အသုံးပြုပါမယ်။

TTS setting ကို ဖုန်းအမျိုးအစားအလိုက်:

**Settings → Language & input / Accessibility → Text-to-speech output**

ကနေ စစ်နိုင်ပါတယ်။

## Background

`ACTION_POWER_CONNECTED` နဲ့ `ACTION_POWER_DISCONNECTED` broadcast ကို `BroadcastReceiver` ဖြင့် လက်ခံထားတဲ့အတွက် app screen ဖွင့်ထားစရာမလိုဘဲ power event ဖြစ်တဲ့အခါ TTS ကို run လုပ်နိုင်ပါတယ်။

အချို့ဖုန်း manufacturer တွေရဲ့ battery optimization က background execution ကို ကန့်သတ်နိုင်ပါတယ်။ အသံမထွက်ရင် app battery setting ကို **Unrestricted / Don't optimize** အဖြစ်ထားကြည့်ပါ။

## Release APK

ဒီ workflow က စမ်းသပ်/အသုံးပြုရန် Debug APK ကို build ပါတယ်။

အများပြည်သူဖြန့်ချိမယ့် Release APK အတွက် signing key ထည့်ပြီး signed release build ပြုလုပ်သင့်ပါတယ်။
