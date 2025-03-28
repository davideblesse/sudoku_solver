# 🔢 Sudoku Solver – One System to Solve Them All

Welcome to the **Sudoku Solver** ecosystem – a smart, modular, and beautifully engineered system that takes you from snapping a photo of a Sudoku puzzle to getting the solution in seconds. This aggregator is your command center – the place where all the action comes together.

Whether you're into mobile dev, backend APIs, authentication, or just want to flex your puzzle-solving brain, this project has something for you.

---

## 🧠 What’s Inside?

The system is made up of **four modular components**, each designed to work together like pieces of a Sudoku grid:

- 📱 **Client (Flutter Mobile App):**  
  Snap a pic or upload a puzzle. Our mobile app detects the grid, extracts the digits, and sends everything to the server with a slick UI.

- ⚙️ **Server (FastAPI + OpenCV + Tesseract):**  
  Receives the image, processes it, recognizes digits, solves the puzzle using a custom depth-first search (DFS) algorithm, and returns the result.

- 🔐 **Auth (FastAPI + MongoDB + JWT):**  
  Keeps everything secure. Users can register, log in, and get authenticated using industry-standard practices.

- 🧩 **Aggregator (This Repo):**  
  The glue that binds it all. It links the other modules together and gives you the full picture of how the system works as a whole.

---

## 🧭 Architecture At a Glance

1. **User opens the app** → takes a photo of a puzzle  
2. **Client** processes the image and sends it to the **Server**  
3. **Server** extracts digits, solves the puzzle, sends back the solution  
4. **Auth** keeps track of users and issues secure access tokens  
5. Everyone’s happy 🎉

---

## 🚀 Getting Started

Want to see it all in action?

### 1. Clone the Aggregator

```bash
git clone https://github.com/davideblesse/sudoku-solver.git
cd sudoku-solver
```

### 2. Initialize Submodules

```bash
git submodule update --init --recursive
```

### 3. Dive Into Each Module

- [`client/`](https://github.com/davideblesse/client): The Flutter app – grab your phone and solve puzzles on the go.  
- [`server/`](https://github.com/davideblesse/server): The engine behind the scenes – OCR, preprocessing, and solving.  
- [`auth/`](https://github.com/davideblesse/sudoku_auth): Handles users, logins, and tokens like a champ.

Check each folder’s `README.md` for detailed instructions.

---

## 🤝 Contributing

Got an idea? Found a bug? Want to build something wild on top of this?

We welcome PRs, issues, and feature suggestions. Let’s build something awesome together.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

Let’s be honest: you could solve Sudoku puzzles by hand...  
But why do that when you can **build an AI-powered system that does it for you**?

Happy hacking! 💻🧩🔥