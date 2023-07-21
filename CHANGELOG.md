# 1.1.1
**fix:** ignore parameter shadowing for `avoid-shadowing` rule
**fix** add short variable exceptions `[ 'x', 'y', 'id' ]` to `prefer-correct-identifier-length`
**fix** ignore static members for `prefer-widget-private-members` rule:

**refactor:** remove `refer-type-over-var`, because of conflict with `avoid-explicit-type-declaration`

# 1.1.0

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
