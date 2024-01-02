# 1.2.1
#### Dart:
- **feat:** additional lint rules:
  - [unnecessary_breaks](https://dart.dev/tools/linter-rules/unnecessary_breaks)
  - [use_rethrow_when_possible](https://dart.dev/tools/linter-rules/use_rethrow_when_possible)
  - [use_string_in_part_of_directives](https://dart.dev/tools/linter-rules/use_string_in_part_of_directives)
  - [constant_identifier_names](https://dart.dev/tools/linter-rules/constant_identifier_names)
  - [use_super_parameters](https://dart.dev/tools/linter-rules/use_super_parameters)

#### DCM:
- **refactor:** remove redundant lint rule `prefer-declaring-const-constructors`
- **refactor** set `ignore-single-boolean` to `true` for `prefer-named-boolean-parameters` lint rule

- **feat:** additional lint rules:
  #### Common:
  - [avoid-referencing-discarded-variables](https://dcm.dev/docs/rules/common/avoid-referencing-discarded-variables/)
  - [avoid-unconditional-break](https://dcm.dev/docs/rules/common/avoid-unconditional-break/)
  - [avoid-weak-cryptographic-algorithms](https://dcm.dev/docs/rules/common/avoid-weak-cryptographic-algorithms/)
  - [avoid-identical-exception-handling-blocks](https://dcm.dev/docs/rules/common/avoid-identical-exception-handling-blocks/)
  - [avoid-recursive-calls](https://dcm.dev/docs/rules/common/avoid-recursive-calls/)
  - [move-variable-closer-to-its-usage](https://dcm.dev/docs/rules/common/move-variable-closer-to-its-usage/)
  - [avoid-missing-interpolation](https://dcm.dev/docs/rules/common/avoid-missing-interpolation/)
  - [avoid-unnecessary-if](https://dcm.dev/docs/rules/common/avoid-unnecessary-if/)
  - [avoid-passing-default-values](https://dcm.dev/docs/rules/common/avoid-passing-default-values/)
  - [avoid-passing-self-as-argument](https://dcm.dev/docs/rules/common/avoid-passing-self-as-argument/)
  - [prefer-trailing-comma](https://dcm.dev/docs/rules/common/prefer-trailing-comma/)

# 1.2.0

#### Dart:
- **feat:** additional lint rules:
  - [avoid_function_literals_in_foreach_calls](https://dart.dev/tools/linter-rules/avoid_function_literals_in_foreach_calls)
  - [prefer_expression_function_bodies](https://dart.dev/tools/linter-rules/prefer_expression_function_bodies)
  - [eol_at_end_of_file](https://dart.dev/tools/linter-rules/eol_at_end_of_file)
  - [always_use_package_imports](https://dart.dev/tools/linter-rules/always_use_package_imports)

#### DCM:
- **refactor:** remove `dart_code_metrics` dependency from `analysis_options.yaml`
- **refactor:** remove [banned-usage](https://dcm.dev/docs/rules/common/banned-usage/) `RichText` identifier in favour of [prefer-text-rich](https://dcm.dev/docs/rules/flutter/prefer-text-rich/)
- **refactor:** increase `max-identifier-length` of [prefer-correct-identifier-length](https://dcm.dev/docs/rules/common/prefer-correct-identifier-length/) to 40

- **fix:** set `ignore-blocs` to `true` for `dispose-fields` (BlocProvider automatically handles disposal of the Bloc that is created via `Create` function)

- **feat:** additional lint rules:
  #### Common:
    - [avoid-map-keys-contains](https://dcm.dev/docs/rules/common/avoid-map-keys-contains/)
    - [avoid-duplicate-mixins](https://dcm.dev/docs/rules/common/avoid-duplicate-mixins/)
    - [avoid-nullable-interpolation](https://dcm.dev/docs/rules/common/avoid-nullable-interpolation/)
    - [prefer-named-boolean-parameters](https://dcm.dev/docs/rules/common/prefer-named-boolean-parameters/)
       ```yaml
        ignore-single: true
       ```
    - [avoid-unused-instances](https://dcm.dev/docs/rules/common/avoid-unused-instances/)
    - [prefer-correct-for-loop-increment](https://dcm.dev/docs/rules/common/prefer-correct-for-loop-increment/)
    - [prefer-public-exception-classes](https://dcm.dev/docs/rules/common/prefer-public-exception-classes/)
    - [match-class-name-pattern](https://dcm.dev/docs/rules/common/match-class-name-pattern/)
       ```yaml
        entries:
          - path: .*_bloc_event.dart'
            pattern: 'Event$'
          - path: 'data/.*_request_body.dart'
            pattern: 'RequestBody$'
          - path: 'data/.*_response.dart'
            pattern: 'Response$'
       ```
    - [avoid-unnecessary-reassignment](https://dcm.dev/docs/rules/common/avoid-unnecessary-reassignment/)
    - [prefer-correct-error-name](https://dcm.dev/docs/rules/common/prefer-correct-error-name/)
      ```yaml
        allowed-names:
          - ex
       ```
    - [avoid-long-functions](https://dcm.dev/docs/rules/common/avoid-long-functions/)
      ```yaml
        exclude:
          - test/**
        ignored-names:
          - build
          - builder
          - listener
          - itemBuilder
       ```

  #### Flutter:
    - [avoid-recursive-widget-calls](https://dcm.dev/docs/rules/flutter/avoid-recursive-widget-calls/)
    - [prefer-text-rich](https://dcm.dev/docs/rules/flutter/prefer-text-rich/)

# 1.1.2

#### DCM:
**refactor:** exclude `/test` folder from `avoid-importing-entrypoint-exports` rule

# 1.1.1

#### DCM:
**fix:** ignore parameter shadowing for `avoid-shadowing` rule
**fix** add short variable exceptions `[ 'x', 'y', 'id' ]` to `prefer-correct-identifier-length`
**fix** ignore static members for `prefer-widget-private-members` rule:

**refactor:** remove `refer-type-over-var`, because of conflict with `avoid-explicit-type-declaration`

# 1.1.0

#### DCM:
- **feat:** update deprecated rule:
    - [ban-name](https://dcm.dev/docs/rules/common/ban-name/) -> [banned-usage](https://dcm.dev/docs/rules/common/banned-usage/)

- **feat:** add new parameter exceptions to [no-equal-arguments](https://dcm.dev/docs/rules/common/no-equal-arguments/) rule:
    - `backgroundColor`
    - `barrierColor`
    - `focusedBorder`
    - `enabledBorder`
    - `topLeft`
    - `topRight`
    - `bottomLeft`
    - `bottomRight`
    - `highlightColor`
    - `splashColor`
    - `selectedItemColor`
    - `unselectedItemColor`
    - `selectedLabelStyle`
    - `unselectedLabelStyle`

- **feat:** update `widgets-oder` config to of [member-ordering](https://dcm.dev/docs/rules/common/member-ordering/#config) rule to keep private methods last:
  - `member-ordering:`\
    &nbsp;&nbsp; `widgets-order:`\
    &nbsp;&nbsp;&nbsp;&nbsp; ...\
    &nbsp;&nbsp;&nbsp;&nbsp; - `private-methods`

- **feat:** additional lint rules:
  #### Common:
    - [prefer-type-over-var](https://dcm.dev/docs/rules/common/prefer-type-over-var/)
    - [avoid-mutating-parameters](https://dcm.dev/docs/rules/common/avoid-mutating-parameters/)
    - [no-equal-nested-conditions](https://dcm.dev/docs/rules/common/no-equal-nested-conditions/)
    - [avoid-negated-conditions](https://dcm.dev/docs/rules/common/avoid-negated-conditions/)
    - [avoid-unnecessary-futures](https://dcm.dev/docs/rules/common/avoid-unnecessary-futures/)
    - [avoid-shadowed-extension-methods](https://dcm.dev/docs/rules/common/avoid-shadowed-extension-methods/)
    - [avoid-importing-entrypoint-exports](https://dcm.dev/docs/rules/common/avoid-importing-entrypoint-exports/)
    - [prefer-date-format](https://dcm.dev/docs/rules/common/prefer-date-format/)
    - [prefer-correct-identifier-length](https://dcm.dev/docs/rules/common/prefer-correct-identifier-length/)
    - [no-equal-conditions](https://dcm.dev/docs/rules/common/no-equal-conditions/)
    - [prefer-returning-conditional-expressions](https://dcm.dev/docs/rules/common/prefer-returning-conditional-expressions/)
    - [avoid-unrelated-type-casts](https://dcm.dev/docs/rules/common/avoid-unrelated-type-casts/)
    - [prefer-declaring-const-constructors](https://dcm.dev/docs/rules/common/prefer-declaring-const-constructors/)
    - [avoid-missed-calls](https://dcm.dev/docs/rules/common/avoid-missed-calls/)

  #### Flutter:
    - [avoid-missing-image-alt](https://dcm.dev/docs/rules/flutter/avoid-missing-image-alt/)
    - [avoid-unnecessary-overrides-in-state](https://dcm.dev/docs/rules/flutter/avoid-unnecessary-overrides-in-state/)
    - [prefer-dedicated-media-query-methods](https://dcm.dev/docs/rules/flutter/prefer-dedicated-media-query-methods/)
    - [use-setstate-synchronously](https://dcm.dev/docs/rules/flutter/use-setstate-synchronously/)


# 1.0.0

- Add `analysis_options` used at [Chili Labs](https://chililabs.io)
