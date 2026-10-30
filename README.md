# Personal Manager — project showcase

Public overview page for **Personal Manager**, a self-hosted income and expense manager with an
offline-capable device app, a credential vault and a personal organizer.

**Live page:** https://dp2kv.github.io/personal-manager-showcase/

[![.NET](https://img.shields.io/badge/.NET-10.0-512BD4)](https://dotnet.microsoft.com/)
[![Blazor](https://img.shields.io/badge/Blazor-Interactive%20Server-5C2D91)](https://learn.microsoft.com/aspnet/core/blazor/)
[![MAUI](https://img.shields.io/badge/.NET%20MAUI-Android%20%7C%20Windows-5C2D91)](https://learn.microsoft.com/dotnet/maui/)
[![EF Core](https://img.shields.io/badge/EF%20Core-10-512BD4)](https://learn.microsoft.com/ef/core/)

---

## What this repository is

This repository contains **only the public showcase page** — a single static HTML file and the
architecture diagrams it displays, served by GitHub Pages.

**It does not contain the application source.** Personal Manager is developed in a private
repository; this page exists to describe the work and the decisions behind it.

## The project in one paragraph

One .NET solution where a Blazor Interactive Server web app, a .NET MAUI Blazor Hybrid device app
(Android and Windows) and an ASP.NET Core API share the same domain, the same Razor UI and the same
database schema. A screen is written once and renders in both hosts. The device app owns a complete
SQLCipher-encrypted local replica with an encrypted outbox, so it is fully usable with no network
and reconciles with the server through an idempotent change feed when one is available.

## Contents

| Path | Purpose |
| --- | --- |
| `index.html` | The showcase page — self-contained, no build step, no external requests |
| `assets/architecture-overview.svg` | How the hosts, shared layers and databases fit together |
| `assets/layers-and-dependencies.svg` | Layering and dependency direction |
| `assets/one-read-two-hosts.svg` | A single read path serving both hosts |
| `assets/sync-engine.svg` | Local write → encrypted outbox → change-feed pull → idempotent replay |
| `assets/icon-192.png`, `assets/favicon.png` | App icon and favicon |
| `.nojekyll` | Serves the files as-is, skipping Jekyll processing |

## Running it locally

No toolchain required — open `index.html` in a browser.

## Licence

No licence is granted. The application source is private, and the diagrams here are from the
project's own design documentation.
