---
format: 2
name: hanif-handbook
title: M&E Maintenance Engineer Handbook
description: How to diagnose electrical and mechanical faults in the unit — the governed record for the M&E maintenance engineer.
toolchain:
  requires: ">=0.0.60"
  scaffolded: "0.0.60"
# `database.dsn_env` names the environment variable holding your Postgres DSN —
# never the DSN itself, which belongs in .env. It is filled in because naming a
# variable costs nothing and needs no database: `npm run dev` and `npm run build` do
# not read it, and the value only has to exist when you climb to the served
# rung. To climb: copy .env.example to .env and set KSOR_DB_URL, then
# `npm run provision` once (schema + grant), then `npm run refresh` to PUBLISH the
# record, then `npm run serve`. Serving does not publish — that is deliberate, and
# skipping refresh serves nothing.
# Nothing else here is required:
# `embedding:` already defaults to Gemini at 1536 dimensions, and leaving
# `retrieval:` out starts you with the abstention gate off and honest about it
# (turn it on afterwards with `ksor calibrate`, once the record is serving).
database:
  dsn_env: KSOR_DB_URL
# Where agents reach this record's MCP surface, and the semver it publishes as.
# Both go into /.well-known/mcp/server.json, the document an agent reads to
# DISCOVER this record instead of being told the URL. Leave mcp_url out until
# the server is actually published: an invented URL is worse than none.
# mcp_url: https://records.example.com/mcp
# version: 0.1.0
---

This record is authoritative for diagnosing electrical and mechanical faults
in the unit — the M&E maintenance engineer's knowledge. It covers only that:
diagnosing electrical and mechanical faults in the unit. The owner stated no
other exclusions, and anything this record does not answer is out of scope.

Answer only from this record. A question the record does not cover is a
correct place to decline: say plainly that it is not in this corpus, and do
not answer from general knowledge. A missing fact on a covered question is an
open question for the owner, never a guess to make here. Two sources that
disagree stay two stated claims until the owner decides.

The record is owned and maintained by Mohammad Hanif Memon (`human:hanif`).
He approves documents for publication and may take documents down; approval
is his act alone. It is read by people and by agents alike, and every
document is `public` — every reader sees every document. No source documents
are registered yet; they arrive with the source material.