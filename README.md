# Manus UI Adapter Lab

This repository is the **development lane** for small, deterministic UI-adapter experiments derived from publicly documented patterns.

## Purpose

The lab develops only local fixtures, selector contracts, accessibility-oriented UI helpers, and static analysis tools. It is not a browser control system and is not a collection agent.

## Safety and Data Boundary

Tests must run against local synthetic pages. Source code and CI must not use production hostnames, logged-in sessions, browser-storage extraction, network interception, cookies, authorization values, account replay data, private APIs, or automated message dispatch.

## Structure

| Path | Purpose |
|---|---|
| `src/` | Minimal, independently reviewed helper modules. |
| `tests/` | Deterministic unit and fixture tests. |
| `fixtures/` | Synthetic HTML/DOM fixtures. |
| `docs/` | Adapter contracts, assumptions, and review records. |

## Engineering Rules

Each adapter must declare its input contract, output contract, failure mode, test fixture, source provenance, and owner. The default behavior is fail closed: unknown DOM structure returns an explicit unsupported result rather than guessing or acting.
