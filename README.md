# solutelabs_lint
 A set of lint rules to follow for coding standard
## Usage

To use the lints, add a dependency in your `pubspec.yaml`:

```yaml
dev_dependencies:
  solutelabs_lint:
    git:
      url: https://github.com/solutelabs/solutelabs_lint
      ref: dev
```
Then, add an include in `analysis_options.yaml`:

```yaml
include: package:solutelabs_lint/analysis_options.yaml
```

## Suppressing Lints

There may be cases where specific lint rules are undesirable. Lint rules can be surpressed at the line, file, or project level.

### Line Level

To surpress a specific lint rule for a specific line of code, use an `ignore` comment directly above the line:

```dart
// ignore: public_member_api_docs
class A {}
```

### File Level

To surpress a specific lint rule of a specific file, use an `ignore_for_file` comment at the top of the file:

```dart
// ignore_for_file: public_member_api_docs

class A {}

class B {}
```

### Project Level

To surpress a specific lint rule for an entire project, modify `analysis_options.yaml`:

```yaml
include: package:solutelabs_lint/analysis_options.yaml
linter:
  rules:
    public_member_api_docs: false
```
