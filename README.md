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

- [Microsoft.Web.WebView2 NuGet Package](https://www.nuget.org/packages/Microsoft.Web.WebView2)

---

## 🚀 Getting Started

1. **Clone this repo:**

   ```bash
   git clone https://github.com/yourusername/WebView2Sample.git
   cd WebView2Sample
   ```

2. **Open the solution in Visual Studio 2022:**

   - Open `WebView2Sample.sln`

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
/WebView2Sample
├── WebView2Sample.sln         # Visual Studio Solution
├── main.cpp                   # Main source file
├── .gitignore
└── README.md
```

---

## 🛠️ Build Notes

- The app uses `ComPtr` from WRL instead of WIL to minimize dependencies.
- Tested on Windows 11 and Visual Studio 2022 (v17.x).
- The WebView2 SDK is installed via NuGet and automatically linked.

---

## 📝 License

MIT License (or choose your preferred license)

---

## 🤝 Contributing

Pull requests and suggestions welcome!