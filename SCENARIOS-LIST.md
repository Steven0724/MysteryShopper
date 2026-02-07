# 🎯 Mock Website Test Scenarios - Complete Guide

## Overview
Comprehensive test suite with **category-based scenarios** for testing AI agents. Each category demonstrates multiple related bugs.

---

## 📁 File Structure

```
/mock-websites
  ├── scenario-1-successful.html          ✅ Baseline (no errors)
  ├── functional-errors.html              ✅ 3 functional bugs
  ├── ux-errors.html                      ✅ 3 UX bugs
  ├── ui-visual-errors.html               ✅ 3 UI/visual bugs
  ├── performance-errors.html             ✅ 3 performance bugs
  ├── accessibility-errors.html           ✅ 4 accessibility bugs
  ├── ai-testing-errors.html              ✅ 4 AI-specific bugs
  ├── security-errors.html                ✅ 4 security/trust bugs
  └── scenario-10-captcha.html            ✅ reCAPTCHA challenge
```

**Total:** 9 files | 24 unique bugs | All complete ✅

---

## 🟢 Scenario 1: Successful Baseline
**File:** `scenario-1-successful.html`  
**Category:** Baseline  
**Status:** ✅ Complete

**Description:** Perfect signup flow with no bugs. Use this as the baseline for comparison.

---

## 🟡 Functional Errors
**File:** `functional-errors.html`  
**Category:** Functional  
**Status:** ✅ Complete  
**Bugs:** 3

### Bug 1: Form Validation Missing
- **Issue:** Accepts invalid emails, empty fields, weak passwords
- **Detection:** Check for validation attributes, test with invalid data
- **Difficulty:** Medium

### Bug 2: Fake Success Message
- **Issue:** Shows success when submission actually failed
- **Detection:** Verify actual API response vs displayed message
- **Difficulty:** Hard

### Bug 3: Silent Failure
- **Issue:** No error feedback provided to user
- **Detection:** Check for error message display after failed submission
- **Difficulty:** Hard

---

## 🟠 UX Errors
**File:** `ux-errors.html`  
**Category:** User Experience  
**Status:** ✅ Complete  
**Bugs:** 3

### Bug 1: Dead Button
- **Issue:** Button looks clickable but has `pointer-events: none`
- **Detection:** Test button interactivity, check CSS properties
- **Difficulty:** Medium

### Bug 2: Broken Navigation Links
- **Issue:** Links point to non-existent pages (404 errors)
- **Detection:** Follow links and check for 404 responses
- **Difficulty:** Easy

### Bug 3: Confusing Flow
- **Issue:** Login button registers, Back button logs out
- **Detection:** Verify action matches button label
- **Difficulty:** Hard

---

## 🔴 UI/Visual Errors
**File:** `ui-visual-errors.html`  
**Category:** UI/Visual  
**Status:** ✅ Complete  
**Bugs:** 3

### Bug 1: Broken Layout
- **Issue:** Elements overflow (120vw), navbar overlaps content, footer floats
- **Detection:** Check for overflow, z-index issues, element positioning
- **Difficulty:** Medium

### Bug 2: Non-Responsive Design
- **Issue:** Fixed pixel widths (500px, 400px), no media queries
- **Detection:** Test in mobile viewport, check for responsive design
- **Difficulty:** Medium

### Bug 3: Low Contrast / Invisible Text
- **Issue:** White text on white background, WCAG violations
- **Detection:** Check color contrast ratios, accessibility standards
- **Difficulty:** Easy

---

## 🔵 Performance Errors
**File:** `performance-errors.html`  
**Category:** Performance  
**Status:** ✅ Complete  
**Bugs:** 3

### Bug 1: Slow Loading Page
- **Issue:** Simulates large unoptimized images (5MB each)
- **Detection:** Measure page load time, check resource sizes
- **Difficulty:** Medium

### Bug 2: Infinite Loading Spinner
- **Issue:** Spinner never stops, unresolved promise
- **Detection:** Check for timeout, verify loading state management
- **Difficulty:** Medium

