# GRT Stop Request App

A web app concept that lets passengers on Grand River Transit (GRT) buses digitally request a stop an alternative to the physical button when it's broken or unavailable and just for ease for people during rush hours or for people planning trips. 

---

## The Problem

A lot of GRT buses in Kitchener-Waterloo have unreliable stop-request buttons. The idea here is to give passengers a way to signal their stop from their phone, with the driver seeing the request on their end in real time. This alongside the normal stop request buttons will help not only disabled passengers but passengers who require more assitance in thier day to day lives.

---

## General Idea

- Passenger opens the app and selects their bus route
- Taps a button to request their stop
- The request shows up on a driver-facing screen in real time

The exact implementation is still being figured out, this repo is for exploring the concept.

---

## Possible Tech Approach

One option that seems realistic for a prototype:

| Layer | Option |
|-------|--------|
| Frontend | React or plain HTML/JS |
| Real-time sync | Firebase Realtime Database |
| Notifications | Firebase Cloud Messaging |
| Route data | GRT GTFS open data |

*CURRENTLY FIREBASE IS DOWN FIX IMMEDIATELY
---

## Route Data

GRT publishes open transit data in GTFS format (routes, stops, schedules), available free from the [Region of Waterloo Open Data portal](https://www.grt.ca/about-grt/open-data/).

---

## Status

Early stage / proof of concept. Nothing is finalized yet this is being built to explore the idea and potentially demo to GRT.

---

## Notes

FIX FIREBASE REBASE ISSUE 
CREATE SO IF IT SENSE YOU ARE NOT ON THE BUS OR NEAR THE AREA THAT YOU CANNOT SUBMIT A REQUEST TO AVOID OVERFLOW
- No login or accounts planned
- No personal data would be collected
- Requests would be anonymous
