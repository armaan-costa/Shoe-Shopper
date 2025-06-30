# Shoe Shopper 🥿📐
Upload a top-down photo of your insole on a sheet of paper and get shoe recommendations tailored to your exact foot shape.

---

## Tech stack

| Layer      | Main tools / libraries                                    |
|------------|-----------------------------------------------------------|
| Front-end  | **Next.js 15** (App Router) · React 18 · TypeScript · Tailwind CSS |
| Back-end   | **Django 5** · Django REST Framework · django-cors-headers |
| Database   | **SQLite** for local dev → **Production DB TBD** (PostgreSQL or Supabase — final decision by **2025-07-02**) |
| Tooling    | ESLint · Prettier · Node 20 · Python 3.11 |

---

## Prerequisites

* **Python ≥ 3.10** (`python --version`)
* **Node ≥ 20** (`node -v`) & npm ≥ 10 (*`.nvmrc` with `20` is in the repo*)
* Optional: `git config --global core.autocrlf input` if you’re on macOS/Linux

---

## Local setup

### Back-end

```bash
# from repo root
python3 -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install -r backend/requirements.txt
cp backend/.env.example backend/.env   # add your SECRET_KEY, etc.
python backend/manage.py migrate
python backend/manage.py runserver 8000

