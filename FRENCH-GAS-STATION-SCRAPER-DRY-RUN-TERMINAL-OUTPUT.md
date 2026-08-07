## Dry run of release.sh replaying real history

Each release below was produced by actually running `release.sh -y -n --since <prev> --to <this>` against a local clone of the repository, oldest-first, using the `--since`/`--to` replay range described in the script's own `--help`. This is the script's own version/notes logic (independent implementation from the hand-reconstructed table above) run against the real repository as a cross-check. No tags were created and nothing was pushed (`--dry-run`).

### v0.0.1

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 1ed47cf
Target ref      : 1ed47cf (tag will be created there, not on HEAD)
Commits scanned : 9

  other     1ed47cf docs: remove socialMediaPublisherApp stale references (#8)
  other     b7cbe53 docs: finalize starting prompts in README.md
  fix       c694167 fix: remove old code from social share app
  fix       d158426 fix: remove old code from social share app
  other     9fdd70a chore: remove useless components + run first build
  other     62258ee chore: init project code using social media sharing app
  other     e415adf ci(agent): init CLAUDE.md
  other     90c0f4c Enhance README with scraping and user interaction details
  other     c6f4898 Initial commit

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Bug fixes

- fix: remove old code from social share app ([c694167](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/c694167bbd1ea4a42603117c86ceadb73333e38c))
- fix: remove old code from social share app ([d158426](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/d158426331fdd3da37efa2cce2d06967bcedb49b))

## Others

- docs: remove socialMediaPublisherApp stale references from agents and ADRs (#8)
- docs: finalize starting prompts in README.md ([b7cbe53](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/b7cbe533b5293adca35072fa78720f877152f47a))
- chore: remove useless components + run first build ([9fdd70a](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/9fdd70a0f6b1e52a2fb15a4cab595745472505c9))
- chore: init project code using social media sharing app ([62258ee](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/62258eef682541edad3cd68a7a536675844f4c5d))
- ci(agent): init CLAUDE.md ([e415adf](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e415adf5070f3e30028bb40cf093d5f4dd7f7675))
- Enhance README with scraping and user interaction details ([90c0f4c](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/90c0f4c092e93c95f35c71acdc86916681aadaf4))
- Initial commit ([c6f4898](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/c6f489809996ffafee3e56d1f5cb916e323c02b0))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 1ed47cf
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.0.2

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 1ed47cf..f9146e3 (last tag: 1ed47cf)
Target ref      : f9146e3 (tag will be created there, not on HEAD)
Commits scanned : 5

  other     f9146e3 ci(agent): fix Step 0 order — create worktree before writing README.md
  other     c869b43 ci(agent): fix git push in Task 5 to use explicit branch for worktrees
  other     9b17878 ci(agent): consolidate guidance into CLAUDE.md, fix orchestrator trigger
  other     9713ea9 ci(agent): integrate rtk
  other     48375e6 ci(agent): fix agent-4-git Task 7 and Task 8 for bare-repo worktree setup (#11)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- ci(agent): fix agent-4-git Task 7 and Task 8 for bare-repo worktree setup (#11)
- ci(agent): fix Step 0 order — create worktree before writing README.md ([f9146e3](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/f9146e302b182d658a9b1bf1a0a247a167cf52d2))
- ci(agent): fix git push in Task 5 to use explicit branch for worktrees ([c869b43](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/c869b43f861cbbfe0de9d385c57a70769275108f))
- ci(agent): consolidate guidance into CLAUDE.md, fix orchestrator trigger ([9b17878](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/9b178781bc878496f008ee71d5f5c59aadae479c))
- ci(agent): integrate rtk ([9713ea9](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/9713ea991a9f70c2efc37e73a765c4a2504b4bfb))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 f9146e3
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.0.3

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : f9146e3..432eb91 (last tag: f9146e3)
Target ref      : 432eb91 (tag will be created there, not on HEAD)
Commits scanned : 1

  other     432eb91 ci(agent): replace stale CLAUDE docs and agent-7 with two skills (#20)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- ci(agent): replace CLAUDE docs and agent-7 with two skills (#20)

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 432eb91
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.0.4

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 432eb91..d08c1fa (last tag: 432eb91)
Target ref      : d08c1fa (tag will be created there, not on HEAD)
Commits scanned : 2

  other     d08c1fa docs: document Claude Code setup and develop worktree creation
  other     a833e10 ci(agent): update agents and skills for develop/ as Claude Code root (#21)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- ci(agent): update agents and skills for develop/ as Claude Code root (#21)
- docs: document Claude Code setup and develop worktree creation ([d08c1fa](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/d08c1fa8f97115957b7cf48cfb49382b7e9471bc))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 d08c1fa
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.1.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : d08c1fa..ed7744a (last tag: d08c1fa)
Target ref      : ed7744a (tag will be created there, not on HEAD)
Commits scanned : 10

  other     ed7744a test: add type-safety specs for domain types introduced in issue #14
  other     e54497a refactor(types): remove stale boilerplate types and add domain types
  other     599475a ci(agent): reviewer must run lint/type-check directly, no package.json inspection
  other     e119d80 ci(agent): run npm install in new worktree after creation (Task 2)
  other     f5d052d ci(agent): orchestrator must use AskUserQuestion to relay subagent questions to human
  other     fd42bd0 ci(agent): fix worktree path — use relative path from bare repo root, not develop/
  other     9dee9e7 ci(agent): fix Step 0 — pass Type/Slug to agent-4-git; write README only after worktree exists
  other     93643ad test(cases): define test scenarios for clean up stale types (#14)
  feature   98eaf8a feat(security): add security guidelines for clean up stale types (#14)
  feature   4dc71dc feat(specs): define specs for clean up stale types and define domain types (#14)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- feat: clean up stale types and define Station, FuelPrice, StationData (#14)

## Others

- refactor(types): remove stale boilerplate types and add domain types ([e54497a](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e54497a839aa1a5f0aa9164ec93a97e7d6e75786))
- ci(agent): reviewer must run lint/type-check directly, no package.json inspection ([599475a](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/599475ac9f4f0d687f7ab804c35b51e2ba152390))
- ci(agent): run npm install in new worktree after creation (Task 2) ([e119d80](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e119d8083f3ab82d9e966e6ca1ecf25cb45c7d47))
- ci(agent): orchestrator must use AskUserQuestion to relay subagent questions to human ([f5d052d](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/f5d052db40864c84bbc59e68da8c00f93cb77a1c))
- ci(agent): fix worktree path — use relative path from bare repo root, not develop/ ([fd42bd0](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/fd42bd0f9d57b7fb9183f815bee1cb58645d4351))
- ci(agent): fix Step 0 — pass Type/Slug to agent-4-git; write README only after worktree exists ([9dee9e7](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/9dee9e7df6546ad579d0b5006ceec76afa6abe63))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 ed7744a
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.2.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : ed7744a..28354ce (last tag: ed7744a)
Target ref      : 28354ce (tag will be created there, not on HEAD)
Commits scanned : 7

  other     28354ce docs: add missing task artifacts and update auto-imports for issue #15
  other     8987022 test(composable): add useStationStorage spec with 14 passing test cases
  feature   80d73bf feat(storage): add useStationStorage composable backed by IndexedDB
  other     e934c71 ci(agent): document lint and type-check scripts in reviewer to avoid inspection
  other     5b7cde4 ci(agent): set fetch refspec before git fetch to keep origin/* refs current
  other     0075c46 test(cases): define test scenarios for useStationStorage composable (#15)
  feature   247c68a feat(security): add security guidelines for useStationStorage composable (#15)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- feat: implement IndexedDB composable for station list persistence (#15)
- feat(storage): add useStationStorage composable backed by IndexedDB ([80d73bf](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/80d73bf746c30a2c65e4a7244ff0882614e2073b))

## Others

- test(composable): add useStationStorage spec with 14 passing test cases ([8987022](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/8987022fe5117aa4f9f18a78729bd7ea0d6c2b4d))
- ci(agent): document lint and type-check scripts in reviewer to avoid inspection ([e934c71](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e934c7191acbda159573985a610532dfde63db8e))
- ci(agent): set fetch refspec before git fetch to keep origin/* refs current ([5b7cde4](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/5b7cde48aaed369552e66b46e5db283b12d50466))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 28354ce
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.3.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 28354ce..e63b868 (last tag: 28354ce)
Target ref      : e63b868 (tag will be created there, not on HEAD)
Commits scanned : 12

  other     e63b868 ci(agent): add rm -rf fallback in Task 8 for already-deregistered worktrees
  other     2302d3c refactor(parser): remove stationName from parser; source name from Station.name
  other     7293741 ci(agent): forbid node:fs and __dirname in tests; use Vite ?raw imports
  other     6137a01 test(parser): replace node:fs fixture loading with Vite raw imports
  other     557faee chore: update lockfile after removing jsdom
  other     7586975 ci(agent): guard test-writer against compile-time-only and filesystem tests
  other     5e0a4a6 test: remove stale types-issue-14 spec (redundant with vue-tsc)
  other     4d9c72e test(parser): add 9 spec tests for stationHtmlParser (issue #16)
  feature   c8bc03d feat(parser): add browser-side HTML parser and station prices composable
  other     bd61585 test(cases): define test scenarios for parse station HTML (#16)
  other     2e23cf2 docs(security): add security guidelines for parse station HTML (#16)
  other     eb49815 docs(specs): define specs for parse station HTML (#16)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- feat(parser): add browser-side HTML parser and station prices composable ([c8bc03d](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/c8bc03d1d0b11e318ffd4626a8ce820c923845a9))

## Others

- feat: enhance fetch-page Netlify function to parse station HTML and return structured JSON (#16)
- ci(agent): add rm -rf fallback in Task 8 for already-deregistered worktrees ([e63b868](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e63b868a08afbba0eede742d91b15ef41591b615))
- refactor(parser): remove stationName from parser; source name from Station.name ([2302d3c](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/2302d3ce07735596de77f296fb66f42a1726f019))
- ci(agent): forbid node:fs and __dirname in tests; use Vite ?raw imports ([7293741](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/7293741f5719dafe8706f3de4c70d877de2a0a0c))
- test(parser): replace node:fs fixture loading with Vite raw imports ([6137a01](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/6137a0119ef5c4f5267760baee44053f365418c0))
- chore: update lockfile after removing jsdom ([557faee](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/557faee497ab5b02cfb441ef949dc0ea218da22a))
- ci(agent): guard test-writer against compile-time-only and filesystem tests ([7586975](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/758697583385979ecc2defbca7fe01ea4cec6143))
- test: remove stale types-issue-14 spec (redundant with vue-tsc) ([5e0a4a6](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/5e0a4a6c69a110e719b2ff7e7ca9bfe337423f2d))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 e63b868
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.4.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : e63b868..fc9862f (last tag: e63b868)
Target ref      : fc9862f (tag will be created there, not on HEAD)
Commits scanned : 15

  other     fc9862f docs(agent-2-coder): add composable caller-responsibility rule
  other     87f1a96 test(station-manager): add TC-25 to TC-31 for inline success notification
  feature   764bbc3 feat(station-manager): show inline success message after a station edit saves
  other     a7b6ffe docs(specs): add inline success notification requirement to station management UI (#17)
  fix       16ca2fa fix(station-storage): strip Vue Proxy before writing to IndexedDB
  fix       ea5bf2d fix(station-manager): prevent false save errors on blur and null IDB rejections
  other     305681e chore(types): regenerate components.d.ts to register StationManager
  other     f2df724 chore(lint): exclude .netlify generated artifacts from ESLint
  fix       fed0a7f fix(station-storage): always merge README defaults into stored list on load
  fix       6b6120e fix(station-manager): call loadStations on mount and widen layout
  other     f638501 test(station-manager): add tests for updateStation and StationManager component
  feature   b1aee9c feat(station-manager): add live-edit station management table UI
  other     c43ced5 test(cases): define test scenarios for station management UI (#17)
  other     36ca2fa docs(security): add security guidelines for station management UI (#17)
  other     9a3ff80 docs(specs): define specs for station management UI (#17)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- feat(station-manager): show inline success message after a station edit saves ([764bbc3](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/764bbc37a94075250f15f2746a956a5b854faf62))
- feat(station-manager): add live-edit station management table UI ([b1aee9c](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/b1aee9c73dbe5a33626a073dccd34396ab8ddea9))

## Bug fixes

- fix(station-storage): strip Vue Proxy before writing to IndexedDB ([16ca2fa](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/16ca2fa71b6be39f06ae4b30be017a3fa17d082b))
- fix(station-manager): prevent false save errors on blur and null IDB rejections ([ea5bf2d](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/ea5bf2d678336ed4b7a685e8e83fa0d4a3c2f79f))
- fix(station-storage): always merge README defaults into stored list on load ([fed0a7f](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/fed0a7fedd8748755b4825bfc8c4f74a07103658))
- fix(station-manager): call loadStations on mount and widen layout ([6b6120e](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/6b6120e48f98cf671a9563627654a2b385bb375c))

## Others

- feat: implement station management UI (view list, add station, validate, save) (#17)
- docs(agent-2-coder): add composable caller-responsibility rule ([fc9862f](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/fc9862ff4307721ef8ebc80d2c7734c6ac87b58b))
- test(station-manager): add TC-25 to TC-31 for inline success notification ([87f1a96](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/87f1a9661f0befd042cca2ea2f041ca81a2b8701))
- chore(types): regenerate components.d.ts to register StationManager ([305681e](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/305681edcee209c6c56467cb164ba5be077ed697))
- chore(lint): exclude .netlify generated artifacts from ESLint ([f2df724](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/f2df724236d7d1061ea2d1d8b8d8ae1091ea5203))
- test(station-manager): add tests for updateStation and StationManager component ([f638501](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/f63850154082a0f882bdbb10d4c4d01d44ee4b57))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 fc9862f
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.5.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : fc9862f..4313ac3 (last tag: fc9862f)
Target ref      : 4313ac3 (tag will be created there, not on HEAD)
Commits scanned : 7

  fix       4313ac3 fix(useStationStorage): hoist stations ref to module level to restore singleton
  feature   35ba3fb feat(useStationPrices): fix composable caller-responsibility violation
  other     2cab35f test(useStationPrices): add unit tests for concurrent fetch composable (#18)
  feature   125d7d7 feat(useStationPrices): rework composable for concurrent multi-station fetching (#18)
  other     8a88abd test(cases): define test scenarios for concurrent fetch composable (#18)
  other     77444a7 docs(security): add security guidelines for concurrent fetch composable (#18)
  other     53868bb docs(specs): define specs for concurrent fetch composable (#18)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- feat: implement price-data composable with concurrent fetching, loading state, and warnings (#18)
- feat(useStationPrices): fix composable caller-responsibility violation ([35ba3fb](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/35ba3fbc531818e1ded38e063c1f38366eb4f5f6))

## Bug fixes

- fix(useStationStorage): hoist stations ref to module level to restore singleton ([4313ac3](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/4313ac342883a12da79081a861ccc408dfb6442c))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 4313ac3
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.6.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 4313ac3..8dfbe25 (last tag: 4313ac3)
Target ref      : 8dfbe25 (tag will be created there, not on HEAD)
Commits scanned : 5

  other     8dfbe25 test(fuel-type-selector): add unit and component tests for selector and price table (#19)
  feature   05ab9a6 feat(fuel-type-selector): add selector and price table to StationPrices (#19)
  other     0133712 test(cases): define test scenarios for fuel-type selector and price table (#19)
  other     11e502d docs(security): add security guidelines for fuel-type selector and price table (#19)
  other     9d6d3fd docs(specs): define specs for fuel-type selector and price table (#19)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- feat: implement fuel-type selector and price table (#19)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 8dfbe25
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.6.1

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 8dfbe25..7e151f5 (last tag: 8dfbe25)
Target ref      : 7e151f5 (tag will be created there, not on HEAD)
Commits scanned : 5

  other     7e151f5 docs: enforce rtk usage for auto-approved commands in CLAUDE.md
  other     fcb9ccc Revert "docs: align shell commands section with settings.local.json auto-approved permissions"
  other     5f48867 docs: align shell commands section with settings.local.json auto-approved permissions
  other     ab2272f ci(agent): update settings.local.json with rtk-prefixed permissions
  other     6ac4a80 ci(agent): reduce verbosity and repetition in specs and security agents (#32)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- ci: reduce verbosity and repetition in specs and security agent outputs (#32)
- docs: enforce rtk usage for auto-approved commands in CLAUDE.md ([7e151f5](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/7e151f56b20fbc065a177330b8238639f4d5a454))
- Revert "docs: align shell commands section with settings.local.json auto-approved permissions" ([fcb9ccc](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/fcb9cccb04b4a6882fe57b0aa3de7aa5103b960c))
- docs: align shell commands section with settings.local.json auto-approved permissions ([5f48867](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/5f48867c21c40caa6e8fcd1436301cf594ef905b))
- ci(agent): update settings.local.json with rtk-prefixed permissions ([ab2272f](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/ab2272f1a8d25b90e9da9b6539e410964e9118b3))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 7e151f5
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.6.2

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 7e151f5..9cc6aee (last tag: 7e151f5)
Target ref      : 9cc6aee (tag will be created there, not on HEAD)
Commits scanned : 15

  fix       9cc6aee fix: reorganize components to use <Suspense> better
  other     77dd62a style: format files and resolve unnecessary import complexity
  other     66a1551 test(results): all 159 tests pass for issue #30 loader + Suspense fix
  other     bbb0787 test(suspense): add Suspense wiring test scenarios for issue #30
  fix       573119f fix(loader): wire Suspense for page-load blank screen fix (#30)
  other     5cb70f4 test(cases): add Suspense wiring test scenarios for fix loader not visible (#30)
  other     94a60aa docs(security): extend security guidelines for Suspense wiring in issue #30
  other     7490b42 docs(specs): expand specs to include Suspense wiring fix for issue #30
  other     044c186 ci(agent): add vitest and npx vitest run permissions to settings.local.json
  other     6a2fc80 test(loader): add AppLoader and StationPrices tests for issue #30
  other     e63a9ef ci(agent): consolidate rtk npm run permissions in settings.local.json
  fix       7b4b60d fix(loader): restore AppLoader visibility during scraping (#30)
  other     50a7ba2 test(cases): define test scenarios for fix loader not visible (#30)
  other     2c86ae9 docs(security): add security guidelines for fix loader not visible (#30)
  other     9e8df86 docs(specs): define specs for fix loader not visible (#30)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Bug fixes

- The loader is not visible while the scraping is ongoing (#30)
- fix: reorganize components to use <Suspense> better ([9cc6aee](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/9cc6aee983757497ede252f3e4e3016cedcf37d9))

## Others

- style: format files and resolve unnecessary import complexity ([77dd62a](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/77dd62af50baa83941f3d272066b24fbe8c8cf66))
- ci(agent): add vitest and npx vitest run permissions to settings.local.json ([044c186](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/044c1864a57efb94d5d45e9c137fd38c16872776))
- ci(agent): consolidate rtk npm run permissions in settings.local.json ([e63a9ef](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e63a9efbc987467e9205db1887e9bf191131f83e))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 9cc6aee
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.6.3

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 9cc6aee..6bafa08 (last tag: 9cc6aee)
Target ref      : 6bafa08 (tag will be created there, not on HEAD)
Commits scanned : 2

  other     6bafa08 test(useStationPrices): confirm 159 tests pass for issue #25
  other     b628518 test(cases): define test scenarios for useStationPrices (#25)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- test(composable): add unit tests for useStationPrices (#25)

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 6bafa08
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.7.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 6bafa08..88d2ee1 (last tag: 6bafa08)
Target ref      : 88d2ee1 (tag will be created there, not on HEAD)
Commits scanned : 14

  other     88d2ee1 ci: remove worktree before gh pr merge to free local branch
  other     e53c61c ci: fix worktree path and use --rebase on post-merge pull
  other     a2e65da docs: use full agent names in Tailwind styling rule
  other     e58f815 docs: clarify Tailwind rule applies to coder (write) and reviewer (enforce)
  other     b24bd83 ci(agent): remove redundant Tailwind rule from coder agent (covered by CLAUDE.md)
  other     64592ab ci(agent): enforce Tailwind CSS utility classes for styling
  other     225a5c4 docs: update review and test result templates to match expected format
  other     f862a08 ci(agent): enforce structured templates in test-runner and reviewer
  other     4da7c9e ci(agent): write nothing on success in test-runner and reviewer
  other     6b3df5a test(reactivity): add tests for incremental price table sync (#31)
  feature   8403b2f feat(reactivity): sync price table with station list changes (#31)
  other     de245a1 test(cases): define test scenarios for station list reactivity (#31)
  feature   c311de6 feat(security): add security guidelines for station list reactivity (#31)
  feature   e86eb7c feat(specs): define specs for station list → price table reactivity (#31)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Making a change to the Station list should update the price table (#31)

## Others

- ci: remove worktree before gh pr merge to free local branch ([88d2ee1](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/88d2ee114a54a823a53aef0a265888bfd41e171d))
- ci: fix worktree path and use --rebase on post-merge pull ([e53c61c](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e53c61c65a07e0d6f4956ca1aa6cbd5d339dea27))
- docs: use full agent names in Tailwind styling rule ([a2e65da](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/a2e65da679481dd4d875dfed74668ab2f36614db))
- docs: clarify Tailwind rule applies to coder (write) and reviewer (enforce) ([e58f815](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e58f8157cc765366e74d792e07b9d98e57cb9580))
- ci(agent): remove redundant Tailwind rule from coder agent (covered by CLAUDE.md) ([b24bd83](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/b24bd8325a777d911205a454948c8dce0eecd6cf))
- ci(agent): enforce Tailwind CSS utility classes for styling ([64592ab](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/64592abc6bdf1533d02bfc53e1354b3e7e3db99e))
- docs: update review and test result templates to match expected format ([225a5c4](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/225a5c4edf0cad0274611a457fdf841fae4ac72f))
- ci(agent): enforce structured templates in test-runner and reviewer ([f862a08](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/f862a08a114b6ce489b5a3171c779c9c3e0e3586))
- ci(agent): write nothing on success in test-runner and reviewer ([4da7c9e](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/4da7c9e2ff792532a4500655e0a52b162d726b72))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 88d2ee1
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.8.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 88d2ee1..75a8198 (last tag: 88d2ee1)
Target ref      : 75a8198 (tag will be created there, not on HEAD)
Commits scanned : 7

  other     75a8198 docs(claude): restructure and expand CLAUDE.md with full project guidance
  fix       2f45f15 fix: resolve linting errors
  other     3d246c9 test(station-manager): add scroll container and table-auto layout tests (#43)
  fix       9013286 fix(station-manager): use table-auto layout to fix column truncation on mobile (#43)
  other     9296d0a test(cases): define test scenarios for mobile station table scroll (#43)
  feature   0b094c1 feat(security): add security guidelines for mobile station table scroll (#43)
  other     14b6926 docs(specs): define specs for mobile station table scroll (#43)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Bug: the station manager in mobile view doesn't display (#43)

## Bug fixes

- fix: resolve linting errors ([2f45f15](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/2f45f153cf8b11f18e283439809c8324a014c469))

## Others

- docs(claude): restructure and expand CLAUDE.md with full project guidance ([75a8198](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/75a8198403102c6224617e74562b1c7945e9d8e7))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 75a8198
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.9.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 75a8198..24f2ed4 (last tag: 75a8198)
Target ref      : 24f2ed4 (tag will be created there, not on HEAD)
Commits scanned : 15

  other     24f2ed4 chore(deps): update @tailwindcss/vite to 4.2.2 for Vite 8 support
  other     7d99c9d chore(deps-dev): bump vite from 7.3.1 to 8.0.0
  other     79514c9 chore(deps-dev): bump @vue/tsconfig from 0.7.0 to 0.9.0
  other     a766d84 chore(deps-dev): bump eslint from 9.39.4 to 10.0.3
  other     55201c0 chore(deps-dev): bump @types/dompurify from 3.0.5 to 3.2.0
  other     f6f88ef test(default-fuel-type): add comprehensive test coverage for fuel type defaults
  feature   30f9184 feat: implement default fuel type selection and persistence (#28)
  other     032e34d test(cases): update test scenarios for default fuel type (#28)
  other     3e23eb9 docs(security): update security guidelines for default fuel type (#28)
  other     317df5c docs(specs): update specs for default fuel type UX changes (#28)
  other     5699784 test(default-fuel-type): add comprehensive test suite for default fuel type feature
  feature   b3f42b7 feat: add default fuel type selection with persistence (#28)
  other     dc5d893 test(cases): define test scenarios for default fuel type (#28)
  other     2038199 docs(security): add security guidelines for default fuel type (#28)
  other     4c4c62f docs(specs): define specs for default fuel type (#28)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Default fuel type (#28)

## Others

- chore(deps): update @tailwindcss/vite to 4.2.2 for Vite 8 support ([24f2ed4](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/24f2ed4300d8667792022d81f91bc3a6bbf81c50))
- chore(deps-dev): bump vite from 7.3.1 to 8.0.0 ([7d99c9d](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/7d99c9dad683f85c85ef30b581c4f6d54de9bc6b))
- chore(deps-dev): bump @vue/tsconfig from 0.7.0 to 0.9.0 ([79514c9](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/79514c9dc6f417827b6a0a4a954eafc80b59ae55))
- chore(deps-dev): bump eslint from 9.39.4 to 10.0.3 ([a766d84](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/a766d849e6776b7a42fc17529e31a6e75e0f9a13))
- chore(deps-dev): bump @types/dompurify from 3.0.5 to 3.2.0 ([55201c0](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/55201c08d2dcb50a6ac78f91ab31ed63fe90e561))
- test(default-fuel-type): add comprehensive test coverage for fuel type defaults ([f6f88ef](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/f6f88efc7b5a0ecb8367dac10b44d657e55cea47))
- test(default-fuel-type): add comprehensive test suite for default fuel type feature ([5699784](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/5699784baa24a04d77abed1637866a2cf9e51be1))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 24f2ed4
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.10.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 24f2ed4..05022b6 (last tag: 24f2ed4)
Target ref      : 05022b6 (tag will be created there, not on HEAD)
Commits scanned : 18

  fix       05022b6 fix: update title and description
  other     3ff0457 ci(agent): fix model value
  other     e34defa ci(agent): make fetch-origin.sh standalone, not called by worktree-create.sh
  other     975e9ee ci(agent): split pr-complete into three focused scripts
  other     e3c4377 ci(agent): skip merge in pr-complete.sh if PR already merged/closed
  other     9a98d1e ci(agent): extract fetch-origin into its own script
  other     fc1803a ci(agent): add pipeline shell scripts for worktree/PR lifecycle
  other     97daa99 test(results): record passing test run for issue #50 home button fix
  feature   6228f5a feat(mentions-legales): add fixed home button; correct ADR-010 to Accepted
  other     1ce174c test(footer): update assertions to French labels after AppFooter translation
  other     c4c6025 refactor(mentions-legales): replace marked + v-html with inline HTML template
  other     fc5b5d1 test(ui): update specs to match French UI labels
  fix       8435177 fix(ui): translate remaining English strings to French and center h1
  other     c04d3d5 test(ux): add tests for rework UX/UI features (#50)
  feature   26db6ad feat(ux): rename app, translate labels, add mentions-légales page (#50)
  other     d1a7e81 test(cases): define test scenarios for rework UX/UI (#50)
  other     95f206e docs(security): add security guidelines for rework UX/UI (#50)
  other     c725453 docs(specs): define specs and ADR-010 for rework UX/UI (#50)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Rework UX / UI (#50)
- feat(mentions-legales): add fixed home button; correct ADR-010 to Accepted ([6228f5a](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/6228f5a7b21b547c44fe64c5dc8ec39b8c571a54))

## Bug fixes

- fix: update title and description ([05022b6](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/05022b6b82506a03fd13a6ce7230c356f10c615d))
- fix(ui): translate remaining English strings to French and center h1 ([8435177](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/843517796c98f65eee5ed59fbf0b9c01598fcb31))

## Others

- ci(agent): fix model value ([3ff0457](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/3ff0457c014e21eaf34efc4a78e98178f4ae6c2c))
- ci(agent): make fetch-origin.sh standalone, not called by worktree-create.sh ([e34defa](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e34defab039dd04a83d2df6c4e9753f577a4090a))
- ci(agent): split pr-complete into three focused scripts ([975e9ee](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/975e9ee09982044cd324ffcbdb7333eda562e55d))
- ci(agent): skip merge in pr-complete.sh if PR already merged/closed ([e3c4377](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e3c4377df19d817bc9f60fa0d4d386d5bceb5982))
- ci(agent): extract fetch-origin into its own script ([9a98d1e](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/9a98d1e779cae832053c7fde31f555224cfc4339))
- ci(agent): add pipeline shell scripts for worktree/PR lifecycle ([fc1803a](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/fc1803a3b620589c61dd8b1f04ffa495b618afbc))
- test(footer): update assertions to French labels after AppFooter translation ([1ce174c](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/1ce174c332868a80fcf7465c7b485f013d6ce7a6))
- refactor(mentions-legales): replace marked + v-html with inline HTML template ([c4c6025](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/c4c6025f070b1da0c5721b48181177217aa2b819))
- test(ui): update specs to match French UI labels ([fc5b5d1](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/fc5b5d1c1eeabf7ae7d77c34bc865a928c3aee25))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 05022b6
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.10.1

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 05022b6..84d89ba (last tag: 05022b6)
Target ref      : 84d89ba (tag will be created there, not on HEAD)
Commits scanned : 10

  other     84d89ba chore(deps-dev): bump unplugin-vue-components from 30.0.0 to 31.0.0
  other     c3192b4 chore(deps-dev): bump vue-tsc from 3.2.5 to 3.2.6
  other     0e7300b chore(deps-dev): bump @netlify/functions from 5.1.3 to 5.1.5
  other     f5757fe chore(deps): bump vue-router from 5.0.3 to 5.0.4
  other     0fb59d7 chore(deps-dev): bump unplugin-auto-import from 20.3.0 to 21.0.0
  other     894c713 ci(agent): clarify Task 7/8 — branch deletion and separate commands
  other     6248413 ci(agent): move branch deletion from pr-complete to worktree-cleanup
  other     80756ad test(ci): verify release pipeline trigger update (#59)
  other     849ee83 test(cases): define test scenarios for release trigger update (#59)
  other     f4ab682 docs(security): add security guidelines for release trigger update (#59)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- Update release pipeline trigger to release/[yyyyMMdd.N] branch pattern (#59)
- chore(deps-dev): bump unplugin-vue-components from 30.0.0 to 31.0.0 ([84d89ba](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/84d89ba6aee0fa20375fb030ffd2a8b3174a2316))
- chore(deps-dev): bump vue-tsc from 3.2.5 to 3.2.6 ([c3192b4](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/c3192b43ebce9d72d837365977ef9e4c0bb18209))
- chore(deps-dev): bump @netlify/functions from 5.1.3 to 5.1.5 ([0e7300b](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/0e7300b46eed96f639cd5c1d7dd0f52dfd6de43d))
- chore(deps): bump vue-router from 5.0.3 to 5.0.4 ([f5757fe](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/f5757fe9cf4d215143a6e159da294d8ad9dc5a02))
- chore(deps-dev): bump unplugin-auto-import from 20.3.0 to 21.0.0 ([0fb59d7](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/0fb59d7cdd189d6d1e695b4c7a919853ca69a565))
- ci(agent): clarify Task 7/8 — branch deletion and separate commands ([894c713](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/894c713cd9575d36a495ac73ee6eea0c64d2f137))
- ci(agent): move branch deletion from pr-complete to worktree-cleanup ([6248413](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/6248413db16437e311e359f8c082a32b9be20001))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 84d89ba
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.11.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 84d89ba..40c1e64 (last tag: 84d89ba)
Target ref      : 40c1e64 (tag will be created there, not on HEAD)
Commits scanned : 13

  other     40c1e64 ci(agent): delegate all git ops in fix-pipeline skill to agent-4-git
  other     a6ac8f3 ci(agent): extract vitest commands into /run-tests skill
  other     d322997 docs: enforce exact vitest JSON reporter commands in CLAUDE.md
  other     aa943cf ci(agent): enforce exact vitest JSON reporter commands in test-runner
  fix       cae5687 fix(import): normalize URLs before matching to ignore query params
  other     e6c9d42 docs: add TODO in /src/utils/preferencesImport.ts
  other     3ab1ad8 docs: save #63 original request
  other     c996f4c ci(agent): always run custom shell script
  other     b1c7b32 test(preferences): add export/import specs and fix StationManager stubs (#63)
  feature   24158b3 feat(preferences): add export/import of user preferences (#63)
  other     772ec80 test(cases): define test scenarios for export/import preferences (#63)
  feature   3c6911a feat(security): add security guidelines for export/import preferences (#63)
  feature   96ef48a feat(specs): define specs for export/import preferences (#63)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Allow Export/Import of user's preference (#63)

## Bug fixes

- fix(import): normalize URLs before matching to ignore query params ([cae5687](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/cae568734d1f903b0cafde27dbf683c1edb31ef0))

## Others

- ci(agent): delegate all git ops in fix-pipeline skill to agent-4-git ([40c1e64](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/40c1e64f7840643f64ba107af3ab91f854d6031e))
- ci(agent): extract vitest commands into /run-tests skill ([a6ac8f3](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/a6ac8f35d36b88b5b05d959a4711149f3e464b37))
- docs: enforce exact vitest JSON reporter commands in CLAUDE.md ([d322997](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/d322997daee326eae51cc6e680e233e62f16c6b7))
- ci(agent): enforce exact vitest JSON reporter commands in test-runner ([aa943cf](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/aa943cfbf88a0fa52a9a59af863db5587539d377))
- docs: add TODO in /src/utils/preferencesImport.ts ([e6c9d42](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/e6c9d42f4b5cc4671d7cca66c5367aef29331c09))
- ci(agent): always run custom shell script ([c996f4c](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/c996f4cbd306856bfec6e8746eea3f3d1b3ad524))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 40c1e64
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.11.1

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 40c1e64..d204c81 (last tag: 40c1e64)
Target ref      : d204c81 (tag will be created there, not on HEAD)
Commits scanned : 7

  other     d204c81 ci(agent): enforce branch suffix question before any file read in orchestrator
  other     39313d6 ci(agent): add optional branch suffix prompt to orchestrator
  other     2c367a4 ci(agent): make digest opt-in via orchestrator question
  other     ce1a6a7 ci(pipeline): add gitingest digest generation after branch push (#70)
  other     f9b9520 test(cases): define test scenarios for gitingest digest (#70)
  other     e43bebe ci(security): add security guidelines for gitingest digest (#70)
  other     331dc23 ci(specs): define specs for gitingest digest (#70)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- ci(pipeline): integrate gitingest to generate codebase digest before PR creation (#70)
- ci(agent): enforce branch suffix question before any file read in orchestrator ([d204c81](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/d204c8188c15bbc6bb53425634fea55ee7e84ebd))
- ci(agent): add optional branch suffix prompt to orchestrator ([39313d6](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/39313d64dd964fbd5d8407bd4e314a2b343b7a23))
- ci(agent): make digest opt-in via orchestrator question ([2c367a4](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/2c367a4b00a893d9bdc2f7305b3592839afe5759))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 d204c81
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.12.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : d204c81..0fb96ef (last tag: d204c81)
Target ref      : 0fb96ef (tag will be created there, not on HEAD)
Commits scanned : 2

  fix       0fb96ef fix: add typing on variables
  feature   25287b6 feat(import): validate fuelTypeDefault against known fuel types (#69)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- feat(import): validate fuelTypeDefault against known fuel types (#69) ([25287b6](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/25287b601761e7a751ee58330e7eda7a26221557))

## Bug fixes

- fix: add typing on variables ([0fb96ef](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/0fb96ef7cc4bd95f69e15d22259e9616caab405c))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 0fb96ef
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.12.1

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 0fb96ef..873ad76 (last tag: 0fb96ef)
Target ref      : 873ad76 (tag will be created there, not on HEAD)
Commits scanned : 1

  other     873ad76 chore(deps-dev): bump happy-dom from 20.8.4 to 20.8.9 (#76)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- chore(deps-dev): bump happy-dom from 20.8.4 to 20.8.9 (#76) ([873ad76](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/873ad76d7dc4de9e867b37edc8d63ab7449ef385))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 873ad76
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.12.2

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 873ad76..84a86ff (last tag: 873ad76)
Target ref      : 84a86ff (tag will be created there, not on HEAD)
Commits scanned : 1

  other     84a86ff chore(deps-dev): bump eslint from 10.0.3 to 10.1.0 (#75)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- chore(deps-dev): bump eslint from 10.0.3 to 10.1.0 (#75) ([84a86ff](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/84a86ffe079955a3e3e7ae693e3898d888b2c252))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 84a86ff
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.12.3

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 84a86ff..83a3b4e (last tag: 84a86ff)
Target ref      : 83a3b4e (tag will be created there, not on HEAD)
Commits scanned : 3

  other     83a3b4e ci(commands): add jli-reviews-specs, dual-mode setup, and sub-issue task folders
  other     85c4191 @ ci(commands): migrate agent pipeline to jli- command chain
  other     fe209b0 chore(deps-dev): bump vite from 8.0.1 to 8.0.3 (#73)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Others

- ci(commands): add jli-reviews-specs, dual-mode setup, and sub-issue task folders ([83a3b4e](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/83a3b4edc90c6568b49dbba5d6d68b78bf09685e))
- @ ci(commands): migrate agent pipeline to jli- command chain ([85c4191](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/85c41918db76b7a76192680675f817329638062d))
- chore(deps-dev): bump vite from 8.0.1 to 8.0.3 (#73) ([fe209b0](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/fe209b0d171bac811fd09f6d2ce59ffd4941d6fc))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 83a3b4e
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.13.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 83a3b4e..2b27a5d (last tag: 83a3b4e)
Target ref      : 2b27a5d (tag will be created there, not on HEAD)
Commits scanned : 12

  other     2b27a5d test(cases): rewrite F-4 to match amended proxy authorization rule (#64)
  feature   89335d4 feat(security): amend GitHub API proxy owner/repo rule for issue #64 (#64)
  other     5deb096 ci(commands): script the sub-issue output-folder creation
  fix       54dc8c5 fix(pipeline): derive bare repo path via git instead of fixed traversal
  other     1b6fdea test(cases): amend test scenarios for GitHub repository preferences (#64)
  other     b286a1c docs(specs): amend GitHub repo preferences specs from PR #87 review (#64)
  other     7664694 docs(adr): update ADR-011 OAuth flow diagram; add task README for #64
  other     f868a1e docs(adr): fix ADR-012 — JSON file created automatically on first write (#64)
  other     047bda8 docs(adr): add ADR-011 (GitHub OAuth) and ADR-012 (GitHub repo sync) for #64
  other     46a33ed test(cases): define test scenarios for GitHub repository preferences (#64)
  feature   ef4352b feat(security): add security guidelines for GitHub repository preferences (#64)
  feature   a5fee20 feat(specs): define specs for GitHub repository preferences (#64)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Create a workflow to allow a user to save / read his preferences to a dedicated repository as database (#64)

## Bug fixes

- fix(pipeline): derive bare repo path via git instead of fixed traversal ([54dc8c5](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/54dc8c5c257204843f7d10de90ab122c2d574884))

## Others

- ci(commands): script the sub-issue output-folder creation ([5deb096](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/5deb09644f7d4c8e70a93889faea93a5f81b3167))
- docs(specs): amend GitHub repo preferences specs from PR #87 review (#64) ([b286a1c](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/b286a1c92de9e1164cc06856a23511f0efc6495a))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 2b27a5d
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.14.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 2b27a5d..37367f2 (last tag: 2b27a5d)
Target ref      : 37367f2 (tag will be created there, not on HEAD)
Commits scanned : 8

  other     37367f2 test: record test results for GitHub OAuth and Contents API proxy (#81)
  other     d76d45b docs(dev): add manual REST Client request collection for OAuth proxy (#81)
  other     da87234 chore(dev): add Proton Pass CLI wrapper for local Netlify dev (#81)
  other     8a0931e test: add tests for GitHub OAuth and Contents API proxy functions (#81)
  other     be1730b docs(review): approve code review for sub-issue F (#81)
  fix       2360d2f fix(functions): fix OAuth state cookie and callback type error (#81)
  other     8e3e6a3 docs(review): record code review findings for sub-issue F (#81)
  feature   5db5a90 feat(functions): add GitHub OAuth and Contents API proxy functions (#81)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Sub-Issue F (#64): Netlify Functions for OAuth and GitHub API Proxy (#81)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 37367f2
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.15.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 37367f2..615d661 (last tag: 37367f2)
Target ref      : 615d661 (tag will be created there, not on HEAD)
Commits scanned : 6

  other     615d661 test: record test results for exclude spec files from build (#96)
  fix       d8dec69 fix: repair lib imports after netlify function directory move (#96)
  fix       f246b88 fix: move netlify functions into per-function directories (#96)
  other     69f3ab4 test(cases): define test scenarios for exclude spec files from build (#96)
  feature   518bd8d feat(security): add security guidelines for exclude spec files from build (#96)
  feature   4b192a2 feat(specs): define specs for exclude spec files from build (#96)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Build error because of netlify function test filed (#96)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 615d661
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.16.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 615d661..fd42116 (last tag: 615d661)
Target ref      : fd42116 (tag will be created there, not on HEAD)
Commits scanned : 7

  other     fd42116 test: record test results for GitHub OAuth login/logout (#82)
  other     579999a chore(types): regenerate auto-import types for GitHub auth (#82)
  other     459f927 test: add tests for GitHub OAuth login/logout composable (#82)
  other     c4f3d72 refactor(auth): extract RepoConfigDraft into src/types (#82)
  other     5d541fc test(cases): rescope sub-issue A test scenarios to login logic (#82)
  feature   7d3def0 feat(specs): rescope OAuth login to logic-only for sub-issue A (#82)
  feature   ad39078 feat(auth): add GitHub OAuth login/logout composable (#82)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Sub-Issue A (#64): GitHub OAuth Login / Logout (#82)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 fd42116
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.17.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : fd42116..5163118 (last tag: fd42116)
Target ref      : 5163118 (tag will be created there, not on HEAD)
Commits scanned : 9

  other     5163118 chore(types): regenerate auto-import types for repo config (#83)
  other     6a30e2f test: record test results for GitHub repo config (#83)
  other     742262b test: add tests for GitHub repo config composable (#83)
  other     fd4fd7c docs: record approved review results for repo config (#83)
  fix       580bb50 fix(repo-config): guard reactive save race and document Calisthenics exception (#83)
  other     62843f4 docs: record re-review results for repo config (#83)
  fix       fb9591e fix(repo-config): apply review-feedback fixes to repo sync validation (#83)
  other     c74bf79 docs: record code review findings for repo config (#83)
  feature   0927b56 feat(repo-config): persist and validate GitHub repo sync config (#83)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Sub-Issue B (#64): Repo Configuration (#83)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 5163118
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.18.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 5163118..9d2d018 (last tag: 5163118)
Target ref      : 9d2d018 (tag will be created there, not on HEAD)
Commits scanned : 2

  feature   9d2d018 feat(settings): add GitHub sync settings UI (#84)
  feature   3549d2d feat(specs): define specs for settings UI repo config and cache (#84)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Sub-Issue E (#64): Settings UI for Repo Config and Cache Parameter (#84)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 9d2d018
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.18.1

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 9d2d018..ccf26d1 (last tag: 9d2d018)
Target ref      : ccf26d1 (tag will be created there, not on HEAD)
Commits scanned : 7

  other     ccf26d1 ci(commands): fix rtk lint resolution and trim review verbosity in jli-reviews-code
  other     ed53da9 test: record passing test results for settings UI repo config (#64)
  other     21d0bb5 docs: record re-review results for settings UI repo config (#64)
  fix       9517d03 fix(settings): normalize revalidate-cache-days input as string or number (#64)
  other     4674722 test: record test results for settings UI repo config (#64)
  other     d219ea1 test: add tests for settings UI repo config and cache (#64)
  other     1f76e8c docs: record approved review results for settings UI repo config (#64)

Bump            : patch
Version         : 0.0.0 -> 0.0.1
-> Continue to step 2 and build the release notes for v0.0.1? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.0.1 ==

## Bug fixes

- Create a workflow to allow a user to save / read his preferences to a dedicated repository as database (#64)

## Others

- ci(commands): fix rtk lint resolution and trim review verbosity in jli-reviews-code ([ccf26d1](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/ccf26d114f137da0beb003e02c77b62731364ac1))

-> Continue to step 3 and create the tag v0.0.1? (auto-confirmed with --yes)

== Step 3 — create and push v0.0.1 ==

[dry-run] git tag -a v0.0.1 -m v0.0.1 ccf26d1
[dry-run] git push origin v0.0.1
-> Continue to step 4 and publish the GitHub release v0.0.1? (auto-confirmed with --yes)

== Step 4 — publish the release v0.0.1 ==

[dry-run] gh release create v0.0.1 --title v0.0.1 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.19.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : ccf26d1..6ea706c (last tag: ccf26d1)
Target ref      : 6ea706c (tag will be created there, not on HEAD)
Commits scanned : 29

  other     6ea706c test: record test results for load-orchestration fix (#85)
  other     86c49a8 test: fix stale loadStations assertion in StationManager spec (#85)
  other     ecdaa81 test: record test results for load-orchestration re-run (#85)
  fix       0fd118b fix(github-sync): import StationPrices explicitly in HomePageContent (#85)
  other     e684718 test: record test results for load-orchestration pass (#85)
  other     f02d5ef test: add tests for empty-state, sync consistency, and bounded fetch (#85)
  other     68f5589 docs: record review approval for load-orchestration pass (#85)
  other     fdfe48f docs: record ADR-013 for page-level load orchestration (#85)
  feature   5497e5f feat(github-sync): centralize load orchestration, add empty state (#85)
  other     97040a3 test(cases): define scenarios for empty state and sync consistency (#85)
  feature   ebcbbc5 feat(security): require bounded wait for remote sync fetch (#85)
  other     a5bb93d docs: record spec-review findings for remote preferences load gap (#85)
  feature   c00609e feat(specs): remove default stations, add sync consistency rule (#85)
  other     f98919b docs: record re-review results for remote preferences read sync (#85)
  fix       9dfd567 fix(github-sync): flatten error-mapping in remote preferences sync (#85)
  other     73c36c5 docs: record code review results for remote preferences read sync (#85)
  fix       82e4324 fix(github-sync): align remote preferences field names with spec (#85)
  other     867198d test(cases): define scenarios for remote preferences field fix (#85)
  feature   82d6952 feat(specs): fix remote preferences field names (#85)
  other     1d7d2fc test: record passing test results for reading remote preferences on load (#85)
  other     9d6d06f test: mock repo-config and auth composables in station price tests (#85)
  other     7988c96 test: record test results for reading remote preferences on load (#85)
  other     e320908 test: add tests for reading remote preferences on load (#85)
  other     030062e docs: record re-review results for remote preferences read sync (#85)
  fix       996d134 fix(github-sync): restore sync timestamp when remote merge rolls back (#85)
  other     b95ee22 docs: record review results for remote preferences read sync (#85)
  fix       a782dbc fix(github-sync): roll back station list on partial remote merge failure (#85)
  other     265a0f1 docs: record code review results for remote preferences read sync (#85)
  feature   2b23e87 feat(github-sync): read remote GitHub preferences on stale app load (#85)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Sub-Issue C (#64): Read Preferences from Remote Repo on Load (#85)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 6ea706c
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.20.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 6ea706c..6cfcba6 (last tag: 6ea706c)
Target ref      : 6cfcba6 (tag will be created there, not on HEAD)
Commits scanned : 3

  other     6cfcba6 test(cases): define test scenarios for github oauth/proxy functions (#64)
  feature   860a9b1 feat(security): add write-confirm diff validation rule (#64)
  feature   940c16b feat(specs): amend sub-issue d spec after coherence review (#64)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Create a workflow to allow a user to save / read his preferences to a dedicated repository as database (#64)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 6cfcba6
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.21.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 6cfcba6..6fd73e2 (last tag: 6cfcba6)
Target ref      : 6fd73e2 (tag will be created there, not on HEAD)
Commits scanned : 9

  other     6fd73e2 test: record passing test results for remote preferences write (#86)
  other     b40f53d test: fix write-response mock missing ok field (#86)
  other     830bd52 test: record test results for remote preferences write (#86)
  other     c2d9a71 test: add tests for remote preferences write (#86)
  other     aae2299 docs(review): approve remote preferences write implementation (#86)
  fix       4344d95 fix(github-sync): notify user when a concurrent local edit skips remote push (#86)
  other     12b500f docs(review): flag isWriting guard race in remote preferences write (#86)
  feature   211d47d feat(tool): add script to initialize env file with proton pass secrets
  feature   9dca4c1 feat(github-sync): write preferences to remote repo on update (#86)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Sub-Issue D (#64): Write Preferences to Remote Repo on Update (#86)
- feat(tool): add script to initialize env file with proton pass secrets ([211d47d](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/211d47d2bdabac94e320216a08c0feb37bd57439))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 6fd73e2
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.22.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 6fd73e2..b429460 (last tag: 6fd73e2)
Target ref      : b429460 (tag will be created there, not on HEAD)
Commits scanned : 13

  fix       b429460 fix: re-enable guards
  fix       dc41334 fix: use `console.log|error` instead node's log
  other     5dcea4b Update scheduled-price-history.ts
  other     65bea2c test: record test results for save daily price history (#112)
  other     aa36475 test: add tests for daily price history lib functions (#112)
  other     71c6efc test(cases): record code review results for save daily price history (#112)
  fix       f6599be fix: address review findings for daily price history function (#112)
  other     e9703f9 test(cases): record code review results for save daily price history (#112)
  feature   b4f0d35 feat: save daily favorite-station prices to history.csv (#112)
  other     770b44d test(cases): define test scenarios for save daily price history (#112)
  feature   2ef8b91 feat(security): add security guidelines for save daily price history (#112)
  feature   f46176a feat(specs): define specs for save daily price history (#112)
  other     8e78769 docs: add ADR-014 for scheduled function PAT auth (#112)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Save daily prices for favorite stations (#112)

## Bug fixes

- fix: re-enable guards ([b429460](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/b429460b0773262bd10a25afc986a58a68030098))
- fix: use `console.log|error` instead node's log ([dc41334](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/dc413346b8600b3b03b14be4d92d47de6d13cb0d))

## Others

- Update scheduled-price-history.ts ([5dcea4b](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/5dcea4b766b3ecb120f467401e70f9e0b404230a))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 b429460
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.23.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : b429460..5b3762c (last tag: b429460)
Target ref      : 5b3762c (tag will be created there, not on HEAD)
Commits scanned : 14

  other     5b3762c test: record test results for fixed scheduled run trigger time (#115)
  fix       48ae62a fix: revert scheduled run trigger to a fixed literal cron expression (#115)
  other     1bad39f test(cases): redefine test scenarios for fixed scheduled run trigger time (#115)
  feature   5ea9023 feat(security): redefine security guidelines for fixed scheduled run trigger time (#115)
  feature   57ab23f feat(specs): redefine specs for fixed scheduled run trigger time (#115)
  other     d672fbc test: record test results for randomize scheduled run trigger time (#115)
  other     19540a9 test: add tests for randomize scheduled run trigger time (#115)
  other     dbed464 test(cases): record code review approval for randomize scheduled run trigger time (#115)
  other     6373859 refactor: split parisUtcOffsetMinutes into calisthenics-compliant helpers (#115)
  other     37be24a test(cases): record code review results for randomize scheduled run trigger time (#115)
  fix       5f2c062 fix: randomize the daily price-history job's trigger time (#115)
  other     6f4e570 test(cases): define test scenarios for randomize scheduled run trigger time (#115)
  feature   5e1fc50 feat(security): add security guidelines for randomize scheduled run trigger time (#115)
  feature   7ae81f3 feat(specs): define specs for randomize scheduled run trigger time (#115)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Remove the broken logic scheduling logic (#115)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 5b3762c
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.24.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 5b3762c..09092fd (last tag: 5b3762c)
Target ref      : 09092fd (tag will be created there, not on HEAD)
Commits scanned : 12

  feature   09092fd feat: update label
  feature   b814335 feat: rename label
  fix       aafa3da fix: remove duplicate label
  other     c4e298f test: record test results for batched station saves and diff readability (#110)
  other     b066d4d test: add tests for batched station saves and diff readability (#110)
  other     abd043e docs(review): approve fuel-type push isolation fix (#110)
  fix       bcbe771 fix(preferences): isolate fuel-type push from pending station changes (#110)
  other     1589a1a docs(review): flag pending station changes leaking into fuel-type push (#110)
  feature   d3c3cd8 feat(ui): batch station-list github saves and improve diff readability (#110)
  other     0899cad test(cases): define test scenarios for ui/ux improvements (#110)
  feature   f4a1a5c feat(security): add security guidelines for ui/ux improvements (#110)
  feature   ce7e682 feat(specs): define specs for ui/ux improvements (#110)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- UI and UX improvements (#110)
- feat: update label ([09092fd](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/09092fd244b44359b11634e4028184996ee27fc8))
- feat: rename label ([b814335](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/b81433596690a0abc03b339cb625e462137a85f4))

## Bug fixes

- fix: remove duplicate label ([aafa3da](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/aafa3da961f27be649cb8e5c72c6324bf2618da7))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 09092fd
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.25.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 09092fd..0b41795 (last tag: 09092fd)
Target ref      : 0b41795 (tag will be created there, not on HEAD)
Commits scanned : 6

  other     0b41795 test: record test results for moving GitHub sync settings (#120)
  other     c088e7b test: add tests for moving GitHub sync settings (#120)
  feature   79ccbc9 feat: move GitHub sync settings into Station Manager (#120)
  other     a189d78 test(cases): define test scenarios for moving GitHub sync settings (#120)
  feature   a57f497 feat(security): add security guidelines for moving GitHub sync settings (#120)
  feature   98eb15c feat(specs): define specs for moving GitHub sync settings into Station Manager (#120)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Move where `GitHubSyncSettings` component is rendered (#120)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 0b41795
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.26.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 0b41795..8755a44 (last tag: 0b41795)
Target ref      : 8755a44 (tag will be created there, not on HEAD)
Commits scanned : 23

  other     8755a44 chore(deps-dev): bump vite-plugin-vue-devtools from 8.1.0 to 8.1.1
  other     9bad3c0 chore(deps-dev): bump conventional-changelog-conventionalcommits
  other     9cfc0cc chore(deps-dev): bump @vitest/coverage-v8 from 4.1.0 to 4.1.2
  other     4177d06 test: mount org-restriction notice via single-root host to fix text assertion (#108)
  other     9e50c96 test: record passing test results for org OAuth 403 restriction handling (#108)
  fix       ea9d1c4 fix(app-link): join org-restriction sentence and link on one line (#108)
  other     938d04a test: record test results for org OAuth 403 restriction handling (#108)
  other     ea57e79 test: add tests for org OAuth 403 restriction handling (#108)
  other     b44fcc5 docs: approve review after org-403 AppLink rel fixes (#108)
  fix       a4818b2 fix(app-link): restore noopener-noreferrer tightening on StationManager link (#108)
  other     b50f046 docs: record review findings for org-403 AppLink rel regression (#108)
  fix       e20363e fix(app-link): add noreferrer to external links (#108)
  other     bdbdd55 docs: record review findings for org-403 link rel attribute (#108)
  feature   c80f489 feat(github-sync): replace org-403 message with fixed owner-linked text (#108)
  feature   49f041a feat(security): revise guidelines for owner-linked org-403 message (#108)
  other     bf0b075 test(cases): redefine org-403 message scenarios for fixed owner-linked text (#108)
  feature   0b21e98 feat(specs): redefine org-403 message as fixed owner-linked text (#108)
  other     0ff1498 docs: flag org-403 message design for spec revision (#108)
  feature   cc913ab feat(github-sync): handle org OAuth 403 restriction with actionable message (#108)
  fix       a51d1e2 fix: remove pass-cli parttern where not needed on .env
  other     8a8e4d1 test(cases): define test scenarios for GitHub OAuth 403 handling (#108)
  feature   07e1a9c feat(security): add security guidelines for GitHub OAuth 403 handling (#108)
  feature   af1a6a1 feat(specs): define specs for GitHub OAuth 403 handling (#108)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Handle GitHub org OAuth restriction (403) with actionable message (#108)

## Bug fixes

- fix: remove pass-cli parttern where not needed on .env ([a51d1e2](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/a51d1e27ffdc31ce8fa230b93cf7bd50da58030d))

## Others

- chore(deps-dev): bump vite-plugin-vue-devtools from 8.1.0 to 8.1.1 ([8755a44](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/8755a442e0780f64380f69523f10590f6a44b02a))
- chore(deps-dev): bump conventional-changelog-conventionalcommits ([9bad3c0](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/9bad3c02593d1c619a7a3e4fe41f6f5e8cd0c688))
- chore(deps-dev): bump @vitest/coverage-v8 from 4.1.0 to 4.1.2 ([9cfc0cc](https://github.com/JeremieLitzler/french-gas-stations-scraper/commit/9cfc0ccaefce790cc228bf36655bca2cfc7aac9c))

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 8755a44
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.27.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 8755a44..5a1c41c (last tag: 8755a44)
Target ref      : 5a1c41c (tag will be created there, not on HEAD)
Commits scanned : 6

  other     5a1c41c test: record test results for bumping vitest and vitest ui to 4.1.2 (#123)
  other     b870934 docs(review): approve vitest and vitest ui 4.1.2 bump (#123)
  other     886a612 chore(deps-dev): bump vitest and @vitest/ui to 4.1.2 (#123)
  other     a8638a5 test(cases): define test scenarios for bumping vitest and vitest ui to 4.1.2 (#123)
  feature   1723e6f feat(security): add security guidelines for bumping vitest and vitest ui to 4.1.2 (#123)
  feature   20ca5fd feat(specs): define specs for bumping vitest and vitest ui to 4.1.2 (#123)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Bump dependencies Vitest and Vitest UI to v4.1.2 (#123)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 5a1c41c
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```

### v0.28.0

```
Fetching tags from origin...

== Step 1 — evaluate the new version ==

Repository      : JeremieLitzler/french-gas-stations-scraper
Branch          : develop
Commit range    : 5a1c41c..eaabb21 (last tag: 5a1c41c)
Target ref      : eaabb21 (tag will be created there, not on HEAD)
Commits scanned : 9

  other     eaabb21 test: record test results for refresh data button (#106)
  other     a25df9a test: add tests for refresh data button (#106)
  other     e73741a docs(review): record approved code review for refresh data button (#106)
  feature   22be58e feat(stations): add on-demand refresh data button (#106)
  other     0340248 test(cases): add pending-changes scenarios for refresh data button (#106)
  feature   8f2e1e9 feat(specs): add pending-changes rule for refresh data button (#106)
  other     2c2f9ce test(cases): define test scenarios for refresh data button (#106)
  feature   e0c201a feat(security): add security guidelines for refresh data button (#106)
  feature   42872bc feat(specs): define specs for refresh data button (#106)

Bump            : minor
Version         : 0.0.0 -> 0.1.0
-> Continue to step 2 and build the release notes for v0.1.0? (auto-confirmed with --yes)
Resolving issue references with gh...

== Step 2 — release notes for v0.1.0 ==

## Features

- Add a button to refresh data from remote source (#106)

-> Continue to step 3 and create the tag v0.1.0? (auto-confirmed with --yes)

== Step 3 — create and push v0.1.0 ==

[dry-run] git tag -a v0.1.0 -m v0.1.0 eaabb21
[dry-run] git push origin v0.1.0
-> Continue to step 4 and publish the GitHub release v0.1.0? (auto-confirmed with --yes)

== Step 4 — publish the release v0.1.0 ==

[dry-run] gh release create v0.1.0 --title v0.1.0 --notes-file <notes>
[dry-run] no tag was pushed, so no release was created
```
