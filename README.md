# **In-House P2P File Sharing System - Roadmap & README**

## **📌 Project Overview**

The In-House P2P File Sharing System is a decentralized peer-to-peer (P2P) file-sharing system optimized for closed environments like university campuses and organizational networks. Inspired by **DC++**, it enables users to securely share files without reliance on external cloud storage.

---

## **📌 Roadmap**

### **Research & Planning**

✅ Understand DC++ and ADC Protocol basics\
✅ Design the **P2P architecture** (Hub-based vs. Fully decentralized)\
✅ Define the **communication protocol** (WebSockets, gRPC, or custom TCP/UDP)\
✅ Select the **tech stack**:

- **Frontend:** Next.js (React framework for UI)
- **Backend:** Django (API, database management, authentication)
- **Networking Module:** C++ (Boost.Asio for peer discovery & file transfers)
- **Database:** PostgreSQL (Stores shared file metadata and user sessions)
- **Security:** TLS for encrypted communication, authentication system

### **Backend Development**

✅ Implement **Django backend** for API & metadata management\
✅ Develop **authentication & access control** in Django\
✅ Implement **File Indexing & Search** using PostgreSQL\
✅ Develop **WebSocket-based real-time updates**\
✅ Implement **C++ networking module** for peer discovery & file transfers

### **Frontend & Communication**

✅ Create Next.js **dashboard for file sharing & search**\
✅ Establish **WebSocket-based communication** with the backend\
✅ Implement **real-time updates** for shared files and peer availability\
✅ Optimize UI for **easy file browsing & downloads**

### **Optimization & Security**

✅ Implement **rate limiting & bandwidth optimization**\
✅ Optimize **file chunking & hashing (Tiger Tree Hashing - TTH)**\
✅ Deploy **Dockerized PostgreSQL + Backend on cloud/local server**\
✅ Set up **logging & monitoring** using Prometheus/Grafana\
✅ Conduct **extensive testing & bug fixes**

### **Deployment & Finalization**

✅ Deploy application on **Linux/Windows/MacOS** using Docker\
✅ Write **detailed documentation & API reference**\
✅ Perform **final security audits & stress testing**\
✅ Release **stable version & future update roadmap**

---

## **📌 Features**

- **P2P File Sharing:** Directly transfer files between peers using efficient chunking.
- **Django Backend:** Manages authentication, metadata storage, and indexing.
- **C++ Networking Module:** Handles peer discovery and file transfers.
- **Hub-Based Discovery:** Centralized hub server maintains an index of shared files.
- **Real-Time Search:** Search files across peers with quick results.
- **Secure Connections:** TLS encryption + authentication for safe transfers.
- **Multi-Platform Support:** Runs on Windows, macOS, and Linux.
- **Bandwidth Optimization:** Rate limits and segmented downloads for smooth performance.

---

## **📌 System Architecture**

- **Frontend (Next.js):** User dashboard for searching & managing shared files.
- **Backend (Django):** Manages API endpoints, authentication, and metadata storage.
- **Networking Module (C++):** Manages peer discovery & file transfers.
- **Database (PostgreSQL):** Stores shared file metadata, user sessions, and access logs.
- **Security:** Encrypted file transfers, JWT authentication, and access control.

---

## **📌 Tech Stack**

| Component      | Technology                           |
| -------------- | ------------------------------------ |
| **Frontend**   | Next.js (React.js framework)         |
| **Backend**    | Django (REST API, authentication)   |
| **Networking** | C++ (Boost.Asio for peer discovery) |
| **Database**   | PostgreSQL (Stores metadata)         |
| **Security**   | TLS encryption, JWT authentication   |
| **Deployment** | Docker (for database & backend)      |

---

## **📌 Project Folder Structure**

```
📂 in-house-p2p
├── 📂 backend            # Django Backend for API & metadata management
│   ├── 📂 api            # Django app for file management API
│   │   ├── models.py     # Database models (File metadata, users, sessions)
│   │   ├── views.py      # API endpoints for file search & management
│   │   ├── urls.py       # URL routing
│   │   └── consumers.py  # WebSocket handling
│   ├── 📂 config         # Django settings & config files
│   ├── manage.py         # Django management script
│   └── README.md         # Backend documentation
├── 📂 networking         # C++ networking module for peer discovery & transfers
│   ├── hub_server.cpp    # Main hub server logic
│   ├── peer_handler.cpp  # Peer-to-peer connection handling
│   ├── file_transfer.cpp # File chunking & transfer logic
│   ├── CMakeLists.txt    # CMake build system
│   └── README.md         # Networking documentation
├── 📂 frontend           # Next.js frontend for UI
│   ├── 📂 src            # React components & pages
│   ├── package.json      # Frontend dependencies
│   ├── next.config.js    # Next.js config
│   └── README.md         # Frontend documentation
├── 📂 database           # PostgreSQL database setup
│   ├── init.sql          # Schema & table creation
│   ├── queries.sql       # SQL queries for indexing & search
│   └── README.md         # Database documentation
├── 📂 deployment         # Docker & deployment scripts
│   ├── Dockerfile        # Backend containerization
│   ├── docker-compose.yml # Multi-container setup
│   └── README.md         # Deployment instructions
└── README.md             # Overall project documentation
```

---

## **📌 Progress & Steps Completed Today**

1. **Installed Boost Library:** Configured Boost C++ Libraries on Windows.
2. **Set Environment Variables:** Added `BOOST_ROOT` and `BOOST_INCLUDE_PATH`.
3. **Verified Boost Installation:** Compiled and ran a test program.
4. **Configured VS Code:** Updated `includePath` to recognize Boost headers.
5. **Compiled First C++ Program with Boost:** Successfully built and executed the test program using `g++`.
6. **Decided on Django for the Backend:** Shifted authentication, metadata storage, and API handling to Django.

---

## **📌 Installation & Setup**

### **1️⃣ Setting Up Django Backend**

```bash
cd backend
python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
pip install django djangorestframework channels psycopg2
python manage.py migrate
python manage.py runserver
```

### **2️⃣ Running the Next.js Frontend**

```bash
cd frontend
npm install
npm run dev
```

### **3️⃣ Running the C++ Networking Module**

```bash
g++ -o server hub_server.cpp -lboost_system -lpqxx -lpq
./server
```

---

## **📌 Future Enhancements**

✅ **Decentralized Mode:** Fully P2P mode without hubs\
✅ **Mobile App:** Android/iOS support\
✅ **AI-Based File Categorization**\
✅ **Anonymity Mode:** Peer masking using onion routing

---

## **📌 License**

This project is **open-source** under the **MIT License**.

---

## **📌 Contact & Support**

📧 Email: [b23ch1033@iitj.ac.in](mailto:b23ch1033@iitj.ac.in)\
🐙 GitHub: [GitHub Repo Link]\
📌 Documentation: [Project Docs Link]