### Bug 3: Render-Blocking JavaScript
- **Issue:** Heavy synchronous JS blocks main thread for 3 seconds
- **Detection:** Analyze critical rendering path, test page responsiveness
- **Difficulty:** Hard

---

## 🟣 Accessibility Errors
**File:** `accessibility-errors.html`  
**Category:** Accessibility (A11y)  
**Status:** ✅ Complete  
**Bugs:** 4

### Bug 1: No ARIA Labels
- **Issue:** Icon-only buttons without aria-label attributes
- **Detection:** Check for aria-label, aria-labelledby attributes
- **Difficulty:** Easy

### Bug 2: Keyboard Navigation Broken
- **Issue:** All inputs have tabindex="-1", Tab key doesn't work
- **Detection:** Test keyboard navigation, check tabindex values
- **Difficulty:** Medium

### Bug 3: Low Contrast
- **Issue:** Text color #cccccc on white (1.6:1 ratio, WCAG requires 4.5:1)
- **Detection:** Calculate contrast ratios (WCAG AA/AAA)
- **Difficulty:** Easy

### Bug 4: Missing Alt Text
- **Issue:** Images without alt attributes
- **Detection:** Check for alt attributes on images
- **Difficulty:** Easy

---

## ⚫ Security/Trust UI Errors
**File:** `security-errors.html`  
**Category:** Security/Trust  
**Status:** ✅ Complete  
**Bugs:** 4

### Bug 1: Fake Security Indicators
- **Issue:** "100% Secure Checkout" claim but page is HTTP (not HTTPS)
- **Detection:** Verify HTTPS, check for misleading security claims
- **Difficulty:** Medium

### Bug 2: Fake Trust Badges
- **Issue:** Displays Norton, McAfee, SSL badges that aren't verified
- **Detection:** Verify badge authenticity, check if clickable
- **Difficulty:** Medium

### Bug 3: Password Visibility Issues
- **Issue:** Password fields use type="text" instead of type="password"
- **Detection:** Check input type, verify password masking
- **Difficulty:** Easy

### Bug 4: No HTTPS Warning
- **Issue:** Collecting SSN and bank account without security warning
- **Detection:** Check protocol, verify security indicators for sensitive data
- **Difficulty:** Easy

---

## 🧠 AI-Specific Testing
**File:** `ai-testing-errors.html`  
**Category:** AI Testing  
**Status:** ✅ Complete  
**Bugs:** 4

### Bug 1: Ambiguous Error Messages
- **Issue:** "Something went wrong" - completely non-informative
- **Detection:** Check error message specificity and usefulness
- **Difficulty:** Medium

### Bug 2: Hidden Errors (Console Only)
- **Issue:** Errors logged to console but no UI feedback
- **Detection:** Monitor console vs UI error display
- **Difficulty:** Hard

### Bug 3: Contradicting UI Signals
- **Issue:** Button says "Saved" but status bar says "Not Saved"
- **Detection:** Check state consistency across UI elements
- **Difficulty:** Hard

### Bug 4: Dark Patterns
- **Issue:** Fake countdown timer (resets at 0) + hidden cancel button
- **Detection:** Identify manipulative UX patterns
- **Difficulty:** Very Hard

---

## 🤖 Special: reCAPTCHA Challenge
**File:** `scenario-10-captcha.html`  
**Category:** Security/Authentication  
**Status:** ✅ Complete

**Description:** Real Google reCAPTCHA v2 integration. Tests AI's ability to handle CAPTCHA challenges.

---

## 📊 Summary Statistics

| Category | File | Bugs | Status |
|----------|------|------|--------|
| Baseline | scenario-1-successful.html | 0 | ✅ |
| Functional | functional-errors.html | 3 | ✅ |
| UX | ux-errors.html | 3 | ✅ |
| UI/Visual | ui-visual-errors.html | 3 | ✅ |
| Performance | performance-errors.html | 3 | ✅ |
| Accessibility | accessibility-errors.html | 4 | ✅ |
| AI Testing | ai-testing-errors.html | 4 | ✅ |
| Security | security-errors.html | 4 | ✅ |
| Special | scenario-10-captcha.html | 1 | ✅ |

