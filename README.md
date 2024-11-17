Here's a complete README in English for your monorepo, which includes all the requirements for building and starting the project. You can use this as a template for your GitHub repository.

---

# **Fit Tracking Monorepo**

This project is a monorepo built with **pnpm** and **TurboRepo**, containing two main applications:

- **Server**: A backend application built with NestJS.
- **Mobile**: A mobile application built with Expo.

---

## **System Requirements**

Ensure you have the following installed on your system to work with this monorepo:

### **General Requirements**

1. **Node.js**: Version `>=16.0.0`. Download it from [Node.js](https://nodejs.org).
2. **pnpm**: The package manager used in this project.
   ```bash
   npm install -g pnpm
   ```
3. **Git**: For version control. Download it from [Git](https://git-scm.com).

---

### **Server (NestJS) Requirements**

1. **Nest CLI** (optional, for local development):
   ```bash
   pnpm add -g @nestjs/cli
   ```

---

### **Mobile (Expo) Requirements**

1. **Expo CLI**:

   ```bash
   pnpm add -g expo-cli
   ```

2. **Android Studio** (for Android emulator):

   - Download from [Android Studio](https://developer.android.com/studio).
   - During installation, ensure the following components are selected:
     - **Android SDK Platform-Tools**
     - **Android Emulator**
     - **Android 13 (API level 33)** or a compatible version.

3. **Expo Go App** (optional, for running the app on a physical Android device):
   - Install it from the [Google Play Store](https://play.google.com/store/apps/details?id=host.exp.exponent).

---

## **Getting Started**

### **1. Clone the Repository**

Clone the repository to your local machine:

```bash
git clone https://github.com/MaRrDG/fit-tracking.git
cd fit-tracking
```

---

### **2. Install Dependencies**

Install all the dependencies using pnpm:

```bash
pnpm install
```

---

### **3. Run Applications**

#### **Server (NestJS)**

To start the backend server:

```bash
pnpm --filter apps/server start:dev
```

#### **Mobile (Expo)**

To start the mobile app:

```bash
pnpm --filter apps/mobile start
```

- **Android Emulator**:
  ```bash
  pnpm --filter apps/mobile android
  ```
- **iOS Simulator** (macOS only):
  ```bash
  pnpm --filter apps/mobile ios
  ```
- **Web**:
  ```bash
  pnpm --filter apps/mobile web
  ```

---

## **Building the Applications**

To build all the applications:

```bash
pnpm build
```

This will run the build pipelines defined in **TurboRepo**.

---

## **Troubleshooting**

- If the Android emulator is not detected, ensure Android Studio is installed and configured properly.
- To verify that the Android device/emulator is connected, run:

  ```bash
  adb devices
  ```

- If `pnpm install` fails, try cleaning the workspace and reinstalling:
  ```bash
  rm -rf node_modules pnpm-lock.yaml
  pnpm install
  ```

---

## **Contributing**

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your message here"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature
   ```
5. Open a pull request.

---

## **License**

This project is licensed under the ISC License.

---

With this README, your team should have all the necessary information to clone, build, and run the monorepo. 😊
