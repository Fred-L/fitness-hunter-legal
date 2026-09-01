---
title: Fitness Hunter Privacy Policy
---

# Fitness Hunter Privacy Policy

## Current version and changes

Last updated 1 September 2026.

This policy describes Fitness Hunter as it ships today. It will be updated before a version with sync or another off-device service is released.

## Information stored on this device

Fitness Hunter keeps application data in an on-device SQLite database. This includes profile and preference information; workout, set, cardio, habit, bodyweight, health-metric, and daily step records; exercise and program data; progression and app-state records; and the optional account-link record described below.

## No Fitness Hunter server or sync

Fitness Hunter has no server and no sync feature. It does not upload the information described above to a Fitness Hunter service.

## Device backups

Your device's own backup service may include Fitness Hunter's database. On iPhone this is iCloud Backup, and on Android it is Google's backup service. Those backups are made and stored by Apple or Google under their own terms, not by Fitness Hunter. You can turn them off in your device settings.

## Optional account linking

If you choose Link with Apple or Link with Google, the relevant provider SDK handles that identity request. Fitness Hunter stores an account record containing the provider, subject identifier, and linked-at time.

The app currently has no server that validates a provider token, so this link is unverified and does not prove identity to another user.

What Apple or Google does with a sign-in request is covered by their own privacy policies, not this one.

## Step data

On iOS, Fitness Hunter reads step counts directly with CoreMotion's CMPedometer. It does not use HealthKit or Apple Health for this feature. Daily step totals are stored locally.

## Export

When you select Export data, the app makes a JSON file containing its raw-log tables, formula versions, and custom exercises, then opens your device's system share sheet. It does not choose a recipient. The file can leave your device only when you select a sharing destination.

## Keeping and removing your data

Because Fitness Hunter stores everything on your device, your data stays there until you remove it. There is no copy on a Fitness Hunter server to delete.

Unlinking an account removes the account record described above. It does not delete your training history, which stays under the local identity the app created the first time you opened it.

Deleting the app removes its database from your device. That cannot be undone, so use Export data first if you want to keep a copy.

## Who provides this app

Fitness Hunter is made by an independent developer based in Ontario, Canada.

Questions about this policy can be sent to maerasoft@gmail.com.

## Governing law

This policy is governed by the laws of the Province of Ontario and the federal laws of Canada that apply there.
