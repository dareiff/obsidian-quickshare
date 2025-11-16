# Obsidian QuickShare - Securely share your Obsidian notes with one click

Self-host your obsidian notes over the internet using end-to-end encryption.

## About This Fork

This project has evolved significantly from the original version. All credit and props go to [mcndt](https://github.com/mcndt) for creating this amazing plugin and the companion service (now dead). The core concept and foundation remain, but this version includes a bit of 2025 modernity and _some_ feature changes.

## How it works

Your notes are stored securely using strong AES-256-CBC encryption. The decryption key is never sent to the server, so not even the server can open your notes.

## Functionality

- AES-256-CBC encryption with single-use encryption keys
- Easy server setup with [docker](https://github.com/dareiff/noteshare.space#deployment)

## Installing

Installation coming, but:

- Clone the repository
- Install dependencies
- Configure environment variables
- Run the server

## Feedback

The preferred way to report bugs or request new features for the web app or the Obsidian plugin is via the [GitHub issues page](https://github.com/dareiff/obsidian-quickshare/issues/new/choose).
