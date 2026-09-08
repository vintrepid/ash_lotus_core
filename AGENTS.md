<!--
SPDX-FileCopyrightText: 2026 Vince Nibler

SPDX-License-Identifier: MIT
-->

# AshLotus Core Agent Rules

1. This repository is the upstream-tracking core fork used by the public
   `ash_lotus` distribution. Keep its downstream patch set exceptionally small.
2. Preserve the Mix/OTP application name `:ash` and the `Ash.*` namespace so
   every Ash extension remains compatible.
3. Do not add JournalAsh, SolidAsh, Cinder, AshPostgres, AshPhoenix, or other
   Ash extensions to this project's dependencies. Those packages depend on
   `:ash`; the dependency policy belongs in the separate `ash_lotus`
   distribution repository.
4. Keep general Ash fixes in isolated commits suitable for contributing to
   `ash-project/ash`. Do not mix them with AshLotus-only maintenance.
5. The `upstream` remote must fetch from
   `https://github.com/ash-project/ash.git` and must remain push-disabled.
6. Before changing tests, follow `.github/CONTRIBUTING.md` and
   `documentation/topics/development/testing.md`, then run the proportionate
   upstream checks.
7. Update the distribution's immutable core pin only after this repository and
   the full AshLotus compatibility matrix pass.
