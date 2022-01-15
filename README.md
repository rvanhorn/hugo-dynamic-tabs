# Hugo Dynamic Tabs

These shortcodes allows you to easily add tabs to your markdown files. There is no hardcoded limit to the number of tab groups you can have or the amount of tabs in a tab group.

### Bootstrap 4

Continue reading if using [Bootstrap 4](https://getbootstrap.com/docs/4.4/) as these shortcodes were originally developed using Bootstrap 4. 

### Bootstrap 5

The following branch, [bootstrap5](https://github.com/rvanhorn/hugo-dynamic-tabs/tree/bootstrap5)  should be used if you'd like to use these shortcodes with Bootstrap 5. 

### Other Framework/Custom

These shortcodes can be easily modified to work with any framework or custom CSS. Please take a look at the demo and the code in **tabs.html** and **tab.html** for a better understanding on how it works and what you'll need to change.

## How to Install

### Theme Component

1. First clone this Git repo into your **themes** folder. ``git clone https://github.com/rvanhorn/hugo-dynamic-tabs themes/hugo-dynamic-tabs``.
2. In your **config.yaml** or **config.toml** file, add the following to your ``theme`` list variable,``hugo-dynamic-tabs``. Please note,``hugo-dynamic-tabs`` needs to be listed before your actual theme. 

**config.yaml Example**
```yaml
theme:
  - hugo-dynamic-tabs
  - my-theme
```

**config.toml Example**
```toml
theme = ["hugo-dynamic-tabs", "my-theme"]
```

### Manual Install

1. Copy or download the two shortcodes files located in **layouts/shortcodes**. 
2. Place both shortcodes in your project's **layouts/shortcodes** folder. 

## How to Use

You need at least one nested tab shortcode inside the tabs shortcode for this theme component to properly work. Please see the **[Shortcodes Explanation](#Shortcodes-Explanation)** section for information on what each variable does. 

```
{{< tabs tabTotal="3">}}
{{< tab tabName="Tab 1" >}}

**Tab 1 Content**

{{< /tab >}}
```

The following is an example of Hugo Dynamic Tabs being used with multiple nested tab shortcodes.

```
{{< tabs tabTotal="3" tabRightAlign="2">}}
{{< tab tabName="Tab 1" >}}

**Tab 1 Content**

{{< /tab >}}
{{< tab tabName="Tab 2" >}}

**Tab 2 Content**

{{< /tab >}}
{{< tab tabName="Tab 3">}}

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
| tabTotal | This variable is used to generate the tab navigation. Simply set it to the amount of tab shortcodes you have. In the above example, since there are **three** nested tab shortcodes, you would set **tabTotal** to **three**.|
| tabRightAlign | This is an optional variable that if used will right align the tab number you inputted and all tabs after it. In the above example, since **tabRightAlign** is set to **two**, tabs 2 and 3 will be right aligned.  |

### tab.html

This is a child shortcode that is nested in the tabs shortcodes. Each tab shortcode equals one tab so add as many as you need. Please note, make sure **tabTotal** in the tabs shortcode is equal to the amount of tab shortcodes you use. 

| Variable  | Description |
| --------- | ----------- |
| tabName | This variable holds the name of the tab.  |

## Common Issues

##### One or Multiple Tabs are not Being Displayed Properly

- Make sure **tabTotal** is equal to the total amount of tab shortcodes you have. 
- Make sure **tabName** exists for each tab shortcode in the tabs shortcode.

##### Multiple Tab Groups Changing With a Single Click

- The **tab** shortcode assigns a randomly generated six letter ID to each tab allowing for 26^6 = 308,915,776 possibilities. If an actual duplication occurs, you'll need to re-build so the code can generate a new six letter ID for all tabs.

##### Markdown not Rendered Properly 

- Some users have reported that changing the shortcode delimiter from **<** and **>** to **%** fixes the issue for them. 

##### Tabs not Showing Properly/CSS Issues.

- This shortcode was built using [Bootstrap 4](https://getbootstrap.com/docs/4.4/) and will require some modification to **tab.html** and **tabs.html** to work with another framework or your own custom code. If you need help, please create an issue, and I can take a look. 

## Demo Site

I've created a simple demo showing the shortcode in action. Please note, this demo site was built using **Bootstrap 4** so your output may vary. 

[Hugo Dynamic Tabs Demo](https://hugo-dynamic-tabs.netlify.com/)

You can find the code in the **demo** folder in the repo. 

## Changelog

2.00 - January 15th, 2022
- Updated **README.md**.
- Added a new shortcode, **tabRightAlign** to allow right aligned tabs.
- Added a Bootstrap 5 version, see [bootstrap5](https://github.com/rvanhorn/hugo-dynamic-tabs/tree/bootstrap5) branch for code. 
- Refactored code in both **tabs.html** & **tab.html**
- The following shortcodes have been removed and are no longer needed.
  - **tabID**, now generated automatically. 
  - **tabNameX**, replaced with **tabName** in  **tab** shortcode.
  - **tabNum**, no longer needed.

1.11 - April 11th, 2020
- Updated **README.md**.
- Added demo site.

1.11 - May 3rd, 2019
- Updated **README.md**.
- Converted into theme component. 

1.10 - April 26th, 2019
- Added a new variable, **tabID** that allows multiple tab groups on the same page to have the same value for **tabNameX**. 

1.00 - April 26th, 2019
- Initial Release

## Credits

Copyright ©2019-©2022, Richard Van Horn.

Thanks to the [Hugo](https://github.com/gohugoio/hugo) team for making this possible!
