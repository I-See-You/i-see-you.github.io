# Privacy Policy for Tab Timer

**Last Updated:** October 20, 2026

Tab Timer ("the Extension") is a Chrome extension that counts the time you spend on websites, shows it on the toolbar icon and, where you allow it, in a floating widget and the tab title, and keeps a local history on the Analytics page. You choose whether it counts every website (except sites you leave out) or only the sites you pick; you can change this at any time.

## 1. What the Extension stores

Data is stored with Chrome's own storage and, only if you choose it, a sync file, folder or your Google Drive. Tab Timer has no servers and no telemetry.

Settings, kept in `chrome.storage.sync` (Chrome syncs them across your signed-in browsers):
- Where time counts (every website, or the sites you pick), the sites you leave out, site categories, limits and countdown rules
- Widget, display and timer preferences
- The sites you chose for "Remember pages and videos"

History is recorded on this device in `chrome.storage.local` while "Save history" is on (it is on for new installs; turn it off on the welcome page or in Settings › History & sync):
- Time per website per day (focused, and listening when a tab plays sound in the background)
- Time per website per hour of the day, and when each session on a site started and ended
- Countdown and daily-limit results per site (for example "limit reached", "+5 min" taken)
- History of your other browsers (other Chrome profiles or computers), only if you restore a backup or connect a sync destination: time per website per day and per hour, and sessions. Page titles and addresses of other browsers are never kept
- Only if you turn on "Remember pages and videos" for a site: the titles and addresses (path only, never the part after "?") of pages on that site, with the time spent on each. A title is what the page calls itself, so it can include what the page shows, such as a search or an email subject

Working data, kept only on this device in `chrome.storage.local`, whether or not history is on:
- Countdowns that are running, and today's time on each site toward your daily limits
- If you close a tab while its countdown runs: the page address and how much time was left, so the countdown can resume when you open that page again (up to 50 pages, kept 7 days)
- The last 20 tabs a countdown closed, with their title and address, so you can reopen them from the notification or from Settings
- A name for this browser (like "Mac · Chrome", which you can change) and a random ID, so backups and Analytics can tell your browsers apart, and the date of your last backup
- A random recognition code for this Chrome profile, kept in Chrome's local extension storage and included with its history in sync and backup files. It helps select an existing profile when linking again. It contains no email address or Google account information, and local file / folder linking requests no account access. Uninstalling or clearing extension storage removes the local code; you can still select a saved profile manually.
- Small app state: how you left the popup's tab list, whether you've seen a tip or rating prompt, and a copy of the running timers kept for a few minutes while the extension updates

Linking your Chrome profiles, only if you set it up in Settings › History & sync (a sync file such as "tab-timer-sync.json", or a folder, that you choose):
- Tab Timer writes this profile's history to that file or folder: time per website per day and per hour, sessions, countdown and daily-limit results, the browser's name, and its settings (sites, limits, display). Page titles and addresses are never written there.
- It reads what your other profiles wrote there. With "Count my other profiles toward daily limits" on, their time today counts toward your daily limits here.
- The file or folder is on your computer. If you choose one that a cloud service keeps (iCloud Drive, Dropbox, OneDrive, Google Drive for desktop), that service copies the files under its own terms. File / folder sync itself makes no network requests.
- To stop, choose "Disconnect file sync" or "Disconnect folder sync" in that destination’s controls. You can also remove this profile's history from the file or folder, or unlink another profile.
- Earlier experimental email / email-derived profile metadata is removed from local profile records when initialized and from this profile's next successful sync. Existing exported backups retain their original contents.

File / folder and Google Drive sync can be connected at the same time:
- Each destination receives this profile’s own history and settings only. Downloaded history from another profile is not uploaded to another destination. Connect each profile separately to the destinations you want it to use.
- The same profile seen through both destinations is stored once locally and counted once in reports and shared daily limits.
- Disconnecting one destination leaves the other connected. Downloaded history stays here by default; optional cleanup removes only profiles not still shared through another connected destination. Retained snapshots remain visible in reports but no longer contribute to shared daily limits.

