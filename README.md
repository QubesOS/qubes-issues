Qubes Issues Repository
=======================

This repository tracks issues and feature development progress for the Qubes OS Project.

**[File a new issue](https://github.com/QubesOS/qubes-issues/issues/new)** | [View all issues](https://github.com/QubesOS/qubes-issues/issues) | [View all unassigned issues](https://github.com/QubesOS/qubes-issues/issues?q=is:open no:milestone no:assignee) | [Search syntax](https://help.github.com/articles/search-syntax/) | [Searching issues](https://help.github.com/articles/searching-issues/)

Main Issue Categories
---------------------

| Release | Critical | Pending Backports |
|:--------|:---------|:------------------|
| [Release 2.1](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 2.1 (post R2)") | [Critical](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 2.1 (post R2)" label:"P: critical" -label:wontfix) | [dom0](https://github.com/QubesOS/qubes-issues/issues?q=is:issue+-label:r2-dom0-stable+-label:r2-dom0-testing+label:r3.1-dom0-stable+is:closed+milestone:"Release+2.0+updates"), [VM](https://github.com/QubesOS/qubes-issues/issues?q=is:issue+-label:r2-fc21-stable+-label:r2-fc21-testing+label:r3.1-fc21-stable+is:closed+milestone:"Release+2.0+updates") |
| [Release 3.0](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 3.0") | [Critical](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 3.0" label:"P: critical" -label:wontfix) | [dom0](https://github.com/QubesOS/qubes-issues/issues?q=is:issue+-label:r3.0-dom0-stable+-label:r3.0-dom0-testing+label:r3.1-dom0-stable+is:closed+milestone:"Release+3.0+updates"), [VM](https://github.com/QubesOS/qubes-issues/issues?q=is:issue+-label:r3.0-fc21-stable+-label:r3.0-fc21-testing+label:r3.1-fc21-stable+is:closed+milestone:"Release+3.0+updates") |
| [Release 3.1](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 3.1") | [Critical](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 3.1" label:"P: critical" -label:wontfix) |
| [Release 3.2](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 3.2") | [Critical](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 3.2" label:"P: critical" -label:wontfix) |
| [Release 4.0](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 4.0") | [Critical](https://github.com/QubesOS/qubes-issues/issues?q=is:open milestone:"Release 4.0" label:"P: critical" -label:wontfix) |
| [no milestone](https://github.com/QubesOS/qubes-issues/issues?q=is:open no:milestone) | [Critical](https://github.com/QubesOS/qubes-issues/issues?q=is:open no:milestone label:"P: critical" -label:wontfix) |


Feature Development Progress
----------------------------

| Feature Name | Current Developers | Status | Last Update | See Also |
|:-------------|:-------------------|:-------|:------------|:---------|
| [Split GPG using GPG v2.1](https://github.com/QubesOS/qubes-issues/issues/474) | [Joanna], [Marek], [HW42] | In progress | [2015-11-16](https://github.com/QubesOS/qubes-issues/issues/474#issuecomment-156885755) | [Discussion](https://groups.google.com/d/msgid/qubes-devel/20150309013432.GA2361%40mail-itl), [Prototype](https://git.ipsumj.de/hw42/qubes/split-gpg2.git) |
| [PV USB](https://github.com/QubesOS/qubes-issues/issues/531) | [Marek], [caschulz88] | In progress | [2016-04-01](https://github.com/QubesOS/qubes-issues/issues/531#ref-commit-046149e) | [USBIP over qrexec proxy](https://github.com/QubesOS/qubes-app-linux-usb-proxy) |
| [Anti-forensic DispVMs](https://github.com/QubesOS/qubes-issues/issues/904) | [Joanna], [Marek] | Planning | [2016-03-08](https://github.com/QubesOS/qubes-issues/issues/904#issuecomment-193953355) | [Separate `volatile.img`](https://github.com/QubesOS/qubes-issues/issues/1527) |
| [Instant DispVMs](https://github.com/QubesOS/qubes-issues/issues/1512) | [qubesuser] | [PoC](https://github.com/qubesuser/qubes-core-admin/tree/insta_dvm), [Waiting](https://github.com/QubesOS/qubes-issues/issues/1512#issuecomment-166640065) | [2015-12-22](https://github.com/QubesOS/qubes-issues/issues/1512#issuecomment-166716447) | -- |
| [Separate `volatile.img`](https://github.com/QubesOS/qubes-issues/issues/1527) | [v6ak] | [PoC](https://groups.google.com/forum/#!topic/qubes-users/X0BBZ-kfix0) | [2015-12-19](https://groups.google.com/d/msg/qubes-users/X0BBZ-kfix0/UADwGKnlBwAJ) | [Discussion](https://groups.google.com/forum/#!topic/qubes-users/X0BBZ-kfix0) |

--

| Status Term | Meaning |
|:------------|:--------|
| In progress | Feature is currently being developed. |
| Planning    | Feature is being discussed to determine scope and goals; development has not yet begun. |
| PoC         | A proof-of-concept has been successfully created, but more work is required to integrate it with Qubes. |
| Waiting     | Feature is partially complete, but is waiting on the completion of another component. |



[Joanna]: https://github.com/rootkovska
[Marek]: https://github.com/marmarek
[HW42]: https://github.com/HW42
[caschulz88]: https://github.com/caschulz88
[qubesuser]: https://github.com/qubesuser
[v6ak]: https://github.com/v6ak
