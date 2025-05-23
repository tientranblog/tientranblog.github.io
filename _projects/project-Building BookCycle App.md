---
title: Building BookCycle App
excerpt: A user-friendly platform for trading books
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/cda06a3e28042dad2b262c018a106a08.png
---
### Business Scenario

BookCycle is designed to provide a seamless, user-friendly platform for individuals to buy, sell, and manage books. The application connects book sellers and buyers, allowing users to upload books for sale, browse available books, and directly contact sellers. The platform leverages Firebase for authentication, storage, and real-time data management, ensuring a reliable and scalable solution for book trading.

### Techniques

- **Platform:** Android
- **Language:** Kotlin
- **UI:** Android XML layouts with Material Design components
- **Build System:** Gradle (Kotlin DSL)
- **Components:**
	- **UI Widgets**:
	    - `EditText` for email and password input (`edtEmail`, `edtPassword`)
	    - `Button` for submitting the sign-in form (`btnSubmit`)
	    - `TextView` for navigation to sign-up and forgot password screens (`txtSignUp`, `txtForgotPassword`)
	- **RecyclerView & Adapters**: Efficient display of book lists and user books.
	- **Intents**: For navigating between activities (`HomeActivity`, `SignUpActivity`, `UpdatePasswordActivity`).
	- **Toast**: For displaying short messages to the user.
	- **Firebase Authentication**: `FirebaseAuth` is used for user sign-in with email and password.
	- **Firestore:** for data storage, and Firebase Storage for images.


### Workflow

Step 1: **User Registration & Authentication**
- Users sign up or sign in using their email and password.
- Password reset functionality is available for account recovery.
Step 2: **Profile Management**
- Users can view and update their profile details, including name, email, phone, address, and postal code.
Step 3: **Book Management**
- Users can upload books for sale, including details such as title, author, category, description, price, contact info, and an image.
- Users can view and delete their uploaded books.
Step 4: **Book Discovery**
- All users can browse the list of available books.
- Search and filter functionality allows users to find books by title or category.
Step 5: **Contact Seller**
- Buyers can contact sellers via SMS or email directly from the book details page.

### Functionalities

- User authentication (sign up, sign in, password reset)

<img src="/assets/obsidian/0fb06eddd4c3de03387aace91ad49ac9.png" />

<img src="/assets/obsidian/e51c569f5cc80e8228079f449e1a9283.png" />

- Profile view and update

<img src="/assets/obsidian/32525317a9abebc5e5f91403c0b84ef8.png" />

- Upload, view, and delete books

<img src="/assets/obsidian/bdba784dbf9343145b6df86f90091fda.png" />

<img src="/assets/obsidian/57be6f0b730df5fecf37f819683f9669.png" />

- Browse all books with search and category filter

<img src="/assets/obsidian/cda06a3e28042dad2b262c018a106a08.png" />

<img src="/assets/obsidian/0ef0075036dc3fc4e9ab4745969bf13d.png" />

- Contact seller via SMS or email

<img src="/assets/obsidian/c5ba3639a873123bdc590b9492d2947e.png" />


### Demo

<iframe width="560" height="315" src="https://www.youtube.com/embed/7-ZVZk0H8uo?si=nwBECvhmEYDxpAn9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