**Total:** 9 files | 25 unique bugs | All complete ✅

---

## 🎨 Design Features

All scenarios include:
- ✨ Animated 4-color gradients (unique per category)
- 🌟 Glassmorphism with backdrop blur
- 💫 Floating animations
- 🎯 Bug selector/switcher UI
- 📱 Mobile responsive design
- 🔮 Modern layered shadows
- 🎨 Unique color theme per category

---

## 🧪 Testing Guide

### For AI Agents:
1. **Start with Baseline** - Test scenario-1 to understand normal flow
2. **Test by Category** - Go through each category file
3. **Switch Between Bugs** - Use bug selector buttons
4. **Verify Detection** - AI should identify and report each bug
5. **Check Console** - Bugs log detailed info to console

### For Judges/Demo:
1. **Show Category Organization** - "We have 7 bug categories + baseline"
2. **Demonstrate Bug Switching** - Click bug selector buttons
3. **Show AI Detection** - Run AI agent on each category
4. **Compare Results** - AI report vs actual bugs
5. **Highlight Difficulty** - Show AI handling hard bugs (dark patterns, contradicting UI)

---

## 🚀 Quick Start

```bash
# Open any scenario in browser
start mock-websites/functional-errors.html

# Or use the index
start mock-websites/index.html
```

---

## 💡 Tips for AI Testing

1. **Console Logging** - All bugs log to console with details
2. **Bug Indicators** - Each bug has a description panel
3. **Multiple Tests** - Switch bugs without page reload
4. **Realistic Bugs** - Based on real-world issues
5. **Difficulty Levels** - From Easy to Very Hard
6. **Category Organization** - Test related bugs together

---

## 🎯 Bug Difficulty Breakdown

- **Easy (8 bugs):** Broken links, low contrast, missing alt text, no ARIA, password visibility, no HTTPS warning
- **Medium (10 bugs):** Dead button, no validation, broken layout, non-responsive, slow loading, infinite spinner, fake security, fake badges, ambiguous errors, keyboard navigation
- **Hard (5 bugs):** Fake success, silent failure, confusing flow, blocking JS, hidden errors, contradicting UI
- **Very Hard (2 bugs):** Dark patterns, CAPTCHA challenge

---

**Perfect for hackathon demos!** 🎉

## Overview
Comprehensive test suite with **category-based scenarios** for testing AI agents. Each category demonstrates multiple related bugs.

---

## 📁 File Structure

```
/mock-websites
  ├── scenario-1-successful.html          ✅ Baseline (no errors)
  ├── functional-errors.html              ✅ 3 functional bugs
  ├── ux-errors.html                      ✅ 3 UX bugs
  ├── ui-visual-errors.html               🔄 3 UI/visual bugs
  ├── performance-errors.html             🔄 3 performance bugs
  ├── accessibility-errors.html           🔄 4 accessibility bugs
  ├── ai-testing-errors.html              🔄 4 AI-specific bugs
  ├── security-errors.html                🔄 4 security/trust bugs
  └── scenario-10-captcha.html            ✅ reCAPTCHA challenge
```

**Legend:** ✅ Complete | 🔄 In Progress | ⏸️ Planned

---

## 🟢 Scenario 1: Successful Baseline
**File:** `scenario-1-successful.html`  
**Category:** Baseline  
**Status:** ✅ Complete

**Description:** Perfect signup flow with no bugs. Use this as the baseline for comparison.

---

## 🟡 Functional Errors
**File:** `functional-errors.html`  
**Category:** Functional  
**Status:** ✅ Complete  
**Bugs:** 3

