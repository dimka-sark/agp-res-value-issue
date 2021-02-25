# resValue with AGP 4.1.2 Issue

## Overview

If application use

```
tasks.whenTaskAdded { task ->}
```

with

```
android.applicationVariants.all { variant ->
  variant.resValue(*, *, *)
}
```

or

```
android.applicationVariants.all { variant ->
  variant.mergedFlavor.manifestPlaceholders
}
```

changed value did not applied to variant

## Step to reproduce bug

1. Open project
2. Select "app_issue" project
3. Run application
4. In open application text in middle text are missing

## Workaround solution

1. Open project
2. Select "app_working" project
3. Run application
4. In open application tkext in middle present

### TLDR:

When use AGP 3.6.4 on current project both solutions work well