Google Drive, only if you choose Connect in Settings:
- The same history and settings as file / folder sync are stored in Tab Timer's hidden app-data folder in the Google account you choose. Other Drive files are outside the requested access. Page titles, page addresses, private browsing, active timers and closed-tab lists are excluded.
- Google asks for access to Tab Timer's own app-data folder and account identification. The chosen Drive account's verified email and stable Google account ID are kept locally to show the destination and prevent accidental account switches. They are not written into profile history / library files. Local profile recognition still uses a random code, even when using Drive.
- One Chrome profile has one Tab Timer history, even when several Google accounts are signed in on websites. History is grouped by website; Tab Timer does not identify the Google account used by each tab or split history by website account. All of this profile's synced history uses the storage account you explicitly chose. Changing website accounts does not change that destination.
- Short-lived access tokens are kept only in Chrome's session storage, not local / synced storage, backup files or logs. Google authentication and signing keys are checked before use; there is no Tab Timer login server or client secret.
- The Chrome identity permission and Google API endpoint access are optional and requested only for Drive. The extension never requests Chrome's `identity.email` permission.
- Disconnecting Google Drive clears this installation's stored account / token and relinquishes its optional Chrome Drive access. It does not sign Google websites out or revoke Google authorization for your other installations. To withdraw Tab Timer's Google authorization across installations, use [Google Account connections](https://myaccount.google.com/connections); those installations may need to reconnect. You may also remove Tab Timer's app data from Google Drive's Manage apps settings. Copies kept in Drive remain there unless you choose to remove them. A random local authorization-generation value prevents a pending sign-in from restoring a disconnected session; it contains no account data and is not exported.

To decide whether time counts, the Extension also checks on your device whether you're away from the computer, whether a tab is playing sound, and whether a browser window can be seen: minimized, on another desktop, or moved off screen, using the position and size of your screens. These checks are used at that moment and are not stored.

The Extension does not read page content, form data, passwords or cookies. Tabs in private (Incognito) windows are never saved to history: their countdowns are kept only in memory until Chrome closes, they are left out of the lists of paused and closed tabs, and widget changes made there aren't synced.

## 2. How the data is used

Only to show you your own time on the Analytics page, in the popup and in the widget, and to run the limits and countdowns you set. Files you export (CSV, JSON or a backup file) are saved by you and go only where you put them. A backup file holds your history, settings and limits, and the history of other browsers restored here; remembered page titles are included only for this browser. Optional Google Drive sync connects only to Google endpoints allowed by the manifest; local file / folder sync needs no network connection from Tab Timer. Tab Timer's use of data adheres to the [Chrome Web Store User Data Policy](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq), including the Limited Use requirements. Data is never sold, never used for advertising, never sent to an advertising or analytics service. Optional Drive data is stored by Google under its own terms.

## 3. Host permissions

Counting time needs no site access: the Extension knows which site a tab shows from Chrome's `tabs` permission. Site access is optional, asked only when you choose to see the clock on a site (or on every website), and used only to show the floating widget, put the time in the tab title, and tell when a page is hidden.

## 4. Retention and deletion

- Pages and videos are kept for 90 days. Everything else in the history is kept until you delete it.
- Paused countdowns of closed tabs are dropped after 7 days. The list of tabs closed by a countdown keeps the last 20; clear it in Settings › Limits.
- Delete one site's history from its page in Analytics, all recorded pages in Settings › History & sync › Advanced settings, or the whole history with "Clear all analytics data".
- Turning off "Save history" stops new history from being saved.
- Remove another browser's history from Settings › History & sync.
- Uninstalling the Extension removes everything it stored. Backup files you saved stay where you put them.

## 5. Children's privacy

Tab Timer does not knowingly collect information from children under 13.

## 6. Changes

Updates to this policy are reflected in the "Last Updated" date above.

## 7. Contact

**Email:** zubayet.zico@practicenumbers.com
