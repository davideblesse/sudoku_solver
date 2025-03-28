# Sudoku Solver

Welcome to **Sudoku Solver** – a complete, multi-module system for capturing, processing, and solving Sudoku puzzles. This repository ties together several key components:

- A **Flutter client** for capturing or selecting puzzle images.
- A **FastAPI server** that processes images (using OpenCV and Tesseract OCR) and solves puzzles with a custom DFS algorithm.
- A secure **Authentication service** using MongoDB Atlas and JWT (HS256).

This repository serves as the central hub for the entire project, providing an overview, integration instructions, and links to the individual modules.

---

## 🚀 What It Does

- **Capture & Process:**  
  The mobile client allows you to capture or select a Sudoku puzzle image. The image is sent to the server where OpenCV preprocesses it and Tesseract OCR extracts the grid digits.

- **Solve:**  
  The server then applies an efficient DFS algorithm (inspired by Peter Norvig’s approach) to compute the solution and returns it for display in the client app.

- **Secure Access:**  
  The authentication module ensures that user registration and login are secure, managing sessions with JWT tokens.

---

## 🛠️ Modules Overview

1. **[Client (Flutter)](https://github.com/davideblesse/sudoku-solver-client)**  
   The mobile interface that lets users capture/upload puzzles and view the solved grid.

2. **[Server (FastAPI)](https://github.com/davideblesse/sudoku-solver-server)**  
   The backend service that handles image processing, OCR, and puzzle solving.

3. **[Auth (MongoDB + JWT)](https://github.com/davideblesse/sudoku-auth)**  
   The authentication service that securely registers and logs in users.

Each module has its own detailed README. This central repository provides a top-level view and instructions for setting up and integrating all components.

---

## 📁 Repository Structure

Below is a high-level look at the structure of this repository:

```plaintext
sudoku_solver/
├── client/        # Flutter mobile client submodule
├── server/        # FastAPI server submodule
├── auth/          # Authentication service submodule
└── README.md      # You are here!
```

## 🚀 Getting Started

### 1. Clone This Repository with Submodules

It’s recommended to clone recursively to pull in the submodules simultaneously:

```bash
git clone --recursive https://github.com/davideblesse/sudoku_solver.git
cd sudoku_solver
```

> **Note:** If you already cloned without --recursive, you can still pull submodules with:
>
```bash
git submodule update --init --recursive
```

### 2. Set Up Each Module

- **Client (Flutter):**  
  Refer to the [Client README](client/README.md) for instructions on installing dependencies and running the Flutter app. You’ll need Flutter SDK, Dart, and an emulator/device.

- **Server (FastAPI):**  
  Check out the [Server README](server/README.md) for steps to install Python dependencies, run FastAPI locally, or build Docker containers.

- **Auth (MongoDB + JWT):**  
  See the [Auth README](auth/README.md) to configure environment variables (Mongo URI, JWT secret) and run the service.

### 3. Connect the Dots

1. **Run the Auth Service** so that user registration and login are available.
2. **Run the Server** to handle image OCR, Sudoku solving, and puzzle processing.
3. **Run the Client** to capture or upload puzzle images, send them to the server, and show solutions.

Optionally, you can containerize some or all services (Auth + Server) and run them alongside the client for a fully containerized setup.