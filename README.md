# 💰 Investment Buddy

**Smart investing guidance for every generation.**

Investment Buddy is a friendly web app that helps you choose between investment
options by analysing your **age**, **generation**, **account type & usage**, and
**risk tolerance** — then recommends a personalised, risk-appropriate portfolio
with clear visual breakdowns and growth projections.

---

## ✨ Features

- **👤 Personal Profile** — Enter your name & birth year; your **generation is
  auto-detected** (Gen Alpha → Silent Generation) and shapes your strategy.
- **💼 Financial Profile** — Capture your account type (Checking, Savings,
  Brokerage, Roth IRA, 401(k), ISA…), monthly investment amount, income,
  how often you check your accounts, experience level, and time horizon.
- **🧠 Risk Assessment Quiz** — 8 behavioural questions produce a 0–100 risk
  score, refined by age, generation, and account type.
- **📊 Personalised Results:**
  - **Portfolio tab** — Asset-allocation donut chart, per-asset risk badges,
    expected/conservative/optimistic returns, and growth-milestone bar chart.
  - **Growth tab** — 30-year multi-scenario area chart, the power of
    compounding, and Rule-of-72 doubling estimate.
  - **Strategies tab** — Generation-specific advice, concrete product ideas
    (VTI, BND, I-Bonds, high-yield savings, etc.), and an action checklist.
- **🛡️ Smart warnings** — Flags high risk near retirement, low savings rates,
  catch-up contribution reminders, and more.

---

## 🚀 Running it

This app is a **single self-contained HTML file** — no build step, no
`npm install`, no dependencies. Just open it:

```bash
# Option 1: open directly in a browser
open investment-buddy/index.html          # macOS
xdg-open investment-buddy/index.html       # Linux

# Option 2: serve it locally (any static server works)
python3 -m http.server 8000                # then visit http://localhost:8000
```

Everything (logic, styling, charts) is written in vanilla JavaScript and CSS,
so it runs in any modern browser offline.

---

## 🧮 How recommendations are calculated

1. **Base equity** uses the classic *Rule of 110* (equity ≈ 110 − age).
2. **Risk score** from the quiz is adjusted by:
   - **Generation bonus** (younger generations lean more aggressive),
   - **Account type** (e.g. Roth IRA / brokerage push toward growth; checking
     pulls toward liquidity).
3. The blended score maps to one of four risk profiles:
   **Very Conservative → Conservative → Moderate → Aggressive**, each with its
   own asset mix, expected-return band, and product suggestions.
4. **Projections** use standard monthly-compounding future-value maths on your
   monthly contribution.

---

## ⚠️ Disclaimer

Investment Buddy is for **educational purposes only** and is **not financial
advice**. Projections are illustrative estimates based on historical averages;
actual returns vary and past performance does not guarantee future results.
Always consult a qualified financial advisor before investing.
