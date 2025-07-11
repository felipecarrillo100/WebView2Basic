# WebView2basic

This is a minimal C++ Win32 application that hosts a web app using [Microsoft Edge WebView2](https://learn.microsoft.com/en-us/microsoft-edge/webview2/).

The application opens a native window and displays a local or remote web app using WebView2.

---

## 🧰 Prerequisites

- Windows 11 (or Windows 10 with WebView2 Runtime)
- [Visual Studio 2022](https://visualstudio.microsoft.com/) with:
  - Desktop development with C++ workload
- WebView2 Runtime:
  - ✅ Windows 11 includes it by default
  - 🔧 For Windows 10, download here: https://developer.microsoft.com/en-us/microsoft-edge/webview2/#download-section

---

## 📦 Dependencies

- [WebView2 SDK](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)
- [nlohmann/json](https://github.com/nlohmann/json) for JSON parsing
- [Windows Implementation Library (WIL)](https://github.com/microsoft/wil) for COM helpers

---

## 🚀 Getting Started

1. **Clone this repo:**

   ```bash
   git clone https://github.com/felipecarrillo100/WebView2Basic.git
   cd WebView2Basic
   ```

2. **Open the solution in Visual Studio 2022:**

   - Open `WebView2Basic.sln`

3. **Restore NuGet packages:**

   - Visual Studio should prompt you to restore packages automatically.
   - Or go to `Tools > NuGet Package Manager > Package Manager Console` and run:
     ```bash
     nuget restore
     ```

4. **Build and run:**

   - Press `F5` to build and run the app.
   - A native window will appear and open your configured web app (e.g., `http://localhost:8080/home/`).

---

## 🌐 Hosting Your Web App

To load a local web app, make sure a web server is running on `http://localhost:8080`.

You can change the loaded URL in `main.cpp`:

```cpp
g_webViewWindow->Navigate(L"http://localhost:8080/home/");
```

---

## 📂 Project Structure

```
WebView2Basic/            # Root folder
├── WebView2Basic.sln     # Visual Studio solution file
├── README.md             # This file
└── WebView2Basic/        # Source code folder
    ├── WebView2Basic.cpp
    ├── WebView2Basic.h
    ├── WebView2Basic.vcxproj
    └── packages.config
```

---

## 🛠️ Build Notes

- The app uses `ComPtr` from WRL instead of WIL to minimize dependencies.
- Tested on Windows 11 and Visual Studio 2022 (v17.x).
- The WebView2 SDK, WIL and nlohmann/json are installed via NuGet and automatically linked.

---

## 📝 License

MIT License (or choose your preferred license)

---

## 🤝 Contributing

Pull requests and suggestions welcome!