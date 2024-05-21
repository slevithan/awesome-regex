<!--lint ignore awesome-heading-->
<div align="center">

[![Awesome Regex](media/awesome-regex-banner.svg)](https://github.com/slevithan/awesome-regex)

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re) &nbsp;<sup>Shortcut URL: [`regex.cool`](https://regex.cool/)</sup>
</div>

Awesome Regex curates the best regular expression tools, tutorials, libraries, and other resources. It covers all major regex flavors, and currently includes especially deep coverage of regular expressions in JavaScript.

> Regular expressions (regex or regexp) are a powerful and concise way to search, parse, and process text. They're built into many programming languages, text editors, IDEs, database engines, word processors, and other tools.

Contributions are welcome. Add links through pull requests ([guidelines](CONTRIBUTING.md)) or create an issue to start a discussion.

<details>
  <summary>📖 <b>Glossary</b></summary>
  <br>

*A brief glossary of regular expression terms as used in this list.*

- **Regex engine:** Software that parses and executes regular expressions, either built into a programming language or as a standalone library (synonym: implementation).
- **Regex flavor:** A unique set of regex syntax and behavior. Basic syntax is typically shared across flavors, but more advanced features often vary, sometimes in subtle or incompatible ways. A flavor might be shared across multiple implementations or programming languages.
  - Ex: The “JavaScript” flavor is defined by the ECMAScript spec; implemented by multiple engines (V8, etc.).
  - Ex: The “PCRE” flavor is the PCRE2 library, used by numerous programming languages and tools.
  - Ex: Ruby swapped its regex implementation twice from version 1.8 ➜ 1.9 ➜ 2.0, so each used a distinct flavor. The Ruby 2.0+ flavor is referred to here as either “Ruby” or “Onigmo” (the underlying regex library).
- **Non-backtracking engine:** Sometimes referred to elsewhere as a “DFA” engine. Non-backtracking engines like RE2 and Rust's `regex` run in linear time because they don't use backtracking. This rules out worst case performance from superlinear backtracking, but it's slower with some patterns and precludes some useful features like backreferences.
</details>

## Contents

- [Testers](#testers)
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
- [Books](#books)
- [Articles](#articles)
- [Communities](#communities)
- [Miscelaneous](#miscelaneous)

## Testers

*For building, testing, and playing with regexes.*

- [regex101](https://regex101.com/) - **Best free and best web-based tester**.
  - Flavors: Java, JavaScript, .NET, PCRE, RE2, Rust, and emulates Python.
  - Includes regex debugger (PCRE only).
- [RegexBuddy](https://www.regexbuddy.com/) (<picture><img src="https://github.com/slevithan/awesome-regex/raw/main/media/windows.svg" title="Windows" height="13"></picture>, $40) - **Best tester**.
  - Flavors: Emulates hundreds of flavors/versions, with deep knowledge of differences.
  - Includes regex debugger.
- [RegExr](https://regexr.com/) [[*GitHub*](https://github.com/gskinner/regexr/)] - **Best open source tester**.
  - Flavors: JavaScript, PCRE.
  - Languages: 🇺🇸, 🇨🇳 ([fork](https://regexr-cn.com/)).
- [RegexLearn](https://regexlearn.com/playground) [[*GitHub*](https://github.com/aykutkardas/regexlearn.com/blob/develop/src/pages/%5Blang%5D/playground.tsx)] - **Best multilingual tester** (JavaScript).
  - Languages: 🇺🇸, 🇹🇷, 🇷🇺, 🇪🇸, 🇨🇳, 🇩🇪, 🇺🇦, 🇫🇷, 🇵🇱, 🇰🇷, 🇧🇷, 🇨🇿, 🇬🇪.
- [regexplained](https://regexplained.com/) [[*GitHub*](https://github.com/LeaVerou/regexplained)] - **Best tester for presentations** (JavaScript).

<details>
  <summary>✳️ <b>Notable mentions</b></summary>
  <br>

**Flavors**

- JavaScript: [RegViz](http://regviz.org/).
- .NET: [Regex Storm](http://regexstorm.net/tester) [[*GitHub*](https://github.com/lonekorean/regex-storm)].
- PCRE: [PHP Live Regex](https://www.phpliveregex.com/).
- Python: [Pythex](https://pythex.org/).
- Ruby: [Rubular](https://rubular.com/).

**Multiple flavors**

- [CyrilEx](https://extendsclass.com/regex-tester.html) [[*GitHub*](https://github.com/cyrilbois/cyrilex)] - Java, JavaScript, MySQL, PHP, Python, Ruby.
- [Patterns](https://krillapps.com/patterns/) (<picture><img src="https://github.com/slevithan/awesome-regex/raw/main/media/macos.svg" title="macOS" height="13"></picture>, $3) - Bash, Emacs, grep, Java, Oniguruma, PCRE, POSIX BRE, POSIX ERE, Ruby, sed.
- [RegexPlanet](https://www.regexplanet.com/) [[*GitHub*](https://github.com/regexplanet)] - Go, Haskell, Java, JavaScript, .NET, Perl, PHP, PostgreSQL, Python, Ruby, Tcl, XRegExp.
</details>

## Syntax-free regex builders

*Build regexes without writing regex syntax or code.*

- [ChatGPT](https://chat.openai.com/) (and other LLMs) - Ex: *"create a regex that matches `X` and explain it step by step"*.
- [RegexMagic](https://www.regexmagic.com/) (<picture><img src="https://github.com/slevithan/awesome-regex/raw/main/media/windows.svg" title="Windows" height="13"></picture>, $40) - Generate regexes using samples and rules.
  - Flavors: Emulates hundreds of flavors/versions.

<details>
  <summary>✳️ <b>Notable mentions</b></summary>
  <br>

- [Regex Generator](https://regex-generator.olafneumann.org/) [[*GitHub*](https://github.com/noxone/regex-generator)] - Generate simple regexes from a sample text.
- [Regex.ai](https://regex.ai/) - Mark samples in a text and use AI to generate potential regexes.
</details>

## Visualizers

*Visualize how your regular expressions are structured or operate.*

- [Regex Vis](https://regex-vis.com/) [[*GitHub*](https://github.com/Bowen7/regex-vis)] - Create railroad diagrams, with visual editor. Flavor: JavaScript.
  - Languages: 🇺🇸, 🇨🇳.
- [Regulex](https://jex.im/regulex/) [[*GitHub*](https://github.com/CJex/regulex)] - Create railroad diagrams. Flavor: JavaScript.
- [Nodexr](https://www.nodexr.net/) [[*GitHub*](https://github.com/Jcparkyn/nodexr)] - Graphical editor with visual hierarchy. Flavor: .NET.

<details>
  <summary>✳️ <b>Notable mentions</b></summary>
  <br>

- [Regex Nodes](https://johannesvollmer.com/regex-nodes/) [[*GitHub*](https://github.com/johannesvollmer/regex-nodes)] - Graphical editor with visual hierarchy. Flavor: JavaScript.
- [Debuggex](https://www.debuggex.com/) - Create railroad diagrams. Flavors: JavaScript, PCRE, Python.
- [RegExper](https://regexper.com/) [[*GitLab*](https://gitlab.com/javallone/regexper-static)] - Create railroad diagrams. Flavor: JavaScript.
</details>

## Search and replace through files

*Grep-like software.*

**Command line**

- [ripgrep](https://github.com/BurntSushi/ripgrep) - Better and faster grep. Recursively searches directories while respecting gitignore rules and skipping hidden/binary files.
  - Flavors: Rust (default), PCRE.

➕ **See also:** [Feature comparison of grep-like tools](https://beyondgrep.com/feature-comparison/).

**GUI**

- [Aba Search and Replace](https://www.abareplace.com/) (<picture><img src="https://github.com/slevithan/awesome-regex/raw/main/media/windows.svg" title="Windows" height="13"></picture>, $30) - Displays matches as you type.
- [PowerGREP](https://www.powergrep.com/) (<picture><img src="https://github.com/slevithan/awesome-regex/raw/main/media/windows.svg" title="Windows" height="13"></picture>, $159) - Can search through archives, binary files, PDFs, docs/sheets, emails, etc., via its GUI or the command line.
  - Flavors: Emulates hundreds of flavors/versions.
- [RegexRenamer](https://regexrenamer.sourceforge.net/) (<picture><img src="https://github.com/slevithan/awesome-regex/raw/main/media/windows.svg" title="Windows" height="13"></picture>) - Rename files using regexes.

## Tutorials

*Learn how to use regular expressions.*

**Traditional**

- [Regular-Expressions.info](https://www.regular-expressions.info/) - Covers numerous regex flavors.
- [The Modern JavaScript Tutorial: Regular expressions](https://javascript.info/regular-expressions) [[*GitHub*](https://github.com/javascript-tutorial/en.javascript.info)] - Guide to using regexes in modern JavaScript.
  - Languages: 🇺🇸, 🇪🇸, 🇫🇷, 🇮🇹, 🇯🇵, 🇷🇺, 🇺🇦, 🇨🇳 (partial for [others](https://javascript.info/translate)).

**With interactive exercises**

- [RegexLearn](https://regexlearn.com/) [[*GitHub*](https://github.com/aykutkardas/regexlearn.com)] - Interactive tutorial and practice problems.
  - Languages: 🇺🇸, 🇹🇷, 🇷🇺, 🇪🇸, 🇨🇳, 🇩🇪, 🇺🇦, 🇫🇷, 🇵🇱, 🇰🇷, 🇧🇷, 🇨🇿, 🇬🇪.
- [RegexOne](https://regexone.com/) - Interactive tutorial and practice problems.
</details>

<details>
  <summary>✳️ <b>Notable mentions</b></summary>
  <br>

- [RexEgg](https://rexegg.com/) - Detailed tutorial with advanced topics.
- [learnbyexample](https://learnbyexample.github.io/books/) [[*GitHub*](https://github.com/learnbyexample)] - Ebooks on regexes ([JavaScript](https://learnbyexample.github.io/learn_js_regexp/), [Python](https://learnbyexample.github.io/py_regular_expressions/), [Ruby](https://learnbyexample.github.io/Ruby_Regexp/)) and command line text processing.
- [Regular Expressions for Regular Folk](https://refrf.dev/) [[*GitHub*](https://github.com/shreyasminocha/regex-for-regular-folk)] - Visual, example-based ebook for beginners.
- [regex101: Regex Quiz](https://regex101.com/quiz) - Exercises only. Requires sign-in.
</details>

### Videos

*Regex video tutorials.*

- [*Demystifying Regular Expressions*](https://www.youtube.com/watch?v=M7vDtxaD7ZU) - Great presentation for beginners, by Lea Verou at HolyJS 2017 (1hr 12m).
- [*Learn Regular Expressions In 20 Minutes*](https://www.youtube.com/watch?v=rhzKDrUiJVk) - Live syntax walkthrough in a regex tester, by Kyle Cook.
- Many options for video courses are available on [Udemy](https://www.udemy.com/topic/regular-expressions/) ($).

## Regex engines

*Major regex implementations, built into programming languages or as standalone libraries.*

### Documentation

*Official regex references and guides.*

**Regex flavors**

- JavaScript (MDN): [RegExp](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp), [Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Regular_expressions), [Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions).
- Boost.Regex: [Manual](https://boost.org/libs/regex).
- C++: [Regular expressions library](https://en.cppreference.com/w/cpp/regex).
- Hyperscan: [Introduction](https://www.hyperscan.io/).
- ICU: [Regular Expressions](https://unicode-org.github.io/icu/userguide/strings/regexp.html).
- Java: [Pattern](https://docs.oracle.com/en/java/javase/22/docs/api/java.base/java/util/regex/Pattern.html), [API](https://docs.oracle.com/en/java/javase/22/docs/api/java.base/java/util/regex/package-summary.html).
- .NET: [Overview](https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions), [Language](https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference), [API](https://learn.microsoft.com/en-us/dotnet/api/system.text.regularexpressions).
- Onigmo: [RE](https://github.com/k-takata/Onigmo/blob/master/doc/RE).
- PCRE: [pcre2pattern](https://pcre2project.github.io/pcre2/doc/html/pcre2pattern.html), [API](https://pcre2project.github.io/pcre2/doc/html/).
- Perl: [Syntax](https://perldoc.perl.org/perlre), [Tutorial](https://perldoc.perl.org/perlretut), [Quick Start](https://perldoc.perl.org/perlrequick).
- Python: [re](https://docs.python.org/library/re.html).
- RE2: [Syntax](https://github.com/google/re2/wiki/Syntax).
- Rust: [regex](https://docs.rs/regex/latest/regex/), [regex_lite](https://docs.rs/regex-lite/latest/regex_lite/).

ℹ️ Raku (formerly Perl 6) reimagines regexes. See: [Grammars](https://docs.raku.org/language/grammars) ([tutorial](https://docs.raku.org/language/grammar_tutorial)), [Regexes](https://docs.raku.org/language/regexes) ([best practices](https://docs.raku.org/language/regexes-best-practices)).

**Without own flavor**

- MySQL: [Regular Expressions](https://dev.mysql.com/doc/refman/en/regexp.html) - Flavor: ICU.
- PHP: [Regular Expressions](https://www.php.net/manual/en/book.pcre.php) - Flavor: PCRE.
- Ruby: [Regexp](https://docs.ruby-lang.org/en/master/Regexp.html) - Flavor: Onigmo.
- Swift: [NSRegularExpression](https://developer.apple.com/documentation/foundation/nsregularexpression) - Flavor: ICU.

### Source code

*Read or contribute to the code behind major regex implementations.*

- [V8: Irregexp](https://github.com/v8/v8/tree/main/src/regexp) - JavaScript `RegExp` engine used by Chrome, etc.
- [Boost.Regex](https://github.com/boostorg/regex) - Popular C++ regex library.
- [Hyperscan](https://github.com/intel/hyperscan) - Intel's high-performance library, used for [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection).
- [ICU](https://github.com/unicode-org/icu/blob/main/icu4c/source/i18n/unicode/regex.h) - Unicode org's package with full Unicode support.
- [Java: java.util.regex](https://github.com/openjdk/jdk/tree/master/src/java.base/share/classes/java/util/regex) - JDK standard regexes.
- [.NET: System.Text.RegularExpressions](https://github.com/dotnet/runtime/tree/main/src/libraries/System.Text.RegularExpressions) - Shared by all .NET languages (C#, VB, etc.).
- [Onigmo](https://github.com/k-takata/Onigmo) - Forked and extended from Oniguruma. Default regex library of Ruby 2.0+.
- [Oniguruma](https://github.com/kkos/oniguruma) - Popular C regex library. Default regex library of Ruby 1.9.
- [PCRE2](https://github.com/PCRE2Project/pcre2) - Popular C regex library used by PHP, R, etc.
- [Perl](https://github.com/Perl/perl5/blob/blead/regexp.h) - See [perlreguts](https://perldoc.perl.org/perlreguts).
- [Python: re](https://github.com/python/cpython/tree/main/Lib/re) and [regex](https://github.com/mrabarnett/mrab-regex) - Standard and extended regex libraries.
- [RE2](https://github.com/google/re2) - Popular C++ regex library used by Go, etc. Non-backtracking engine.
- [Rust: regex](https://github.com/rust-lang/regex) - Non-backtracking engine.

### Flavor differences

*Syntax and behavior differences between regex flavors.*

- Ron Buckton: [Regular Expression Feature Comparisons](https://rbuckton.github.io/regexp-features/) [[*GitHub*](https://github.com/rbuckton/regexp-features)].
- Regular-Expressions.info: [Tools & Languages](https://www.regular-expressions.info/tools.html).
- Steven Levithan: [Named capture](https://xregexp.com/syntax/named_capture_comparison/), [Lookbehind](https://stevenlevithan.com/regex/tests/lookbehind.html).
- Wikipedia: [Comparison of regular expression engines](https://en.wikipedia.org/wiki/Comparison_of_regular_expression_engines).

## Performance

*Pattern and engine performance, benchmarks, and [ReDoS](https://en.wikipedia.org/wiki/ReDoS) prevention.*

**Crafting efficient regexes**

- [Runaway Regular Expressions: Catastrophic Backtracking](https://www.regular-expressions.info/catastrophic.html) - Exploration and solutions for superlinear backtracking.
- [Book: High Performance JavaScript](https://www.amazon.com/dp/059680279X/?tag=slev-20) (2010) - *Chapter 5: Strings and Regular Expressions*.
- [Book: Mastering Regular Expressions, 3rd Edition](https://www.amazon.com/Mastering-Regular-Expressions-Jeffrey-Friedl/dp/0596528124/?tag=slev-20) (2006) - *Chapter 6: Crafting an Efficient Expression*.
- [Performance of Greedy vs. Lazy Regex Quantifiers](https://blog.stevenlevithan.com/archives/greedy-lazy-performance) - Illustrates the mechanics of backtracking.

ℹ️ With backtracking engines, how you craft a regex can affect how fast it finds matches or reports failures.

**Regex engine optimizations**

- [Regular Expression Matching Can Be Simple And Fast](https://swtch.com/~rsc/regexp/regexp1.html) - On non-backtracking engines. A [follow up](https://swtch.com/~rsc/regexp/regexp3.html) includes comparisons of RE2 and PCRE performance.
- [Regular Expression Improvements in .NET 7](https://devblogs.microsoft.com/dotnet/regular-expression-improvements-in-dotnet-7/) and [.NET 5](https://devblogs.microsoft.com/dotnet/regex-performance-improvements-in-net-5/) - Includes detailed explanations of performance optimizations.
- [ripgrep is faster than {grep, …}](https://blog.burntsushi.net/ripgrep/) - Includes details about what makes ripgrep and Rust's `regex` fast.

**Benchmarking**

- Libraries for cross-engine benchmarking: [rebar](https://github.com/BurntSushi/rebar), [regex-benchmark](https://github.com/mariomka/regex-benchmark), [sljit/regex_perf.html](https://zherczeg.github.io/sljit/regex_perf.html).
- [Boost.Regex: Performance](https://www.boost.org/doc/libs/release/libs/regex/doc/html/boost_regex/background/performance.html) - Compares Boost, C++'s `std::regex`, and others.

**ReDoS checkers**

- [recheck](https://github.com/makenowjust-labs/recheck) [[*home*](https://makenowjust-labs.github.io/recheck/)] - JavaScript and Scala library for detecting ReDoS vulnerability. Can be used as an ESLint plugin.
- [vuln-regex-detector](https://github.com/davisjam/vuln-regex-detector) - Perl library for detecting ReDoS vulnerability.

## Collections of patterns

*Prewritten regexes for specific tasks.*

- [Book: Regular Expressions Cookbook, 2nd Edition](https://www.amazon.com/Regular-Expressions-Cookbook-Solutions-Programming/dp/1449319432/?tag=slev-20) (2012) - High-quality solutions with detailed explanations.
  - Flavors: Java, JavaScript, .NET, PCRE, Perl, Python, Ruby, XRegExp.
- [Regex DB](https://rgxdb.com/) - Solutions include basic descriptions and examples of matching and non-matching text.

<details>
  <summary>⚠️ <b>Word of warning</b></summary>
  <br>

Many regexes found online are low quality. It's risky to use regexes you don't fully understand in code, since they might have false positives/negatives, be vulnerable to performance problems with certain target strings, or assume a different regex flavor.
</details>

## JavaScript regex libraries

*Open source JavaScript libraries for advanced regex use and processing.*

**Regex processors**

- AST builders: [regexpp](https://github.com/eslint-community/regexpp) (used by ESLint), [regexp-tree](https://github.com/DmitrySoshnikov/regexp-tree) (includes optimizer, etc.), [regjsparser](https://github.com/jviereck/regjsparser)/[regjsgen](https://github.com/bnjmnt4n/regjsgen).
  - [AST Explorer: RegExp](https://astexplorer.net/#/gist/56d33dc28d07c7f57bdf5ca0f4061320/c6b67a829334151af01ba55960c653e4462df437) - View ASTs generated by regexp-tree, regexpp, and regjsparser.
  - [regexp-ast-analysis](https://github.com/RunDevelopment/regexp-ast-analysis) [[*docs*](https://rundevelopment.github.io/regexp-ast-analysis/docs/latest/)] - Analyze AST nodes produced by regexpp.
- Generate strings that match a given regex: [randexp.js](https://github.com/fent/randexp.js), [regex-to-strings](https://github.com/wimpyprogrammer/regex-to-strings).
- Generate a regex from given strings: [regexgen](https://github.com/devongovett/regexgen).
- Highlight regex syntax: [Regex Colorizer](https://github.com/slevithan/regex-colorizer) [[*home*](https://slevithan.github.io/regex-colorizer/demo/)], [CodeMirror PCRE mode](https://github.com/xavierog/codemirror-mode-pcre).
- Find regex mistakes and improvements: [eslint-plugin-regexp](https://github.com/ota-meshi/eslint-plugin-regexp) [[*home*](https://ota-meshi.github.io/eslint-plugin-regexp/)], [eslint-plugin-optimize-regex](https://github.com/BrainMaestro/eslint-plugin-optimize-regex).

**Alternative regex builders and engines**

- [XRegExp](https://github.com/slevithan/xregexp) [[*home*](https://xregexp.com/)] - Extended regex syntax, flags, and utils.
- String template tags: [regexp-make-js](https://github.com/mikesamuel/regexp-make-js), [`XRegExp.tag`](https://github.com/slevithan/xregexp?tab=readme-ov-file#xregexptag-included-with-xregexpbuild).
- [incr-regex-package](https://github.com/nurulc/incr-regex-package) - Partial/incremental matching, used by [react-rxinput](https://github.com/nurulc/react-rxinput) for input validation with a regex mask.
- [@iter-tools/regex](https://github.com/iter-tools/regex) - Non-backtracking engine for streaming evaluation.

**Readable regex composers**

- [Rexx](https://github.com/yyytcool/rexx) - Structured syntax with variables and comments.
- [compose-regexp.js](https://github.com/compose-regexp/compose-regexp.js) - Compose with functions. Includes extra regex features like `atomic`, `bound`.
- More: [VerbalExpressions](https://github.com/VerbalExpressions/JSVerbalExpressions) (has implementations for [many languages](https://verbalexpressions.github.io/)), [magic-regexp](https://github.com/unjs/magic-regexp) [[*home*](https://regexp.dev/)], [Super Expressive](https://github.com/francisrstokes/super-expressive) [[*playground*](https://nartc.github.io/ng-super-expressive/)], [Melody](https://github.com/yoav-lavi/melody) [[*docs*](https://yoav-lavi.github.io/melody/book/)].

## JavaScript regex evolution

*A concise history of improvements to regular expressions in the JavaScript [standard](https://tc39.es/ecma262/), with links to the [TC39](https://tc39.es/) proposals where features were developed and discussed.*

- ES3 (1999) introduced powerful regular expressions, though limited compared to other major flavors.
- ES5 (2009) fixed unintuitive behavior by creating a new object every time regex literals are evaluated [[*explainer*](https://whereswalden.com/2010/01/15/more-es5-incompatible-changes-regular-expressions-now-evaluate-to-a-new-object-not-the-same-object-each-time-theyre-encountered/)], and allowed regex literals to use unescaped forward slashes within character clases (`/[/]/`).
- ES6/ES2015 added: [[*explainer*](https://2ality.com/2015/07/regexp-es6.html)]
  - Flag `y` (`sticky`), which anchors matches to `lastIndex`.
  - Flag `u` (`unicode`) [[*explainer*](https://mathiasbynens.be/notes/es6-unicode-regex)] [[*2016 spec fix*](https://github.com/tc39/ecma262/pull/525)], which adds Unicode code point escapes via `\u{…}`, errors for unreserved letter escapes, impact on flag `i`, and surrogate pairs as code points (with impact on quantifiers, character classes, character class ranges, and built-in sets like `.` and `\W`).
  - Getter `RegExp.prototype.flags`.
  - Can subclass `RegExp`, plus `RegExp.prototype[Symbol.match`/`replace`/`search`/`split]` and `RegExp[Symbol.species]` for use in subclasses.
  - Use `RegExp` to copy a regex, optionally with new flags.
- ES2018 added [flag `s`](https://github.com/tc39/proposal-regexp-dotall-flag) (`dotAll`), [lookbehind](https://github.com/tc39/proposal-regexp-lookbehind), [named capture](https://github.com/tc39/proposal-regexp-named-groups), and [Unicode properties](https://github.com/tc39/proposal-regexp-unicode-property-escapes) via `\p{…}` and `\P{…}` behind flag `u` (see [list](https://github.com/mathiasbynens/regexpu-core/blob/main/property-escapes.md)).
- ES2020 added string method [`matchAll`](https://github.com/tc39/proposal-string-matchall) (which returns an iterator), plus `RegExp.prototype[Symbol.matchAll]`.
- ES2021 added [`replaceAll`](https://github.com/tc39/proposal-string-replaceall).
- ES2022 added [flag `d`](https://github.com/tc39/proposal-regexp-match-indices) (`hasIndices`), which provides start/end indices for matched substrings.
- ES2024 added [flag `v`](https://github.com/tc39/proposal-regexp-v-flag) (`unicodeSets`) [[*explainer*](https://v8.dev/features/regexp-v-flag)] as an upgrade to flag `u` (can't be used together), which adds a set of multicharacter "properties of strings" to `\p{…}`, multicharacter elements within character classes via `\p{…}` and `\q{…|…}`, nested character classes, set operators `[…--…]` and `[…&&…]`, improved case-insensitive matching, and different escaping rules within character classes.

> ES2019, ES2020, ES2021, ES2022, and ES2023 each added additional Unicode properties that can be used via `\p{…}` and `\P{…}` (see [lists](https://github.com/eslint-community/regexpp/blob/main/src/unicode/properties.ts)).

<details>
  <summary>➕ <b>See also</b></summary>
  <br>

- Backcompat libraries: [regexpu](https://github.com/mathiasbynens/regexpu), [regenerate](https://github.com/mathiasbynens/regenerate) ([Unicode property sets](https://github.com/mathiasbynens/regenerate-unicode-properties)).
- Chrome's `l` (`linear`) regex flag, behind a V8 flag [[*explainer*](https://v8.dev/blog/non-backtracking-regexp)] [[*how to run*](https://www.chromium.org/developers/how-tos/run-chromium-with-flags/)].
- [Can I use](https://caniuse.com/) - Up-to-date browser support tables for individual features.
</details>

<details>
  <summary>🔮 <b>Future: Active proposals</b></summary>
  <br>

- [Duplicate named capturing groups](https://github.com/tc39/proposal-duplicate-named-capturing-groups) (2022) - Ex: `(?<a>…)|(?<a>…)`.
- [Extended mode and comments](https://github.com/tc39/proposal-regexp-x-mode) (2021) - Flag `x` (`extended`) with insignificant whitespace and line comments (`#…`), plus inline comments via `(?#…)`.
- [Pattern modifiers](https://github.com/tc39/proposal-regexp-modifiers) (2021) - Ex: `(?imsx-imsx:…)`.
- [Atomic operators](https://github.com/tc39/proposal-regexp-atomic-operators) (2021) - Atomic groups via `(?>…)` and possessive quantifiers (ex: `*+`, `++`).
- [Buffer boundaries](https://github.com/tc39/proposal-regexp-buffer-boundaries) (2021) - Anchors `\A` and `\z`, not affected by flag `m`.
- [\R escape](https://github.com/tc39/proposal-regexp-r-escape) (2021) - Outside character classes, `\R` matches any line terminator.
- [Restrict subclassing support in built-ins](https://github.com/tc39/proposal-rm-builtin-subclassing) (2020) - Scaled back `RegExp` subclassing.
- [RegExp escaping](https://github.com/tc39/proposal-regex-escaping) (2015) - `RegExp.escape`.
- [Legacy RegExp features](https://github.com/tc39/proposal-regexp-legacy-features) (2015) - Standardization of legacy features.
</details>

## Books

*A curated list of regex books.*

- [*Regular Expressions Cookbook, 2nd Edition*](https://www.amazon.com/dp/1449319432/?tag=slev-20) (2012) by Jan Goyvaerts and Steven Levithan - Regex tutorial with code samples for eight programming languages, 100+ regex recipes for practical problems, and a deep focus on cross-flavor differences.
  - Flavors: Java, JavaScript, .NET, PCRE, Perl, Python, Ruby, XRegExp.
- [*Mastering Regular Expressions, 3rd Edition*](https://www.amazon.com/dp/0596528124/?tag=slev-20) (2006) by Jeffrey Friedl - A computer science classic, best for people who already know the basics. Includes good coverage of crafting efficient regexes.
  - Flavors: Dedicated chapters on Java, .NET, Perl, and PHP (PCRE), with more limited coverage of Python, Tcl, command line tools, etc.
- [*Introducing Regular Expressions*](https://www.amazon.com/dp/1449392687/?tag=slev-20) (2012) by Michael Fitzgerald - An intro for programmers new to regular expressions that sticks to the basics.

## Articles

*A curated list of regex articles.*

- [*The World's Shortest Regex Compiler?*](https://jasonhpriestley.com/regex) and a [follow up](https://jasonhpriestley.com/regex-dfa) on optimization - Introduction to writing a non-backtracking regex engine (in JavaScript).
- [*Regex Legends: The People Behind the Magic*](https://blog.stevenlevithan.com/archives/regex-legends) - Influential people behind the technology.
- [*Fun With .NET Regex Balancing Groups*](https://blog.stevenlevithan.com/archives/balancing-groups) - Advanced usage of a .NET-only regex feature.

## Communities

*Discuss, assist, and get help with regular expressions.*

- [Reddit: r/regex](https://www.reddit.com/r/regex/)
- [Stack Overflow: [regex]](https://stackoverflow.com/questions/tagged/regex?tab=Votes)

## Miscelaneous

*Other interesting, fun, and useful stuff.*

- Chrome extension: [Regex](https://chromewebstore.google.com/detail/regex/pmihaiejckejbpjdnildimfkpcpnohlo) - Regex search on webpages via `Ctrl+Shift+F`.
- Games: [Regex Crossword](https://regexcrossword.com/), [Redoku](https://padolsey.github.io/redoku/).
- Comics: [xkcd](https://xkcd.com/208/), [Garabato Kid](https://twitter.com/garabatokid/status/1147063121678389253).
