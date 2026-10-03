---
title: Fitness Hunter Privacy Policy
---

# Fitness Hunter Privacy Policy

## Current version and changes

Last updated 30 September 2026.

This policy describes Fitness Hunter as it ships today, including its communication with a Fitness Hunter server.

## Information stored on this device

Fitness Hunter keeps application data in an on-device SQLite database. This includes profile and preference information; workout, set, cardio, habit, bodyweight, health-metric, and daily step records; exercise and program data; progression and app-state records; and the optional account-link record described below.

## Fitness Hunter server and profile publication

Fitness Hunter has a server operated by the developer on Cloudflare Workers and Cloudflare D1. It stores an optional linked-account identity, session metadata, a derived profile snapshot, the username and tag described below, and friendship records; it does not sync the on-device database.

The derived profile snapshot contains your overall rank (or no rank), Power Level (or no Power Level), titles and cosmetics, and any enabled applicable sharing fields. The applicable sharing fields are the STR, END, and VIT domain ranks, your rounded current-week average steps, and your training days per week. A disabled field is omitted from the snapshot rather than sent empty. Titles and cosmetics are currently sent as empty lists because those features are not built.

The raw training log stays on your device. Fitness Hunter does not upload workout or set rows, cardio rows, bodyweight rows, health-metric rows, or daily step rows. It also does not upload the rest of your on-device database.

When you have linked an account with a valid session, the app makes a best-effort upload after you finish a training session and when the app resumes, but only when the derived snapshot has changed. The app never reads its own profile snapshot back from the server; local data remains authoritative. The app can read a friend's derived snapshot when the server authorizes that friendship, and a friend can read yours on the same basis.

The server stores a generated user ID and its creation time; the linked provider name, provider subject identifier, associated server user ID, and link time; a hash of each session token with its associated server user ID, creation time, and expiry time; the associated profile snapshot JSON with its last-update time; your username and tag with their claim time; a permanent record of every username and tag pair ever claimed, described below; and friendship rows with the two server user IDs, state, creation time, and update time.

## Friends

Your username is a name you choose plus a tag of 3 to 5 letters or digits that you also choose. The name and tag together must be unique, compared without regard to letter case, and let another user send you an invite.

Once a name and tag pair is claimed, the server keeps a permanent record of it, even after you stop using it or unlink your account. This is so an old invite link can never come to point at a different person: the pair is never released for someone else to claim.

A friendship is one server row for a pair of users. Its state can be pending, accepted, or blocked. Blocking is a stored state, not a deletion, so the row remains while the pair is blocked.

The server authorizes every friend-data read. A request for a friend's profile is allowed only for an accepted friendship; otherwise the server returns the same not-found response used when no profile exists.

You can choose whether your stat ranks, steps, training days, and workout history are included in your derived profile snapshot for friends. Disabled fields are omitted rather than sent empty. Stat ranks sends the letter grade of each of your six stats. Workout history sends up to your 12 most recent workouts, each with its name if you named it, the muscles it worked, its lifting minutes, which exercises you did together as a superset, and its exercises with their working sets, warm-up sets, and drop-set stages, including each set's weight, reps, RPE, and whether it was a personal record. It also sends a set note only when you chose to share that note with friends; notes you keep private are never sent. Turning workout history off removes all of this from your snapshot.

An invite link contains your username and tag in its URL. You choose the app or destination through which to share it, and the developer does not control where it travels. The server stores no record of invite links. A browser fallback page is built from the name and tag in the URL without a database lookup and shows nothing beyond that handle.

You can report a friend from their profile. A report needs an existing friendship record between you and that person. The server sends the reported handle, your own handle, and any reason you write, by email to the developer through Resend, a third-party email delivery service. Reports are not stored in the server's database and there is no moderation queue.

## Contributing to rankings

Contributing to rankings is off unless you turn it on, and it works only with a linked account. When it is on, after you finish a workout the app sends, at most once a month for each exercise, your best estimated 1-rep max for that exercise together with your bodyweight, height and sex (male or female), rounded. It never sends your name, handle, account, friends, date of birth, notes or custom exercise names. The server stores each entry with the month only and no identifier, and separately counts how many entries each account sent that month, to cap them at 60, but never which ones. Turning it off stops future contributions. Past contributions stay in the pool because nothing identifies them.

## Device backups

Your device's own backup service may include Fitness Hunter's database. On iPhone this is iCloud Backup, and on Android it is Google's backup service. Those backups are made and stored by Apple or Google under their own terms, not by Fitness Hunter. You can turn them off in your device settings.

## Optional account linking

If you choose Link with Apple or Link with Google, the relevant provider SDK handles that identity request. Fitness Hunter stores an account record containing the provider, subject identifier, linked-at time, and, when the provider supplies one, the email address for that account. The app shows that email in Settings so you can see which account is linked. The email stays on your device and is not sent to the Fitness Hunter server. If you use Apple's Hide My Email, the stored address is the relay address Apple provides.

The Fitness Hunter server verifies the provider token before creating a server session. It stores a hash of that session token, rather than the token itself.

What Apple or Google does with a sign-in request is covered by their own privacy policies, not this one.

## Step data

On iOS, Fitness Hunter reads step counts directly with CoreMotion's CMPedometer. It does not use HealthKit or Apple Health for this feature. Daily step totals are stored locally.

## Export

When you select Export data, the app makes a JSON file containing its raw-log tables, formula versions, and custom exercises, then opens your device's system share sheet. It does not choose a recipient. The file can leave your device only when you select a sharing destination.

## Feedback

If you choose Send feedback, or Suggest a machine from Merge to catalogue, the message is sent to the Fitness Hunter server along with your app version, phone model, and a random installation identifier, and is kept there so the developer can read it.

## Keeping and removing your data

Your raw training log and other app data stay on your device until you remove them. The server copy is limited to the linked-account identity and session metadata, derived profile snapshot, username and tag, and friendship records described above.

Unlinking removes the account record, including its stored email address, and the session from this device and attempts to delete that session from the server. It does not delete the server-side linked-account identity, derived profile snapshot, username, or friendship records, and it does not delete your training history, which stays under the local identity the app created the first time you opened it. The permanent record of any username and tag pair you claimed is also not deleted, for the reason described above. To ask for deletion of server-side data, contact maerasoft@gmail.com.

Deleting the app removes its database from your device. That cannot be undone, so use Export data first if you want to keep a copy.

## Who provides this app

Fitness Hunter is made by an independent developer based in Ontario, Canada.

Questions about this policy can be sent to maerasoft@gmail.com.

## Governing law

This policy is governed by the laws of the Province of Ontario and the federal laws of Canada that apply there.
