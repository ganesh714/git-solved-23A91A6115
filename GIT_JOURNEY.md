\# My Git Mastery Challenge Journey



\## Student Information

\- Name: ELISETTI VEERA VENKATA GANESH

\- Student ID: 23A91A6115

\- Repository: https://github.com/ganesh714/git-solved-23A91A6115

\- Date Started: 29-10-2025

\- Date Completed: 29-10-2025



\## Task Summary

Cloned instructor's repository with pre-built conflicts and resolved all

merge conflicts across multiple branches using proper Git workflows. Practiced

advanced Git commands like stash, cherry-pick, rebase, reset, and revert.



\## Commands Used



| Command       | Times Used | Purpose                                  |

|---------------|------------|------------------------------------------|

| git clone     | 1          | Clone instructor's repository            |

| git checkout  | ~15+       | Switch between branches                  |

| git branch    | ~10+       | View and manage branches                 |

| git merge     | 2          | Merge dev and conflict-simulator         |

| git add       | ~20+       | Stage resolved conflicts \& changes       |

| git commit    | ~10+       | Commit resolved changes \& features       |

| git push      | ~10+       | Push to my repository (origin)           |

| git fetch     | 1          | Fetch updates from instructor            |

| git pull      | 1          | Pull updates from instructor             |

| git stash     | 1 (push+pop) | Save temporary work                    |

| git cherry-pick | 2        | Copy specific commit (feature, revert) |

| git rebase    | 1          | Rebase feature branch onto main          |

| git reset     | 3          | Undo commits (soft/mixed/hard)           |

| git revert    | 1          | Safe undo commit                         |

| git tag       | 2          | Create release tags (v1.0.0, v1.1.0)     |

| git status    | ~30+       | Check repository state                   |

| git log       | ~10+       | View history                             |

| git diff      | ~5+        | Compare changes                          |

| git remote    | 3 (rename, add, -v) | Manage remote repositories       |

| git reflog    | 1          | Recover lost commit after reset --hard |



\## Conflicts Resolved



\### Merge 1: main + dev (6 files)



\#### Conflict 1: config/app-config.yaml

\- \*\*Issue\*\*: Production (port 8080, prod env) vs Development (port 3000, dev env, hot reload).

\- \*\*Resolution\*\*: Kept production settings, added `development` block with dev settings.

\- \*\*Strategy\*\*: Unified config, controlled by environment variable (implied).

\- \*\*Difficulty\*\*: Medium

\- \*\*Time\*\*: ~10 minutes



\#### Conflict 2: config/database-config.json

\- \*\*Issue\*\*: Production DB details vs Development DB details (host, username, ssl, pool size, backup, replication). Added dev-specific features.

\- \*\*Resolution\*\*: Created distinct `production` and `development` top-level keys. Moved respective configs under them. Added dev features under `development`.

\- \*\*Strategy\*\*: Separate config profiles within one file.

\- \*\*Difficulty\*\*: Medium

\- \*\*Time\*\*: ~10 minutes



\#### Conflict 3: scripts/deploy.sh

\- \*\*Issue\*\*: Simple production script vs Development script with npm install, tests, docker-compose, health check.

\- \*\*Resolution\*\*: Created unified script using `if/elif/else` based on `DEPLOY\_ENV` variable. Included logic for both prod and dev.

\- \*\*Strategy\*\*: Conditional execution based on environment.

\- \*\*Difficulty\*\*: Hard

\- \*\*Time\*\*: ~15 minutes



\#### Conflict 4: scripts/monitor.js

\- \*\*Issue\*\*: Production monitoring (60s interval) vs Development monitoring (5s interval, debug mode, verbose logging, random metrics, memory log).

\- \*\*Resolution\*\*: Created config object with `production` and `development` keys. Used `process.env.NODE\_ENV` to select config. Combined logic.

\- \*\*Strategy\*\*: Environment-based configuration loading.

\- \*\*Difficulty\*\*: Medium

\- \*\*Time\*\*: ~10 minutes



\#### Conflict 5: docs/architecture.md

\- \*\*Issue\*\*: Production architecture description vs Development architecture with Docker, OAuth, more details.

\- \*\*Resolution\*\*: Merged descriptions, creating distinct sections/points for Prod vs Dev features.

\- \*\*Strategy\*\*: Combine and clarify documentation for both environments.

\- \*\*Difficulty\*\*: Easy

\- \*\*Time\*\*: ~5 minutes



\#### Conflict 6: README.md

\- \*\*Issue\*\*: Production README vs Development README (different version, features, setup instructions, contributing section).

\- \*\*Resolution\*\*: Combined content, listing both versions, separating Prod/Dev features, adding both Quick Start sections.

\- \*\*Strategy\*\*: Create a comprehensive README covering both states.

\- \*\*Difficulty\*\*: Easy

\- \*\*Time\*\*: ~10 minutes



\### Merge 2: main + conflict-simulator (6 files)



\#### Conflict 1: config/app-config.yaml

\- \*\*Issue\*\*: Merged Prod/Dev config vs Experimental config (different name, version, port, AI features, experimental block).

