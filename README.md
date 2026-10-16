# twc-outage-ping

Scheduler for Tutoring with Chubbs' course-site outage monitor. Every ~15 minutes
it calls `https://twc-reminders.vercel.app/api/outage`, which checks Moodle and
emails students if the site is confirmed down. The logic and data live in the
private Vercel project; this repo holds no student information.

If the checks ever stop, the Vercel app's daily watchdog emails an alert.
Fix: Actions → "Ping outage monitor" → Enable workflow.
