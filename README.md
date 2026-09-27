# Express + Multer File Upload System 🚀

এই প্রজেক্টটি Express.js এবং Multer ব্যবহার করে তৈরি করা একটি File Upload System।

## 📁 Project Structure

```
express-multer-upload/
├── uploads/              # Uploaded files saved here
│   └── image.jpg
├── public/
│   └── index.html        # Interactive UI for browser testing
├── server.js             # Express server & Multer diskStorage logic
├── package.json          # Project dependencies
└── README.md             # Project documentation
```

---

## 🛠 Setup & Run Instructions

### 1. Dependencies Install করুন
```bash
npm install
```

### 2. Server Start করুন
```bash
npm start
```
সার্ভারটি `http://localhost:3000` এ রান করবে।

---

## 📬 Postman Testing Steps

1. **Method**: `POST`
2. **URL**: `http://localhost:3000/upload`
3. **Body** tab সিলেক্ট করুন -> `form-data` রেডিও বাটন সিলেক্ট করুন।
4. **Key**: `file` (Dropdown থেকে **File** সিলেক্ট করুন)।
5. **Value**: আপনার কম্পিউটার থেকে যেকোনো একটি ছবি সিলেক্ট করুন (`image.jpg`)।
6. **Send** বাটনে চাপুন।

### Expected Response:
```json
{
  "message": "File uploaded successfully",
  "filename": "image-1727446500000-123456789.jpg",
  "originalname": "image.jpg",
  "path": "uploads/image-1727446500000-123456789.jpg",
  "size": 45210
}
```

আপলোড হওয়া ফাইলটি `uploads/` ফোল্ডারের মধ্যে সংরক্ষিত হবে।

---

## 🌐 Browser UI Testing
সার্ভার চালু থাকা অবস্থায় যেকোনো ব্রাউজারে `http://localhost:3000` এ ভিজিট করে সরাসরি ওয়েব পেজ থেকেও ফাইল আপলোড টেস্ট করতে পারবেন।
