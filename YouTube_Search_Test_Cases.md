# Project: YouTube Mobile App Search Feature Test Suite

This test suite contains 10 manual test cases designed to verify the functionality, stability, and edge cases of the YouTube mobile app's search bar.

---

## Test Cases Summary

| Test Case ID | Test Description | Status |
|---|---|---|
| [YT_Search_001](#tc-yt_search_001) | Verify search behavior when the device is offline. | **PASS** |
| [YT_Search_002](#tc-yt_search_002) | Verify search functionality using numbers and emojis. | **PASS** |
| [YT_Search_003](#tc-yt_search_003) | Verify search functionality using a non-English language. | **PASS** |
| [YT_Search_004](#tc-yt_search_004) | Verify search button behavior when the search bar is completely blank. | **PASS** |

---

<a id="tc-yt_search_001"></a>
### Test Case ID: YT_Search_001
* **Test Description:** Verify search feature behaves correctly when the device is offline.
* **Pre-conditions:**
  1. The YouTube mobile app is installed.
  2. The mobile device is completely disconnected from the internet (Wi-Fi and Mobile Data are turned off).

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Open the YouTube app. | N/A | App opens normally. | App opens normally. | Pass |
| 2 | Tap on the search bar icon. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 3 | Type the search query and tap the search key. | `"software testing mentor"` | No search results are displayed. The app displays an offline error message along with a "Tap to retry" button. | Did not get search results. Message displayed: "You’re offline. Explore downloads? Tap to retry". | Pass |

---

<a id="tc-yt_search_002"></a>
### Test Case ID: YT_Search_002
* **Test Description:** Verify search functionality using numbers and emojis.
* **Pre-conditions:** The YouTube app is open and connected to the internet.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Tap on the search bar. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 2 | Type the search query and tap the search key. | `"23 🔥"` | Relevant video suggestions and results appear based on the numerical value and contextual meaning of the typed emoji. | Search results and suggestions appeared corresponding to the number "23" and the flame emoji. | Pass |

---

<a id="tc-yt_search_003"></a>
### Test Case ID: YT_Search_003
* **Test Description:** Verify search functionality using a non-English language.
* **Pre-conditions:** The YouTube app is open and connected to the internet.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Tap on the search bar. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 2 | Type the search query in Bengali and tap the search key. | `"চিকেন রোস্ট রেসিপি"` | Relevant video suggestions and search results appear matching the exact query in the non-English language script. | Search suggestions and videos loaded correctly matching the query "চিকেন রোস্ট রেসিপি". | Pass |

---

<a id="tc-yt_search_004"></a>
### Test Case ID: YT_Search_004
* **Test Description:** Verify search button behavior when the search bar is completely blank.
* **Pre-conditions:** The YouTube app is open, and the search bar is empty.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Tap on the search bar. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 2 | Tap the search/enter key on the virtual keyboard without entering any text. | `None (Blank input)` | The search query does not execute, and the app remains on the current screen (no page refresh or empty loading state). | The search key did not execute any action. | Pass |
