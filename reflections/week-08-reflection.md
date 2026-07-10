# Week 8 Reflection

**Name:** Jama Rufai
**Date:** 7/9/26

---

## Commits This Week

<!-- Paste a link to your commits for this week. The easiest way: go to your repo on GitHub,
     click "commits", and copy the URL after filtering by your name or branch. -->

**Link:**
https://github.com/JamaRufai/media-tracker-android/pull/6/
---

## Code Review

<!-- Every week you leave a review on a pod mate's pull request. Fill in both parts below.
     Part 1 is the link — I will verify the review exists on GitHub.
     Part 2 is your written assessment — what you actually looked at and what you found. -->

**Reviewed:** Nathan Perfetti
**Link to my review:**
https://github.com/perfettiful/media-tracker-android/pull/10/changes#r3556280653
### What I Looked At

I reviewed the changes made to the Media Detail ViewModel. I focused on the new refresh() and 
onAddWantTo() functions to understand how media details are refreshed and how items are added to the user's library.
I followed the state updates and repository calls to see how the UI reacts to user actions.

### What I Noticed

I noticed that the code uses guard clauses well to prevent duplicate requests and invalid states. 
I also noticed that if a repository call fails, the UI state may not be updated properly. In particular, isAddingToLibrary could potentially remain true, 
which might prevent the user from trying the action again.

### Comments I Left

I left a comment suggesting that error cases be handled more explicitly. 
I mentioned that if a request fails, isAddingToLibrary could stay true and prevent another attempt. 
I also pointed out that handling failures could help keep the UI responsive and allow users to retry actions when something goes wrong.

---

## One Thing I Understood More Deeply

I gained a better understanding of how a ViewModel manages UI state in Jetpack Compose.
Seeing the use of _uiState.update helped me understand how state changes are pushed to the UI and how guard clauses can prevent unnecessary work or duplicate requests.

---

## One Thing I'm Still Confused About

I'm still a little confused about the best way to handle errors in asynchronous ViewModel functions. 
I understand how to update the UI when a request succeeds, but I'm not always sure what the best pattern is for handling failures 
and displaying error messages to users.

---

## Anything Else *(optional)*

<!-- Did you help a pod mate work through something? Did you discover something cool or frustrating?
     Did something from a previous week finally click? This is a good place to put it. -->

---

## Rubric

*You don't need to self-assess — this is here so you know what I'm looking at.*

| Section | Points | Full Credit | Half Credit | No Credit |
|:---|:---:|:---|:---|:---|
| **Reflection** | 10 | Specific, honest responses to "More Deeply" and "Still Confused" sections. Shows genuine thinking — not just "I learned X." | Responses are present but vague or generic ("I got better at Compose"). | Missing or one-word answers. |
| **Code Review** | 10 | Specific observation about the code with explanation of why it matters (or a substantive positive comment). Link to review present and verified. | A question or comment that shows you read the code, but lacks explanation. | "Looks good!" or equivalent. Missing link. Review not found on GitHub. |
| **Total** | **20** | | | |

**A note on the code review score:** I check that the review actually exists on GitHub before grading. The written summary here and the GitHub comment should match. If the review isn't there, the written summary can't earn credit.
