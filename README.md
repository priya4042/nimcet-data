# nimcet-data

Expected exam dates and application-form links used by the NIMCET Prep app.

The app downloads `exam_dates.json` from this repo when it opens. If the file is newer than the dates built into the app, the app uses it, so a new exam year only needs this file updated - no new app release.

## Updating for a new year
1. Open `exam_dates.json` and change the dates (`month`, `day`) of any exam whose schedule changed. `yearOffset` is relative to the year the exam is held (for example `-1` means the previous December).
2. Change `applyUrl` if an exam moved its application portal.
3. Update the `updated` date at the top.
4. Commit. Phones pick up the change the next time the app is opened.

Allowed `kind` values: notice, formOpen, formClose, correction, admitCard, exam, answerKey, result, counselling.
