# Week 3 Reflection

**Name:** Jama Rufai
**Date:** 6/4/26

---

## Commits This Week

<!-- Paste a link to your commits for this week. The easiest way: go to your repo on GitHub,
     click "commits", and copy the URL after filtering by your name or branch. -->

**Link:**

---

## Code Review

<!-- Every week you leave a review on a pod mate's pull request. Fill in both parts below.
     Part 1 is the link — I will verify the review exists on GitHub.
     Part 2 is your written assessment — what you actually looked at and what you found. -->

**Reviewed:** *(pod mate's name)* Nathan Perfetti
**Link to my review:** https://github.com/perfettiful/media-tracker-android/pull/3/changes/1cc9799713198fff872b037a2b9cd317b2bd6e4b#r3359892897

### What I Looked At

The PR was adding functionality to the registration screen. 
I focused on the RegisterScreen composable and the code that handles form submission and error messages. 
I also looked at how the input fields interact with the ViewModel 
and how errors are cleared when the user starts editing a field again.

### What I Noticed

I noticed that the CreateUserRequest and TokenRequest classes are separated instead of using one model for everything. 
This matters because registration and login require different information, 
which keeps the API requests organized and easier to maintain.

### Comments I Left

I left a positive comment about the clearRegisterError() call. 
I mentioned that it was a good idea to clear the error message when the user starts typing again 
because it makes the registration form easier to use and prevents old errors from staying on the screen.

---

## One Thing I Understood More Deeply

One thing I understood more deeply was how the RegisterScreen works with the AuthViewModel. 
Looking through the registration code helped me see how user input from the text fields is passed to the ViewModel when the Register button is pressed. 
It also helped me understand how error messages and loading states are handled separately from the UI, which keeps the code more organized.

---

## One Thing I'm Still Confused About

I am still confused about how access and refresh tokens fit into the overall authentication flow. 
We covered the topic fairly quickly in class, so I understand the general purpose of the tokens, 
but I would like a better understanding of how they are used throughout the application after login.

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