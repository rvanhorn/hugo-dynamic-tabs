# Hugo Dynamic Tabs
This shortcodes allows you to easily add tabs to your markdown files. There is no hardcoded limit to the number of tab groups you can have or the amount of tabs in a tab group. 

Please note, both shortcodes use [Bootstrap Tabs](https://getbootstrap.com/docs/4.1/components/navs/#tabs) but can be changed to fit your needs.

## How to Install

### Theme Component

1. First clone this Git repo ``git clone https://github.com/rvanhorn/hugo-dynamic-tabs themes/hugo-dynamic-tabs``.
2. In your **config.yaml** or **config.toml** file, add the following to your ``theme`` list variable,``hugo-dynamic-tabs``. Please note,``hugo-dynamic-tabs`` needs to be listed before your actual theme. 

**config.yaml Example**

```
theme: ["hugo-dynamic-tabs", "my-theme"]
```

**config.toml Example**
```
theme = ["hugo-dynamic-tabs", "my-theme"]

```

### Manual Install

1. Copy or download the two shortcodes files located in **layouts/shortcodes**. 
2. Place both shortcodes in your project's **layouts/shortcodes** folder. 

## How to Use

You need at least one nested tab shortcode inside the tabs shortcode for this theme component to properly work. Please see the **Shortcodes Explanation** section for information on what each variable does. 

```
{{< tabs tabTotal="1" tabID="1" tabName1="Tab 1" >}}
{{< tab tabNum="1" >}}

**Tab 1 Content**

{{< /tab >}}
{{< /tabs >}}
```

The following is an example of a Hugo Dynamic Tabs being used with multiple nested tab shortcodes.

```
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
```

## Shortcodes Explanation

Hugo Dynamic Tabs uses two shortcodes each with their own user-defined variables that generate each tab group and each individual tab within that group. 

### tabs.html

This is the parent shortcodes that wraps around all nested tab shortcodes in the tab group and generates the tab navigation. 

| Variable  | Description |
| --------- | ----------- |
| tabTotal | This variable is used to generate the tab navigation. Simply set it to the amount of tab shortcodes you have. In the above example, since there are **three** nested tab shortcodes, you would set **tabTotal** to **three**.
| tabID     | This variable is used to assign a unique number to the tab group allowing you to have multiple tab groups with the same values for **tabNameX**. Please note, each tab group must have its own unique number. 
| tabNameX  | This variable is used to generate each tab header based on how many nested tab shortcodes there are. Where **X** in the is the next sequential number, always starting at **one**. In the above example, there are **three** nested tab shortcodes so **tabName1**, **tabName2** & **tabName3** were added.  

### tab.html

This is a child shortcode that is nested in the tabs shortcodes. Each tab shortcode equals one tab so add as many as you need. Please note, make sure **tabTotal** in the tabs shortcode is equal to the amount of tab shortcodes you use. 


| Variable  | Description |
| --------- | ----------- |
| tabNum    |  This variable relates directly to the tab's number and should always start at **one**. In the above example, there are three nested tab shortcodes with **tabNum** starting at **one** and ending at **three** |

## Common Issues

##### One or Multiple Tabs are not Being Displayed Properly

- Make sure **tabTotal** is equal to the total amount of tab shortcodes you have. 
- Make sure **tabNameX** exists for each tab shortcode in the tabs shortcode. 
- Make sure your nested tab shortcodes **tabNum** are in sequential order. 

##### Multiple Tab Groups Changing With a Single Click

- Make sure each tab group has a unique **tabID**. 

## Changelog

1.11 - May 3rd, 2019
- Updated **README.md**.
- Converted into theme component. 

1.10 - April 26th, 2019
- Added a new variable, **tabID** that allows multiple tab groups on the same page to have the same value for **tabNameX**. 

1.00 - April 26th, 2019
- Initial Release

## Credits

Copyright ©2019, Richard Van Horn.

Thanks to the [Hugo](https://github.com/gohugoio/hugo) team for making this possible!