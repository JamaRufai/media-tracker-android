# Week 5 Reflection

**Name:** Jama Rufai
**Date:** 6/18/26

---

## Commits This Week

<!-- Paste a link to your commits for this week. The easiest way: go to your repo on GitHub,
     click "commits", and copy the URL after filtering by your name or branch. -->

**Link:**
https://github.com/JamaRufai/media-tracker-android/pull/4/commits

---

## Code Review

<!-- Every week you leave a review on a pod mate's pull request. Fill in both parts below.
     Part 1 is the link — I will verify the review exists on GitHub.
     Part 2 is your written assessment — what you actually looked at and what you found. -->

**Reviewed:** Nathan Perfetti
**Link to my review:**
https://github.com/perfettiful/media-tracker-android/pull/6/changes#r3439823612

### What I Looked At

I reviewed AuthViewModel.kt, which is responsible for handling the login process and managing 
the authentication state for the UI. I focused on the AuthUiState sealed class, 
the onLoginClick() function, and how the ViewModel communicates with the UserRepository 
to process login requests. I also looked at how errors and success states are handled 
and how the ViewModel is created using the factory pattern.

### What I Noticed

I noticed that the login state is handled clearly with Idle, Loading, Success, and Error. 
This makes it easier for the UI to know what to show during login. I also noticed that the email 
is trimmed before logging in, which helps prevent login issues caused by extra spaces. 
Another good part is that empty email or password fields are checked before the API call, 
so the app does not make an unnecessary network request.

### Comments I Left

I left a positive comment noting that the Retrofit configuration is clean and easy to understand. 
I also mentioned that using ignoreUnknownKeys helps make the app more resilient to API changes and 
that the logging interceptor will be helpful when troubleshooting network issues.

---

## One Thing I Understood More Deeply

I have a better understanding of how a ViewModel manages UI state during an API request. 
Before, I knew that ViewModels stored data and helped preserve state during configuration changes, 
but I was not completely sure how they handled different stages of a login process. 
Looking at the AuthUiState sealed class helped me see how the ViewModel can switch between states 
like Loading, Success, and Error while the UI reacts to those changes. It also helped me understand 
why separating these states makes the code easier to maintain and debug.

---

## One Thing I'm Still Confused About

I am still a little confused about what happens inside the UserRepository after the login() function is called. 
From this file, I can see that the ViewModel sends the email and password to the repository and receives a result back, 
but I cannot see exactly how the network request is made or how the response is processed. 
I would like to learn more about what happens between the repository and the API service so I can better understand the full login flow.

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