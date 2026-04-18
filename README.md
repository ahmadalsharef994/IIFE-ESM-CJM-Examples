# JavaScript Module Systems: IIFE, ESM, CommonJS

<p align="center">
  <img src="https://img.shields.io/badge/javascript-ES2020+-yellow?logo=javascript" alt="JavaScript">
  <img src="https://img.shields.io/badge/Node.js-18+-green?logo=node.js" alt="Node.js">
  <img src="https://img.shields.io/badge/Jenkins-CI%2FCD-red?logo=jenkins" alt="Jenkins">
  <img src="https://img.shields.io/badge/modules-IIFE%20%7C%20ESM%20%7C%20CJS-blue" alt="Modules">
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License">
</p>

Side-by-side **code examples** comparing the three JavaScript module systems — IIFE, ECMAScript Modules (ESM), and CommonJS (CJS) — plus a Jenkins CI/CD pipeline to automate testing and delivery.

---

## 📖 What This Covers

| Pattern | File | Use case |
|---|---|---|
| **IIFE** | `IIFE.js` | Encapsulate code without a module system (legacy browsers, scripts) |
| **CommonJS** | `CJM.js` | Node.js standard module system (`require` / `module.exports`) |
| **ESM** | `ESM.js` | Modern JavaScript native modules (`import` / `export`) |

---

## 🔍 Key Differences

```mermaid
flowchart TD
    subgraph "IIFE (Immediately Invoked)"
        I1["(function() { ... })()"] --> I2["No exports\nSelf-contained scope"]
    end
    subgraph "CommonJS (CJS)"
        C1["module.exports = ..."] --> C2["require('./module')"]
        C2 --> C3["Synchronous\nNode.js default"]
    end
    subgraph "ESM (ES Modules)"
        E1["export default ..."] --> E2["import x from './module.js'"]
        E2 --> E3["Async / static analysis\nBrowser + Node.js"]
    end
```

---

## 🚀 Run the Examples

```bash
git clone https://github.com/ahmadalsharef994/IIFE-ESM-CJM-Examples.git
cd IIFE-ESM-CJM-Examples

node IIFE.js
node CJM.js
node ESM.js      # requires "type": "module" in package.json or .mjs extension
```

---

## ⚙️ Jenkins Pipeline

The included `Jenkinsfile` sets up a CI pipeline with Test and Deliver stages:

```
Pipeline: Install → Test → Deliver
```

```bash
# Stages defined in .jenkins/
├── Jenkinsfile
└── .jenkins/
    ├── test.sh
    └── deliver.sh
```

---

## 📄 License

MIT
