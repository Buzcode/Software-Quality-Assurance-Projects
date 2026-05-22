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
| [YT_Search_005](#tc-yt_search_005) | Verify auto-suggestion list is displayed when typing keywords in the search bar. | **PASS** |
| [YT_Search_006](#tc-yt_search_006) | Verify search history list is displayed when clicking the empty search bar. | **PASS** |
| [YT_Search_007](#tc-yt_search_007) | Verify search results can be filtered by upload date and video length. | **PASS** |
| [YT_Search_008](#tc-yt_search_008) | Verify search functionality using the microphone (voice search). | **PASS** |
| [YT_Search_009](#tc-yt_search_009) | Verify search results and "Did you mean?" suggestions when typing an incorrect or misspelled word. | **FAIL** |
| [YT_Search_010](#tc-yt_search_010) | Verify search functionality when querying an exact song or channel title. | **PASS** |

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

---

<a id="tc-yt_search_005"></a>
### Test Case ID: YT_Search_005
* **Test Description:** Verify auto-suggestion list is displayed when typing keywords in the search bar.
* **Pre-conditions:** The YouTube app is open and connected to the internet.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Tap on the search bar. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 2 | Type the keyword "software" (Do not press search or enter). | `"software"` | A dropdown menu dynamically appears directly below the search bar showing search phrase suggestions starting with or matching the keyword "software". | A dropdown menu appeared showing suggestions like "software testing mentor" and "software engineering". | Pass |

---

<a id="tc-yt_search_006"></a>
### Test Case ID: YT_Search_006
* **Test Description:** Verify search history list is displayed when clicking the empty search bar.
* **Pre-conditions:** 
  1. The user is logged into their YouTube account.
  2. The account has a pre-existing search history.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Open the YouTube app. | N/A | App opens normally. | App opens normally. | Pass |
| 2 | Tap on the empty search bar. | N/A | A dropdown list displays the user's recent search queries. | A dropdown list appeared displaying the user's previously searched queries. | Pass |

---

<a id="tc-yt_search_007"></a>
### Test Case ID: YT_Search_007
* **Test Description:** Verify search results can be filtered by upload date and video length.
* **Pre-conditions:** The YouTube app is open and connected to the internet.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Tap on the search bar. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 2 | Type "software testing" and tap the search key. | `"software testing"` | Search results screen loads. | Search results screen loads. | Pass |
| 3 | Tap the "Filters" option (three dots or filter icon) at the top of the search results screen. | N/A | Filter options panel opens. | Filter options panel opens. | Pass |
| 4 | Set "Upload Date" to "This week" and "Duration" to "Under 4 minutes". | `Upload Date: This Week, Duration: Short` | The search results page updates to display only videos meeting both criteria (recent uploads and shorter video lengths). | The search results updated and displayed only videos uploaded recently and matching the short duration filter. | Pass |

---

<a id="tc-yt_search_008"></a>
### Test Case ID: YT_Search_008
* **Test Description:** Verify search functionality using the microphone (voice search).
* **Pre-conditions:** 
  1. The YouTube app is open and connected to the internet.
  2. YouTube app has microphone permissions enabled in the device settings.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Tap on the search bar. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 2 | Tap on the microphone icon. | N/A | Voice recording overlay appears and starts listening. | Voice recording overlay appears and starts listening. | Pass |
| 3 | Speak "software testing mentor" clearly into the microphone. | Voice input: `"software testing mentor"` | The app successfully captures the speech, displays the text inside the search field, and automatically loads the search results page. | Voice input was recognized, and the correct search results page loaded. | Pass |

---

<a id="tc-yt_search_009"></a>
### Test Case ID: YT_Search_009
* **Test Description:** Verify search results and "Did you mean?" suggestions when typing an incorrect or misspelled word.
* **Pre-conditions:** The YouTube app is open and connected to the internet.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Tap on the search bar. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 2 | Type the misspelled word "micsic video" and tap the search key. | `"micsic video"` | Search results for the corrected term "music video" load, and a message stating "Did you mean: music video?" is displayed at the top of the results page. | Search results for "music video" loaded, but the top section did not show the "Did you mean: music video?" correction message. | **Fail** |

---

<a id="tc-yt_search_010"></a>
### Test Case ID: YT_Search_010
* **Test Description:** Verify search functionality when querying an exact song or channel title.
* **Pre-conditions:** The YouTube app is open and connected to the internet.

| Step | Test Step Description | Test Data | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Tap on the search bar. | N/A | Search bar becomes active. | Search bar becomes active. | Pass |
| 2 | Type "I Want It That Way" and tap the search key. | `"I Want It That Way"` | The search results page loads displaying the official music video by the original artists/band at the very top, followed by relevant covers and edited videos below. | Results page loaded with the official video of the song at the top, with covers and fan-edited videos listed below it. | Pass |
