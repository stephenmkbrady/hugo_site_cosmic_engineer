---
title: "MD Reference"
date: 2018-04-22T18:11:37+01:00
draft: true
---
# Reference file for editing

``` [Assemble](http://assemble.io "hint hint") ```

 [Assemble](http://assemble.io "hint hint")


```_italics_``` _for italics_

```**bold**``` **for bold**

```~~strikethrough~~``` ~~strikethrough~~

` double` ` inline code

` triple` ` code block

`1.` ordered list, don't need to number, just use 1

1. hi
1. you

` * or - or + ` don't forget a space 

- unodered list

` > ` 

>_quote_

For ```<hr>```:
```
___
---
***
```

---

<!--
	Comments are html
-->
GFM, or “GitHub Flavored Markdown” also supports syntax highlighting.
```js
grunt.initConfig({
  assemble: {
    options: {
      assets: 'docs/assets',
      data: 'src/data/*.{json,yml}',
      helpers: 'src/custom-helpers.js',
      partials: ['src/partials/**/*.{hbs,md}']
    },
    pages: {
      options: {
        layout: 'default.hbs'
      },
      files: {
        './': ['src/templates/pages/index.hbs']
      }
    }
  }
};
```
Tables: 

| Option | Description |
| ------: | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

```
add : to right align the column
| Option | Description |
| ------: | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

Anchor links

```
# Table of Contents
  * [Chapter 1](#anchor1)
  * [Chapter 2](#anchor2)
  * [Chapter 3](#chapter-3)
 ```

# Table of Contents
  * [Chapter 1](#anchor1)
  * [Chapter 2](#anchor2)
  * [Chapter 3](#chapter-3)

Images
![randomtitle](http://octodex.github.com/images/minion.png?width=10pc "kill me")

``` ![Alt text][id] ```

![Alt text][id]

``` [id]: http://octodex.github.com/images/dojocat.jpg  "The Dojocat" ```
[id]: http://octodex.github.com/images/dojocat.jpg  "The Dojocat" 

![Alt text][id]

[id]: http://octodex.github.com/images/dojocat.jpg?height=50px&width=300px&classes=shadow  "The Dojocat" 

Attach files, by putting files in subfolder names same as the page you want to attach them to and use

{{%attachments style="green" /%}}


```
{{% button href="https://getgrav.org/" %}}Get Grav{{% /button %}}
{{% button href="https://getgrav.org/" icon="fa fa-download" %}}Get Grav with icon{{% /button %}}
{{% button href="https://getgrav.org/" icon="fa fa-download" icon-position="right" %}}Get Grav with icon right{{% /button %}}
```
{{% button href="https://getgrav.org/" %}}Get Grav{{% /button %}}
{{% button href="https://getgrav.org/" icon="fa fa-download" %}}Get Grav with icon{{% /button %}}
{{% button href="https://getgrav.org/" icon="fa fa-download" icon-position="right" %}}Get Grav with icon right{{% /button %}}


To list child pages:

Expand

{{%expand "Is this learn theme rocks ?" %}}Yes !.{{% /expand%}}


{{%expand%}}
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
{{% /expand%}}

Flow and GANTT charts https://learn.netlify.com/en/shortcodes/mermaid/

Note


{{% notice note %}}
A notice disclaimer
{{% /notice %}}


{{% notice tip %}}
A tip disclaimer
{{% /notice %}}


{{% notice warning %}}
An warning disclaimer
{{% /notice %}}

```
[params]
  editURL = "https://github.com/matcornic/hugo-theme-learn/edit/master/exampleSite/content/"
Use the siteparam shortcode to display its value.
'editURL' Value : {{% siteparam "editURL" %}}
```