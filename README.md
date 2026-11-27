# 🛡️ MyShadow - Secure Password Vault

MyShadow is a private, secure vault for passwords and personal media. Your information stays in your browser and is protected by a Master Password.

## Features

- Store and organize passwords
- Search passwords quickly
- Generate strong passwords
- Save favorite credentials
- Copy usernames and passwords
- Fill login details on websites
- Store private images and PDF files
- Create a local backup copy
- Lock the vault instantly
- Hide the screen when you leave the browser

## How to Install

### Chrome

1. Download and extract the MyShadow extension folder.
2. Open Chrome and visit `chrome://extensions/`.
3. Turn on **Developer mode** in the top-right corner.
4. Click **Load unpacked**.
5. Select the folder containing `manifest.json`.
6. Pin **MyShadow** to the Chrome toolbar for quick access.

### Microsoft Edge

1. Download and extract the MyShadow extension folder.
2. Open Edge and visit `edge://extensions/`.
3. Turn on **Developer mode**.
4. Click **Load unpacked**.
5. Select the folder containing `manifest.json`.
6. Pin **MyShadow** to the toolbar.

### Brave

1. Download and extract the MyShadow extension folder.
2. Open Brave and visit `brave://extensions/`.
3. Turn on **Developer mode**.
4. Click **Load unpacked**.
5. Select the folder containing `manifest.json`.
6. Pin **MyShadow** to the toolbar.

## How to Use

### Set Up Your Vault

1. Click the MyShadow icon in the browser toolbar.
2. Create a strong Master Password.
3. Confirm the password and open the vault.
4. Keep your Master Password somewhere safe.

> Your Master Password cannot be recovered. Do not forget it.

### Save a Password

1. Open the MyShadow popup.
2. Select **Passwords**.
3. Add the website name, username, and password.
4. Save the entry to your vault.

### Fill a Login Form

1. Open a website and focus a username or password field.
2. Click the MyShadow shield that appears near the field.
3. Unlock the vault if needed.
4. Select the saved login to fill the form.

### Save Private Media

1. Open the MyShadow popup.
2. Select **Media**.
3. Choose an image or PDF.
4. The file will be stored securely in the extension.

### Lock the Vault

- Click **Lock** in MyShadow

Locking the vault requires the Master Password to access your saved information again.

### Create a Safety Copy

1. Open MyShadow.
2. Use the backup option in the vault.
3. Choose a safe location on your computer.
4. Keep the backup file in a secure place.

## Privacy and Safety

- All vault data is stored only on your device. MyShadow cannot store or recover your data on an external server.
- Do not share your Master Password.
- Protect any backup file you create.
- Clearing browser extension data may permanently remove your saved vault.
- On a shared computer, lock MyShadow after every use.

## How to Use in Bengali

### ইনস্টল করার নিয়ম

1. MyShadow এক্সটেনশন ফাইলটি ডাউনলোড করে এক্সট্র্যাক্ট করুন।
2. Chrome ব্যবহার করলে `chrome://extensions/` খুলুন।
3. **Developer mode** চালু করুন।
4. **Load unpacked** বাটনে ক্লিক করুন।
5. `manifest.json` থাকা ফোল্ডারটি সিলেক্ট করুন।
6. সহজে ব্যবহার করার জন্য এক্সটেনশনটি টুলবারে পিন করুন।

### ব্যবহার করার নিয়ম

1. MyShadow আইকনে ক্লিক করে একটি শক্তিশালী Master Password দিয়ে ভল্ট তৈরি করুন।
2. **Passwords** সেকশন থেকে Password সেভ করুন।
3. লগইন পেজে ইউজারনেম বা পাসওয়ার্ড ফিল্ডে ক্লিক করুন।
4. Shild আইকন বা Mini-Vault থেকে সেভ করা লগইনটি নির্বাচন করুন।
5. মিডিয়া সেভ করতে **Media** সেকশন ব্যবহার করুন।

