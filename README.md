
---

### 📱 B. `mobile-test-farm/README.md`

```markdown
# 📲 Mobile App Testing Infrastructure

Automated mobile testing on **real devices** using cloud test farms (AWS Device Farm / Firebase Test Lab).

This repository shows how to:
- Integrate mobile CI with GitHub Actions
- Upload APK/IPA builds securely
- Trigger tests on real Android/iOS devices
- Collect logs, screenshots, and crash reports

---

## 🧪 Supported Backends

| Provider        | Status     | Notes |
|-----------------|------------|-------|
| AWS Device Farm | ✅ Ready   | Requires AWS account |
| Firebase Test Lab | ⏳ Planned | For Android only |
| BrowserStack    | ❌ Not used | Paid, external |

---

## 🛠️ Workflow Overview

1. Build your APK (e.g., via Gradle)
2. Upload to AWS Device Farm via CLI
3. Schedule test run on selected device pool
4. Poll for completion
5. Download and archive results

> ⚠️ **Note**: AWS credentials must be stored as GitHub Secrets.

---

## 🔐 Secrets Required

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_DEFAULT_REGION` (e.g., `us-west-2`)

---

## 📁 Output

- Test run URL
- Device logs (`logcat.txt`, `system.log`)
- Screenshots & videos (if enabled)
- Crash reports (ANR, native crashes)

---

## 📈 Why This Matters

Mobile apps **behave differently** on real hardware. Emulators miss:
- Sensor interactions
- Memory pressure
- GPU driver quirks
- Network handoffs

Real-device testing is non-negotiable for production apps.

---

Built by **Arkadiy Voronov** — because mobile users deserve flawless experiences.
