# 🍛 Taste of Tamil Nadu — Mobile App

A mobile app for *Taste of Tamil Nadu*, an authentic South Indian restaurant. It is built to work on both Android and iPhone from one codebase.

---

## 📱 Screenshots

<table>
  <tr>
    <td align="center"><img src="screenshots/01_splash_screen.png" width="220" alt="Splash screen"/><br/><b>Splash</b><br/><sub>Restaurant logo shown on launch</sub></td>
    <td align="center"><img src="screenshots/02_onboarding_welcome.png" width="220" alt="Welcome slide"/><br/><b>Welcome</b><br/><sub>Introduction to the restaurant</sub></td>
    <td align="center"><img src="screenshots/03_onboarding_cafe.png" width="220" alt="Cafe slide"/><br/><b>A Cafe Beyond Ordinary</b><br/><sub>"Relax, sip, and savor the moment"</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="screenshots/04_onboarding_coffee_tea.png" width="220" alt="Coffee and tea slide"/><br/><b>Finest Coffee, Purest Tea</b><br/><sub>"Brewed just for you"</sub></td>
    <td align="center"><img src="screenshots/05_onboarding_meals.png" width="220" alt="Meals slide"/><br/><b>From Meals to Biscuits</b><br/><sub>"Always cooked fresh"</sub></td>
    <td align="center"><img src="screenshots/06_home_screen.png" width="220" alt="Home screen"/><br/><b>Home</b><br/><sub>Promotions, menu categories and dish photos</sub></td>
  </tr>
</table>

<table>
  <tr>
    <td align="center"><img src="screenshots/07_about_us.png" width="220" alt="About Us screen"/><br/><b>About Us</b><br/><sub>Story, mission, vision and opening hours</sub></td>
    <td align="center"><img src="screenshots/08_about_feedback.png" width="220" alt="Feedback form"/><br/><b>Feedback</b><br/><sub>Guests share feedback after logging in</sub></td>
    <td align="center"><img src="screenshots/09_profile.png" width="220" alt="Profile screen"/><br/><b>Profile</b><br/><sub>Log in or sign up to join in</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="screenshots/10_login.png" width="220" alt="Sign up or login screen"/><br/><b>Sign Up / Login</b><br/><sub>Enter a phone number</sub></td>
    <td align="center"><img src="screenshots/11_otp.png" width="220" alt="Verification screen"/><br/><b>Verification</b><br/><sub>Enter the 6-digit code</sub></td>
    <td align="center"><img src="screenshots/12_complete_profile.png" width="220" alt="Complete profile screen"/><br/><b>Complete Profile</b><br/><sub>Username, optional email and birthdate</sub></td>
  </tr>
</table>

---

## ✨ What the App Does

* **Welcome walkthrough:** Four intro slides introduce the restaurant. Users can swipe or tap **Next**, then **Get Started** to enter the app.
* **Home screen:** A friendly *Vanakkam* greeting, a "What's for today?" section showing when it was last updated, and pull-to-refresh to reload.
* **Promotions banner:** Promotional images are built into the app and appear as a swipeable banner.
* **Menu categories:** Four categories (Tiffin, Roti Canai, Dosa Treats, Chicken), each with its own dishes and photos. Dishes that are sold out appear faded.
* **About Us:** The restaurant's story, mission, vision, address (tap to open in Maps), opening hours, and a feedback form.
* **Profile:** Log in or sign up, or view your details and log out.
* **Easy navigation:** Three tabs at the bottom: **Home**, **About Us**, and **Profile**.

---

## 🚧 Current Status

This is an early version of the app, and some parts are still placeholders:

* **Menu:** The categories and dishes are sample content. Dish names and prices will be updated once the restaurant's real menu is confirmed. Photos are from free-license sources (see the credits file in the app project).
* **Accounts:** Sign up and login use a phone number and a verification code. The code is not checked yet, and no SMS is sent, so any code works. Accounts are not saved between app launches.
* **Feedback:** Logged-in guests can send feedback from the About Us tab, but feedback is not stored yet. It shows a thank-you message after submitting.

> **Note on project status:** This app was built as a client product for the *Taste of Tamil Nadu* restaurant. After the restaurant's physical business closed, this repository was kept as a showcase of the app's design and mobile engineering work.

---

## 🛠️ Built With

* **React Native** and **TypeScript** for the app
* **Wikimedia Commons** photos for the menu (free-license, credited)
* **Android and iOS** native projects

For setup steps, versions, and architecture details, see [TECHNICAL_NOTES.md](TECHNICAL_NOTES.md).

---

## 👤 Developer

* **Developer:** Gokul Nath ([@GokulNath20](https://github.com/GokulNath20))
* **Role:** Mobile Application Developer (React Native & Native Tooling)
