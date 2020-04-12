+++
title = "Hugo Dynamic Tabs"
date = 2020-04-11
+++

# Hugo Dynamic Tabs Examples

A quick and simple example showing how to use the **Hugo Dynamic Tabs** shortcode.

Github Repo: [Hugo Dynamic Tabs](https://github.com/rvanhorn/hugo-dynamic-tabs)

## Simple Tabs

{{< tabs tabTotal="3" tabID="1" tabName1="Tab 1" tabName2="Tab 2" tabName3="Tab 3" >}}
{{< tab tabNum="1" >}}

**Tab 1 Content**

{{< /tab >}}
{{< tab tabNum="2" >}}

**Tab 2 Content**

{{< /tab >}}
{{< tab tabNum="3" >}}

**Tab 3 Content**

{{< /tab >}}
{{< /tabs >}}

---

## Tabs With Mixed Content

{{< tabs tabTotal="3" tabID="2" tabName1="Tab 1" tabName2="Click Me!" tabName3="Tab 3" >}}
{{< tab tabNum="1" >}}

Check **Tab 2** for the example.

{{< /tab >}}
{{< tab tabNum="2" >}}

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum

```javascript
var test = "not formatted"
```

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum

![Image Example](https://i.insider.com/5e32f2a324306a19834af322?width=1100&format=jpeg&auto=webp "Its Baby Yoda!")

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum

{{< /tab >}}
{{< tab tabNum="3" >}}

**Tab 3 Content**

{{< /tab >}}
{{< /tabs >}}

