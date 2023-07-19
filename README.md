# Chili Flutter Analysis

## Static code analysis rules used in Chili projects

### Installing:

Add `chili_flutter_analysis library` to your `dev_dependencies`:

```
dev_dependencies:
  chili_flutter_analysis:
    git:
      url: https://github.com/ChiliLabs/chili-flutter-analysis.git
      ref: 1.0.0
```

### Running the analyzer

Switch to root directory where your `pubspec.yaml` is located and execute this command in terminal:

```
dart run dart_code_metrics:metrics analyze lib
```
