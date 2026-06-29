# 📘 Astra AI — MuleRun Development Logs

This section documents the development journey of **Astra AI**, from the initial idea to continuous improvements and feature refinements.

---

<details>
<summary><b>1. Idea Creation</b></summary>
<br>
<img src="/logs/src/idea_creation_astra_ai.jpg" width="800">
</details>

---

<details>
<summary><b>2. Menu & Feature Development</b></summary>
<br>
<img src="/logs/src/menu_feature_development_astra_ai.jpg" width="800">
</details>

---

<details>
<summary><b>3. Bitget API Integration</b></summary>
<br>
<img src="/logs/src/bitget_api_integration_astra_ai.jpg" width="800">
<br><br>
<img src="/logs/src/bitget_api_integration2_astra_ai.jpg" width="800">
<br><br>
<img src="/logs/src/bitget_api_integration3_astra_ai.jpg" width="800">
</details>

---

<details>
<summary><b>4. Deploy & UI/UX Refinement</b></summary>
<br>
<img src="/logs/src/deploy_ui_ux_refinement_astra_ai.jpg" width="800">
</details>

---

<details>
<summary><b>5. Continuous Improvements</b></summary>
<br>
<img src="/logs/src/continuous_improvement_astra_ai.jpg" width="800">

<br><br>

### 📅 27-06-2026 — 01:30 UTC

#### Frontend Fixes (`app.js`)
- Fixed eligibility wrapper mismatch (`evaluation.eligible`)
- Fixed LONG/SHORT side case mismatch for UI color state
- Fixed missing `ptEntry` element → now uses `ptLimitPrice`
- Order type auto-switches to **LIMIT** for playbook entries
- Synced side button active state when updated programmatically
- Playbooks now reload properly when trading symbol changes

#### Backend Improvements (`server.js`)
- Added tech-field pre-validation for all evaluators
- Added detailed `reasons[]` and `blockers[]`
- Added `safeEvaluatePlaybook()` validation wrapper
- Funding / LSR fetch failures no longer break response
- Added insufficient candle protection (`< 60 candles`)
- Improved flat + nested evaluation response compatibility
- Adjusted funding squeeze thresholds (`1.5 / 0.7`)
- Refined Donchian breakout stop-loss logic

#### UI Improvements
- Added:
  - `.pb-card.neg`
  - `.pb-tag.neg`
  - `.pb-reasons`
- Evaluation grid now responsive on mobile
- Cards now show:
  - **Why** → when setup is active
  - **Blocked By** → when setup fails

#### Verification
✅ `trend_follow_ema` successfully returns:
- `eligible: true`
- `side: SHORT`
- All 8 playbooks evaluated without errors

<br>

<img src="/logs/src/update_improvement1.jpg" width="800">

</details>