### ডাটা সেভ করার সিস্টেম ও লোকাল ড্রাইভে ব্যাকআপ

MyShadow সম্পূর্ণ **Zero-Knowledge** এবং **Local-First** আর্কিটেকচারে কাজ করে—অর্থাৎ কোনো সার্ভারে বা ক্লাউডে আপনার কোনো ডাটা পাঠানো হয় না।

1. **ব্রাউজার ভল্ট ও এনক্রিপশন (`chrome.storage.local`):**
   - আপনার সব পাসওয়ার্ড, নোট, মিডিয়া (ছবি ও PDF) এবং ভল্ট মেটাডেটা ব্রাউজারের লোকাল স্টোরেজে (`chrome.storage.local` ও `unlimitedStorage` পারমিশন ব্যবহার করে) সংরক্ষিত থাকে।
   - প্রতিটি সেন্সিটিভ তথ্য সেভ হওয়ার আগে আপনার Master Password থেকে **PBKDF2** (SHA-256, `600,000` iterations ও 32-byte random salt) দিয়ে ডিরাইভ করা কী ব্যবহার করে **AES-256-GCM** অ্যালগরিদমে এনক্রিপ্ট করা হয়।
   - ব্যাকআপ তৈরির সময় সব ডাটা ও মিডিয়া gzip-কম্প্রেস ও এনক্রিপ্ট করে একটি সিল করা ব্যাকআপ প্যাকেজ (`myshadow_sealed_backup`) হিসেবেও সংরক্ষণ করা হয়।

2. **লোকাল ড্রাইভে স্বয়ংক্রিয় ব্যাকআপ (Safety Copy):**
   - সেটিংসের **Safety Copy** সেকশন থেকে **Choose Location** বাটনে ক্লিক করে আপনি আপনার কম্পিউটারের লোকাল ড্রাইভের যেকোনো ফোল্ডারে `myshadow-backup.json` নামে একটি এনক্রিপ্টেড ব্যাকআপ ফাইল লিংক করতে পারবেন।
   - ব্রাউজারের **File System Access API** ব্যবহার করে এই ফাইল হ্যান্ডেলটি `IndexedDB`-তে সংরক্ষিত থাকে।
   - **Keep safety copy updated automatically** অপশনটি চালু থাকলে ভল্টে কোনো পাসওয়ার্ড বা মিডিয়া যোগ, পরিবর্তন বা ডিলিট করার সাথে সাথেই ব্যাকগ্রাউন্ডে নীরবে লোকাল ড্রাইভের ওই ব্যাকআপ ফাইলটি আপডেট হয়ে যায়। চাইলে **Backup Now** বাটনে ক্লিক করেও সাথে সাথে ব্যাকআপ আপডেট করতে পারবেন।
   - এছাড়াও, প্রতিদিন নির্দিষ্ট সময় পরপর (`1440` মিনিট) ব্রাউজারের ডিফল্ট ডাউনলোড ফোল্ডারের `MyShadow-Backups/myshadow-backup.json` লোকেশনে অটো-ব্যাকআপ নেওয়ার ব্যবস্থাও রয়েছে।

### ব্যাকআপ ফাইল ভুলবশত ডিলিট হয়ে গেলে কী হবে?

লোকাল ড্রাইভ থেকে আপনার `myshadow-backup.json` ফাইলটি যদি ভুলবশত ডিলিট হয়ে যায়, তবুও আপনার ভল্টের ডাটা সাথে সাথে নষ্ট হয় না:

