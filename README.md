# CGU Final Project: Android Real-Time Chat Application

![Android_ChatApp_UI](https://github.com/user-attachments/assets/2be65636-ca9c-412c-bf1e-50c533881b33)

## Overview
This repository contains a real-time Android messaging application built with **Java** and **Firebase**. The application allows users to create accounts, set up profile pictures, and engage in real-time conversations with other registered users. It also features push notifications for incoming messages and tracks users' online/offline availability.

## Features
* **User Authentication:** Secure Sign-Up and Sign-In functionality using Firebase.
* **Real-Time Messaging:** Instant message delivery and retrieval utilizing Firebase Cloud Firestore.
* **Push Notifications:** Integrated Firebase Cloud Messaging (FCM) and Retrofit to push notifications when new messages are received.
* **Recent Conversations:** A dedicated home screen (`MainActivity`) displaying a list of recent chats sorted by the latest message.
* **Online Availability:** Real-time tracking of user status (Online/Offline) visible within the chat interface.
* **Profile Image Support:** Users can upload profile pictures, which are encoded in Base64 and stored seamlessly in the database.

## Tech Stack & Libraries
* **Language:** Java
* **Architecture / UI:** Android SDK, XML Layouts, ViewBinding
* **Database:** Firebase Cloud Firestore (NoSQL)
* **Messaging Service:** Firebase Cloud Messaging (FCM)
* **Networking API:** Retrofit2 & Scalars Converter (for handling FCM requests)
* **Image Processing:** [RoundedImageView](https://github.com/vinc3m1/RoundedImageView) for circular profile pictures, Android native `Bitmap` / `Base64` encoding.
* **Local Storage:** `SharedPreferences` (managed via a custom `PreferenceManager`) for keeping users logged in locally.

## Project Structure
* `activities/`: Contains all the UI controllers (`MainActivity`, `ChatActivity`, `SignInActivity`, `SignUpActivity`, `UsersActivity`, and a `BaseActivity` for lifecycle tracking).
* `adapters/`: RecyclerView adapters (`ChatAdapter`, `RecentConversationsAdapter`, `UsersAdapter`) to bind data to the UI efficiently.
* `models/`: Data models representing `User` and `ChatMessage`.
* `network/`: API client and interface for Retrofit to send remote FCM messages.
* `firebase/`: Custom `MessagingService` extending `FirebaseMessagingService` to handle incoming notification payloads.
* `utilities/`: `Constants` for database keys and `PreferenceManager` for session management.

## Getting Started

### Prerequisites
* Android Studio (latest version recommended)
* Minimum SDK Version: API 24 (Android 7.0) or higher.
* A registered Firebase Project.

### Installation
1. Clone this repository:
   ```bash
   git clone [https://github.com/B0821123/CguFinalProject.git](https://github.com/B0821123/CguFinalProject.git)
