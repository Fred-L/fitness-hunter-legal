# Fitness Hunter Privacy Policy

## Current version and changes

Last updated 3 September 2026.

This policy describes Fitness Hunter as it ships today, including its communication with a Fitness Hunter server.

## Information stored on this device

Fitness Hunter keeps application data in an on-device SQLite database. This includes profile and preference information; workout, set, cardio, habit, bodyweight, health-metric, and daily step records; exercise and program data; progression and app-state records; and the optional account-link record described below.

## Fitness Hunter server and profile publication

Fitness Hunter has a server operated by the developer on Cloudflare Workers and Cloudflare D1. It stores only an optional linked-account identity, session metadata, and a derived profile snapshot; it does not sync the on-device database.

The derived profile snapshot contains these fields: your overall rank (or no rank), Power Level (or no Power Level), the STR, END, and VIT domain ranks (each of which may be absent), your rounded current-week average steps (or no step value), your current streak, and lists for titles and cosmetics. Titles and cosmetics are currently sent as empty lists because those features are not built.

The raw training log stays on your device. Fitness Hunter does not upload workout or set rows, cardio rows, bodyweight rows, health-metric rows, or daily step rows. It also does not upload the rest of your on-device database.

When you have linked an account with a valid session, the app makes a best-effort upload after you finish a training session and when the app resumes, but only when the derived snapshot has changed. The app never reads its own profile snapshot back from the server; local data remains authoritative.

The server stores a generated user ID and its creation time; the linked provider name, provider subject identifier, associated server user ID, and link time; a hash of each session token with its associated server user ID, creation time, and expiry time; and the associated profile snapshot JSON with its last-update time.

## Device backups

Your device's own backup service may include Fitness Hunter's database. On iPhone this is iCloud Backup, and on Android it is Google's backup service. Those backups are made and stored by Apple or Google under their own terms, not by Fitness Hunter. You can turn them off in your device settings.

## Optional account linking

If you choose Link with Apple or Link with Google, the relevant provider SDK handles that identity request. Fitness Hunter stores an account record containing the provider, subject identifier, and linked-at time.

The Fitness Hunter server verifies the provider token before creating a server session. It stores a hash of that session token, rather than the token itself.

What Apple or Google does with a sign-in request is covered by their own privacy policies, not this one.

## Step data

On iOS, Fitness Hunter reads step counts directly with CoreMotion's CMPedometer. It does not use HealthKit or Apple Health for this feature. Daily step totals are stored locally.

## Export

When you select Export data, the app makes a JSON file containing its raw-log tables, formula versions, and custom exercises, then opens your device's system share sheet. It does not choose a recipient. The file can leave your device only when you select a sharing destination.

## Keeping and removing your data

Your raw training log and other app data stay on your device until you remove them. The server copy is limited to the linked-account identity and session metadata, plus the derived profile snapshot described above.

Unlinking removes the account record and session from this device and attempts to delete that session from the server. It does not delete the server-side linked-account identity or derived profile snapshot, and it does not delete your training history, which stays under the local identity the app created the first time you opened it. To ask for deletion of server-side data, contact maerasoft@gmail.com.

Deleting the app removes its database from your device. That cannot be undone, so use Export data first if you want to keep a copy.

## Who provides this app

Fitness Hunter is made by an independent developer based in Ontario, Canada.

Questions about this policy can be sent to maerasoft@gmail.com.

## Governing law

This policy is governed by the laws of the Province of Ontario and the federal laws of Canada that apply there.
