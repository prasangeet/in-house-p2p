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
- **Backend:** C++ (Boost.Asio for networking, LibPQ for PostgreSQL)
- **Database:** PostgreSQL (Stores shared file metadata and user sessions)
- **Security:** TLS for encrypted communication, authentication system

### **Backend Development**

✅ Implement **Hub Server** in C++ using **Boost.Asio** for peer discovery\
✅ Develop **Peer-to-Peer file transfer** using direct socket connections\
✅ Implement **File Indexing & Search** using PostgreSQL\
✅ Develop **multi-threaded segmented downloads** for efficient transfers\
✅ Integrate **authentication & access control**

### **Frontend & Communication**

✅ Create Next.js **dashboard for file sharing & search**\
✅ Establish **WebSocket-based communication** with the C++ backend\
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
- **Hub-Based Discovery:** Centralized hub server maintains an index of shared files.
- **Real-Time Search:** Search files across peers with quick results.
- **Secure Connections:** TLS encryption + authentication for safe transfers.
- **Multi-Platform Support:** Runs on Windows, macOS, and Linux.
- **Bandwidth Optimization:** Rate limits and segmented downloads for smooth performance.

---

## **📌 System Architecture**

- **Frontend (Next.js):** User dashboard for searching & managing shared files.
- **Backend (C++):** Manages hub server, peer connections, and file transfers.
- **Database (PostgreSQL):** Stores shared file metadata, user sessions, and access logs.
- **Security:** Encrypted file transfers, JWT authentication, and access control.

---

## **📌 Tech Stack**

| Component      | Technology                           |
| -------------- | ------------------------------------ |
| **Frontend**   | Next.js (React.js framework)         |
| **Backend**    | C++ (Boost.Asio for networking)      |
| **Database**   | PostgreSQL (Stores metadata)         |
| **Networking** | WebSockets or gRPC for communication |
| **Security**   | TLS encryption, JWT authentication   |
| **Deployment** | Docker (for database & backend)      |

---

## **📌 Project Folder Structure**

```
📂 in-house-p2p
├── 📂 backend            # C++ Backend for peer discovery & file sharing
│   ├── 📂 src            # Source files
│   │   ├── hub_server.cpp # Main hub server logic
│   │   ├── peer_handler.cpp # Peer-to-peer connection handling
│   │   ├── file_transfer.cpp # File chunking & transfer logic
│   │   └── database.cpp  # PostgreSQL interactions
│   ├── 📂 include        # Header files
│   ├── 📂 config         # Config files (DB, security settings)
│   ├── CMakeLists.txt    # CMake build system
│   └── README.md         # Backend documentation
├── 📂 frontend           # Next.js frontend for UI
│   ├── 📂 src            # React components & pages
│   │   ├── components    # UI Components (FileList, SearchBar, etc.)
│   │   ├── pages         # Next.js pages (Dashboard, Login, etc.)
│   │   ├── api           # Frontend API calls to backend
│   │   └── styles        # CSS & Tailwind styling
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
│   ├── k8s/              # Kubernetes configurations (if needed)
│   └── README.md         # Deployment instructions
└── README.md             # Overall project documentation
```

---

## **📌 Installation & Setup**

### **1️⃣ Prerequisites**

- Install **PostgreSQL** (Ensure it's running)
- Install **Boost C++ Libraries** (`boost::asio` for networking)
- Install **WebSockets (uWebSockets) or gRPC** for frontend-backend communication
- Install **Docker** (For deployment & containerization)

### **2️⃣ Setting Up PostgreSQL**

```sql
CREATE DATABASE p2p_network;
CREATE TABLE files (
    id SERIAL PRIMARY KEY,
    name TEXT,
    hash TEXT UNIQUE,
    peer_ip TEXT
);
```

### **3️⃣ Running the C++ Backend**

```bash
g++ -o server hub_server.cpp -lboost_system -lpqxx -lpq
./server
```

### **4️⃣ Running the Next.js Frontend**

```bash
cd frontend
npm install
npm run dev
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

📧 Email: [b23ch1033@iitj.ac.in](mailto\:b23ch1033@iitj.ac.in)\
🐙 GitHub: [GitHub Repo Link]\
📌 Documentation: [Project Docs Link]

