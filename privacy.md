---
title: Budget Saver Privacy Policy
---

# Savings Challenge & Budget Privacy Policy

Effective date: 2026-11-22

This policy explains how Savings Challenge & Budget (shown as "Budget Saver" on your Home
Screen, the "App"), made by Stanislau Malchanau ("we", "us"), handles your information.
Short version: **we do not collect, sell or share your personal data. Your budget stays on
your device and in your own iCloud account. The App does not hold or move money, is not
connected to any bank, and does not give financial advice.**

## 1. Data the App stores

The App stores the following on your device: your expenses, income and refunds (the amount,
its currency and the exchange rate used, the category, a note, the date, time and time zone,
and how the entry was added, for example typed, from a receipt or from Apple Pay), your
categories and their limits, your monthly budget and its settings (the day your month starts,
whether what is left carries over), your recurring payments, your savings goals with what you
put aside and took out, your savings challenges, the exchange rates you typed yourself, the
shared budget you keep with one person you invite (section 3), your answers to the first
launch's questions, and your settings (the reminder time, the Face ID lock, sound and
vibration). Deleted entries are kept in "Recently Deleted" for 30 days so that you can bring
them back.

These records describe how you spend and save, and some laws treat such information as
financial or sensitive. They never leave your device and your iCloud account (sections 2 and
3). We do not run servers that receive your records, we have no access to them, and the App
never sends your entries to an online AI service or to anyone else. The one small server we do
run (section 6) answers with exchange rates and signs discount offers; it never receives your
records.

## 2. iCloud sync

