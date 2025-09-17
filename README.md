# RollCall Rooms

A **secure, fast, and proxy-proof attendance management system** built as a full-stack web application.
It leverages **dynamic QR codes** to ensure that attendance can only be marked in real time by physically present participants.

---

## 🏆 Core Idea

Traditional attendance methods are slow and prone to proxies.
This system solves both by:

* Generating **time-bound, auto-refreshing QR codes**.
* Embedding a **secure session token** within the QR for validation.
* Validating scans server-side before marking attendance.

Result:
**No QR reuse, no fake check-ins, and drastically reduced attendance time.**

---

## ⚡ Workflow Overview

1. **Admin Generates QR** → Session-specific token embedded.
2. **QR Auto-Updates** every set interval (e.g., 20–30s).
3. **Students Scan** using any device with a camera.
4. **Server Verifies** → Token validity, expiry, and one-time usage.
5. **Attendance Stored** securely in the backend.

---

## 🛠 Tech Highlights

**Frontend:**

* React.js for dynamic UI and real-time QR updates.
* HTML, CSS, JavaScript for responsive design.

**Backend:**

* Node.js with Express.js API endpoints.
* Token-based security (JWT/session tokens).

**Data Layer:**

* MongoDB (for development; removed from public commits for security).

**Other Key Tools:**

* QR Code generation via npm libraries.
* Token expiry handling for anti-proxy measures.

---

## 🔒 Security Measures

* **Dynamic Token Rotation** — QR content changes before it can be shared.
* **One-Time Validation** — Scans are marked invalid if reused.
* **Short Expiry Windows** — Tokens expire within seconds to prevent abuse.
* **DB Credentials Sanitization** — No sensitive configs committed to repo.

---

## 🎯 Impact

* **Attendance Time** reduced from minutes to seconds.
* **Eliminated Proxy Attendance** with dynamic QR rotation.
* **Scalable Design** ready for deployment in classrooms, events, or corporate meetings.

---

## 📜 License

Licensed under the **MIT License** with additional clauses to protect source usage and redistribution specifics (see `LICENSE` file for full terms).


