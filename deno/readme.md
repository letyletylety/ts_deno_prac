** deno 1.29 버전 기준으로 설명합니다.**

https://deno.land/manual@v1.29.0/introduction

# Introduction

Deno(dee-no) 는 JS, TS, WA 런타임입니다.

It's built on V8, Rust, and Tokio.

## Feature highlights

- Provides web platform functionality and adopts web platform standards. For
  example using ES modules, web workers, and support fetch().
- 기본적으로 안전하다. file, network, environment 에 명시적으로 접근을 가능하게
  하지 않으면 접근할 수 없다.
- 타입스크립트를 즉시 지원한다.
- 하나의 exe 로 모든 것을 사용할 수 있다.
- 개발 툴을 빌트인으로 제공. 린터, 포매터, 테스터, 랭귀지 서버 포함
- Has a set of reviewed (audited) standard modules that are guaranteed to work
  with Deno.
- Can bundle scripts into a single JavaScript file or executable.
- Supports the use of existing npm modules

## Philosophy

Deno aims to be a productive and secure scripting environment for the modern
programmer.

Deno will always be distributed as a single executable. Given a URL to a Deno
program, it is runnable with nothing more than the ~31 megabyte zipped
executable. Deno explicitly takes on the role of both runtime and package
manager. It uses a standard browser-compatible protocol for loading modules:
URLs.

Among other things, Deno is a great replacement for utility scripts that may
have been historically written with Bash or Python.

## Goals

- Ship as just a single executable (deno).
- Provide secure defaults.
  - Unless specifically allowed, scripts can't access files, the environment, or
    the network.
- Be browser-compatible.
  - The subset of Deno programs which are written completely in JavaScript and
    do not use the global Deno namespace (or feature test for it), ought to also
    be able to be run in a modern web browser without change.
- Provide built-in tooling to improve developer experience.
  - E.g. unit testing, code formatting, and linting.
- Keep V8 concepts out of user land.
- Serve HTTP efficiently.

## Other key behaviors

Fetch and cache remote code upon first execution, and never update it until the
code is run with the --reload flag. (So, this will still work on an airplane.)

Modules/files loaded from remote URLs are intended to be immutable and
cacheable.

---

# Installation

(macOs and Linux)

```bash
curl -fsSL https://deno.land/x/install/install.sh | sh
```

# 개발 환경 세팅

vscode + deno 플러그인

# 실행

deno run [...].ts
