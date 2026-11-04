# Accessibility Audit Report

**Project:** My Personal Website – About Me  
**Student:** Shaniz Ann Mumbua  
**Task:** 2.3 – Accessibility Audit  
**Date:** 5 November 2026

## 1. Introduction

The purpose of this accessibility audit was to evaluate my personal website and identify areas that could prevent people with disabilities from accessing or understanding its content.

I used Chrome DevTools Lighthouse and the WAVE Web Accessibility Evaluation Tool to check my webpage.

## 2. Accessibility Issues Found

I reviewed the five required accessibility areas:

| Area | What I Checked | Result |
|---|---|---|
| Images | Added descriptive alternative text to the profile image. | Passed |
| Headings | Checked the heading hierarchy from H1 to H2. | Passed |
| Links | Ensured links have meaningful and descriptive text. | Passed |
| Language | Added `lang="en"` to the HTML element. | Passed |
| Form Labels | Checked whether form inputs have associated labels. | Not applicable – no form inputs on this page. |

## 3. How I Fixed the Issues

### A. Images – Alternative Text

I added descriptive alternative text to my profile image so that screen readers can describe it to visually impaired users.

```html
<img
    src="./images/photo.jpg"
    alt="Portrait of Shaniz Ann Mumbua"
    width="300"
    height="400"
>
```

### B. Headings – Proper Hierarchy

I organized the headings to follow a logical structure:

- `<h1>` – Main page heading: Hi, I'm Shaniz Ann Mumbua.
- `<h2>` – Section headings, including About Me, My Hobbies and Interests, My Favorite Website, and Contact Me.

This makes the page structure easier to understand and navigate.

### C. Links – Descriptive Link Text

I used meaningful link text instead of vague phrases such as "click here".

For example:

```html
<a href="https://github.com/">
    GitHub
</a>
```

I also included descriptive text for my email link.

### D. Language – HTML Language Attribute

I confirmed that my HTML document declares English as its language.

```html
<html lang="en">
```

This helps browsers and screen readers identify the language of the page.

### E. Form Labels

My About Me page does not contain form inputs, so this requirement was not applicable during this audit.

## 4. Accessibility Testing Results

### A. Chrome DevTools Lighthouse

I used Chrome DevTools Lighthouse with Navigation mode and the Accessibility category selected.

**Final Accessibility Score: 100/100**

<badge color="success">100/100 – Excellent</badge>

The Lighthouse audit gave my webpage a perfect accessibility score.

### B. WAVE Web Accessibility Evaluation Tool

I tested my webpage using the WAVE Web Accessibility Evaluation Tool.

**WAVE Results:**

| Category | Result |
|---|---:|
| Errors | 0 |
| Contrast Errors | 0 |
| Alerts | 0 |
| Features | 3 |
| Structural Elements | 9 |
| ARIA | 5 |
| WAVE AIM Score | 10/10 |

WAVE detected no accessibility errors, contrast errors, or alerts.

It also identified the following accessibility features:

**Features (3):**
- Alternative text
- Figure
- Language

**Structural Elements (9):**
- 1 Heading Level 1
- 4 Heading Level 2
- 1 Unordered List
- 1 Header
- 1 Main Content
- 1 Footer

**ARIA (5):**
- 5 ARIA labels

### C. Overall Results

Both accessibility testing tools gave positive results:

- Lighthouse Accessibility: **100/100**
- WAVE AIM Score: **10/10**
- WAVE Errors: **0**
- WAVE Contrast Errors: **0**
- WAVE Alerts: **0**

## 5. Conclusion

The accessibility audit helped me understand the importance of creating websites that are usable by everyone, including people who rely on assistive technologies.

I improved the alternative text for my profile image, checked my heading hierarchy, ensured that my links were descriptive, and confirmed that my HTML document included a language attribute.

The final results showed that my webpage achieved a Lighthouse Accessibility score of 100/100 and a WAVE AIM Score of 10/10, with no detected errors, contrast errors, or alerts.

I also learned that automated accessibility tools are helpful, but manual testing is still necessary to ensure a website provides a good experience for all users.
