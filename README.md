# DURGAPUR BUZZ

বাংলা সংবাদপত্র-স্টাইলের responsive news web app. Vite + React.

## লোকাল কম্পিউটারে চালানো
1. Node.js 18+ ইনস্টল করুন।
2. এই ফোল্ডারে terminal খুলুন।
3. `npm install`
4. `npm run dev`

## GitHub Pages-এ প্রকাশ (এই repository-এর জন্য ঠিক করা)
এই প্রজেক্টে `vite.config.js`-এ `base: '/Durgapurbuzz-/'` সেট করা আছে এবং `.github/workflows/deploy.yml` যোগ করা হয়েছে।

1. ZIP extract করুন।
2. সব ফাইল ও `.github` hidden folder-সহ আপনার GitHub repository `Durgapurbuzz-`-এর `main` branch-এ upload/commit করুন। আগের ফাইল replace করুন।
3. GitHub repository → **Settings → Pages** খুলুন।
4. **Build and deployment → Source** থেকে **GitHub Actions** নির্বাচন করুন।
5. উপরের **Actions** tab-এ গিয়ে workflow শেষ হওয়া পর্যন্ত অপেক্ষা করুন। সবুজ check হলে deploy সম্পূর্ণ।
6. সাইটের URL হবে: `https://sekhsahinurislam.github.io/Durgapurbuzz-/`

প্রতিবার `main` branch-এ নতুন commit push করলে সাইট স্বয়ংক্রিয়ভাবে build ও deploy হবে।

## Demo Admin
ওয়েবসাইটের উপরের ডানদিকে **Admin Login** চাপুন। এটি আপাতত demo panel; authentication নেই। খবর যোগ, edit, delete করলে browser-এর LocalStorage-এ থাকবে। অন্য ডিভাইসে দেখা যাবে না এবং browser data clear করলে মুছে যেতে পারে।

## Firebase পরবর্তী ধাপ
- Firebase Authentication: Admin sign-in
- Cloud Firestore: news collection, published/draft status
- Firebase Storage: news images
- Firestore Security Rules: কেবল অনুমোদিত admin create/update/delete করতে পারবে; public শুধু published news পড়বে।

**নিরাপত্তা:** বর্তমান Admin Panel-এ কোনো পাসওয়ার্ড বা access control নেই। লাইভে প্রকাশের আগে Firebase Authentication ও Security Rules অবশ্যই যোগ করতে হবে। Demo news-এর নমুনা কনটেন্ট বাস্তব খবর হিসেবে প্রকাশ করবেন না।