\- \*\*Resolution\*\*: Kept the merged Prod/Dev config. Added the entire experimental config block as comments at the end.

\- \*\*Strategy\*\*: Prioritize stable code, keep experimental code commented out for reference.

\- \*\*Difficulty\*\*: Medium

\- \*\*Time\*\*: ~10 minutes



\#### Conflict 2: config/database-config.json

\- \*\*Issue\*\*: Prod/Dev profiles vs Experimental distributed DB config (different structure, hosts array, AI optimization, monitoring).

\- \*\*Resolution\*\*: Kept the Prod/Dev profiles. Added the entire experimental config under a new top-level key `experimental\_config\_from\_simulator`.

\- \*\*Strategy\*\*: Isolate experimental config under an inactive key since JSON doesn't support comments easily.

\- \*\*Difficulty\*\*: Medium

\- \*\*Time\*\*: ~10 minutes



\#### Conflict 3: scripts/deploy.sh

\- \*\*Issue\*\*: Merged multi-environment script vs Experimental AI-powered multi-cloud canary deployment script.

\- \*\*Resolution\*\*: Kept the merged multi-environment script. Added the entire experimental script as comments at the end.

\- \*\*Strategy\*\*: Prioritize stable script, comment out experimental script.

\- \*\*Difficulty\*\*: Medium

\- \*\*Time\*\*: ~10 minutes



\#### Conflict 4: scripts/monitor.js

\- \*\*Issue\*\*: Merged Prod/Dev monitor script vs Experimental AI-enhanced predictive monitoring script (ML models, multi-cloud checks).

\- \*\*Resolution\*\*: Kept the merged Prod/Dev script. Added the entire experimental script as comments at the end.

\- \*\*Strategy\*\*: Prioritize stable script, comment out experimental script.

\- \*\*Difficulty\*\*: Medium

\- \*\*Time\*\*: ~10 minutes



\#### Conflict 5: docs/architecture.md

\- \*\*Issue\*\*: Merged Prod/Dev architecture vs Experimental event-driven AI/ML architecture doc.

\- \*\*Resolution\*\*: Kept the merged Prod/Dev doc. Added the experimental architecture description inside Markdown comment tags (``).

\- \*\*Strategy\*\*: Prioritize stable documentation, comment out experimental doc.

\- \*\*Difficulty\*\*: Easy

\- \*\*Time\*\*: ~5 minutes



\#### Conflict 6: README.md

\- \*\*Issue\*\*: Merged README vs Experimental README (different title, features, AI focus, warnings). Had two conflict blocks.

\- \*\*Resolution\*\*: Kept the merged README. Added all experimental content inside a single Markdown comment block (``) at the end.

\- \*\*Strategy\*\*: Prioritize stable README, comment out experimental content.

\- \*\*Difficulty\*\*: Medium (due to multiple blocks)

\- \*\*Time\*\*: ~10 minutes





\## Most Challenging Parts



1\.  \*\*Resolving 3-Way Conflicts (Phase 3)\*\*: Understanding how the code evolved from the common ancestor to the two diverging branches (`main` after Phase 2 merge, and `conflict-simulator`) was complex. Deciding how to integrate experimental features without breaking stable code required careful commenting/isolation.

2\.  \*\*`git reset` Practice\*\*: Understanding the difference between `--soft`, `--mixed`, and `--hard` resets and seeing their effects with `git status` was tricky but essential. Recovering with `reflog` after `--hard` was a good safety lesson.

3\.  \*\*Windows Multi-line Commit Issue\*\*: The initial trouble with pasting multi-line commit messages into the default editor was frustrating, but learning the `-F <file>` method was a valuable workaround.



\## Key Learnings



\### Technical Skills

\- Confidently resolved basic and complex (3-way) merge conflicts.

\- Understood and used merge conflict markers effectively.

\- Applied advanced commands: `stash`, `cherry-pick`, `rebase`, `reset` (all modes), `revert`, `reflog`.

\- Managed multiple remotes (`instructor`, `origin`).

\- Created and pushed annotated tags.



\### Best Practices

\- Prioritize keeping the main branch stable when merging experimental code (comment out or use feature flags).

\- Write detailed commit messages, especially for merges, explaining \*why\* resolutions were chosen.

\- Use `git status` constantly to understand the repository state.

\- `reflog` is a powerful tool for recovering from mistakes, especially after `reset --hard` or rebase issues.

\- Test code after resolving conflicts.



\### Git Workflow Insights

\- Conflicts are a natural part of collaborative development, not errors to be feared.

\- Rebasing provides cleaner history but requires caution (force push, potential for complex conflict resolution). Merging is safer for shared branches.

\- Understanding the \*purpose\* of conflicting changes is key to making good resolution decisions.



\## Reflection

This challenge provided intense, practical experience far beyond basic Git tutorials. Facing pre-built, complex conflicts forced me to understand the merging process deeply. The second merge (Phase 3) was particularly insightful, showing how experimental features clash with stable code and how to handle that safely. Practicing `rebase`, `reset`, and `revert` clarified their use cases and risks. I feel much more prepared to handle version control in a team environment now, especially understanding how to recover from mistakes using `reflog`.

