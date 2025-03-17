### ✅ **Tiger Tree Hashing (TTH) Algorithm** 

The **Tiger Tree Hashing (TTH)** algorithm is a **hash tree (Merkle Tree) structure** used in **DC++ and ADC protocols** for **file integrity verification** and **duplicate detection** in **peer-to-peer (P2P) networks**.

---

## 🔥 **What is TTH?**
Tiger Tree Hashing is a **balanced binary hash tree**, where:
- **Leaves represent small chunks of a file.**
- **Parent nodes represent the hash of two child nodes combined.**
- The **root node (top hash)** represents the **unique fingerprint of the entire file**.

---

## 🛤️ **How TTH Works:**

### 📂 Step 1: **Chunk the file**
- The file is **split into small fixed-size blocks (e.g., 64 KB each)**.
- Each block is **hashed using the Tiger Hash function** (a fast 192-bit cryptographic hash function).

### 🌲 Step 2: **Build the Binary Tree**
- The **hash of two adjacent chunks is combined** to create a **parent node**.
- This process is repeated until a **single root hash is generated**, representing the **entire file’s fingerprint**.

### 🌿 Step 3: **Root Hash Verification**
- If even **one chunk of the file is modified**, the **root hash changes**, allowing **efficient integrity checking.**

---

## 🎯 **Why is TTH Used in DC++?**
| Feature              | Purpose in P2P Networks |
|-----------------|---------------------------|
| **File Integrity Check** | Ensures no data corruption during transfer |
| **Duplicate Detection** | Quickly identifies identical files |
| **Efficient Resumable Downloads** | Only re-download corrupted chunks |
| **Reduced Bandwidth Usage** | No need to hash the entire file repeatedly |
| **Fast Search & Indexing** | Use TTH to search files across peers |

---

## 🌟 **Structure of TTH Binary Tree**
```
          Root Hash
           /   \
      H12       H34
      / \       / \
   H1   H2   H3   H4
```

---

## 🔒 **Tiger Hash Function**
- **Highly secure and fast cryptographic hash.**
- Outputs a **192-bit hash value**.
- Resistant to **collision attacks**.

---

## 🧐 **Why not use SHA-256 or MD5 instead?**
| Tiger Tree Hashing        | SHA-256/MD5 |
|-----------------|------------------|
| Hashes individual file chunks | Hashes the entire file |
| Supports resumable downloads | No chunk-level verification |
| High speed (optimized for 64-bit systems) | Slower than Tiger Hash |
| Reduces redundancy across files | No built-in deduplication |

---

## 📌 **In Our In-House P2P Project:**
- We'll **use TTH to calculate file fingerprints**.
- Store **TTH hashes in PostgreSQL for fast indexing**.
- Allow **partial download & resume functionality**.

---

## 📚 **References:**
- [Tiger Tree Hashing Explained](https://en.wikipedia.org/wiki/Tiger_tree_hash)
- [DC++ TTH Specification](https://dcplusplus.sourceforge.io/)
