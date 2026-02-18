# Sprint X – Test Coverage Report

This report summarizes automated test coverage across both project platforms:

- React Web Application
- Android Kotlin Application

Coverage is generated from automated test runs executed during this sprint.

---

## 1. Tool & Setup

### Web / React Application
- **Languages:** JavaScript (React)
- **Tests:** Jest
- **Coverage Tool:** Istanbul (via npm run coverage)

### Android Application
- **Languages:** Kotlin
- **Tests:** JUnit / Android Instrumented Tests
- **Coverage Tool:** JaCoCo

> Note:
> Istanbul reports line/statement/function metrics, while JaCoCo reports instruction and branch metrics.
> Percentages are therefore comparable at a high level but derived differently internally.

---

## 2. Coverage Metrics (REQUIRED)

### Platform Metrics

| Platform | Line / Instruction Coverage | Branch Coverage | Function Coverage | Statement Coverage |
|---|---:|---:|---:|---:|
| React Web | 18.68% | 17.80% | 16.66% | 18.07% |
| Android App | 20.78% | 12% | N/A | N/A |

Android totals derived from JaCoCo summary. :contentReference[oaicite:1]{index=1}

---

### ⭐ Overall Combined Coverage (Sprint Total)

Weighted by total executable lines/instructions across platforms.

- React/Firebase: **253 / 1354**
- Android: **900 / 4332** :contentReference[oaicite:2]{index=2}

**Overall Coverage:**

```
1153 / 5686 = 20.28%
```

This represents the current total automated test reach across the full project stack.

---

## 3. Scope of Coverage

### Included
- React components, hooks, and Firebase logic
- Android Activities, adapters, and helper utilities inside `com.example.bonfire`

### Excluded (and why)
- Static assets (images, svg, png)
- CSS styling files
- Android XML layouts (non-executable UI declarations)
- Third-party libraries and SDK internals

These exclusions ensure coverage reflects only code owned and maintained by the team.

---

## 4. Coverage Trend

| Sprint | Overall Coverage |
|---|---:|
| Sprint X-1 | N/A |
| Sprint X | 20.28% |

Baseline sprint — no prior comparison available.

---

## 5. Weak Areas (Honest Reflection)

Coverage gaps are primarily caused by UI-driven architecture and Firebase-dependent flows.

### React Application
1. **NotificationListener.jsx (~1%)**  
   Event-driven listeners require mocking Firebase observers; testing strategy still evolving.

2. **Messages.jsx (~3%)**  
   Complex async UI logic; prioritized feature work over tests this sprint.

3. **useFriends.js / useChat.js (~1–2%)**  
   Hooks tightly coupled to backend services; isolation refactor planned.

### Android Application
1. **FriendAddActivity (0%)** :contentReference[oaicite:3]{index=3}  
   Heavy UI navigation logic; Espresso tests not implemented yet.

2. **AccountActivity / SignInActivity / SignUpActivity (0%)** :contentReference[oaicite:4]{index=4}  
   Authentication workflows depend on Firebase; mocking infrastructure still under development.

3. **MessageAdapter (12%)** :contentReference[oaicite:5]{index=5}  
   RecyclerView testing requires additional test doubles and instrumentation setup.

Overall, backend logic and core messaging flows received higher priority for testing this sprint.

---

## 6. Evidence

- React Coverage Report: [PASTE REPO LINK HERE]
- Android JaCoCo Report: [PASTE REPO LINK HERE]

---

## 7. Statement of Integrity

> “This coverage was generated from automated tests executed during this sprint.”
