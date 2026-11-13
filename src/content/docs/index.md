---
title: Aside icon repro
---

An unknown icon name fails the build with "Invalid aside icon", as documented:

<!-- :::note{icon="not-an-icon"} -->

But an icon name that matches an `Object.prototype` property is accepted:

:::note{icon="constructor"}
The icon of this aside is the text `function Object() { [native code] }`.
:::

:::tip{icon="toString"}
The icon of this aside is the text `function toString() { [native code] }`.
:::