### Bug 1: Form Validation Missing
- **Issue:** Accepts invalid emails, empty fields, weak passwords
- **Detection:** Check for validation attributes, test with invalid data
- **Difficulty:** Medium

### Bug 2: Fake Success Message
- **Issue:** Shows success when submission actually failed
- **Detection:** Verify actual API response vs displayed message
- **Difficulty:** Hard

### Bug 3: Silent Failure
- **Issue:** No error feedback provided to user
- **Detection:** Check for error message display after failed submission
- **Difficulty:** Hard

---

## 🟠 UX Errors
**File:** `ux-errors.html`  
**Category:** User Experience  
**Status:** ✅ Complete  
**Bugs:** 3

### Bug 1: Dead Button
- **Issue:** Button looks clickable but has `pointer-events: none`
- **Detection:** Test button interactivity, check CSS properties
- **Difficulty:** Medium

### Bug 2: Broken Navigation Links
- **Issue:** Links point to non-existent pages (404 errors)
- **Detection:** Follow links and check for 404 responses
- **Difficulty:** Easy

### Bug 3: Confusing Flow
- **Issue:** Login button registers, Back button logs out
- **Detection:** Verify action matches button label
- **Difficulty:** Hard

---

## 🔴 UI/Visual Errors
**File:** `ui-visual-errors.html`  
**Category:** UI/Visual  
**Status:** 🔄 In Progress  
**Bugs:** 3

### Bug 1: Broken Layout
- **Issue:** Elements overflow, navbar overlaps content
- **Detection:** Check for overflow, z-index issues, element positioning
- **Difficulty:** Medium

### Bug 2: Non-Responsive Design
- **Issue:** Mobile view broken, horizontal scrolling
- **Detection:** Test in mobile viewport, check media queries
- **Difficulty:** Medium

### Bug 3: Low Contrast / Invisible Text
- **Issue:** White text on white background, WCAG violations
- **Detection:** Check color contrast ratios, accessibility standards
- **Difficulty:** Easy

---

## 🔵 Performance Errors
**File:** `performance-errors.html`  
**Category:** Performance  
**Status:** 🔄 In Progress  
**Bugs:** 3

### Bug 1: Slow Loading Page
- **Issue:** Large unoptimized images, blocking resources
- **Detection:** Measure page load time, check resource sizes
- **Difficulty:** Medium

### Bug 2: Infinite Loading Spinner
- **Issue:** Spinner never stops, unresolved promise
- **Detection:** Check for timeout, verify loading state management
- **Difficulty:** Medium

### Bug 3: Render-Blocking Resources
- **Issue:** CSS/JS blocks page render
- **Detection:** Analyze critical rendering path
- **Difficulty:** Hard

---

## 🟣 Accessibility Errors
**File:** `accessibility-errors.html`  
**Category:** Accessibility (A11y)  
**Status:** 🔄 In Progress  
**Bugs:** 4

### Bug 1: No ARIA Labels
- **Issue:** Icon-only buttons without labels
- **Detection:** Check for aria-label, aria-labelledby attributes
- **Difficulty:** Easy

### Bug 2: Keyboard Navigation Broken
- **Issue:** Tab key doesn't work, focus trap
- **Detection:** Test keyboard navigation, check tabindex
- **Difficulty:** Medium

### Bug 3: Low Contrast
- **Issue:** Text fails WCAG contrast requirements
- **Detection:** Calculate contrast ratios (WCAG AA/AAA)
- **Difficulty:** Easy

### Bug 4: Missing Alt Text
- **Issue:** Images without descriptions
- **Detection:** Check for alt attributes on images
- **Difficulty:** Easy

---

## ⚫ Security/Trust UI Errors
**File:** `security-errors.html`  
**Category:** Security/Trust  
**Status:** 🔄 In Progress  
**Bugs:** 4

### Bug 1: Fake Security Indicators
- **Issue:** "Secure Checkout" text without HTTPS
- **Detection:** Verify HTTPS, check for misleading claims
- **Difficulty:** Medium

