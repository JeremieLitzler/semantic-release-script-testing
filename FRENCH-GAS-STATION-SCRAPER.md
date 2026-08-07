# french-gas-stations-scraper release history

Reconstructed from the commit history at https://github.com/JeremieLitzler/french-gas-stations-scraper.
No tags or GitHub releases exist yet — this is a projection of what the release
history would look like if the repository's semantic-release script had run
after every issue's commits landed on the default branch.

Grouping rules:

- Each contiguous run of commits sharing the same linked issue (`(#N)` at the
  end of the subject) forms one release. If an issue's commits are interrupted
  by another issue's commits and then resume later, the resumed run is its own
  separate release.
- Commits with no linked issue join whichever release closes next.
- Version bump per release: any `breaking` commit -> major; else any
  `feature` (feat) commit -> minor; else patch (covers `fix` and
  `other`-only releases).
- Commits are listed newest-first within each release; releases are listed
  newest-first overall.

```
release v0.28.0
  other     eaabb21 test: record test results for refresh data button (#106)
  other     a25df9a test: add tests for refresh data button (#106)
  other     e73741a docs(review): record approved code review for refresh data button (#106)
  feature   22be58e feat(stations): add on-demand refresh data button (#106)
  other     0340248 test(cases): add pending-changes scenarios for refresh data button (#106)
  feature   8f2e1e9 feat(specs): add pending-changes rule for refresh data button (#106)
  other     2c2f9ce test(cases): define test scenarios for refresh data button (#106)
  feature   e0c201a feat(security): add security guidelines for refresh data button (#106)
  feature   42872bc feat(specs): define specs for refresh data button (#106)

release v0.27.0
  other     5a1c41c test: record test results for bumping vitest and vitest ui to 4.1.2 (#123)
  other     b870934 docs(review): approve vitest and vitest ui 4.1.2 bump (#123)
  other     886a612 chore(deps-dev): bump vitest and @vitest/ui to 4.1.2 (#123)
  other     a8638a5 test(cases): define test scenarios for bumping vitest and vitest ui to 4.1.2 (#123)
  feature   1723e6f feat(security): add security guidelines for bumping vitest and vitest ui to 4.1.2 (#123)
  feature   20ca5fd feat(specs): define specs for bumping vitest and vitest ui to 4.1.2 (#123)

release v0.26.0
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

release v0.25.0
  other     0b41795 test: record test results for moving GitHub sync settings (#120)
  other     c088e7b test: add tests for moving GitHub sync settings (#120)
  feature   79ccbc9 feat: move GitHub sync settings into Station Manager (#120)
  other     a189d78 test(cases): define test scenarios for moving GitHub sync settings (#120)
  feature   a57f497 feat(security): add security guidelines for moving GitHub sync settings (#120)
  feature   98eb15c feat(specs): define specs for moving GitHub sync settings into Station Manager (#120)

release v0.24.0
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

release v0.23.0
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

release v0.22.0
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

release v0.21.0
  other     6fd73e2 test: record passing test results for remote preferences write (#86)
  other     b40f53d test: fix write-response mock missing ok field (#86)
  other     830bd52 test: record test results for remote preferences write (#86)
  other     c2d9a71 test: add tests for remote preferences write (#86)
  other     aae2299 docs(review): approve remote preferences write implementation (#86)
  fix       4344d95 fix(github-sync): notify user when a concurrent local edit skips remote push (#86)
  other     12b500f docs(review): flag isWriting guard race in remote preferences write (#86)
  feature   211d47d feat(tool): add script to initialize env file with proton pass secrets
  feature   9dca4c1 feat(github-sync): write preferences to remote repo on update (#86)

release v0.20.0
  other     6cfcba6 test(cases): define test scenarios for github oauth/proxy functions (#64)
  feature   860a9b1 feat(security): add write-confirm diff validation rule (#64)
  feature   940c16b feat(specs): amend sub-issue d spec after coherence review (#64)

release v0.19.0
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

release v0.18.1
  other     ccf26d1 ci(commands): fix rtk lint resolution and trim review verbosity in jli-reviews-code
  other     ed53da9 test: record passing test results for settings UI repo config (#64)
  other     21d0bb5 docs: record re-review results for settings UI repo config (#64)
  fix       9517d03 fix(settings): normalize revalidate-cache-days input as string or number (#64)
  other     4674722 test: record test results for settings UI repo config (#64)
  other     d219ea1 test: add tests for settings UI repo config and cache (#64)
  other     1f76e8c docs: record approved review results for settings UI repo config (#64)

release v0.18.0
  feature   9d2d018 feat(settings): add GitHub sync settings UI (#84)
  feature   3549d2d feat(specs): define specs for settings UI repo config and cache (#84)

release v0.17.0
  other     5163118 chore(types): regenerate auto-import types for repo config (#83)
  other     6a30e2f test: record test results for GitHub repo config (#83)
  other     742262b test: add tests for GitHub repo config composable (#83)
  other     fd4fd7c docs: record approved review results for repo config (#83)
  fix       580bb50 fix(repo-config): guard reactive save race and document Calisthenics exception (#83)
  other     62843f4 docs: record re-review results for repo config (#83)
  fix       fb9591e fix(repo-config): apply review-feedback fixes to repo sync validation (#83)
  other     c74bf79 docs: record code review findings for repo config (#83)
  feature   0927b56 feat(repo-config): persist and validate GitHub repo sync config (#83)

release v0.16.0
  other     fd42116 test: record test results for GitHub OAuth login/logout (#82)
  other     579999a chore(types): regenerate auto-import types for GitHub auth (#82)
  other     459f927 test: add tests for GitHub OAuth login/logout composable (#82)
  other     c4f3d72 refactor(auth): extract RepoConfigDraft into src/types (#82)
  other     5d541fc test(cases): rescope sub-issue A test scenarios to login logic (#82)
  feature   7d3def0 feat(specs): rescope OAuth login to logic-only for sub-issue A (#82)
  feature   ad39078 feat(auth): add GitHub OAuth login/logout composable (#82)

release v0.15.0
  other     615d661 test: record test results for exclude spec files from build (#96)
  fix       d8dec69 fix: repair lib imports after netlify function directory move (#96)
  fix       f246b88 fix: move netlify functions into per-function directories (#96)
  other     69f3ab4 test(cases): define test scenarios for exclude spec files from build (#96)
  feature   518bd8d feat(security): add security guidelines for exclude spec files from build (#96)
  feature   4b192a2 feat(specs): define specs for exclude spec files from build (#96)

release v0.14.0
  other     37367f2 test: record test results for GitHub OAuth and Contents API proxy (#81)
  other     d76d45b docs(dev): add manual REST Client request collection for OAuth proxy (#81)
  other     da87234 chore(dev): add Proton Pass CLI wrapper for local Netlify dev (#81)
  other     8a0931e test: add tests for GitHub OAuth and Contents API proxy functions (#81)
  other     be1730b docs(review): approve code review for sub-issue F (#81)
  fix       2360d2f fix(functions): fix OAuth state cookie and callback type error (#81)
  other     8e3e6a3 docs(review): record code review findings for sub-issue F (#81)
  feature   5db5a90 feat(functions): add GitHub OAuth and Contents API proxy functions (#81)

release v0.13.0
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

release v0.12.3
  other     83a3b4e ci(commands): add jli-reviews-specs, dual-mode setup, and sub-issue task folders
  other     85c4191 @
  other     fe209b0 chore(deps-dev): bump vite from 8.0.1 to 8.0.3 (#73)

release v0.12.2
  other     84a86ff chore(deps-dev): bump eslint from 10.0.3 to 10.1.0 (#75)

release v0.12.1
  other     873ad76 chore(deps-dev): bump happy-dom from 20.8.4 to 20.8.9 (#76)

release v0.12.0
  fix       0fb96ef fix: add typing on variables
  feature   25287b6 feat(import): validate fuelTypeDefault against known fuel types (#69)

release v0.11.1
  other     d204c81 ci(agent): enforce branch suffix question before any file read in orchestrator
  other     39313d6 ci(agent): add optional branch suffix prompt to orchestrator
  other     2c367a4 ci(agent): make digest opt-in via orchestrator question
  other     ce1a6a7 ci(pipeline): add gitingest digest generation after branch push (#70)
  other     f9b9520 test(cases): define test scenarios for gitingest digest (#70)
  other     e43bebe ci(security): add security guidelines for gitingest digest (#70)
  other     331dc23 ci(specs): define specs for gitingest digest (#70)

release v0.11.0
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

release v0.10.1
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

release v0.10.0
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

release v0.9.0
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

release v0.8.0
  other     75a8198 docs(claude): restructure and expand CLAUDE.md with full project guidance
  fix       2f45f15 fix: resolve linting errors
  other     3d246c9 test(station-manager): add scroll container and table-auto layout tests (#43)
  fix       9013286 fix(station-manager): use table-auto layout to fix column truncation on mobile (#43)
  other     9296d0a test(cases): define test scenarios for mobile station table scroll (#43)
  feature   0b094c1 feat(security): add security guidelines for mobile station table scroll (#43)
  other     14b6926 docs(specs): define specs for mobile station table scroll (#43)

release v0.7.0
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

release v0.6.3
  other     6bafa08 test(useStationPrices): confirm 159 tests pass for issue #25
  other     b628518 test(cases): define test scenarios for useStationPrices (#25)

release v0.6.2
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

release v0.6.1
  other     7e151f5 docs: enforce rtk usage for auto-approved commands in CLAUDE.md
  other     fcb9ccc Revert "docs: align shell commands section with settings.local.json auto-approved permissions"
  other     5f48867 docs: align shell commands section with settings.local.json auto-approved permissions
  other     ab2272f ci(agent): update settings.local.json with rtk-prefixed permissions
  other     6ac4a80 ci(agent): reduce verbosity and repetition in specs and security agents (#32)

release v0.6.0
  other     8dfbe25 test(fuel-type-selector): add unit and component tests for selector and price table (#19)
  feature   05ab9a6 feat(fuel-type-selector): add selector and price table to StationPrices (#19)
  other     0133712 test(cases): define test scenarios for fuel-type selector and price table (#19)
  other     11e502d docs(security): add security guidelines for fuel-type selector and price table (#19)
  other     9d6d3fd docs(specs): define specs for fuel-type selector and price table (#19)

release v0.5.0
  fix       4313ac3 fix(useStationStorage): hoist stations ref to module level to restore singleton
  feature   35ba3fb feat(useStationPrices): fix composable caller-responsibility violation
  other     2cab35f test(useStationPrices): add unit tests for concurrent fetch composable (#18)
  feature   125d7d7 feat(useStationPrices): rework composable for concurrent multi-station fetching (#18)
  other     8a88abd test(cases): define test scenarios for concurrent fetch composable (#18)
  other     77444a7 docs(security): add security guidelines for concurrent fetch composable (#18)
  other     53868bb docs(specs): define specs for concurrent fetch composable (#18)

release v0.4.0
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

release v0.3.0
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

release v0.2.0
  other     28354ce docs: add missing task artifacts and update auto-imports for issue #15
  other     8987022 test(composable): add useStationStorage spec with 14 passing test cases
  feature   80d73bf feat(storage): add useStationStorage composable backed by IndexedDB
  other     e934c71 ci(agent): document lint and type-check scripts in reviewer to avoid inspection
  other     5b7cde4 ci(agent): set fetch refspec before git fetch to keep origin/* refs current
  other     0075c46 test(cases): define test scenarios for useStationStorage composable (#15)
  feature   247c68a feat(security): add security guidelines for useStationStorage composable (#15)

release v0.1.0
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

release v0.0.4
  other     d08c1fa docs: document Claude Code setup and develop worktree creation
  other     a833e10 ci(agent): update agents and skills for develop/ as Claude Code root (#21)

release v0.0.3
  other     432eb91 ci(agent): replace stale CLAUDE docs and agent-7 with two skills (#20)

release v0.0.2
  other     f9146e3 ci(agent): fix Step 0 order — create worktree before writing README.md
  other     c869b43 ci(agent): fix git push in Task 5 to use explicit branch for worktrees
  other     9b17878 ci(agent): consolidate guidance into CLAUDE.md, fix orchestrator trigger
  other     9713ea9 ci(agent): integrate rtk
  other     48375e6 ci(agent): fix agent-4-git Task 7 and Task 8 for bare-repo worktree setup (#11)

release v0.0.1
  other     1ed47cf docs: remove socialMediaPublisherApp stale references (#8)
  other     b7cbe53 docs: finalize starting prompts in README.md
  other     597427f chore: merge main to develop
  fix       c694167 fix: remove old code from social share app
  fix       d158426 fix: remove old code from social share app
  other     20112f2 chore: init project code using social media sharing app
  other     9fdd70a chore: remove useless components + run first build
  other     62258ee chore: init project code using social media sharing app
  other     e415adf ci(agent): init CLAUDE.md
  other     90c0f4c Enhance README with scraping and user interaction details
  other     c6f4898 Initial commit
```
