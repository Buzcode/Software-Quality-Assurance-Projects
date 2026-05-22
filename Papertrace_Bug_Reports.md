# Project: Papertrace Web Application Bug Reports

This document contains 3 detailed bug reports identified during exploratory and functional testing of the Papertrace web application. 

---

## Bug Log Summary

| Bug ID | Title | Severity | Priority | Status |
|---|---|---|---|---|
| [PT_BUG_001](#pt_bug_001) | [Search Bar] No visual warning when pasted text exceeds 500-character limit | Minor | Medium | Open |
| [PT_BUG_002](#pt_bug_002) | [Filters] "Max Papers" slider control is unresponsive and frozen | Major | High | Open |
| [PT_BUG_003](#pt_bug_003) | [Authentication] Tab toggle does not update form layout or action button | Minor | Medium | Open |

---

<a id="pt_bug_001"></a>
## Bug Report 1: Search Input Limit Behavior

* **Bug ID:** PT_BUG_001
* **Bug Title:** [Search Bar] No visual error or warning is displayed when pasted text exceeds the 500-character input limit
* **Environment:** Desktop Chrome (Latest Version)
* **Severity:** Minor | **Priority:** Medium

### Steps to Reproduce:
1. Navigate to the Papertrace application home page.
2. Paste a text block containing more than 500 characters into the main AI search text area.
3. Observe the input area and the character count.

### Expected Result:
The input box should show a clear validation warning (e.g., text counter turning red, or a message saying *"Maximum limit of 500 characters reached"*) to inform the user why their text was truncated.

### Actual Result:
The text box silently cuts off the pasted text at 500 characters without displaying any error message, warning, or indication to the user.

### Attachment:
*(Placeholder: If you have a screenshot for this bug, you can place it here)*  
`![Input Limit Bug](./screenshots/input_limit_bug.png)`

---

<a id="tc-pt_bug_002"></a>
## Bug Report 2: Frozen Slider Filter

* **Bug ID:** PT_BUG_002
* **Bug Title:** [Filters] "Max Papers" slider control is unresponsive and cannot be adjusted by the user
* **Environment:** Desktop Chrome (Latest Version)
* **Severity:** Major | **Priority:** High

### Steps to Reproduce:
1. Navigate to the Papertrace application.
2. Type a query in the search box (e.g., `"early cancer symptoms"`).
3. Click on the **Filters** button to open the filter options panel.
4. Attempt to click and drag the "Max Papers" slider handle to adjust the paper count.

### Expected Result:
The slider handle should slide smoothly left or right, and the "Max Papers" count should update dynamically based on the handle position.

### Actual Result:
The slider handle is completely locked/frozen and does not respond to mouse click-and-drag actions.

### Attachment:
`![Frozen Slider Bug](./screenshots/frozen_slider_bug.png)`

---

<a id="tc-pt_bug_003"></a>
## Bug Report 3: Tab State Issue on Auth Modal

* **Bug ID:** PT_BUG_003
* **Bug Title:** [Authentication] Toggling between 'Log In' and 'Create Account' tabs does not clearly update the form state or button action
* **Environment:** Desktop Chrome (v124.0 or latest)
* **Severity:** Minor | **Priority:** Medium

### Steps to Reproduce:
1. Navigate to the Papertrace application.
2. Click the **Log In** button at the top right of the navigation header.
3. Click the **Create Account** tab at the top of the authentication modal.
4. Observe the form fields and the main submission button.

### Expected Result:
Selecting the "Create Account" tab should clearly transition the modal state to a registration form (e.g., updating the submit button to "Create Account" and updating any password requirements or helper text).

### Actual Result:
The tab visual changes, but the form layout remains identical to the log-in page without clear visual confirmation of the registration state, leading to user confusion about whether they are logging in or signing up.

### Attachment:
`![Auth Modal Bug](./screenshots/auth_modal_bug.png)`