If you are signed in to iCloud, the App syncs your budget through Apple's CloudKit, in the
private database of your own iCloud account, so that it is there on a new phone and after a
reinstall. This data is stored and protected by Apple under Apple's Privacy Policy
(https://www.apple.com/legal/privacy/). We cannot see, read or export it. When something
changes in iCloud, Apple's push service may wake the App so that it fetches the change; that
notification carries none of your records. You can turn sync off in iOS Settings >
[your name] > iCloud; your budget then stays only on this iPhone.

## 3. The shared budget

You can invite one person to a budget you keep together. The invitation is an iCloud link
that you send yourself, and the shared budget is stored by Apple in a CloudKit shared zone that
only the two of you can open. What either of you adds to it is seen by the other person, and
each entry shows who added it; your own budget is never shared. If you type your name for the
shared budget, the other person sees it with your entries; it is stored with your budget in
your iCloud account and in the shared zone. The App tells the person you
invited whether your subscription is active, so that they can add entries to the shared budget
for free (section 2 of the Terms of Use). Either of you can leave or close the shared budget in
the App at any time. If you stop sharing, the other person may keep a read-only copy of what
was in the shared budget until then. When Apple notifies the App that the other person added
something, the notification goes through Apple's push service.

## 4. Receipt scanner and the camera

The App uses the camera only when you open the receipt scanner, and iOS asks for your
permission the first time. The photo of the receipt is read on your iPhone: Apple's Vision
framework finds its text and any QR code, and on iPhones with Apple Intelligence, Apple's
on-device language model helps find the total, the currency and the shop's name. The photo and
the recognized text stay only in the phone's memory while they are read and are deleted right
after. They are never saved, never uploaded and never sent to us or to any online service.
Only the expense you then save (its amount, currency, date and the shop's name in the note) is
stored, like any other entry.

## 5. Apple Pay through Shortcuts

The App does not read your Wallet, your cards or your bank. If you choose to set up a personal
automation in Apple's Shortcuts app with its "Transaction" trigger, then each time you pay with
Apple Pay in a shop, Shortcuts passes the amount and the merchant's name to the App's action
for adding an expense, on the same iPhone, and the App records an expense from them. Nothing of
this is sent to us; the entry is stored and synced like any other (sections 1 and 2). Nothing
happens unless you set the automation up yourself, and you can change or delete it in
Shortcuts at any time.

## 6. Exchange rates and discount offers (our server)

We run one small server, on Cloudflare Workers, for two jobs. Neither of them receives your
records.

- **Exchange rates.** When an expense is in a currency other than your main one, or you change
  your main currency, the App asks the server for the rates of that day. The request carries
  only the date: no amount, no currency and nothing about you. The server takes the day's
  reference rates from the European Central Bank and, for currencies the bank does not publish,
  central bank rates gathered by the open Frankfurter service, and sends back the whole table
  for that day; your iPhone picks the rate it needs. Expenses in your main currency never need
  the server.
- **Discount offers.** If you turn off renewal, the App may offer you a lower price for your
  next period (section 2 of the Terms of Use). Apple requires such an offer to be signed by
  us, so right before the purchase the App sends the server only the App's own identifier, the
  identifiers of the plan and of the offer and, where Apple asks for it, the App Store's
  number of your current subscription purchase. The server adds a random one-time number, signs
  them, replies and keeps nothing. It learns nothing about who you are: no name, no Apple
  Account and none of your records.

Like any server, ours sees the IP address of a request in order to answer it. It does not
store that address in anything it keeps and does not link requests to a person. Cloudflare,
which runs the server, may keep short-lived technical logs of requests for security and
reliability under its own privacy policy (https://www.cloudflare.com/privacypolicy/).

## 7. Notifications and widgets

The evening reminder is scheduled on your iPhone, and only if you allow notifications. No data
is sent to us to deliver it. Widgets read your budget on your device.

## 8. Face ID lock

If you turn on the lock, the App asks iOS to check your Face ID, or your passcode. Face ID is
handled entirely by iOS: the App never sees your face data and learns only whether the check
passed.

## 9. Purchases

Subscriptions are sold and processed by Apple through the App Store. We do not receive your
payment details. Apple tells the App whether your subscription is active, which plan you chose
with its price, whether renewal is on, and whether an offer is available to your Apple
Account; section 10 says what of it goes to our usage analytics.

## 10. Usage analytics and crash reports

To learn which features help and where the App gets in the way, the App sends anonymous usage
signals to TelemetryDeck, an analytics service of TelemetryDeck GmbH (Augsburg, Germany) with
servers in the EU. Its code is the only code in the App that does not come from Apple or from
us. A signal names an action in the App: for example, that a step of the first launch was
finished and which of its multiple-choice answers was picked (what got in the way before,
whether you set a monthly budget, the day your month starts, the kind of your first goal from
the list and in how many months), how long the first expense took, that an expense or income
was added and how (typed, from a widget, a receipt, Apple Pay or a file) and whether it was in
your main currency, that a goal was created (its kind from the list and whether it has a
date), that money was put aside, a challenge started or a cell marked, that a sheet was opened
or a file imported (with a rough count of its lines), that the subscription screen or an offer
was shown, a plan picked, or a subscription started, renewed or restored, that the App asked
for a rating, or, as a short error code, that something did not work, such as the App Store not
answering. It comes with a timestamp rounded to the hour and general technical details: the App
and iOS versions, the device model, the language, region and time zone, and display and
accessibility settings such as dark mode or text size. When a subscription starts or renews,
its signal also carries the plan, its price converted to US dollars, the currency and the
country of your App Store, so that we can see which plans people choose.

A signal never contains your amounts, balances or budget figures, your categories, notes or
goal names, shop or merchant names, receipt photos or their text, the exchange rates you typed,
your name, email address, Apple Account or location, or anything about the person you share a
budget with. Your installation is identified only by a random identifier that the App salts and
hashes before sending, so the signals cannot be traced back to you or followed across apps.
TelemetryDeck stores no IP addresses and uses no cookies. We look at these signals only as
statistics to improve the App; we do not sell them, share them with advertisers or use them to
track you. The App contains no advertising or tracking code and does not track you across other
apps or websites.

Separately, if you choose to share analytics with app developers in iOS Settings > Privacy &
Security > Analytics & Improvements, Apple may give us aggregated, anonymous usage statistics
and crash reports. They do not identify you.

## 11. Game Center

If you are signed in to Game Center, achievements for your savings milestones are reported to
Apple's Game Center under your Game Center account and handled under Apple's Privacy Policy. An
achievement says only that a milestone was reached; your entries, notes and goal names are not
sent. We do not receive your Game Center identity.

## 12. Import and export

An export of your expenses and income as a CSV file, and an import of a CSV file from another
budget app, are made on your device. The App reads only the file you pick, and an exported file
goes only where you send it with the share sheet.

## 13. What the App does not do

The App does not hold, move, invest or lend money. It is not connected to any bank, card or
payment account, and it does not give financial, tax or investment advice. It does not read
your Wallet, location, contacts, photo library or microphone, and it has no account, sign-in,
advertising, chat or public feed.

## 14. Children

The App is suitable for all ages (rated 4+) and does not knowingly collect personal information
from anyone, including children under 13 (or the equivalent age in your country).

## 15. Data retention and deletion

Data stays as long as you keep it. You can delete an entry in the App at any time; it waits in
"Recently Deleted" for 30 days and is then gone. You can delete everything by deleting the App
and, for synced data, in iOS Settings > [your name] > iCloud > Manage Account Storage > Budget
Saver. What you added to a shared budget stays there for the other person until one of you
deletes it or the shared budget is closed. Because we hold no copy, there is nothing further
for us to delete. Usage signals are anonymous and cannot be matched to you, and our server
keeps nothing about you, so there is no personal record of either to look up or delete.

## 16. Your rights

Depending on where you live (for example under the GDPR in the EU, UK GDPR, CCPA/CPRA in
California, APPI in Japan, PIPA in Korea or LGPD in Brazil), you may have the right to access,
correct, delete or port your personal data, and to object to or restrict its processing. Since
we do not hold your data, you can exercise these rights directly on your device and in iCloud
as described above; the CSV export in Settings gives you all of your expenses and income in one
file. You can also contact us with any request or question, and you may complain to your local
data protection authority.

We do not sell or share personal information as defined by the CCPA/CPRA.

## 17. Changes

If this policy changes, we will update the effective date above and, for material changes,
tell you in the App.

## 18. Contact

Stanislau Malchanau, Belarus
Email: 7tam.official@gmail.com
