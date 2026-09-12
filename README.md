# Maths4

## Starlight Maths — Saved Learner Progress (v1)

This version adds a learner profile and automatic progress saving while keeping the original maths activity interface and question engine.

### What is saved

- Learner name
- Starpoints, correct answers and incorrect answers
- Up to 100 recent history records
- Current maths mode
- Current generated problem
- Answers, carry/exchange boxes, borrowing marks and division working boxes already entered
- Last activity time

### How it works on GitHub Pages

The app uses the browser's `localStorage`, so no server or database is required for this first version. The saved record is tied to the browser/device being used. GitHub Pages continues to host only the website files.

### First use

Open the site and enter the learner's name. Progress is then saved automatically as the learner types and after every checked answer.

### Returning

On the next visit in the same browser/device, the app detects the saved learner and shows a welcome-back screen with the stored totals and a **Continue Learning** button. The last unfinished problem can be restored with its entered working.

### Starting another learner

Use **↔ Change learner** from the learner bar. Because this v1 stores one learner profile per browser, replacing the learner replaces the saved records currently stored in that browser.

### Resetting saved data during testing

Open the browser developer console and run:

```js
localStorage.removeItem('starlightMathsLearner_v1');
```

Then refresh the page.

### Next production step

For cross-device accounts, teacher/parent views, multiple learner profiles and centralised records, the next step is to replace the local storage adapter with a cloud database/authentication service such as Supabase. The maths UI can remain largely unchanged.

