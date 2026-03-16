# Instagram "Pixel-Perfect" Feed Replica

A highly polished, visually identical replication of the modern Instagram Home Feed built with Flutter. This project was developed as a technical challenge to demonstrate an "obsessive" eye for detail, clean architectural patterns, and advanced gesture handling.

## 🚀 Features

### UI & Interaction
- **Mirror-Exact UI:** Replicated the latest Instagram Home Feed, including the AppBar with Follower/Favorite menu, Stories tray, and Post Feed.
- **Advanced Media Handling:**
  - **Carousel:** Smooth horizontal scrolling for multi-image posts with synchronized dot indicators (`smooth_page_indicator`).
  - **Pinch-to-Zoom:** Using `InteractiveViewer` with custom snap-back animations.
  - **Overlays:** 1/8 page indicators, mute buttons, and floating user tags exactly matching the latest UI.
- **Stateful Interactions:** Instant local UI updates for "Like" and "Save" toggles.
- **Custom Navigation:** Functional "Notifications" and "New Post" screens.
- **Feedback:** Custom Snackbars for unimplemented buttons.

### Technical & Architecture
- **Clean Architecture:** Strict separation of concerns across `models/`, `widgets/`, `providers/`, `repositories/`, and `screens/`.
- **State Management:** Powered by **Provider** for efficient, reactive, and scalable state handling.
- **Mock Data Layer:** `PostRepository` simulates real-world conditions with a **1.5-second latency** to showcase loading states.
- **Loading Strategy:** Professional-grade **Shimmer** effects (skeleton screens) instead of standard spinners.
- **Asset Strategy:** Optimized image loading using `cached_network_image` with high-quality public URLs for memory and disk caching.
- **Infinite Scroll:** Implemented "lazy loading" pagination that fetches the next page of 10 posts seamlessly.

## 🛠️ State Management Choice: Provider

For this project, **Provider** was chosen as the primary state management solution.
- **Efficiency:** It offers a lightweight approach to rebuild only the necessary parts of the widget tree.
- **Readability:** Provides a clean way to separate business logic (in `HomeProvider`) from the UI (in `HomeScreen`).
- **Scalability:** Easily allows for `MultiProvider` setups as the app grows, ensuring that state is accessible exactly where it's needed without "prop drilling."

## 📦 How to Run

Follow these steps to get the project running on your local machine:

1. **Clone the repository:**
   ```bash
   git clone <your-repo-link>
   cd instagram
   ```

2. **Install dependencies:**
   Make sure you have Flutter installed. Then run:
   ```bash
   flutter pub get
   ```

3. **Run the app:**
   Connect your device or start an emulator and run:
   ```bash
   flutter run
   ```

## 📝 Prerequisites
- Flutter SDK: `^3.5.0`
- Dart SDK: `^3.5.0`

---
*Developed with an obsessive eye for detail.*
