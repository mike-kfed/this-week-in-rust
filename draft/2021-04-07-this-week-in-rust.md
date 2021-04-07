Title: This Week in Rust 385
Number: 385
Date: 2021-04-07
Category: This Week in Rust

Hello and welcome to another issue of *This Week in Rust*!
[Rust](http://rust-lang.org) is a systems language pursuing the trifecta: safety, concurrency, and speed.
This is a weekly summary of its progress and community.
Want something mentioned? Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) or [send us a pull request](https://github.com/rust-lang/this-week-in-rust).
Want to get involved? [We love contributions](https://github.com/rust-lang/rust/blob/master/CONTRIBUTING.md).

*This Week in Rust* is openly developed [on GitHub](https://github.com/rust-lang/this-week-in-rust).
If you find any errors in this week's issue, [please submit a PR](https://github.com/rust-lang/this-week-in-rust/pulls).

# Updates from Rust Community

No newsletters this week.

### Official

### Project/Tooling Updates
* [A new Left Recursive PEG Parser Generator for rust](https://www.mess.org/2021/03/26/Left-Recursive-PEG-Parser-Generator/)

### Observations/Thoughts
* [Interfacing a low-level actor system to Rust async/await, part 1](https://uazu.github.io/blog/20210406.html)

### Rust Walkthroughs
* [How we built our Python Client that's mostly Rust](https://www.fluvio.io/blog/2021/03/python-client/)
* [Hello world with KAS GUI](https://kas-gui.github.io/tutorials/hello.html)
* [How to create small Docker images for Rust](https://kerkour.com/blog/rust-small-docker-image/)

### Papers and Research Projects

### Miscellaneous
* [best-of-ml-rust: A ranked list of awesome machine learning Rust libraries](https://github.com/e-tony/best-of-ml-rust)

# Crate of the Week

This week's crate is [rs-pbrt](https://crates.io/crates/rs_pbrt), a counterpart to the PBRT book's (3rd edition) C++ code.

Thanks to [Jan Walter](https://users.rust-lang.org/t/crate-of-the-week/2704/900) for the suggestion!

[Submit your suggestions and votes for next week][submit_crate]!

[submit_crate]: https://users.rust-lang.org/t/crate-of-the-week/2704

# Call for Participation

Always wanted to contribute to open-source projects but didn't know where to start?
Every week we highlight some tasks from the Rust community for you to pick and get started!

Some of these tasks may also have mentors available, visit the task page for more information.

If you are a Rust project owner and are looking for contributors, please submit tasks [here][guidelines].

[guidelines]: https://users.rust-lang.org/t/twir-call-for-participation/4821

# Updates from Rust Core

313 pull requests were [merged in the last week][merged]

[merged]: https://github.com/search?q=is%3Apr+org%3Arust-lang+is%3Amerged+merged%3A2021-03-29..2021-04-05

* [fix stack overflow detection on FreeBSD 11.1+](https://github.com/rust-lang/rust/pull/83771)
* [disallow the use of high byte registes as operands on `x86_64`](https://github.com/rust-lang/rust/pull/83853)
* [resolve/expand: cache intermediate results of `#[derive]` expansion](https://github.com/rust-lang/rust/pull/82907)
* [panic early when `TrustedLen` indicates a `length > usize::MAX`](https://github.com/rust-lang/rust/pull/83726)
* [suggest `box`/`pin`/`arc`ing receiver on method calls](https://github.com/rust-lang/rust/pull/83667)
* [run LLVM coverage instrumentation passes before optimization passes](https://github.com/rust-lang/rust/pull/83666)
* [simplify logical operations CFG](https://github.com/rust-lang/rust/pull/83663)
* [remove unneeded type resolving](https://github.com/rust-lang/rust/pull/83839)
* [unaligned_references: `align(N)` fields in `packed(N)` structs are fine](https://github.com/rust-lang/rust/pull/83605)
* [prevent very long compilation runtimes in `LateBoundRegionNameCollector`](https://github.com/rust-lang/rust/pull/83406)
* [reduce the impact of `Vec::reserve` calls that do not cause any allocation](https://github.com/rust-lang/rust/pull/83357)
* [BTree: no longer search arrays twice to check `Ord`](https://github.com/rust-lang/rust/pull/83267)
* [stream the dep-graph to a file instead of storing it in-memory](https://github.com/rust-lang/rust/pull/82780)
* [implement `SourceIterator` and `InPlaceIterable` for `ResultShunt`](https://github.com/rust-lang/rust/pull/81619)
* [optimize jumps in `PartialOrd::le`](https://github.com/rust-lang/rust/pull/83819)
* [`ffi::c_str` removed bound checks on `as_bytes`, `to_bytes`](https://github.com/rust-lang/rust/pull/83609)
* [added `as_slice` method to `BinaryHeap` collection](https://github.com/rust-lang/rust/pull/82331)
* [use `#[inline(always)]` on trivial `UnsafeCell` methods](https://github.com/rust-lang/rust/pull/83858)
* [add `#[inline]` to `IpAddr` methods](https://github.com/rust-lang/rust/pull/83831)
* [disallow octal format in Ipv4 string](https://github.com/rust-lang/rust/pull/83652)
* [constify methods of `std::net::SocketAddr`, `SocketAddrV4` and `SocketAddrV6`](https://github.com/rust-lang/rust/pull/82487)
* [constify some slice methods](https://github.com/rust-lang/rust/pull/83571)
* [stdsimd: add saturating abs/neg](https://github.com/rust-lang/stdsimd/pull/87)
* [hashbrown: make `RawTable::insert_no_grow` unsafe](https://github.com/rust-lang/hashbrown/pull/254)
* [cargo: add cargo config subcommand](https://github.com/rust-lang/cargo/pull/9302)
* [rustdoc: only look at blanket impls in `get_blanket_impls`](https://github.com/rust-lang/rust/pull/83681)
* [rustdoc: add unstable option to only emit shared/crate-specific files](https://github.com/rust-lang/rust/pull/83478)
* [rustdoc: don't enter an `infer_ctxt` in `get_blanket_impls` for impls that aren't blanket impls](https://github.com/rust-lang/rust/pull/82864)
* [rustdoc: highlight macros more efficiently](https://github.com/rust-lang/rust/pull/83793)
* [clippy: add `non_octal_unix_permissions` lint](https://github.com/rust-lang/rust-clippy/pull/7001)
* [clippy: don't lint `manual_map` in const functions](https://github.com/rust-lang/rust-clippy/pull/6976)
* [clippy: new Lint: `needless_for_each`](https://github.com/rust-lang/rust-clippy/pull/6706)
* [clippy: new Lint: `branches_sharing_code`](https://github.com/rust-lang/rust-clippy/pull/6463)
* [clippy: lint: `filter(Option::is_some).map(Option::unwrap)`](https://github.com/rust-lang/rust-clippy/pull/6342)
* [clippy: remove author requirement for `cargo_common_metadata`](https://github.com/rust-lang/rust-clippy/pull/7026)
* [Clippy going dark: adding a dark theme to Clippy's lint list](https://github.com/rust-lang/rust-clippy/pull/7030)
* [crates.io: topologically sort `db-dump.tar.gz`](https://github.com/rust-lang/crates.io/pull/3409)
* [parallelize tidy](https://github.com/rust-lang/rust/pull/82347)

## Rust Compiler Performance Triage

An overall busy but decent week for performance. While there were some performance regressions they were mostly small, and they were outnumbered by performance gains. Perhaps the most interesting news is not a compiler performance improvement but rather the introduction of no-alias optimizations at the LLVM level. This slightly hurts optimized build time performance in some cases, but it should make some workloads run faster after compilation.

Triage done by **@rylev**.
Revision range: [f24ce9b0..9b6339e4](https://perf.rust-lang.org/?start=f24ce9b0140d9be5a336954e878d0c1522966bb8&end=9b6339e4b9747d473270baa42e77e1d2fff39bf4&absolute=false&stat=instructions%3Au)

2 Regressions, 5 Improvements, 3 Mixed

1 of them in rollups

## Approved RFCs

Changes to Rust follow the Rust [RFC (request for comments) process](https://github.com/rust-lang/rfcs#rust-rfcs). These
are the RFCs that were approved for implementation this week:

* [RFC: Declarative macro metavariable expressions](https://github.com/rust-lang/rfcs/pull/3086)

## Final Comment Period

Every week [the team](https://www.rust-lang.org/team.html) announces the
'final comment period' for RFCs and key PRs which are reaching a
decision. Express your opinions now.

### [RFCs](https://github.com/rust-lang/rfcs/labels/final-comment-period)

* [Raw Keywords](https://github.com/rust-lang/rfcs/pull/3098)

### [Tracking Issues & PRs](https://github.com/rust-lang/rust/labels/final-comment-period)

* [disposition: merge] [Add strong_count mutation methods to Rc](https://github.com/rust-lang/rust/pull/83476)
* [disposition: merge] [Turn old edition lint (anonymous-parameters) into warn-by-default on 2015](https://github.com/rust-lang/rust/pull/82918)
* [disposition: merge] [reduce threads spawned by ui-tests](https://github.com/rust-lang/rust/pull/81942)
* [disposition: merge] [Stabilize `peekable_peek_mut`](https://github.com/rust-lang/rust/pull/81938)
* [disposition: merge] [Stabilize `rustdoc::bare_urls` lint](https://github.com/rust-lang/rust/pull/81764)
* [disposition: merge] [Adding diesel to the cargotest suite](https://github.com/rust-lang/rust/pull/81507)
* [disposition: merge] [Stabilize `cmp_min_max_by`](https://github.com/rust-lang/rust/pull/81047)
* [disposition: merge] [Allow qualified paths in struct construction (both expressions and patterns)](https://github.com/rust-lang/rust/pull/80080)
* [disposition: merge] [Tracking issue for RFC 2457, "Allow non-ASCII identifiers"](https://github.com/rust-lang/rust/issues/55467)

## New RFCs

* [RFC: Add a standard trait for getting many &mut to places](https://github.com/rust-lang/rfcs/pull/3100)
* [RFC: `cargo`-`miri` integration](https://github.com/rust-lang/rfcs/pull/3099)
* [Raw Keywords](https://github.com/rust-lang/rfcs/pull/3098)
* [rustdoc URL conflict resolution](https://github.com/rust-lang/rfcs/pull/3097)

# Upcoming Events

### Online
* [April 1, Berlin, DE - Rust Hack and Learn - Berline.rs](https://www.meetup.com/opentechschool-berlin/events/txcprryccgbcb/)
* [April 6, Buffalo, NY, US - Buffalo Rust User Group - Buffalo Rust Meetup](https://www.meetup.com/Buffalo-Rust-Meetup/events/276717867/)
* [April 7, Johannesburg, ZA - Monthly Joburg Rust Chat! - Johannesburg Rust Meetup](https://www.meetup.com/Johannesburg-Rust-Meetup/events/277133126/)
* [April 7, Indianapolis, IN, US - Indy.rs - with Social Distancing - Indy Rust](https://www.meetup.com/indyrs/events/jhfstryccgbkb/)
* [April 13, Seattle, WA, US - Monthly Meetup - Seattle Rust Meetup](https://www.meetup.com/Seattle-Rust-Meetup/events/gskksryccgbrb/)
* [April 13, Saarbrücken, Saarland, DE - **Rust Saar** 10u16](https://www.meetup.com/de-DE/Rust-Saar/events/276873622/)

### North America

* [April 8, Columbus, OH, US - Monthly Meetup - Columbus Rust Society](https://www.meetup.com/columbus-rs/events/dpkhgryccgblb/)
* [April 14, Atlanta, GA, US - Grab a beer with fellow Rustaceans - Rust Atlanta](https://www.meetup.com/Rust-ATL/events/qxqdgryccgbsb/)

If you are running a Rust event please add it to the [calendar] to get
it mentioned here. Please remember to add a link to the event too.
Email the [Rust Community Team][community] for access.

[calendar]: https://www.google.com/calendar/embed?src=apd9vmbc22egenmtu5l6c5jbfc%40group.calendar.google.com
[community]: mailto:community-team@rust-lang.org

# Rust Jobs

*Tweet us at [@ThisWeekInRust](https://twitter.com/ThisWeekInRust) to get your job offers listed here!*

# Quote of the Week

Sadly there was no quote nominated for this week.

[Please submit quotes and vote for next week!](https://users.rust-lang.org/t/twir-quote-of-the-week/328)

*This Week in Rust is edited by: [nellshamrell](https://github.com/nellshamrell), [llogiq](https://github.com/llogiq), and [cdmistman](https://github.com/cdmistman).*

<small>[Discuss on r/rust](https://www.reddit.com/r/rust/comments/k5nsab/this_week_in_rust_367/)</small>