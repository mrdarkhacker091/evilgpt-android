# EvilGPT Android wrapper

This repository is an Android Trusted Web Activity (TWA) wrapper for the hosted EvilGPT site:

- Launch URL: https://evil-gpt-sepia.vercel.app/chat
- Android application ID: `com.evilgpt.app`
- Minimum Android version: API 23
- Compile/target SDK: API 34

## Build

Use JDK 17, Android SDK platform 34, and Gradle 8.7. The GitHub Actions workflow generates the Gradle wrapper and builds `assembleRelease`.

A release can be built unsigned when signing secrets are not configured. To produce a signed release, configure these GitHub Actions secrets: `KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS`, and `KEY_PASSWORD`. Keep signing keys outside the repository and rotate any key that has been exposed.

## Project scope

This archive contains the TWA launcher configuration and Android resources. It does not contain a native Kotlin/Java application source tree; the app opens the hosted web application. Changes to the website itself must be made in its web project.
