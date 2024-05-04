An opinionated list of awesome regular expression tools, tutorials, libraries, and other resources. Currently includes especially deep coverage of regular expressions in JavaScript.

Your contributions are welcome! Please take a look at the [contribution guidelines](CONTRIBUTING.md) first.

## Contents

- [Glossary](#glossary)
- [Testers](#testers)
  - [Best testers](#best-testers)
  - [More testers](#more-testers)
- [Syntax-free regex builders](#syntax-free-regex-builders)
- [Visualizers](#visualizers)
- [Search and replace through files](#search-and-replace-through-files)
- [Tutorials](#tutorials)
  - [Videos](#videos)
- [Regex engines](#regex-engines)
  - [Documentation](#documentation)
  - [Source code](#source-code)
  - [Flavor differences](#flavor-differences)
- [Performance](#performance)
- [Collections of patterns](#collections-of-patterns)
- [JavaScript regex libraries](#javascript-regex-libraries)
- [JavaScript regex evolution](#javascript-regex-evolution)
  - [Future: Active proposals](#future-active-proposals)
- [Books](#books)
- [Articles](#articles)
- [Communities](#communities)
- [Miscelaneous](#miscelaneous)

## Glossary

*A brief glossary of regular expression terms as used in this list.*

<details>
  <summary>Show the glossary.</summary>
  <br>

- **Regex engine:** Software that parses and executes regular expressions, often built into a programming language (synonym: implementation).
- **Regex flavor:** A unique set of regex syntax and behavior. Basic syntax is typically shared across flavors, but more advanced features often vary, sometimes in subtle ways. A flavor might be shared across multiple implementations or programming languages.
  - Ex: The “JavaScript” flavor is defined by the ECMAScript standard and implemented by multiple engines (V8, etc.).
  - Ex: The “PCRE” flavor is the PCRE2 library, used by numerous programming languages and tools (including PHP’s [`preg_*`](https://www.php.net/manual/en/ref.pcre.php) functions).
  - Ex: Ruby changed its regex implementation twice from version 1.8 ➜ 1.9 ➜ 2.0, so each used a distinct flavor. In this list, the Ruby 2.0+ flavor is referred to as either “Ruby” or “Onigmo” (the regex library adopted by Ruby 2.0).
- **Non-backtracking engine:** Sometimes referred to elsewhere as a “DFA” engine (as opposed to a “traditional NFA” engine). Non-backtracking engines like RE2 and Rust’s `regex` run in linear time because they don’t require/allow backtracking. This precludes “catastrophic backtracking”, but it’s also slower with some common patterns and prevents some useful features like backreferences and lookaround. See also: [Performance](#performance).
</details>

## Testers

*For building, testing, and playing with regexes. All of these include live match highlighting, and many include regex syntax highlighting and other advanced features.*

### Best testers

*The very best, in several categories.*

- [regex101](https://regex101.com/) — **Best free and best web-based tester**.
  - Flavors: Java, JavaScript, .NET, PCRE, RE2, Rust, and emulates Python.
  - Includes debugger (PCRE only).
- [RegexBuddy](https://www.regexbuddy.com/) (<picture><img src="public/images/ms-logo.svg" title="Windows" height="12"></picture>, $40) — **Best tester**.
  - Flavors: Emulates hundreds of flavors/versions, with deep knowledge of differences.
  - Includes debugger.
- [RegExr](https://regexr.com/) [[*GitHub*](https://github.com/gskinner/regexr/)] — **Best open source tester**.
  - Flavors: JavaScript, PCRE.
- [RegexLearn](https://regexlearn.com/playground) [[*GitHub*](https://github.com/aykutkardas/regexlearn.com)] — **Best multilingual tester** (JavaScript).
  - Languages: 🇺🇸, 🇹🇷, 🇷🇺, 🇪🇸, 🇨🇳, 🇩🇪, 🇺🇦, 🇫🇷, 🇵🇱, 🇰🇷, 🇧🇷, 🇨🇿, 🇬🇪.
- [regexplained](https://regexplained.com/) [[*GitHub*](https://github.com/LeaVerou/regexplained)] — **Best tester for presentations** (JavaScript).

### More testers

*Additional testing options that still meet the quality bar or include unique features.*

- Flavors:
  - JavaScript: [RegViz](http://regviz.org/).
  - .NET: [Regex Storm](http://regexstorm.net/tester) [[*GitHub*](https://github.com/lonekorean/regex-storm)], [Regex Hero](https://regexhero.net/tester/) (<picture><img src="public/images/ms-logo.svg" title="Windows" height="12"></picture>), [Expresso](https://ultrapico.com/Expresso.htm) (<picture><img src="public/images/ms-logo.svg" title="Windows" height="12"></picture>).
  - PCRE: [PHP Live Regex](https://www.phpliveregex.com/).
  - Python: [Pythex](https://pythex.org/).
  - Ruby: [Rubular](https://rubular.com/).
- Multiple flavors:
  - [CyrilEx](https://extendsclass.com/regex-tester.html) [[*GitHub*](https://github.com/cyrilbois/cyrilex)]: Java, JavaScript, MySQL, PHP, Python, Ruby.
  - [RegexPlanet](https://www.regexplanet.com/) [[*GitHub*](https://github.com/regexplanet)]: Go, Haskell, Java, JavaScript, .NET, Perl, PHP, PostgreSQL, Python, Ruby, Tcl, XRegExp.

## Syntax-free regex builders

*Build regexes without writing regex syntax or code. See also: [Readable regex composers](#javascript-regex-libraries).*

- [ChatGPT](https://chat.openai.com/) (and other LLMs) — Ex: *"create a regex that matches `X` and explain it step by step"*.
- [RegexMagic](https://www.regexmagic.com/) (<picture><img src="public/images/ms-logo.svg" title="Windows" height="12"></picture>, $40).

## Visualizers

*Visualize how your regular expressions are structured or operate.*

- [Regulex](https://jex.im/regulex/) [[*GitHub*](https://github.com/CJex/regulex)] — Flavor: JavaScript.
- [Nodexr](https://www.nodexr.net/) [[*GitHub*](https://github.com/Jcparkyn/nodexr)] — Flavor: .NET.
- [Regex Nodes](https://johannesvollmer.com/regex-nodes/) [[*GitHub*](https://github.com/johannesvollmer/regex-nodes)] — Flavor: JavaScript.

More: [RegExper](https://regexper.com/) [[*GitLab*](https://gitlab.com/javallone/regexper-static)], [Debuggex](https://www.debuggex.com/).

## Search and replace through files

*Software for grepping through files, on the command line or visually.*

- [GNU Grep](https://www.gnu.org/software/grep/manual/grep.html).
- [Aba Search and Replace](https://www.abareplace.com/) (<picture><img src="public/images/ms-logo.svg" title="Windows" height="12"></picture>, $30).
- [PowerGREP](https://www.powergrep.com/) (<picture><img src="public/images/ms-logo.svg" title="Windows" height="12"></picture>, $159) — Can search through archives, binary files, PDFs, docs/sheets, Outlook emails, etc., via GUI or command line.
- [RegexRenamer](https://regexrenamer.sourceforge.net/) (<picture><img src="public/images/ms-logo.svg" title="Windows" height="12"></picture>) — Rename files using regexes.

## Tutorials

*Learn how to use regular expressions.*

- Traditional:
  - [Regular-Expressions.info](https://www.regular-expressions.info/) — Covers numerous regex flavors.
  - [The Modern JavaScript Tutorial: Regular expressions](https://javascript.info/regular-expressions) [[*GitHub*](https://github.com/javascript-tutorial/en.javascript.info)] — Languages: 🇺🇸, 🇪🇸, 🇫🇷, 🇮🇹, 🇯🇵, 🇷🇺, 🇺🇦, 🇨🇳 (partial for [others](https://javascript.info/translate)).
- With interactive exercises:
  - [RegexLearn](https://regexlearn.com/) [[*GitHub*](https://github.com/aykutkardas/regexlearn.com)] — Languages: 🇺🇸, 🇹🇷, 🇷🇺, 🇪🇸, 🇨🇳, 🇩🇪, 🇺🇦, 🇫🇷, 🇵🇱, 🇰🇷, 🇧🇷, 🇨🇿, 🇬🇪.
  - [RegexOne](https://regexone.com/).
- Exercises only:
  - [regex101: Regex Quiz](https://regex101.com/quiz) — Requires sign-in.

More: [RexEgg](https://rexegg.com/).

### Videos

*Regex video tutorials.*

- [*Demystifying Regular Expressions*](https://www.youtube.com/watch?v=M7vDtxaD7ZU), by Lea Verou.
- [*Learn Regular Expressions In 20 Minutes*](https://www.youtube.com/watch?v=rhzKDrUiJVk), by Kyle Cook.
- Many options for video courses are available on [Udemy](https://www.udemy.com/topic/regular-expressions/) ($).

## Regex engines

*Major regex implementations, built into programming languages or as standalone libraries.*

### Documentation

*Official regex references and guides.*

- Regex flavors:
  - JavaScript [MDN]: [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp), [Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Regular_expressions), [Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions).
  - Boost.Regex: [Manual](https://boost.org/libs/regex).
  - Hyperscan: [Introduction](https://www.hyperscan.io/).
  - ICU: [Regular Expressions](https://unicode-org.github.io/icu/userguide/strings/regexp.html).
  - Java: [java.util.regex](https://docs.oracle.com/en/java/javase/22/docs/api/java.base/java/util/regex/package-summary.html), [Pattern](https://docs.oracle.com/en/java/javase/22/docs/api/java.base/java/util/regex/Pattern.html).
  - .NET: [.NET regular expressions](https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions), [System.Text.RegularExpressions](https://learn.microsoft.com/en-us/dotnet/api/system.text.regularexpressions).
  - PCRE2: [pcre2pattern](https://www.pcre.org/current/doc/html/pcre2pattern.html).
  - Perl: [perlre](https://perldoc.perl.org/perlre), [perlretut](https://perldoc.perl.org/perlretut), [perlrequick](https://perldoc.perl.org/perlrequick).
  - Python: [re](https://docs.python.org/library/re.html).
  - RE2: [Syntax](https://github.com/google/re2/wiki/Syntax).
  - Rust: [regex](https://docs.rs/regex/latest/regex/).
- Non-unique:
  - [MySQL](https://dev.mysql.com/doc/refman/en/regexp.html) — Flavor: ICU.

### Source code

*Read or contribute to the code behind major implementations.*

- [V8: Irregexp](https://github.com/v8/v8/tree/main/src/regexp) (Chrome, etc.) — JavaScript `RegExp`.
- [Boost.Regex](https://github.com/boostorg/regex) (C++, Sublime Text, etc.).
- [Hyperscan](https://github.com/intel/hyperscan) — Intel’s high-performance library, used for [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection).
- [ICU](https://github.com/unicode-org/icu/blob/main/icu4c/source/i18n/unicode/regex.h) — Unicode org’s package with full Unicode support.
- [Java: java.util.regex](https://github.com/openjdk/jdk/tree/master/src/java.base/share/classes/java/util/regex).
- [.NET: System.Text.RegularExpressions](https://github.com/dotnet/runtime/tree/main/src/libraries/System.Text.RegularExpressions).
- [Onigmo](https://github.com/k-takata/Onigmo) (Ruby 2.0+, etc.) and [Oniguruma](https://github.com/kkos/oniguruma) (Ruby 1.9, etc.).
- [PCRE2](https://github.com/PCRE2Project/pcre2) (PHP, R, etc.).
- [Perl](https://github.com/Perl/perl5/blob/blead/regexp.h) (see [perlreguts](https://perldoc.perl.org/perlreguts)).
- [Python: re](https://github.com/python/cpython/tree/main/Lib/re) and [regex](https://github.com/mrabarnett/mrab-regex) (with extended features).
- [RE2](https://github.com/google/re2) (Go, etc.) — Non-backtracking engine.
- [Rust: regex](https://github.com/rust-lang/regex) — Non-backtracking engine.

### Flavor differences

*Syntax and behavior differences between regex flavors.*

- Ron Buckton: [Regular Expression Feature Comparisons](https://rbuckton.github.io/regexp-features/) [[*GitHub*](https://github.com/rbuckton/regexp-features)].
- Regular-Expressions.info: [Tools & Languages](https://www.regular-expressions.info/tools.html).
- Steven Levithan: [Named capture](https://xregexp.com/syntax/named_capture_comparison/), [Lookbehind](https://stevenlevithan.com/regex/tests/lookbehind.html).
- Wikipedia: [Comparison of regular expression engines](https://en.wikipedia.org/wiki/Comparison_of_regular_expression_engines).

## Performance

*Guides, benchmarks, and tools for regex performance.*

- Learn:
  - [*Runaway Regular Expressions: Catastrophic Backtracking*](https://www.regular-expressions.info/catastrophic.html), by Jan Goyvaerts.
  - Book chapter: *“Strings and Regular Expressions”*, by Steven Levithan, in [*High Performance JavaScript*](https://www.amazon.com/dp/059680279X/?tag=slev-20) [2010], by Nicholas C. Zakas et al. — Deep dive into backtracking and writing regexes for optimal performance.
  - [*Regular Expression Matching Can Be Simple And Fast*](https://swtch.com/~rsc/regexp/regexp1.html), by Russ Cox — On non-backtracking engines.
- Benchmark:
  - Cross-regex-engine performance comparisons: [rebar](https://github.com/BurntSushi/rebar), [regex-benchmark](https://github.com/mariomka/regex-benchmark), [sljit/regex_perf.html](https://zherczeg.github.io/sljit/regex_perf.html).
  - [octane/regexp.js](https://github.com/chromium/octane/blob/master/regexp.js) — Regex workload for performance testing.
- Tools:
  - [SDL Regex Fuzzer](https://download.cnet.com/sdl-regex-fuzzer/3000-2383_4-75321803.html) (<picture><img src="public/images/ms-logo.svg" title="Windows" height="12"></picture>) — Finds strings that trigger catastrophic backtracking (requires [.NET Framework 3.5](https://learn.microsoft.com/en-us/dotnet/framework/install/dotnet-35-windows)).

## Collections of patterns

*Prewritten regexes for specific tasks.*

- Book: [*Regular Expressions Cookbook, 2nd Edition*](https://www.amazon.com/dp/1449319432/?tag=slev-20) [2012], by Jan Goyvaerts, Steven Levithan — Includes detailed explanations and analysis.
  - Flavors: Java, JavaScript, .NET, PCRE, Perl, Python, Ruby, XRegExp.
- [RegexHub](https://projects.lukehaas.me/regexhub/) [[*GitHub*](https://github.com/lukehaas/RegexHub)].
- [RegexLib: Browse Expressions](https://regexlib.com/DisplayPatterns.aspx).
- Perl: `Regexp::Common` [[*MetaCPAN*](https://metacpan.org/pod/Regexp::Common)] [[*GitHub*](https://github.com/Abigail/Regexp--Common)].

## JavaScript regex libraries

*Open source JavaScript libraries for advanced regex use and processing.*

- Regex processors:
  - AST builders: [regexp-tree](https://github.com/DmitrySoshnikov/regexp-tree) (includes optimizer, etc.), [regexpp](https://github.com/eslint-community/regexpp) (used by ESLint), [regjsparser](https://github.com/jviereck/regjsparser)/[regjsgen](https://github.com/bnjmnt4n/regjsgen), [ret.js](https://github.com/fent/ret.js), [RegexAnalyzer](https://github.com/foo123/RegexAnalyzer).
  - Generate strings that match a given regex: [randexp.js](https://github.com/fent/randexp.js), [regex-to-strings](https://github.com/wimpyprogrammer/regex-to-strings).
  - Generate regex from given strings: [retrie](https://github.com/satyr/retrie).
  - Highlight regex syntax: [Regex Colorizer](https://github.com/slevithan/regex-colorizer) [[*home*](https://stevenlevithan.com/regex/colorizer/)].
- Alternative regex builders and engines:
  - [XRegExp](https://github.com/slevithan/xregexp) [[*home*](https://xregexp.com/)] — Extended regex syntax, flags, and utils.
  - String template tags: [regexp-make-js](https://github.com/mikesamuel/regexp-make-js), [`XRegExp.tag`](https://github.com/slevithan/xregexp?tab=readme-ov-file#xregexptag-included-with-xregexpbuild).
  - [incr-regex-package](https://github.com/nurulc/incr-regex-package) — Partial/incremental matching, used by [react-rxinput](https://github.com/nurulc/react-rxinput) for input validation with a regex mask.
  - [@iter-tools/regex](https://github.com/iter-tools/regex) — Non-backtracking engine for streaming evaluation.
- Readable regex composers:
  - [Rexx](https://github.com/yyytcool/rexx) — Structured syntax with variables and comments.
  - [compose-regexp.js](https://github.com/compose-regexp/compose-regexp.js) — Includes some extra features like `atomic`.
  - More: [VerbalExpressions](https://github.com/VerbalExpressions/JSVerbalExpressions) (has implementations for [many languages](https://verbalexpressions.github.io/)), [magic-regexp](https://github.com/unjs/magic-regexp) [[*home*](https://regexp.dev/)], [Super Expressive](https://github.com/francisrstokes/super-expressive) [[*playground*](https://nartc.github.io/ng-super-expressive/)], [Melody](https://github.com/yoav-lavi/melody).

## JavaScript regex evolution

*A concise history of improvements to regular expressions in the JavaScript [standard](https://tc39.es/ecma262/), with links to the [TC39](https://tc39.es/) proposals where features were developed and discussed.*

- ES3 [1999] introduced powerful regular expressions, though limited compared to other major flavors.
- ES6/ES2015 added: [[*explainer*](https://exploringjs.com/es6/ch_regexp.html)]
  - Flag `/y` (`sticky`).
  - Flag `/u` (`unicode`) [[*explainer*](https://mathiasbynens.be/notes/es6-unicode-regex)] [[*2016 spec fix*](https://github.com/tc39/ecma262/pull/525)] with errors for unreserved letter escapes, Unicode code point escapes `\u{…}`, impact on flag `/i`, and surrogate pairs as code points (with impact on quantifiers, character classes, character class ranges, and built-in classes like dot and `\W`).
  - Getter `flags`.
  - Can subclass `RegExp`, and `RegExp.prototype[Symbol.match/replace/search/split]` for use in subclasses.
  - Use `RegExp` to copy a regex, optionally with new flags.
- ES2018 added [flag `/s`](https://github.com/tc39/proposal-regexp-dotall-flag) (`dotAll`), [lookbehind](https://github.com/tc39/proposal-regexp-lookbehind), [named capture](https://github.com/tc39/proposal-regexp-named-groups), and [Unicode properties](https://github.com/tc39/proposal-regexp-unicode-property-escapes) via `\p{…}` and `\P{…}` behind flag `/u` (see [property list](https://github.com/mathiasbynens/regexpu-core/blob/main/property-escapes.md)).
- ES2020 added string method [`matchAll`](https://github.com/tc39/proposal-string-matchall) (which returns an iterator) and `RegExp.prototype[Symbol.matchAll]`.
- ES2021 added [`replaceAll`](https://github.com/tc39/proposal-string-replaceall).
- ES2022 added [flag `/d`](https://github.com/tc39/proposal-regexp-match-indices) (`hasIndices`), which provides start/end indices for matched substrings.
- ES2024 added [flag `/v`](https://github.com/tc39/proposal-regexp-v-flag) (`unicodeSets`) [[*explainer*](https://v8.dev/features/regexp-v-flag)] as an upgrade to flag `/u` (can't be used together); adds properties of *strings* to `\p{…}`, multicharacter elements within character classes via `\p{…}` and `\q{…|…}`, nested character classes, set operators `[…--…]` and `[…&&…]`, improved case-insensitive matching, and different escaping rules within character classes.

See also: Backcompat libraries: [regexpu](https://github.com/mathiasbynens/regexpu), [regenerate](https://github.com/mathiasbynens/regenerate).

### Future: Active proposals

*Learn about regex features potentially coming to future JavaScript versions.*

- [Duplicate named capturing groups](https://github.com/tc39/proposal-duplicate-named-capturing-groups) [2022] — `(?<a>…)|(?<a>…)`.
- [Extended mode and comments](https://github.com/tc39/proposal-regexp-x-mode) [2021] — Flag `/x` (`extended`) with insignificant whitespace and line comments `#…`, inline comments `(?#…)`.
- [Pattern modifiers](https://github.com/tc39/proposal-regexp-modifiers) [2021] — `(?imsx-imsx:…)`.
- [Atomic operators](https://github.com/tc39/proposal-regexp-atomic-operators) [2021] — Atomic groups `(?>…)` and possessive quantifiers (ex: `*+`, `++`).
- [Buffer boundaries](https://github.com/tc39/proposal-regexp-buffer-boundaries) [2021] — `\A` and `\z`, not affected by flag `/m`.
- [\R escape](https://github.com/tc39/proposal-regexp-r-escape) [2021] — `\R` for any line terminator.
- [RegExp escaping](https://github.com/tc39/proposal-regex-escaping) [2015] — `RegExp.escape`.
- [Legacy RegExp features](https://github.com/tc39/proposal-regexp-legacy-features) [2015] — Standardization of legacy features.

See also: Chrome’s `/l` (`linear`) flag, behind a V8 flag [[*explainer*](https://v8.dev/blog/non-backtracking-regexp)] [[*how to run*](https://www.chromium.org/developers/how-tos/run-chromium-with-flags/)].

## Books

*Curated list of regex books.*

- [*Regular Expressions Cookbook, 2nd Edition*](https://www.amazon.com/dp/1449319432/?tag=slev-20) [2012], by Jan Goyvaerts, Steven Levithan.
- [*Mastering Regular Expressions, 3rd Edition*](https://www.amazon.com/dp/0596528124/?tag=slev-20) [2006], by Jeffrey Friedl.

More: [*Regular Expression Puzzles and AI Coding Assistants*](https://www.amazon.com/dp/1633437817/?tag=slev-20) [2023], [*Regular Expression Pocket Reference, 2nd Edition*](https://www.amazon.com/dp/0596514271/?tag=slev-20) [2007], [*Mastering Python Regular Expressions*](https://www.amazon.com/dp/1783283157/?tag=slev-20) [2014], [*Introducing Regular Expressions*](https://www.amazon.com/dp/1449392687/?tag=slev-20) [2012], [*Learning Regular Expressions*](https://www.amazon.com/dp/0134757068/?tag=slev-20) [2018], [*Regex Quick Syntax Reference*](https://www.amazon.com/dp/1484238753/?tag=slev-20) [2018], [*Regular Expressions: Pocket Primer*](https://www.amazon.com/dp/1683922271/?tag=slev-20) [2018], [*Sams Teach Yourself Regular Expressions in 10 Minutes*](https://www.amazon.com/dp/0672325667/?tag=slev-20) [2004].

## Articles

*Curated list of regex articles.*

- [*The World's Shortest Regex Compiler?*](https://jasonhpriestley.com/regex) and a [follow up](https://jasonhpriestley.com/regex-dfa) on optimization, by Jason H Priestley.

## Communities

*Discuss, assist, and get help with regular expressions.*

- [Reddit: /r/regex](https://www.reddit.com/r/regex/).
- [Stack Overflow: [regex]](https://stackoverflow.com/questions/tagged/regex?tab=Votes).

## Miscelaneous

*Other interesting, fun, and useful stuff.*

- Chrome extension: [Regex](https://chromewebstore.google.com/detail/regex/pmihaiejckejbpjdnildimfkpcpnohlo) — Regex search on webpages via `Ctrl+Shift+F`.
- Games: [Regex Crossword](https://regexcrossword.com/), [Redoku](https://padolsey.github.io/redoku/).
