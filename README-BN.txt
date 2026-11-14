JK THREAD & ONLINE CENTRE — ওয়েবসাইট + Admin Panel

এই প্যাকেজে:
- index.html : গ্রাহকদের মূল ওয়েবসাইট
- admin.html : অ্যাডমিন লগইন, নোটিশ প্রকাশ ও মুছে ফেলার প্যানেল
- supabase-setup.sql : নোটিশ ডেটাবেস ও নিরাপত্তা নিয়ম
- SETUP-BN.txt : ধাপে ধাপে বাংলা নির্দেশিকা

গুরুত্বপূর্ণ:
Admin Panel সত্যিকারের অনলাইন নোটিশ প্রকাশ করতে Supabase backend প্রয়োজন। ZIP ফাইলটি তৈরি আছে, কিন্তু আপনার Supabase অ্যাকাউন্ট/প্রজেক্ট তৈরি বা সংযোগ করা হয়নি। তাই কনফিগারেশন না বসানো পর্যন্ত Admin Panel কাজ করবে না।

সেটআপ:
1) https://supabase.com/ খুলে আপনার ইমেইল দিয়ে সাইন আপ/লগইন করুন।
2) New project তৈরি করুন; নাম দিতে পারেন jk-thread-online-centre। শক্তিশালী database password নিজের কাছে রাখুন।
3) Project তৈরি হলে Project Settings > API থেকে Project URL এবং anon/public (কিছু নতুন UI-তে publishable) key কপি করুন।
4) Supabase-এর SQL Editor খুলে supabase-setup.sql ফাইলের সম্পূর্ণ SQL পেস্ট করে Run করুন।
5) Authentication > Users থেকে Add user করে নিজের ইমেইল ও শক্তিশালী পাসওয়ার্ড দিয়ে অ্যাডমিন অ্যাকাউন্ট তৈরি করুন। Email confirmation চালু থাকলে ইমেইল নিশ্চিত করুন।
6) index.html ও admin.html—দুই ফাইলেই নিচের placeholder দুটো খুঁজে আপনার Project URL এবং anon/publishable key বসান:
   PASTE_YOUR_SUPABASE_PROJECT_URL_HERE
   PASTE_YOUR_SUPABASE_ANON_KEY_HERE
   (এটি public browser key; RLS policy ছাড়া ডেটা উন্মুক্ত করবেন না। কখনও service_role/secret key বসাবেন না।)
7) তিনটি ফাইল (index.html, admin.html, supabase-setup.sql) GitHub repository-তে আপলোড/কমিট করুন। SQL ফাইল ওয়েবসাইটে চলবে না; সেটি শুধু Supabase SQL Editor-এ চালাতে হবে।
8) মূল ওয়েবসাইট খুলে নোটিশ বোর্ড দেখুন। Admin পেজ খুলুন:
   https://skjahidalom-oss.github.io/Jk-thread-online-center/admin.html
9) আপনার তৈরি করা admin email/password দিয়ে লগইন করে নোটিশ প্রকাশ করুন। মূল ওয়েবসাইটের নোটিশ বোর্ডে সবাই তা দেখতে পাবে।

WhatsApp নম্বর:
আগের ব্যবহৃত +91 85148 79701 রাখা হয়েছে। বদলাতে হলে দুই HTML ফাইলে 918514879701 খুঁজে নতুন নম্বর বসান।

নিরাপত্তা:
- service_role/secret key কখনও HTML/JavaScript-এ দেবেন না।
- Admin password কারও সঙ্গে শেয়ার করবেন না।
- গ্রাহকের OTP, PIN, ব্যাংক পাসওয়ার্ড নেবেন না।
- Admin user ছাড়া অন্য কাউকে Supabase dashboard access দেবেন না।
