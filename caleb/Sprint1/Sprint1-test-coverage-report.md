# Sprint 1 – Bonfire Test Coverage Report

This report summarizes automated test coverage across two project platforms:

- React Web Application
- Android Kotlin Application

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


---

## 2. Coverage Metrics

### Platform Metrics

| Platform | Line / Instruction Coverage | Branch Coverage | Function Coverage | Statement Coverage |
|---|---:|---:|---:|---:|
| React Web | 18.68% | 17.80% | 16.66% | 18.07% |
| Android App | 20.78% | 12% | N/A | N/A |


---

###  Overall Combined Coverage (Sprint Total)

- React/Firebase: **253 / 1354**
- Android: **900 / 4332** :contentReference[oaicite:2]{index=2}

```
1153 / 5686 = 20.28%
```

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

Mostly excluded due to being unnecessary to test. 

---

## 4. Coverage Trend

| Sprint | Overall Coverage |
|---|---:|
| Sprint X-1 | N/A |
| Sprint X | 20.28% |

Baseline sprint — no prior comparison available. Prior Spring gave us a starting point of 0%

---

## 5. Weak Areas (Honest Reflection)

Coverage gaps are primarily caused by UI-driven architecture and Firebase-dependent flows.

### React Application
1. **NotificationListener.jsx (~1%)**  
   Notifications are still being heavily worked on, testing is needed for ensuring compliance with our standards.

2. **Messages.jsx (~3%)**  
   Needs to be worked on, complexity is a bottleneck.

### Android Application

3. **MessageAdapter (12%)** :contentReference[oaicite:5]{index=5}  
   RecyclerView testing requires additional tests and instrumentation setup.

---

## 6. Evidence

- React Coverage Report: [PASTE REPO LINK HERE]
- Android JaCoCo Report: [PASTE REPO LINK HERE]

---

## 7. Statement of Integrity

> “This coverage was generated from automated tests executed during this sprint.”
