# Voter Search — GitHub থেকে APK বানানোর নিয়ম

এই ফোল্ডারটি একটি সম্পূর্ণ Capacitor প্রজেক্ট। GitHub-এ আপলোড করলে GitHub নিজেই
(বিনামূল্যে GitHub Actions ব্যবহার করে) একটি আসল Android APK বানিয়ে দেবে — আপনার
কম্পিউটারে Android Studio বা কিছুই ইনস্টল করা লাগবে না।

## ধাপ

1. github.com-এ গিয়ে একটি নতুন **public** বা **private** repository বানান (যেমন `voter-search`)।
2. এই পুরো ফোল্ডারটি সেই repo-তে আপলোড করুন (GitHub ওয়েবসাইটের "Upload files" দিয়েও করা যায়,
   বা `git push` দিয়ে)।
3. Upload হওয়ার পর repo-র উপরে **"Actions"** ট্যাবে ক্লিক করুন।
4. "Build APK" workflow-টি স্বয়ংক্রিয়ভাবে শুরু হবে (৩-৫ মিনিট সময় লাগবে)।
5. শেষ হলে সেই run-এর পেজে নিচে **"Artifacts"** অংশে `voter-search-debug-apk` নামে একটি ফাইল
   পাবেন — সেটা ডাউনলোড করুন, ভেতরে `app-debug.apk` থাকবে।
6. ঐ APK ফাইলটি আপনার Android ফোনে পাঠিয়ে ইনস্টল করুন (প্রথমবার "Unknown sources" অনুমতি
   দিতে হতে পারে, ফোনের Settings থেকে)।

## সব ১৮টি PDF-এর ডেটা অ্যাপে ঢোকাতে চাইলে

`voter_search_toolkit` ফোল্ডারের পাইপলাইন চালিয়ে পাওয়া নতুন `data.js` ফাইলটি দিয়ে
এই ফোল্ডারের `www/data.js` replace করুন, তারপর আবার GitHub-এ push করুন —
GitHub Actions আবার নতুন APK বানিয়ে দেবে সব ৯ ওয়ার্ডের ডেটা সহ।

## এই প্রজেক্ট আমি নিজে রান/টেস্ট করতে পারিনি

আমার sandbox-এ ইন্টারনেট/Android SDK নেই, তাই এই workflow আমি নিজে চালিয়ে দেখতে
পারিনি। এটি Capacitor-এর স্ট্যান্ডার্ড, সুপরিচিত পদ্ধতি, তাই কাজ করার কথা — কিন্তু
GitHub Actions-এ যদি কোনো error আসে, আমাকে error message-টা দেখালে আমি ঠিক করে দেব।
