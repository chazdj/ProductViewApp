# Product View App 

## Overview
Product View App is an Android application that displays a catalog of products stored locally in an SQLite database. Users can select multiple products, view the selected items on a second screen, and share the product details via email.

## Features
- Scrollable product list with images, names, descriptions, and prices  
- Multi‑select products using checkboxes  
- Pass selected products to another screen using Parcelable  
- Share selected product details through email  
- Fully offline — no network access required  

## Tech Stack
- Java (Android SDK)  
- Android Studio  
- SQLite local database  
- Parcelable for inter‑activity data transfer

## Project Structure
- `activities/` — Main and secondary activities for UI screens  
- `adapters/` — Adapter binding product data to RecyclerView  
- `database/` — SQLite helper for storing and retrieving products  
- `models/` — `Product` data class implementing Parcelable  
- `res/layout/` — UI XML layouts  
- `res/drawable/` — Product images and assets

## How to Build and Run
1. Clone the repository
  ```bash
  git clone https://github.com/chazdj/ProductViewApp.git
  ```
2. Open the project in Android Studio
3. Sync Gradle and build the project
4. Run on an emulator or physical Android device

## Usage
1. **Launch the app.**
2. The product catalog will be shown in a scrollable list.
   - ![Product Catolog](screenshots/main_page.png)
4. Tap the checkboxes to select products.
   - ![Selected items](screenshots/selected_items.png)
6. After selecting at least 3 products, tap the **Next** button.
8. The app navigates to the next screen to display your selections.
   - ![Display Page](screenshots/second_page.png)
9. To share your selection, tap the **Send via Email** button:
   - This opens your email app with the product details pre-filled.
   - Choose the recipient and send the email.
   - ![Email Render](screenshots/email_rendered.png)
   - ![Email](screenshots/email.png)

## What I Learned
- Working with RecyclerView and custom adapters
- Using SQLite for persistent local storage
- Passing data between screens with Parcelable
- Integrating Android intents to send email from the app

### Notes
> - All product data is stored locally in SQLite.
> - The database is **reset and repopulated** every time `MainActivity` starts.
> - Product images are stored as byte arrays (BLOB).
> - To view the database click **View > Tool Windows > App Inspection
  ![Database](screenshots/database.png)

## Author
Created by **Chastidy Joanem**  
GitHub: @chazdj(https://github.com/chazdj)