### Bug 2: Fake Trust Badges
- **Issue:** Misleading security badges
- **Detection:** Verify badge authenticity
- **Difficulty:** Medium

### Bug 3: Password Visibility Issues
- **Issue:** Password shown in plain text
- **Detection:** Check input type, password masking
- **Difficulty:** Easy

### Bug 4: No HTTPS Warning
- **Issue:** Sensitive form without security warning
- **Detection:** Check protocol, security indicators
- **Difficulty:** Easy

---

## 🧠 AI-Specific Testing
**File:** `ai-testing-errors.html`  
**Category:** AI Testing  
**Status:** 🔄 In Progress  
**Bugs:** 4

### Bug 1: Ambiguous Error Messages
- **Issue:** "Something went wrong" - non-informative
- **Detection:** Check error message specificity
- **Difficulty:** Medium

### Bug 2: Hidden Errors
- **Issue:** Errors only in console, no UI feedback
- **Detection:** Monitor console vs UI error display
- **Difficulty:** Hard

### Bug 3: Contradicting UI Signals
- **Issue:** Button says "Saved" but status says "Not saved"
- **Detection:** Check state consistency across UI elements
- **Difficulty:** Hard

### Bug 4: Dark Patterns
- **Issue:** Fake countdown, hidden cancel button
- **Detection:** Identify manipulative UX patterns
- **Difficulty:** Very Hard

---

## 🤖 Special: reCAPTCHA Challenge
**File:** `scenario-10-captcha.html`  
**Category:** Security/Authentication  
**Status:** ✅ Complete

**Description:** Real Google reCAPTCHA v2 integration. Tests AI's ability to handle CAPTCHA challenges.

---

## 📊 Summary Statistics

| Category | File | Bugs | Status |
|----------|------|------|--------|
| Baseline | scenario-1-successful.html | 0 | ✅ |
| Functional | functional-errors.html | 3 | ✅ |
| UX | ux-errors.html | 3 | ✅ |
| UI/Visual | ui-visual-errors.html | 3 | 🔄 |
| Performance | performance-errors.html | 3 | 🔄 |
| Accessibility | accessibility-errors.html | 4 | 🔄 |
| AI Testing | ai-testing-errors.html | 4 | 🔄 |
| Security | security-errors.html | 4 | 🔄 |
| Special | scenario-10-captcha.html | 1 | ✅ |

**Total:** 10 files | 25 unique bugs | 3 complete | 6 in progress

---

## 🎨 Design Features

All scenarios include:
- ✨ Animated 4-color gradients
- 🌟 Glassmorphism with backdrop blur
- 💫 Floating animations
- 🎯 Bug selector/switcher UI
- 📱 Mobile responsive design
- 🔮 Modern layered shadows

---

## 🧪 Testing Guide

### For AI Agents:
1. **Start with Baseline** - Test scenario-1 to understand normal flow
2. **Test by Category** - Go through each category file
3. **Switch Between Bugs** - Use bug selector buttons
4. **Verify Detection** - AI should identify and report each bug
5. **Check Console** - Bugs log detailed info to console

### For Judges/Demo:
1. **Show Category Organization** - "We have 7 bug categories"
2. **Demonstrate Bug Switching** - Click bug selector buttons
3. **Show AI Detection** - Run AI agent on each category
4. **Compare Results** - AI report vs actual bugs
5. **Highlight Difficulty** - Show AI handling hard bugs

---

## 🚀 Quick Start

```bash
# Open any scenario in browser
open mock-websites/functional-errors.html

# Or use the index
open mock-websites/index.html
```

---

## 💡 Tips for AI Testing

1. **Console Logging** - All bugs log to console with details
2. **Bug Indicators** - Each bug has a description panel
3. **Multiple Tests** - Switch bugs without page reload
4. **Realistic Bugs** - Based on real-world issues
5. **Difficulty Levels** - From Easy to Very Hard

---

**Perfect for hackathon demos!** 🎉