- **মূল ভল্ট সুরক্ষিত থাকে:** আপনার পাসওয়ার্ড ও মিডিয়া ব্রাউজারের `chrome.storage.local`-এ আলাদাভাবে সংরক্ষিত থাকে। তাই শুধু লোকাল ড্রাইভের ব্যাকআপ ফাইল ডিলিট হলে ব্রাউজার ভল্টের কোনো ডাটা মুছে যায় না।
- **স্বয়ংক্রিয়ভাবে ফাইল পুনরায় তৈরি (Auto-Recreate):** ভল্ট আনলক বা ডাটা আপডেট করার সময় এক্সটেনশন চেক করে যে লিংক করা ব্যাকআপ ফাইলটি ড্রাইভে আছে কি না। যদি ফাইলটি ডিলিট হয়ে থাকে কিন্তু ব্রাউজারের কাছে ওই ফোল্ডার/ফাইলের `readwrite` পারমিশন থাকে, তাহলে এক্সটেনশন সিল করা ব্যাকআপ ডাটা থেকে **স্বয়ংক্রিয়ভাবে একই জায়গায় নতুন করে `myshadow-backup.json` ফাইলটি তৈরি করে দেয়**।
- **যদি পারমিশন বা ফোল্ডার না পাওয়া যায়:** যদি পুরো ফোল্ডারটি ডিলিট হয়ে যায় বা ফাইল পারমিশন বাতিল হয়ে যায়, তবে এক্সটেনশন পুরোনো লিংকটি রিসেট করে এবং আপনাকে পুনরায় **Choose Location** ব্যবহার করে নতুন একটি ব্যাকআপ লোকেশন সেট করতে বলে।
- **গুরুত্বপূর্ণ সতর্কতা:** যদি ব্রাউজার থেকে এক্সটেনশন আনইনস্টল বা ব্রাউজার ডাটা ক্লিয়ার করার **পাশাপাশি** লোকাল ড্রাইভের ব্যাকআপ ফাইলটিও ডিলিট হয়ে যায়, তবে ডাটা আর রিকভার করা সম্ভব হবে না।

### ব্যাকআপ ইমপোর্ট (Import) করার নিয়ম

নতুন ব্রাউজারে, এক্সটেনশন রি-ইনস্টল করার পর, অথবা আগের কোনো ব্যাকআপ ফাইল থেকে ডাটা ফিরিয়ে আনতে **Import** অপশন ব্যবহার করুন:

1. MyShadow পপআপ ওপেন করে ভল্ট আনলক করুন এবং সেটিংসের **Safety Copy** সেকশনে যান।
2. **Import** বাটনে ক্লিক করুন এবং আপনার লোকাল ড্রাইভে সেভ থাকা এনক্রিপ্টেড `.json` ব্যাকআপ ফাইলটি সিলেক্ট করুন।
3. **Import Encrypted Backup** পপআপে ওই ব্যাকআপ ফাইলটি তৈরি করার সময় যে **Master Password** ছিল, সেটি দিন। *(বর্তমান ভল্টের Master Password ও পুরোনো ব্যাকআপের Master Password আলাদা হলেও ইমপোর্ট করা যাবে।)*
4. এক্সটেনশন ব্যাকআপ ফাইলটি যাচাই ও ডিক্রিপ্ট করে বর্তমান ভল্টের Master Password দিয়ে পুনরায় এনক্রিপ্ট করে সেভ করবে।
5. **ডুপ্লিকেট এড়ানো:** ইমপোর্টের সময় প্রতিটি পাসওয়ার্ড ও মিডিয়ার আইডি (`id`) চেক করা হয়—যেগুলো আগে থেকেই ভল্টে আছে সেগুলো স্কিপ করা হয় এবং কেবল নতুন আইটেম ও মিডিয়াগুলো ভল্টে যোগ হয়। ইমপোর্ট শেষে কতগুলো সিক্রেট ও মিডিয়া যোগ হয়েছে তা স্ক্রিনে দেখাবে।

> আপনার সব ডেটা শুধুমাত্র আপনার নিজের ডিভাইসে সংরক্ষিত থাকে। Master Password ভুলে গেলে ভল্টের তথ্য আর রিকভার করা যাবে না, কারণ সেগুলো কোনো সার্ভারে সংরক্ষণ বা ব্যাকআপ করা হয় না।

---

Developed by [Ripon](https://riponmondalbd.vercel.app)
