# Test Approach Document

**Project:** Gmail Compose Functionality Validation  
**Target Capability:** Compose & Send Email Workflow  
**Assessment Criteria:** Subject = `"Incubyte"`, Body = `"QA test for Incubyte"`  
**Role Scope:** Automation & GenAI-Integrated Quality Assurance Engineering  

---

## 1. Executive Strategy & Test Objectives
The primary focus of this testing cycle is to establish absolute functional reliability, data sanitization integrity, and user experience resilience for the Gmail Compose window modal. Testing validates that core workflows conform strictly to requirements while demonstrating that edge cases, network disruptions, script injection threats, and rich media assets (such as auto-signatures and banners) degrade gracefully without breaking application availability.

---

## 2. Testing Types & Scope Matrix

### In-Scope Verification Focus
* **Functional Testing:** Creation, formatting, draft saving, transmission, and validation of emails within the *Sent* folder.
* **Boundary & Input Validation:** Extreme character limitations, blank fields handling, whitespace trimming, and invalid international domain rejection rules.
* **Negative & Exception Testing:** Network drops mid-flight, concurrent click race-conditions, invalid session tokens, and scheduling failures.
* **UI & Responsive UX Testing:** Compose modal scaling during browser zoom transitions, multi-window minimization behaviors, and layout preservation across screen profiles.
* **Security & Sanitation Testing:** Verifying non-execution of active HTML/XSS scripts wrapped in field strings.

---

## 3. Engineering Workflows: Combining GenAI with Manual QA
This approach models advanced modern QA practices by dividing test engineering tasks into a symbiotic **AI-Plus-Human Architecture**:


[ GenAI Engine ] ──────> Generates Baseline Flows & Generic Outlines
│
▼
[ Manual Engineering ] ──> Corrects & Refines Specific Assessment Strings ("Incubyte")
│
▼
[ Advanced Manual QA ] ──> Engineers Edge Cases, Media Layouts, & Security Scenarios


1. **Accelerated Bootstrapping (GenAI):** GenAI models were targeted to generate foundational sanity checks and generic structural frameworks (`AI_001` - `AI_015`).
2. **Deterministic Correction:** Every AI-produced text matrix was manually evaluated and re-written to strictly integrate specific requirements, ensuring no generic boilerplate strings remained.
3. **Advanced Manual Layering:** Specialized high-severity edge cases were added entirely by hand. 
---

## 4. Defect Severity Classification Matrix
To help project teams prioritize engineering triage cycles, every traditional scenario is mapped to a strict, impact-driven severity scale:
* **Critical:** Core email transmission fails entirely, or application crashes/freezes with no structural workaround.
* **High:** Features fail to execute as requested (e.g., character data corruption inside the Sent folder, or failure to auto-save drafts).
* **Medium:** Validation warnings fail to display, or functional elements behave incorrectly under specialized network/boundary bounds.
* **Low:** minor interface anomalies, cosmetic alignment variations, or non-blocking keyboard/zoom quirks.
