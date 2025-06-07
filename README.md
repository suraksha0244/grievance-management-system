
# 📢 Grievance Management System 🚀

A centralized AI-driven web portal for Indian citizens to submit and track government grievances efficiently, built during my internship at **Niveus Solutions**. The platform resolves inefficiencies in the existing grievance redressal system by automating complaint categorization and routing through an AI model — improving resolution times, transparency, and citizen experience.

## 📺 Demo Video

👉 [Watch the Demo](https://drive.google.com/file/d/1Qy9zXUXX_WcGIUG82drNATQupFwzmWij/view)

---

## 📌 Problem Statement

Current grievance systems in India suffer from:

* **Decentralization**
* **Misdirected complaints**
* **Limited transparency and delayed resolutions**

Complaints are often routed improperly, causing delays in reaching responsible departments and slowing down the grievance resolution process.

---

## 💡 Solution Overview

The **Grievance Management Portal** addresses these challenges by:

✅ Offering a **centralized platform** for citizens to submit grievances.
✅ Using an **AI-driven decision model** to automatically assign complaints to the correct department based on content.
✅ Providing **department-specific admin dashboards** for efficient complaint handling.
✅ Enabling **real-time status updates** for citizens.

---

## 🛠️ Tech Stack

| Layer                  | Technologies                               |
| :--------------------- | :----------------------------------------- |
| Frontend               | React.js, HTML, CSS, JavaScript            |
| Backend                | Node.js, Express.js, MongoDB               |
| AI Model               | Python, scikit-learn (Naive Bayes, TF-IDF) |
| API Integration        | Flask (for AI model inference)             |
| Authentication         | JWT                                        |
| File Uploads           | multer                                     |
| Geolocation Extraction | EXIF parsing from images                   |

---

## 📈 Key Features

* ✨ **AI-Powered Complaint Routing**
  Uses a trained **Naive Bayes classifier** to categorize complaints and direct them to the appropriate department.

* 📊 **Department-specific Admin Dashboards**
  Only relevant admins can access and resolve complaints assigned to their department, avoiding overlap.

* 📝 **Complaint Submission with Geo-tagged Images**
  Citizens can upload photos, from which location details are extracted via image EXIF data.

* 🔒 **JWT-based Authentication**
  Separate roles for admins and citizens.

* 📲 **Real-Time Complaint Status Tracking**
  Citizens can track the live status of their complaints post submission.

---

## 🔍 System Architecture Overview

**End-to-End Flow:**

1. **User Registration & Login**
   Citizens create an account and authenticate via JWT.

2. **Complaint Submission**
   Users fill a form, upload optional geo-tagged images, and submit grievances.

3. **AI Model Prediction**
   Complaint text sent via REST API to Flask server → AI model categorizes issue using TF-IDF & Naive Bayes.

4. **Complaint Routing & Storage**
   Backend assigns complaints to appropriate department collections in MongoDB.

5. **Admin Dashboard Management**
   Department admins view and act on complaints from their dashboard.

6. **Real-Time Status Update**
   Citizens receive live updates on complaint progress.

---

## 🧠 AI Decision Model

* **Text Classification**:
  Uses **TF-IDF vectorization** and **Naive Bayes (MultinomialNB)** for categorizing complaints into department labels.

* **Data Preparation**:

  * Complaint text from various departments
  * Preprocessing: Cleaning, TF-IDF conversion

* **Deployment**:

  * Model saved using `joblib`
  * Integrated via a **Flask REST API**

* **Optimizations**:
  Limited feature set (max 10,000 TF-IDF features) for faster real-time predictions.

---

## 📦 Backend Architecture

* **Framework**: Node.js + Express.js
* **Database**: MongoDB (NoSQL with Mongoose)
* **Structure**: MVC (Model-View-Controller) pattern

**Modules:**

* Controllers: Handle business logic
* Routes: Define API endpoints
* Middlewares: Auth, location extraction, file upload
* Models: Mongoose schemas for complaints, actions, and users

---

## ⚙️ Key Backend Features

* **JWT-based Authentication**
* **AI-Based Complaint Routing via Flask**
* **Image Uploads with multer**
* **EXIF-based Geolocation Extraction**
* **Real-time Complaint Status Management**

---

## 🚀 Outcomes & Impact

* ✅ **Reduced complaint misdirection**
* ✅ **Faster, automated department routing**
* ✅ **Increased transparency with real-time tracking**
* ✅ **Higher citizen engagement via intuitive portal**
* ✅ **Scalable, modular architecture for future extensions**

---

## 📊 Challenges Tackled

| Challenge                          | Solution                                |
| :--------------------------------- | :-------------------------------------- |
| Collecting balanced complaint data | Curated diverse, representative dataset |
| Real-time AI model performance     | Optimized TF-IDF feature space          |
| Seamless AI-backend integration    | Flask REST API                          |

---

## 📌 Future Improvements

* 📱 **Mobile App Integration**
* 📈 **Complaint Analytics Dashboard**
* 🗣️ **Multi-language Complaint Support**
* 📣 **Push Notifications**

---

## 📞 Contact

**Suraksha**
[LinkedIn](https://www.linkedin.com/) | [Email](mailto:youremail@example.com)

---


