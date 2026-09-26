# Pinata Ruby Gem Instructions

`lib/pinata/` implements the gem’s Pinata API client and `spec/pinata_spec.rb` is its only checked-in specification. Read the relevant client method and that specification before changing request construction or response handling. Run `bin/setup` to install dependencies when the legacy Ruby toolchain is available.

The Rakefile sets its default task to `:spec`, but it does not define that task; `bundle exec rake` is therefore an incomplete test command until the task wiring is repaired in a separately scoped change. Do not report it as a passing suite. Use a focused RSpec invocation only after confirming its compatibility with the installed dependencies, and report any unsupported test tooling precisely.

Never place Pinata API keys, secret keys, or real pin identifiers in fixtures, logs, or commits. `bundle exec rake release` builds and publishes a gem and pushes a tag; use it only under an explicit release task or applicable standing authorization and report its remote result separately.
