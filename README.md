# DURGAPUR BUZZ

বাংলা সংবাদপত্র-স্টাইলের responsive news web app. Vite + React.

## চালানোর নিয়ম
1. Node.js 18+ ইনস্টল করুন।
2. এই ফোল্ডারে terminal খুলুন।
3. `npm install`
4. `npm run dev`
5. ব্রাউজারে Vite যে local URL দেখাবে সেটি খুলুন।

## GitHub-এ আপলোড
GitHub-এ নতুন repository তৈরি করে এই প্রজেক্টের সব ফাইল push করুন। GitHub Pages-এর বদলে Vercel/Netlify-তে deploy করা সহজ:
- Vercel: Import Git Repository → Framework Vite → Build `npm run build` → Output `dist`
- Netlify: Build command `npm run build`, Publish directory `dist`

## Demo Admin
ওয়েবসাইটের উপরের ডানদিকে **Admin Login** চাপুন। এটি আপাতত demo panel; authentication নেই। খবর যোগ, edit, delete করলে browser-এর LocalStorage-এ থাকবে। অন্য ডিভাইসে দেখা যাবে না এবং browser data clear করলে মুছে যেতে পারে।

## Firebase পরবর্তী ধাপ
Firebase যুক্ত করার সময়:
- Firebase Authentication: Admin sign-in
- Cloud Firestore: news collection, published/draft status
- Firebase Storage: news images
- Firestore Security Rules: কেবল অনুমোদিত admin create/update/delete করতে পারবে; public শুধু published news পড়বে।

**গুরুত্বপূর্ণ:** বর্তমান Admin Panel-এ কোনো নিরাপত্তা নেই। লাইভে প্রকাশের আগে Firebase Authentication ও Security Rules অবশ্যই যোগ করতে হবে। Demo news-এ নমুনা কনটেন্ট ব্যবহার করা হয়েছে; বাস্তব খবর হিসেবে প্রকাশ করবেন না।
