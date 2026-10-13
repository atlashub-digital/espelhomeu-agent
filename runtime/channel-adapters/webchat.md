# WebChat Adapter — Target Contract

## Purpose

Provide EspelhoMeu inside the website/app with the richest direct connection to authenticated identity and entitlements.

## Anonymous state

Mode:
PRIVATE_FREE

May:
- introduce EspelhoMeu;
- offer public/sample content;
- answer catalogue questions.

## Authenticated state

Resolve:
- user;
- entitlements;
- progress;
- consent;
- selected memory.

## Reader integration

WebChat should be able to receive safe contextual references such as:
- current publication;
- current chapter/unit;
- current Reader route.

Do not send the full protected publication as conversational context unless necessary and authorized.

## Deep links

May return:
- continue reading;
- open workbook;
- view Library;
- open My Evolution;
- manage reminders;
- account/privacy controls.

## Human handoff

Show clear state if conversation has moved to a human support flow.

## Privacy

Do not expose memory in browser payloads that do not need it.

The server should build the minimum context envelope.
