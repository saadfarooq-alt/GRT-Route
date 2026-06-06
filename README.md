# GRT Stop Request App

A web app concept that lets passengers on Grand River Transit (GRT) buses digitally request a stop — an alternative to the physical button when it's broken or unavailable.

This is a work in progress and the approach may change as the project develops.

---

## The Problem

A lot of GRT buses in Kitchener-Waterloo have unreliable stop-request buttons. The idea here is to give passengers a way to signal their stop from their phone, with the driver seeing the request on their end in real time.

---

## General Idea

- Passenger opens the app and selects their bus route
- Taps a button to request their stop
- The request shows up on a driver-facing screen in real time

The exact implementation is still being figured out — this repo is for exploring the concept.

---

## Possible Tech Approach

One option that seems realistic for a prototype:

| Layer | Option |
|-------|--------|
| Frontend | React or plain HTML/JS (PWA) |
| Real-time sync | Firebase Realtime Database |
| Notifications | Firebase Cloud Messaging |
| Route data | GRT GTFS open data |

This isn't set in stone — the stack may change depending on what direction things go.

---

## Route Data

GRT publishes open transit data in GTFS format (routes, stops, schedules), available free from the [Region of Waterloo Open Data portal](https://www.regionofwaterloo.ca/en/living-here/grt-open-data.aspx).

---

## Status

Early stage / proof of concept. Nothing is finalized yet — this is being built to explore the idea and potentially demo to GRT.

---

## Notes

- No login or accounts planned
- No personal data would be collected
- Requests would be anonymous
