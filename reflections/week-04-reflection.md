# Week 4 Reflection

**Name:** Jama Rufai
**Date:** 6/11/26

---

## Commits This Week


**Link:**

https://github.com/JamaRufai/media-tracker-android/pull/3/commits
---

## Code Review

<!-- Every week you leave a review on a pod mate's pull request. Fill in both parts below.
     Part 1 is the link — I will verify the review exists on GitHub.
     Part 2 is your written assessment — what you actually looked at and what you found. -->

**Reviewed:** *(pod mate's name)* Nathan Perfetti
**Link to my review:**
https://github.com/perfettiful/media-tracker-android/pull/5/changes/772e1d09a977451ff3992045d1ba4ba8317c430d#r3400174483

### What I Looked At

I reviewed the Register screen changes in the PR. The PR was working on the registration UI and 
how the screen responds after the user fills out the form. I focused on the state being collected 
from the ViewModel, the LaunchedEffect that reacts to a successful validation state, 
and the custom SnackbarHost inside the Scaffold.

### What I Noticed

One thing I noticed was the use of LaunchedEffect to respond to changes in the registration state. 
When validation succeeds, the screen automatically displays a Snackbar message and then resets 
the state so the user can continue interacting with the form. I thought this was a good approach 
because it keeps the UI responsive to state changes without requiring additional button clicks.

### Comments I Left

I left a positive comment on the snackbar customization. I mentioned that using theme colors 
and a rounded shape provides a more consistent user experience throughout the app. 
These design choices help the notifications feel integrated with the rest of the interface 
rather than using the default styling.
---

## One Thing I Understood More Deeply

Working on the RegisterViewModel helped me better understand how ViewModels act as a bridge between 
the UI and application logic. Before this week, I understood that ViewModels stored data, 
but I did not fully understand how user actions triggered updates. 
While implementing functions such as onEmailChange, onPasswordChange, and onRegisterClick, 
I saw how user input updates StateFlow values and how the ViewModel controls validation and UI state changes. 


---

## One Thing I'm Still Confused About

I am still trying to better understand when logic should be placed inside a ViewModel 
and when it should be placed somewhere else. I understand why form validation is handled in the RegisterViewModel, 
but I am not always sure what responsibilities belong in the ViewModel versus the UI.

---

## Anything Else *(optional)*

Nathan recommended that I try GitHub Desktop to help with merge conflicts. 
I have not used it yet, but after dealing with some  conflicts this week, 
I plan to download it and give it a try. One thing that interests me is the ability to visually 
see the differences between files and better understand which changes are being kept or removed.


---

## Rubric

*You don't need to self-assess — this is here so you know what I'm looking at.*

| Section | Points | Full Credit | Half Credit | No Credit |
|:---|:---:|:---|:---|:---|
| **Reflection** | 10 | Specific, honest responses to "More Deeply" and "Still Confused" sections. Shows genuine thinking — not just "I learned X." | Responses are present but vague or generic ("I got better at Compose"). | Missing or one-word answers. |
| **Code Review** | 10 | Specific observation about the code with explanation of why it matters (or a substantive positive comment). Link to review present and verified. | A question or comment that shows you read the code, but lacks explanation. | "Looks good!" or equivalent. Missing link. Review not found on GitHub. |
| **Total** | **20** | | | |

**A note on the code review score:** I check that the review actually exists on GitHub before grading. The written summary here and the GitHub comment should match. If the review isn't there, the written summary can't earn credit.