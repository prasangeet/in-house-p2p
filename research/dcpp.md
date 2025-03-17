### ✅ **DC++ (Direct Connect) Protocol:**

DC++ (Direct Connect++) is an open-source **peer-to-peer (P2P) file-sharing client** that allows users to **directly share files** over a local network or the internet without relying on a central server.

---

## 📌 **How does DC++ work?**
- **Hub-Based Architecture**: Unlike fully decentralized systems like BitTorrent, DC++ relies on a **central hub server** to handle peer discovery and communication.  
- **Peers connect to a hub**, which acts as a mediator, but **file transfers happen directly between peers (users)**.  
- **Hub manages the file index, user list, and chat functionality** while ensuring security and access control.  
- **Users can search for files shared by others and download them directly.**  

---

## 📌 **ADC Protocol (Advanced Direct Connect Protocol):**
ADC is the **underlying protocol used by DC++**, responsible for communication between hubs and peers.

### 🔗 **ADC Protocol Architecture:**
1. **Hub (Central Node):**
   - Acts as a server that **manages peers (clients)**.
   - Maintains **user metadata**, shared file indexes, and handles **peer authentication**.

2. **Client (Peer Node):**
   - Connects to the hub and **shares file metadata (file name, size, hash)**.
   - Handles **direct peer-to-peer file transfer**.

3. **Direct File Transfer:**
   - Once a file is requested, the **hub facilitates the connection between peers**, but the **file transfer happens directly between them.**

---

## ⚡️ **Key Components of ADC Protocol:**
| Component             | Description                                         |
|----------------|-------------------------------------------|
| **Handshake Protocol** | Authenticates peers and handles connection setup |
| **Search Protocol** | Allows peers to search for files across the hub |
| **File Indexing** | Maintains file hashes and metadata |
| **File Chunking** | Transfers files in chunks for speed optimization |
| **Tiger Tree Hashing (TTH)** | Used to verify file integrity and avoid duplication |
| **Encryption (TLS Support)** | Secures the communication between peers |

---

## ✅ **How Our In-House P2P Project Will Use ADC Concepts:**
| DC++ Concept           | Our Implementation |
|----------------|--------------------|
| Hub-Based Model | Hub Server in C++ (Boost.Asio) |
| Peer Discovery | PostgreSQL for file indexing |
| File Chunking & Hashing | Tiger Tree Hashing (TTH) |
| Direct File Transfer | C++ socket programming |
| Secure Communication | TLS encryption |

---

## 🌐 **Reference Resources:**
- [ADC Protocol Specification](https://adc.sourceforge.net/ADC.html)
- [DC++ Official Documentation](https://dcplusplus.sourceforge.io/)
- [Tiger Tree Hashing Algorithm](https://en.wikipedia.org/wiki/Tiger_tree_hash)
