# Virtual Environments in Python - Deep Dive

> virtual env are isolated python sandboxes. No polluton. No conflicts. No regrets.

## what is virtual environment?

A **venv** is a self contained directory that contains:
- its own python interpreter.
- its own installed packages
- isolated from the global python system

> TL;DR: you get a clean slate every time, so one's projects's packages dont screw up another's.

---

## why use venv?
| Benifit | Description |
|---------|-------------|
| 🧼 Clean Isolation | Avoids version conflicts across projects |
| 🧪 Testing | Test libraries in different environments |
| 🛡️ Safety | Keeps your global Python install clean |
| 📦 Reproducibility | Easily replicate the environment with `requirements.txt` |

---
# creating venevs(standard way)

<python -m venv venv

# activating the venv

- windows(cmd)  -> venv\Scripts\activate.bat
-windows(powershell) -> venv\Scripts\Activate/ps1

## deactivating
deactivate

# common mistakes: forgotting to activate
If you install packages without activating, they go to the global Python environment. Always check your shell prompt (you’ll see (venv) when it's active).

# what is inside the venv folder?

venv/
├── bin/ or Scripts/
│   ├── python (or python.exe)
│   └── pip
├── lib/
│   └── site-packages/
└── pyvenv.cfg
