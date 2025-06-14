---

## 🗂️ Project Structure

```
node-server-modules/
│
├── server.js               # Main server file (custom HTTP server)
├── osModule.js            # Module demonstrating Node.js 'os' features
├── pathModule.js          # Module demonstrating Node.js 'path' features
├── eventModule.js         # Module demonstrating event handling
└── README.md              # This explanation file
```

---

## 📦 Prerequisites

- Install Node.js from [https://nodejs.org](https://nodejs.org)
- Ensure Node.js and npm are available using:
  ```bash
  node -v
  npm -v
  ```

---

## 1️⃣ HTTP Module - Creating a Custom Server

> `http` is a built-in module in Node.js that allows us to create a basic web server without any external dependencies.

### 🔍 Key Concepts:
- No need for Express or other frameworks.
- The server listens on a specific port (e.g., 3000).
- Handles requests and sends back responses.
- Basic routing can be done using `req.url`.

---

## 2️⃣ OS Module - System Information

> `os` is used to fetch **system-level information**, such as memory, platform, CPU details, hostname, uptime, etc.

### 🔍 Key Functions:
- `os.hostname()` → Returns the host name of the operating system.
- `os.platform()` → Returns the OS platform (e.g., `linux`, `win32`).
- `os.arch()` → Returns the CPU architecture (`x64`, `arm`, etc).
- `os.cpus()` → Gives CPU core info.
- `os.freemem()` / `os.totalmem()` → Memory stats.
- `os.uptime()` → System uptime in seconds.

---

## 3️⃣ Path Module - File and Directory Paths

> `path` provides utilities for working with **file and directory paths** in a cross-platform way.

### 🔍 Key Functions:
- `path.basename()` → Extracts the filename from a path.
- `path.dirname()` → Gets the directory name of a file path.
- `path.extname()` → Extracts the file extension.
- `path.join()` → Joins path segments using correct separators.
- `path.resolve()` → Resolves absolute paths.

---

## 4️⃣ Events Module - Handling Custom Events

> `events` allows you to define and **handle custom events** in Node.js using `EventEmitter`.

### 🔍 Key Concepts:
- `EventEmitter` is a class provided by `events` module.
- You can `.emit()` an event and `.on()` to listen to it.
- Very useful in asynchronous programming.

### 🔍 Example Use Cases:
- Logging system
- Chat applications
- Notification systems
- Custom event-driven applications

---

## 🏗️ Implementation Flow (What Each File Represents)

### `server.js` (Main HTTP Server File)
- Creates an HTTP server using `http.createServer()`.
- Listens for client requests.
- Responds with different messages depending on the URL (e.g., `/`, `/about`).
- Uses `res.write()` to send data and `res.end()` to close the response.

---

### `osModule.js` (System Info Output)
- Imports `os` module.
- Logs system information to console (hostname, memory, platform, etc).
- Can be used to monitor server health/status.

---

### `pathModule.js` (Path Handling)
- Imports `path` module.
- Demonstrates file extension, directory, joining paths, etc.
- Useful when handling file uploads, directory creation, etc.

---

### `eventModule.js` (Custom Events)
- Imports `events` module.
- Creates custom `EventEmitter`.
- Emits and listens for user-defined events.
- Demonstrates how to pass data with events.

---

## 📌 Summary

| Module | Purpose                          | Common Functions/Uses                          |
|--------|----------------------------------|------------------------------------------------|
| `http` | Create custom server             | `createServer`, `listen`, `write`, `end`       |
| `os`   | System-level info                | `hostname`, `platform`, `arch`, `cpus`, `uptime` |
| `path` | File and directory handling      | `join`, `resolve`, `extname`, `basename`       |
| `events` | Custom asynchronous events    | `EventEmitter`, `on`, `emit`                   |

---

## 📚 Further Exploration

- Try combining `fs` module (File System) with `path` to read/write files.
- Explore `process` module for environment variables and runtime data.
- Use external packages like `nodemon` for automatic reloading.

---

## ✅ Best Practices

- Always handle errors with `try-catch` or `error` events.
- Use modular code (separate logic in different files).
- Prefer `path.join()` over hard-coded paths for cross-platform compatibility.
- Never block the main thread (use async methods).

---

## 🧠 Next Steps

- Build a mini REST API with Node.js using only core modules.
- Add file reading using `fs`.
- Create a CLI tool using `os` and `events`.

---
