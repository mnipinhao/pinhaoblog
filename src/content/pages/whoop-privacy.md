---
title: Privacy Policy for a Personal WHOOP Integration
description: How the owner's personal WHOOP integration reads, uses, and stores sleep and workout data.
---
Last updated: 2026-11-05

This policy covers the personal WHOOP integration run by the owner of this website (“the App”). The owner is the App’s only user: it is not offered to anyone else, and only the owner’s WHOOP account is connected to it.

## What the App reads

With the owner’s authorization, the App reads two kinds of records through the WHOOP API:

- Sleep (`read:sleep`): start and end times, time zone offset, whether it was a nap, scoring status, and the time spent in light, slow-wave, and REM sleep.
- Workouts (`read:workout`): start and end times and time zone offset.

It also requests `offline` access, which gives it a refresh token so the owner does not have to sign in every day. It does not request profile, recovery, cycle, or body measurement data. Other fields returned by the API are discarded.

## How the data is used

On the owner’s Mac, once a day and whenever the owner records a week, the App turns these records into two weekly numbers:

- the number of days with at least 20 minutes of workouts, and
- the average nightly sleep in hours, excluding naps.

The records are processed in memory and are never written to disk. Only the two weekly numbers are kept.

## Where the weekly numbers are kept

- In a private Git repository on the owner’s Mac and on the owner’s home server.
- They may also be shown in the owner’s own apps on the owner’s Mac and iPhone.

Data moves between these devices only over encrypted connections. The owner reviews the numbers with an AI assistant (Anthropic’s Claude), so they are sent to Anthropic during those reviews and handled under Anthropic’s terms.

## Sharing

The App does not sell, rent, or share WHOOP data, and does not use it for advertising. Apart from the AI assistant described above, no third party receives it.

## Retention and deletion

The weekly numbers are kept until the owner deletes them. If the owner stops using the WHOOP API, the owner will revoke the App’s access and delete the stored numbers, including from the repository’s history.

## Credentials

The App’s client credentials and refresh token are stored only in the macOS Keychain on the owner’s Mac. They are never written to files.

## Revoking access

The owner can revoke the App’s access at any time. The App then calls WHOOP’s revoke endpoint and deletes its stored token.

## Contact

The owner is the App’s only user. WHOOP can reach the owner through the contact email registered for the App in the WHOOP Developer Dashboard.
