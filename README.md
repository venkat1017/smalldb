# MiniSQLite from Scratch

A 10-part, first-principles tutorial for building a small relational database engine in Go.

**Website:** https://venkat1017.github.io/smalldb/

The series progresses from raw bytes and fixed records to pages, checksums, B+trees, schemas, SQL parsing, query execution, transactions, secondary indexes, WAL, concurrency, and hardening.

## Chapters

1. [Build a Database From Bytes](part-01.html) — Start from an empty Go project and build persistent fixed-size records from raw bytes.
2. [Pages: The Unit of Disk I/O](part-02.html) — Replace scattered raw offsets with 4096-byte pages, a pager, caching, dirty pages, and flushing.
3. [Reliable File Format](part-03.html) — Add page headers, metadata, checksums, validation, and experiments that detect corruption and torn writes.
4. [B-Tree Indexing](part-04.html) — Separate logical row IDs from physical locations and build a persistent B+tree for fast lookup.
5. [Tables, Rows, and Schemas](part-05.html) — Move beyond one hard-coded record shape with typed schemas, row encoding, and a persistent catalog.
6. [SQL Parsing](part-06.html) — Turn SQL text into tokens and an AST using a lexer and recursive-descent parser.
7. [Query Execution](part-07.html) — Execute ASTs through binders and pull-based cursors, including scans, filters, and indexed rowid lookups.
8. [Transactions and Recovery](part-08.html) — Implement BEGIN/COMMIT/ROLLBACK with a rollback journal, crash simulation, and startup recovery.
9. [Secondary Indexes and Planning](part-09.html) — Add persistent secondary indexes and a planner that chooses rowid lookup, index lookup, or full scan.
10. [Concurrency, WAL, and Hardening](part-10.html) — Finish with reader/writer locking, WAL commits, checkpoints, durability modes, benchmarks, and hardening tests.

## GitHub Pages

This repository is ready to deploy with the included GitHub Pages workflow in `.github/workflows/pages.yml`.

If Pages has not been enabled yet, open **Settings → Pages** in the repository and select **GitHub Actions** as the source. A push to `main` will deploy the site.
