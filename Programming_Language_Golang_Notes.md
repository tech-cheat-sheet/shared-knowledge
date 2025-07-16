- [Golang on Ubuntu](#golang-on-ubuntu)
  - [Install via Terminal (Manual Setup)](#install-via-terminal-manual-setup)
- [📚 Mini Go API: Book List](#-mini-go-api-book-list)
  - [1. Create a new file 'main.go'](#1-create-a-new-file-maingo)
  - [2. Compile and run](#2-compile-and-run)
  - [3A. Test with a web browser](#3a-test-with-a-web-browser)
  - [3B. Test with cURL](#3b-test-with-curl)
- [📊 cURL vs. Postman](#-curl-vs-postman)
  - [🧠 TL;DR:](#-tldr)
- [🛠️ Updated main.go – Protect /books Route After Login](#️-updated-maingo--protect-books-route-after-login)
# Golang on Ubuntu
## Install via Terminal (Manual Setup)
```shell
# 0. Open a terminal and run:
hostnamectl | grep -i architecture

# 1. Visit: 
https://go.dev/dl/

# 2. Download the latest tarball for your OS
cd ~/Downloads
wget https://go.dev/dl/go1.24.5.linux-amd64.tar.gz
ls -la | grep -i go

# 3. Extract and move to /usr/local
sudo tar -C /usr/local -xzf go1.24.5.linux-amd64.tar.gz
ls -la /usr/local | grep -i go

# 4. Add Go to your PATH Edit your profile file:
gedit ~/.profile
# then add at the end:
export PATH=$PATH:/usr/local/go/bin
# save & exit

# 5. Reload changes
source ~/.profile

# 6. Verify installation
go version
```
# 📚 Mini Go API: Book List
## 1. Create a new file 'main.go'
```go
package main

import (
    "encoding/json"
    "log"
    "net/http"
)

type Book struct {
    ID     int    `json:"id"`
    Title  string `json:"title"`
    Author string `json:"author"`
}

var books = []Book{
    {ID: 1, Title: "1984", Author: "George Orwell"},
    {ID: 2, Title: "Brave New World", Author: "Aldous Huxley"},
    {ID: 3, Title: "Fahrenheit 451", Author: "Ray Bradbury"},
}

func getBooks(w http.ResponseWriter, r *http.Request) {
    w.Header().Set("Content-Type", "application/json")
    json.NewEncoder(w).Encode(books)
}

func main() {
    http.HandleFunc("/books", getBooks)
    log.Println("🚀 API is running at http://localhost:8080")
    log.Fatal(http.ListenAndServe(":8080", nil))
}
```
## 2. Compile and run
```shell
go run main.go
```
## 3A. Test with a web browser
```shell
Visit http://localhost:8080/books
```
## 3B. Test with cURL
```shell
curl -X POST http://localhost:8080/login \
     -H "Content-Type: application/json" \
     -d '{"username":"admin","password":"secret123"}'

curl -H "Authorization: logged-in-token" http://localhost:8080/books
```
# 📊 cURL vs. Postman
| Feature                 | cURL                                               | Postman                                              |
|------------------------|----------------------------------------------------|------------------------------------------------------|
| **Type**               | Command-line tool                                  | Graphical user interface (GUI) application           |
| **Ease of Use**        | Requires CLI knowledge, less intuitive             | User-friendly with visual controls                   |
| **Installation**       | Built-in or install via package manager            | Requires download and installation                   |
| **Platform Support**   | Cross-platform (Linux, macOS, Windows)             | Cross-platform (Desktop + Web app)                   |
| **Request Types**      | Supports all HTTP methods via flags                | Supports all HTTP methods via dropdowns              |
| **Environment Support**| Manual scripting or shell variables                | Built-in environments and variable management        |
| **Scripting & Automation** | Easy to script in bash or other CLI tools     | Uses Postman Collection Runner and Newman CLI        |
| **Documentation Tools**| Limited                                            | Rich API documentation and sharing features          |
| **Testing Capabilities**| Basic, manual response inspection                 | Advanced testing with test scripts and assertions    |
| **Use Cases**          | Lightweight, automation, terminal workflows        | Interactive API development, testing, collaboration  |
## 🧠 TL;DR:
- Use cURL when you want speed, simplicity, or automation from the terminal.
- Use Postman when you’re working collaboratively, testing APIs extensively, or prefer a visual approach.
# 🛠️ Updated main.go – Protect /books Route After Login
Here’s a version with basic session tracking via an in-memory token. It's simple and works for development or demos.
```shell
package main

import (
    "encoding/json"
    "log"
    "net/http"
    "sync"
)

// Book struct
type Book struct {
    ID     int    `json:"id"`
    Title  string `json:"title"`
    Author string `json:"author"`
}

// Login payload
type LoginRequest struct {
    Username string `json:"username"`
    Password string `json:"password"`
}

var books = []Book{
    {ID: 1, Title: "1984", Author: "George Orwell"},
    {ID: 2, Title: "Brave New World", Author: "Aldous Huxley"},
    {ID: 3, Title: "Fahrenheit 451", Author: "Ray Bradbury"},
}

// In-memory session store
var (
    sessionToken string
    mu           sync.Mutex
)

const (
    validUsername = "admin"
    validPassword = "secret123"
)

// Login handler
func loginHandler(w http.ResponseWriter, r *http.Request) {
    var creds LoginRequest
    err := json.NewDecoder(r.Body).Decode(&creds)
    if err != nil {
        http.Error(w, "Invalid request body", http.StatusBadRequest)
        return
    }

    if creds.Username == validUsername && creds.Password == validPassword {
        // Set fake session token
        mu.Lock()
        sessionToken = "logged-in-token"
        mu.Unlock()

        w.WriteHeader(http.StatusOK)
        w.Write([]byte(`{"message":"Login successful", "token":"logged-in-token"}`))
    } else {
        http.Error(w, `{"error":"Invalid username or password"}`, http.StatusUnauthorized)
    }
}

// Middleware to check login token
func isAuthenticated(r *http.Request) bool {
    token := r.Header.Get("Authorization")
    mu.Lock()
    defer mu.Unlock()
    return token == sessionToken
}

// Protected book handler
func getBooks(w http.ResponseWriter, r *http.Request) {
    if !isAuthenticated(r) {
        http.Error(w, `{"error":"Unauthorized"}`, http.StatusUnauthorized)
        return
    }

    w.Header().Set("Content-Type", "application/json")
    json.NewEncoder(w).Encode(books)
}

func main() {
    http.HandleFunc("/login", loginHandler)
    http.HandleFunc("/books", getBooks)
    log.Println("🚀 Secure API is running at http://localhost:8080")
    log.Fatal(http.ListenAndServe(":8080", nil))
}
```
